# AutoCAD MCP

**AI assistants that work with the drawings open in Autodesk AutoCAD 2020–2027 — and with DXF files.**

AutoCAD MCP is a free [MCP](https://modelcontextprotocol.io) server for Windows. Claude, ChatGPT, Cursor, VS Code, Windsurf,
Gemini, Codex and other AI assistants use it to read and work with the drawings open in AutoCAD on your PC, through a small
AutoCAD plug-in that only programs of your own Windows account can reach, and to read, check, compare and write DXF files
without AutoCAD.

**Download:** [the latest release](https://github.com/SHMH-MCPs/autocad-mcp-releases/releases/latest) — run
`Install-AUTOCAD-MCP.cmd` from it (no administrator rights needed). Then start AutoCAD; if it asks
"Security - Unsigned Executable File" about AutoCadMcp.dll, choose Always Load.

## What it does
- **Drawings:** open, create, save (only when you ask), units, statistics, drawing properties, system variables
- **Entities:** list, count, filter, read every property; create lines, polylines, arcs, circles, splines, text, MTEXT,
  hatches, dimensions, multileaders, tables, 3D solids; move, rotate, scale, mirror, copy, arrays; offset, join, split, extend
- **Organisation:** layers, layer states, linetypes, text and dimension styles, blocks, attributes, dynamic blocks, groups
- **Sheets:** layouts, viewports, PDF plotting, DXF and WBLOCK export
- **References:** external references and every dependency (images, underlays, fonts, plot styles) with missing files
- **Quality:** drawing checks with findings by handle, comparison with a standard drawing, purge, audit
- **Many drawings at once:** inspect, export or update text in DWG files without opening them
- **Any other part of AutoCAD's .NET API**, checked against a catalogue of every 2020–2027 release

Anything that erases, purges, replaces, closes or overwrites is shown as a preview first and needs your OK. Every change is
one AutoCAD transaction and one undo step, read back and reported as verified or not. Running commands, AutoLISP and API
methods is off unless you switch it on.

## Versions
| AutoCAD | Plug-in build | Status |
|---|---|---|
| 2026 | R25 (.NET 8) | **tested** in AutoCAD 2026 (25.1s): read self-test 36/36, write self-test 89/89 |
| 2025 | R25 (.NET 8) | designed for, **not yet tested** |
| 2021–2024 | R24 (.NET Framework) | designed for, **not yet tested** |
| 2020 | R23 (.NET Framework) | designed for, **not yet tested** |
| 2027 | R26 (.NET 10) | designed for, **not yet tested** |

AutoCAD-based products (Civil 3D, Architecture …) run the plug-in as plain AutoCAD. AutoCAD LT has no .NET API and cannot.

AutoCAD is a trademark of Autodesk, Inc. AutoCAD MCP is not affiliated with or endorsed by Autodesk. Nothing of Autodesk is
included: the plug-in uses the AutoCAD installed and licensed on your PC.
