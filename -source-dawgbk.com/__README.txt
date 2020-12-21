to build...

$ lektor build --output-path ../dawgbk.com/

to deploy

$ lektor build && lektor deploy

or

$ lektor deploy production --output-path ../dawgbk.com/

which might be...

$ lektor build --output-path ../dawgbk.com/ && lektor deploy production --output-path ../dawgbk.com/


the distributed version of lektor may not have fixes for the broken html parsing in mistune.
to fix, check the source in lektor/markdown.py and remove the 2 options if present:

    -        'parse_block_html': True,
    -        'parse_inline_html': True,
