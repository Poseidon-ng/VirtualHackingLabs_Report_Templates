Author: Nino (Poseidon-ng)

Date: 09APR2020

# VirtualHackingLab Report Template in Markdown

I created an **VHL Report Template in Markdown** to make it easier on future students of VirtualHackingLabs with writing their Certificate of Completetion report for both the Basic and Advanced+ Certificate!

Now all future students will have an easy to follow and professional looking report!

## Requirements

- [Pandoc](https://pandoc.org/installing.html)
- LaTeX (eg. [TeX Live](http://www.tug.org/texlive/)) in order to get ```pdflatex``` or ```xelatex```
- [Eisvogel Pandoc LaTeX PDF Template](https://github.com/Wandmalfarbe/pandoc-latex-template#installation)
- [p7zip](http://p7zip.sourceforge.net/) if you want to use the script, for generating the archive

## Usage
Write your report in **markdown.**

### Automatic
There is a script writtin in bash to generate your report!

```./generate.sh (input.md) (output.pdf)```

### Manual
Generate the report PDF from the markdown template:
```
pandoc src/OSCP-exam-report-template_whoisflynn_v3.2.md \
-o output/OSCP-OS-XXXXX-Exam-Report.pdf \
--from markdown+yaml_metadata_block+raw_html \
--template eisvogel \
--table-of-contents \
--toc-depth 6 \
--number-sections \
--top-level-division=chapter \
--highlight-style breezedark
```
You can change the code syntax highlight theme with ```[--highlight-style](https://pandoc.org/MANUAL.html#option--highlight-style)```

## Color sets
Well rendering color sets you can use in the template YAML frontmatter:

|: titlepage-color :|: titlepage-text-color :|: titlepage-rule-color :|
|:---------------:|:--------------------:|:--------------------:|
|:```DC143C```(Crimson):|:```FFFFFF```(White):|:```FFFFFF```(White):|
|:```00FF7F```(SpringGreen):|:```006400```(DarkGreen):|:```000000```(Black):|
|:```1E90FF```(DodgeBlue):|:```FFFAFA```(Snow):|:```FFAFA```(Snow):|
|:```483D8B```(DarkSlateBlue):|:```FFFAFA```(Snow):|```FFFAFA```(Snow):|
|:```FFD700```(Gold):|:```000000```(Black):|:```000000```(Black):|
|:```FFEFD5```(PapayaWhip):|:```000000```(Black):|:```000000```(Black):|
|:```FF8C00```(DarkOrange):|:```000000```(Black):|:```000000```(Black):|
|:```FFEF96```(no name):|:```50394C```(no name):|:```50394C```(no name):|

## Mentions

This report is based off of noraj OSCP template
- Noraj - https://github.com/noraj

## Credits

Report Templates:

- Official Offensive Security Template v3 (UNLICENSED): https://support.offensive-security.com/oscp-exam-guide/#suggested-documentation-templates
- whoisflynn improved template v3.2 (UNLICENSED): https://github.com/whoisflynn/OSCP-Exam-Report-Template

Pandoc Template:

- Eisvogel ([LICENSE](https://github.com/Wandmalfarbe/pandoc-latex-template/blob/master/LICENSE)): https://github.com/Wandmalfarbe/pandoc-latex-template

