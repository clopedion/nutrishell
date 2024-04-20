# nutrishell

A readline-based interface for [nutrimatic](https://github.com/PuzzleTechHub/nutrimatic).

## Requirements
Meant for MacOS, UNIX, or Windows under WSL. 
- [nutrimatic](https://github.com/PuzzleTechHub/nutrimatic) and an index file
- perl with `String::ShellQuote` and `Term::ReadLine::Gnu` or `Term::ReadLine::Perl` (can install via cpan)
- environment variables `NUTRIMATIC` and `NUTRI_INDEX` set to the locations of the nutrimatic executable and index file

## Usage
Basic nutrimatic queries will output the first 20 results. `Enter` on a blank line will give full results for the previous query. Exit with Ctrl-C or Ctrl-D.

### Commands
- `~aa`: Almost anagrams: find anagrams with one letter changed

  Examples:
  - `~aa nutrimatic`:
    ```
    <Autrimatic>|<nAtrimatic>|<nuArimatic>|<nutAimatic>|<nutrAmatic>|<nutriAatic>|<nutrimAtic>|<nutrimaAic>|<nutrimatAc>|<nutrimatiA>
    1905 train music
    1667 rms titanic
    ...
    ```
  - `~aa "nutrimatic"`:
    ```
    "<Autrimatic>|<nAtrimatic>|<nuArimatic>|<nutAimatic>|<nutrAmatic>|<nutriAatic>|<nutrimAtic>|<nutrimaAic>|<nutrimatAc>|<nutrimatiA>"
    286 urticating
    242 intricatus
    ...
    ```
- `~t9`: Telephone code: replace `2` by `[abc]`, `3` by `[def]`, etc. as in T9 code
