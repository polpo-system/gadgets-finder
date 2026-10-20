# gadgets-finder

Finder for the gadgets of [polpo](https://github.com/polpo-system/polpo): a gadget that lists the
open documents, to bring one to the front, and the templates of new documents, to open one:
the entries of the section FinderTemplates of Oberon.Text whose files are there, every installed
panel (X.Panel in share/ or tools/), and Tools, a document listing the tool texts of the
installed packages with their first lines, each one opened by a middle click.

```
portia.Install gadgets-finder
```

## Using

    Gadgets.Insert Finder.NewFrame ~    a finder at the caret
    Finder.Minimize                     (in the menu of a document) puts the document away into
                                        the list of the finder; click it there to get it back
    Desktops.OpenDoc (Finder.NewToolsDoc) ~   the list of the tool texts (Tools in the finder)

## What is here

    src/Finder.Mod        the finder
    tools/Finder.Tool
    test/FinderTest.Mod

Finder is by Emil Zeller. The source comes from ETH Linux Oberon (OLR, 2017-06-18), converted from an Oberon text to plain
text; the first commit has it unchanged. It compiles unchanged with all five of polpo's compilers
(x86, ARM, ARMv7, RISC-V, MIPS).

## Tests

    FinderTest.Run      1 check: a finder gadget made; it needs the desktop's display

The license is GPL-3 (`LICENSE`); the code comes from ETH Oberon, whose license (`LICENSE.ETH`)
asks to keep its copyright notice and conditions, which `LICENSE.ETH` does.
