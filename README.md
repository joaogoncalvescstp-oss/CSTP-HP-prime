# CSTP-HP-Prime

HP Prime calculator programs for construction/survey field work.

## Programs

### Programs/PipeGrade.hpprgm

Pipe grade, invert, and cut/fill-to-hub calculator for staking storm/sewer
pipe. Three menu options:

1. **Grade From Inverts** — enter pipe length and the invert elevation at
   the start and end. Returns the grade (%) and, if you give it a station
   interval, an invert-elevation table dividing the run into stations of
   that spacing.
2. **Invert From Grade** — enter a start station, start invert elevation,
   and a design grade (%). Either solve the invert at one station, or
   generate a table over a length at a chosen station interval. Grade
   convention: positive grade falls (invert drops) as station increases;
   use a negative grade for a rising line.
3. **Cut/Fill To Hub** — enter a measured hub/stake elevation and compare
   it to a design elevation (either the grade/invert last computed in
   options 1–2 at a given station and optional vertical offset, or a
   design elevation entered directly). Reports **CUT** (hub is above
   grade, cut down to reach it) or **FILL** (hub is below grade, fill up
   to reach it).

## Loading onto a calculator

`PipeGrade.hpprgm` is plain PPL source text. To load it:

- **HP Connectivity Kit**: connect the calculator (or open the Virtual
  Calculator), drag `PipeGrade.hpprgm` into the Programs list, then open
  it once on the calculator and press **Check** — this resaves it in the
  current program format.
- **Type it in directly**: create a new program named `PipeGrade` in the
  calculator's Program Catalog and paste in the contents.
- **[Xprime](https://github.com/Insoft-UK/Xprime)** (macOS only): open the
  file as `.hpppl` source in the Xprime editor to check/build it and
  export a `.hpprgm`/`.hpappprgm` for the Virtual Calculator or a real
  Prime. Xprime also offers a `.hppplplus` macro dialect (C-style
  operators, dictionaries, includes) that expands to plain PPL — not
  required for this program, but useful if you want to extend it.

Run it from Home by typing `PipeGrade()` or selecting it in the Program
Catalog.
