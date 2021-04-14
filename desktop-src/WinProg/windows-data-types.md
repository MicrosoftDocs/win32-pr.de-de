---
title: Windows-Datentypen (BaseTsd.h)
description: Die von Windows unterstützten Datentypen werden verwendet, um Funktions Rückgabewerte, Funktions-und Nachrichten Parameter sowie Strukturmember zu definieren.
ms.assetid: 4553cafc-450e-4493-a4d4-cb6e2f274d46
keywords:
- Datentypen
- Datentypen, Windows
- Windows-API
- Windows-API, Datentypen
- Apientry
- ATOM
- BOOL
- BOOLEAN
- BYTE
- Rück
- CChar
- CHAR
- COLORREF
- CONST
- DWORD
- DWORDLONG
- DWORD_PTR
- DWORD32
- DWORD64
- GLEITKOMMAZAHL
- Haccel
- HALF_PTR
- HANDLE
- HBITMAP
- HBrush
- Hcolorspace
- Has
- Hvlist
- Hcursor
- HDC
- Hddecodata
- Hdesk
- HDROP
- Hdwp
- "\"HENHMETAFILE\""
- HFILE
- HFONT
- Hgdiobj
- HGLOBAL
- Hhook
- HICON
- HINSTANCE
- HKEY
- HKL
- Hlocal
- HMENU
- HMETAFILE
- HMODULE
- Hmonitor
- HPALETTE
- HPEN
- HRESULT
- HRGN
- Hrsrc
- Hsz
- Hwinsta
- HWND
- INT
- INT_PTR
- Int8
- INT16
- INT32
- INT64
- LANGID
- LCID
- LCTYPE
- Lgrpid
- LONG
- LONGLONG
- LONG_PTR
- LONG32
- LONG64
- LParam
- LPBOOL
- LPBYTE
- Lpcolorref
- LPCSTR
- LPCTSTR
- Lpcvoid
- LPCWSTR
- LPDWORD
- Lphandle
- Lpint
- Lplong
- LPSTR
- LPTSTR
- LPVOID
- Lpword
- LPWSTR
- LRESULT
- Pbool
- Pboolescher Wert
- PBYTE
- PChar
- Pcstr
- Pctstr
- PCWSTR
- PDWORD
- Pdwordlong
- PDWORD_PTR
- PDWORD32
- PDWORD64
- Pfloat
- PHALF_PTR
- Phandle
- Phkey
- Zeigen
- PINT_PTR
- PINT8
- PINT16
- PINT32
- PINT64
- Plcid
- Plong
- Plonglong
- PLONG_PTR
- PLONG32
- PLONG64
- POINTER_32
- POINTER_64
- POINTER_SIGNED
- POINTER_UNSIGNED
- Pshort
- PSIZE_T
- PSSIZE_T
- Pstr
- Ptbyte
- Ptchar
- Ptstr
- Puchar
- PUHALF_PTR
- Puint
- PUINT_PTR
- PUINT8
- PUINT16
- PUINT32
- PUINT64
- Pulong
- Pulonglong
- PULONG_PTR
- PULONG32
- PULONG64
- Pushort
- PVoid
- Pwchar
- PWORD
- Pwstr
- QWORD
- SC_HANDLE
- SC_LOCK
- SERVICE_STATUS_HANDLE
- SHORT
- SIZE_T
- SSIZE_T
- TBYTE
- TCHAR
- UCHAR
- UHALF_PTR
- UINT
- UINT_PTR
- UINT8
- UInt16
- UINT32
- UINT64
- ULONG
- ULONGLONG
- ULONG_PTR
- ULONG32
- ULONG64
- UNICODE_STRING
- USHORT
- USN
- Blutung
- WCHAR
- WINAPI
- WORD
- WParam
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf3a23e816a78f0dcae9c2fbd6e6979b936451c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391845"
---
# <a name="windows-data-types"></a><span data-ttu-id="db7a9-280">Windows-Datentypen</span><span class="sxs-lookup"><span data-stu-id="db7a9-280">Windows Data Types</span></span>

<span data-ttu-id="db7a9-281">Die von Windows unterstützten Datentypen werden verwendet, um Funktions Rückgabewerte, Funktions-und Nachrichten Parameter sowie Strukturmember zu definieren.</span><span class="sxs-lookup"><span data-stu-id="db7a9-281">The data types supported by Windows are used to define function return values, function and message parameters, and structure members.</span></span> <span data-ttu-id="db7a9-282">Sie definieren die Größe und Bedeutung dieser Elemente.</span><span class="sxs-lookup"><span data-stu-id="db7a9-282">They define the size and meaning of these elements.</span></span> <span data-ttu-id="db7a9-283">Weitere Informationen zu den zugrunde liegenden C/C++-Datentypen finden Sie unter [Datentyp Bereiche](/cpp/cpp/data-type-ranges?view=vs-2019).</span><span class="sxs-lookup"><span data-stu-id="db7a9-283">For more information about the underlying C/C++ data types, see [Data Type Ranges](/cpp/cpp/data-type-ranges?view=vs-2019).</span></span>

<span data-ttu-id="db7a9-284">Die folgende Tabelle enthält die folgenden Typen: Zeichen, Ganzzahl, boolescher Wert, Zeiger und handle.</span><span class="sxs-lookup"><span data-stu-id="db7a9-284">The following table contains the following types: character, integer, Boolean, pointer, and handle.</span></span> <span data-ttu-id="db7a9-285">Die Typen "Character", "Integer" und "Boolean" sind für die meisten C-Compiler üblich.</span><span class="sxs-lookup"><span data-stu-id="db7a9-285">The character, integer, and Boolean types are common to most C compilers.</span></span> <span data-ttu-id="db7a9-286">Die meisten Zeiger Typennamen beginnen mit einem Präfix von P oder LP.</span><span class="sxs-lookup"><span data-stu-id="db7a9-286">Most of the pointer-type names begin with a prefix of P or LP.</span></span> <span data-ttu-id="db7a9-287">Handles verweisen auf eine Ressource, die in den Arbeitsspeicher geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="db7a9-287">Handles refer to a resource that has been loaded into memory.</span></span>

<span data-ttu-id="db7a9-288">Weitere Informationen zum Verarbeiten von 64-Bit-Ganzzahlen finden Sie unter [große ganze](large-integers.md)Zahlen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-288">For more information about handling 64-bit integers, see [Large Integers](large-integers.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db7a9-289">Datentyp</span><span class="sxs-lookup"><span data-stu-id="db7a9-289">Data type</span></span></th>
<th><span data-ttu-id="db7a9-290">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="db7a9-290">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="db7a9-291"><span id="APIENTRY"></span><span id="apientry"></span><strong>Apientry</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-291"><span id="APIENTRY"></span><span id="apientry"></span><strong>APIENTRY</strong></span></span></td>
<td><span data-ttu-id="db7a9-292">Die Aufruf Konvention für Systemfunktionen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-292">The calling convention for system functions.</span></span><br/> <span data-ttu-id="db7a9-293">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-293">This type is declared in WinDef.h as follows:</span></span><br/> <code>#define APIENTRY WINAPI</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-294"><span id="ATOM"></span><span id="atom"></span><strong>DAT</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-294"><span id="ATOM"></span><span id="atom"></span><strong>ATOM</strong></span></span></td>
<td><span data-ttu-id="db7a9-295">Ein Atom.</span><span class="sxs-lookup"><span data-stu-id="db7a9-295">An atom.</span></span> <span data-ttu-id="db7a9-296">Weitere Informationen finden Sie unter Informationen <a href="/windows/desktop/dataxchg/about-atom-tables">zu Atom-Tabellen</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-296">For more information, see <a href="/windows/desktop/dataxchg/about-atom-tables">About Atom Tables</a>.</span></span><br/> <span data-ttu-id="db7a9-297">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-297">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef WORD ATOM;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-298"><span id="BOOL"></span><span id="bool"></span><strong>BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-298"><span id="BOOL"></span><span id="bool"></span><strong>BOOL</strong></span></span></td>
<td><span data-ttu-id="db7a9-299">Eine boolesche Variable (sollte " <strong>true</strong> " oder " <strong>false</strong>" lauten).</span><span class="sxs-lookup"><span data-stu-id="db7a9-299">A Boolean variable (should be <strong>TRUE</strong> or <strong>FALSE</strong>).</span></span><br/> <span data-ttu-id="db7a9-300">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-300">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef int BOOL;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-301"><span id="BOOLEAN"></span><span id="boolean"></span><strong>Booleschen</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-301"><span id="BOOLEAN"></span><span id="boolean"></span><strong>BOOLEAN</strong></span></span></td>
<td><span data-ttu-id="db7a9-302">Eine boolesche Variable (sollte " <strong>true</strong> " oder " <strong>false</strong>" lauten).</span><span class="sxs-lookup"><span data-stu-id="db7a9-302">A Boolean variable (should be <strong>TRUE</strong> or <strong>FALSE</strong>).</span></span><br/> <span data-ttu-id="db7a9-303">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-303">This type is declared in WinNT.h as follows:</span></span><br/> <code>typedef BYTE BOOLEAN;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-304"><span id="BYTE"></span><span id="byte"></span><strong>Hobby</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-304"><span id="BYTE"></span><span id="byte"></span><strong>BYTE</strong></span></span></td>
<td><span data-ttu-id="db7a9-305">Ein Byte (8 Bits).</span><span class="sxs-lookup"><span data-stu-id="db7a9-305">A byte (8 bits).</span></span><br/> <span data-ttu-id="db7a9-306">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-306">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef unsigned char BYTE;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-307"><span id="CALLBACK"></span><span id="callback"></span><strong>Rück</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-307"><span id="CALLBACK"></span><span id="callback"></span><strong>CALLBACK</strong></span></span></td>
<td><span data-ttu-id="db7a9-308">Die Aufruf Konvention für Rückruf Funktionen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-308">The calling convention for callback functions.</span></span><br/> <span data-ttu-id="db7a9-309">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-309">This type is declared in WinDef.h as follows:</span></span><br/> <code>#define CALLBACK __stdcall</code><br/> <span data-ttu-id="db7a9-310"><strong>Callback</strong>, <strong>WinAPI</strong>und <strong>apientry</strong> werden verwendet, um Funktionen mit der __stdcall-Aufruf Konvention zu definieren.</span><span class="sxs-lookup"><span data-stu-id="db7a9-310"><strong>CALLBACK</strong>, <strong>WINAPI</strong>, and <strong>APIENTRY</strong> are all used to define functions with the __stdcall calling convention.</span></span> <span data-ttu-id="db7a9-311">Die meisten Funktionen in der Windows-API werden mithilfe von <strong>WinAPI</strong>deklariert.</span><span class="sxs-lookup"><span data-stu-id="db7a9-311">Most functions in the Windows API are declared using <strong>WINAPI</strong>.</span></span> <span data-ttu-id="db7a9-312">Möglicherweise möchten Sie den <strong>Rückruf</strong> für die von Ihnen implementierten Rückruf Funktionen verwenden, um die Funktion als Rückruffunktion zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="db7a9-312">You may wish to use <strong>CALLBACK</strong> for the callback functions that you implement to help identify the function as a callback function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-313"><span id="CCHAR"></span><span id="cchar"></span><strong>CChar</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-313"><span id="CCHAR"></span><span id="cchar"></span><strong>CCHAR</strong></span></span></td>
<td><span data-ttu-id="db7a9-314">Ein 8-Bit-Windows-Zeichen (ANSI).</span><span class="sxs-lookup"><span data-stu-id="db7a9-314">An 8-bit Windows (ANSI) character.</span></span><br/> <span data-ttu-id="db7a9-315">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-315">This type is declared in WinNT.h as follows:</span></span><br/> <code>typedef char CCHAR;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-316"><span id="CHAR"></span><span id="char"></span><strong>Char</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-316"><span id="CHAR"></span><span id="char"></span><strong>CHAR</strong></span></span></td>
<td><span data-ttu-id="db7a9-317">Ein 8-Bit-Windows-Zeichen (ANSI).</span><span class="sxs-lookup"><span data-stu-id="db7a9-317">An 8-bit Windows (ANSI) character.</span></span> <span data-ttu-id="db7a9-318">Weitere Informationen finden Sie unter <a href="/windows/desktop/gdi/character-sets-used-by-fonts">von Schriftarten verwendete Zeichensätze</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-318">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span><br/> <span data-ttu-id="db7a9-319">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-319">This type is declared in WinNT.h as follows:</span></span><br/> <code>typedef char CHAR;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-320"><span id="COLORREF"></span><span id="colorref"></span><strong>COLORREF</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-320"><span id="COLORREF"></span><span id="colorref"></span><strong>COLORREF</strong></span></span></td>
<td><span data-ttu-id="db7a9-321">Der rote, grüne, blaue (RGB) Farbwert (32 Bits).</span><span class="sxs-lookup"><span data-stu-id="db7a9-321">The red, green, blue (RGB) color value (32 bits).</span></span> <span data-ttu-id="db7a9-322">Weitere Informationen zu diesem Typ finden Sie unter <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="db7a9-322">See <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> for information on this type.</span></span><br/> <span data-ttu-id="db7a9-323">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-323">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef DWORD COLORREF;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-324"><span id="CONST"></span><span id="const"></span><strong>CONST</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-324"><span id="CONST"></span><span id="const"></span><strong>CONST</strong></span></span></td>
<td><span data-ttu-id="db7a9-325">Eine Variable, deren Wert während der Ausführung konstant bleiben soll.</span><span class="sxs-lookup"><span data-stu-id="db7a9-325">A variable whose value is to remain constant during execution.</span></span> <br/> <span data-ttu-id="db7a9-326">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-326">This type is declared in WinDef.h as follows:</span></span><br/> <code>#define CONST const</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-327"><span id="DWORD"></span><span id="dword"></span><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-327"><span id="DWORD"></span><span id="dword"></span><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="db7a9-328">Eine 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-328">A 32-bit unsigned integer.</span></span> <span data-ttu-id="db7a9-329">Der Bereich liegt zwischen 0 und 4294967295 Decimal.</span><span class="sxs-lookup"><span data-stu-id="db7a9-329">The range is 0 through 4294967295 decimal.</span></span><br/> <span data-ttu-id="db7a9-330">Dieser Typ wird in "inzafe. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-330">This type is declared in IntSafe.h as follows:</span></span><br/> <code>typedef unsigned long DWORD;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-331"><span id="DWORDLONG"></span><span id="dwordlong"></span><strong>DWORDLONG</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-331"><span id="DWORDLONG"></span><span id="dwordlong"></span><strong>DWORDLONG</strong></span></span></td>
<td><span data-ttu-id="db7a9-332">Eine 64-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-332">A 64-bit unsigned integer.</span></span> <span data-ttu-id="db7a9-333">Der Bereich liegt zwischen 0 und 18446744073709551615 Decimal.</span><span class="sxs-lookup"><span data-stu-id="db7a9-333">The range is 0 through 18446744073709551615 decimal.</span></span><br/> <span data-ttu-id="db7a9-334">Dieser Typ wird in "inzafe. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-334">This type is declared in IntSafe.h as follows:</span></span><br/> <code>typedef unsigned __int64 DWORDLONG;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-335"><span id="DWORD_PTR"></span><span id="dword_ptr"></span><strong>DWORD_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-335"><span id="DWORD_PTR"></span><span id="dword_ptr"></span><strong>DWORD_PTR</strong></span></span></td>
<td><span data-ttu-id="db7a9-336">Ein Long-Typ ohne Vorzeichen für die Zeiger Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="db7a9-336">An unsigned long type for pointer precision.</span></span> <span data-ttu-id="db7a9-337">Verwenden Sie, wenn Sie einen Zeiger auf einen Long-Typ umwandeln, um Zeigerarithmetik auszuführen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-337">Use when casting a pointer to a long type to perform pointer arithmetic.</span></span> <span data-ttu-id="db7a9-338">(Wird auch häufig für allgemeine 32-Bit-Parameter verwendet, die auf 64 Bits in 64-Bit-Fenstern erweitert wurden.)</span><span class="sxs-lookup"><span data-stu-id="db7a9-338">(Also commonly used for general 32-bit parameters that have been extended to 64 bits in 64-bit Windows.)</span></span><br/> <span data-ttu-id="db7a9-339">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-339">This type is declared in BaseTsd.h as follows:</span></span><br/> <code>typedef ULONG_PTR DWORD_PTR;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-340"><span id="DWORD32"></span><span id="dword32"></span><strong>DWORD32</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-340"><span id="DWORD32"></span><span id="dword32"></span><strong>DWORD32</strong></span></span></td>
<td><span data-ttu-id="db7a9-341">Eine 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-341">A 32-bit unsigned integer.</span></span><br/> <span data-ttu-id="db7a9-342">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-342">This type is declared in BaseTsd.h as follows:</span></span><br/> <code>typedef unsigned int DWORD32;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-343"><span id="DWORD64"></span><span id="dword64"></span><strong>DWORD64</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-343"><span id="DWORD64"></span><span id="dword64"></span><strong>DWORD64</strong></span></span></td>
<td><span data-ttu-id="db7a9-344">Eine 64-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-344">A 64-bit unsigned integer.</span></span><br/> <span data-ttu-id="db7a9-345">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-345">This type is declared in BaseTsd.h as follows:</span></span><br/> <code>typedef unsigned __int64 DWORD64;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-346"><span id="FLOAT"></span><span id="float"></span><strong>Hafen</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-346"><span id="FLOAT"></span><span id="float"></span><strong>FLOAT</strong></span></span></td>
<td><span data-ttu-id="db7a9-347">Eine Gleit Komma Variable.</span><span class="sxs-lookup"><span data-stu-id="db7a9-347">A floating-point variable.</span></span><br/> <span data-ttu-id="db7a9-348">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-348">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef float FLOAT;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-349"><span id="HACCEL"></span><span id="haccel"></span><strong>Haccel</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-349"><span id="HACCEL"></span><span id="haccel"></span><strong>HACCEL</strong></span></span></td>
<td><span data-ttu-id="db7a9-350">Ein Handle für eine Zugriffstasten <a href="/windows/desktop/menurc/keyboard-accelerators">Tabelle</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-350">A handle to an <a href="/windows/desktop/menurc/keyboard-accelerators">accelerator table</a>.</span></span><br/> <span data-ttu-id="db7a9-351">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-351">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef HANDLE HACCEL;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-352"><span id="HALF_PTR"></span><span id="half_ptr"></span><strong>HALF_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-352"><span id="HALF_PTR"></span><span id="half_ptr"></span><strong>HALF_PTR</strong></span></span></td>
<td><span data-ttu-id="db7a9-353">Die Hälfte der Größe eines Zeigers.</span><span class="sxs-lookup"><span data-stu-id="db7a9-353">Half the size of a pointer.</span></span> <span data-ttu-id="db7a9-354">Verwenden Sie innerhalb einer-Struktur, die einen Zeiger und zwei kleine Felder enthält.</span><span class="sxs-lookup"><span data-stu-id="db7a9-354">Use within a structure that contains a pointer and two small fields.</span></span><br/> <span data-ttu-id="db7a9-355">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-355">This type is declared in BaseTsd.h as follows:</span></span><br/> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db7a9-356">C++</span><span class="sxs-lookup"><span data-stu-id="db7a9-356">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef _WIN64
 typedef int HALF_PTR;
#else
 typedef short HALF_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-357"><span id="HANDLE"></span><span id="handle"></span><strong>Bewältigen</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-357"><span id="HANDLE"></span><span id="handle"></span><strong>HANDLE</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-358">Ein Handle für ein-Objekt.</span><span class="sxs-lookup"><span data-stu-id="db7a9-358">A handle to an object.</span></span></p>
<p><span data-ttu-id="db7a9-359">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-359">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef PVOID HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-360"><span id="HBITMAP"></span><span id="hbitmap"></span><strong>HBITMAP</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-360"><span id="HBITMAP"></span><span id="hbitmap"></span><strong>HBITMAP</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-361">Ein Handle für eine <a href="/windows/desktop/gdi/bitmaps">Bitmap</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-361">A handle to a <a href="/windows/desktop/gdi/bitmaps">bitmap</a>.</span></span></p>
<p><span data-ttu-id="db7a9-362">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-362">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HBITMAP;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-363"><span id="HBRUSH"></span><span id="hbrush"></span><strong>HBrush</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-363"><span id="HBRUSH"></span><span id="hbrush"></span><strong>HBRUSH</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-364">Ein Handle für einen <a href="/windows/desktop/gdi/brushes">Pinsel</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-364">A handle to a <a href="/windows/desktop/gdi/brushes">brush</a>.</span></span></p>
<p><span data-ttu-id="db7a9-365">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-365">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HBRUSH;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-366"><span id="HCOLORSPACE"></span><span id="hcolorspace"></span><strong>Hcolorspace</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-366"><span id="HCOLORSPACE"></span><span id="hcolorspace"></span><strong>HCOLORSPACE</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-367">Ein Handle für einen <a href="/previous-versions//dd316799(v=vs.85)">Farbraum</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-367">A handle to a <a href="/previous-versions//dd316799(v=vs.85)">color space</a>.</span></span></p>
<p><span data-ttu-id="db7a9-368">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-368">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HCOLORSPACE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-369"><span id="HCONV"></span><span id="hconv"></span><strong>Has</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-369"><span id="HCONV"></span><span id="hconv"></span><strong>HCONV</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-370">Ein Handle für eine DDE-Konversation (Dynamic Data Exchange).</span><span class="sxs-lookup"><span data-stu-id="db7a9-370">A handle to a dynamic data exchange (DDE) conversation.</span></span></p>
<p><span data-ttu-id="db7a9-371">Dieser Typ wird in "Ddeml. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-371">This type is declared in Ddeml.h as follows:</span></span></p>
<p><code>typedef HANDLE HCONV;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-372"><span id="HCONVLIST"></span><span id="hconvlist"></span><strong>Hvlist</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-372"><span id="HCONVLIST"></span><span id="hconvlist"></span><strong>HCONVLIST</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-373">Ein Handle für eine DDE-Konversations Liste.</span><span class="sxs-lookup"><span data-stu-id="db7a9-373">A handle to a DDE conversation list.</span></span></p>
<p><span data-ttu-id="db7a9-374">Dieser Typ wird in "Ddeml. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-374">This type is declared in Ddeml.h as follows:</span></span></p>
<p><code>typedef HANDLE HCONVLIST;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-375"><span id="HCURSOR"></span><span id="hcursor"></span><strong>Hcursor</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-375"><span id="HCURSOR"></span><span id="hcursor"></span><strong>HCURSOR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-376">Ein Handle für einen <a href="/windows/desktop/menurc/cursors">Cursor</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-376">A handle to a <a href="/windows/desktop/menurc/cursors">cursor</a>.</span></span></p>
<p><span data-ttu-id="db7a9-377">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-377">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HICON HCURSOR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-378"><span id="HDC"></span><span id="hdc"></span><strong>HDC</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-378"><span id="HDC"></span><span id="hdc"></span><strong>HDC</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-379">Ein Handle für einen <a href="/windows/desktop/gdi/device-context-types">Gerätekontext</a> (DC).</span><span class="sxs-lookup"><span data-stu-id="db7a9-379">A handle to a <a href="/windows/desktop/gdi/device-context-types">device context</a> (DC).</span></span></p>
<p><span data-ttu-id="db7a9-380">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-380">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HDC;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-381"><span id="HDDEDATA"></span><span id="hddedata"></span><strong>Hddecodata</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-381"><span id="HDDEDATA"></span><span id="hddedata"></span><strong>HDDEDATA</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-382">Ein Handle für DDE-Daten.</span><span class="sxs-lookup"><span data-stu-id="db7a9-382">A handle to DDE data.</span></span></p>
<p><span data-ttu-id="db7a9-383">Dieser Typ wird in "Ddeml. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-383">This type is declared in Ddeml.h as follows:</span></span></p>
<p><code>typedef HANDLE HDDEDATA;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-384"><span id="HDESK"></span><span id="hdesk"></span><strong>Hdesk</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-384"><span id="HDESK"></span><span id="hdesk"></span><strong>HDESK</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-385">Ein Handle für einen <a href="/windows/desktop/winstation/desktops">Desktop</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-385">A handle to a <a href="/windows/desktop/winstation/desktops">desktop</a>.</span></span></p>
<p><span data-ttu-id="db7a9-386">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-386">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HDESK;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-387"><span id="HDROP"></span><span id="hdrop"></span><strong>HDROP</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-387"><span id="HDROP"></span><span id="hdrop"></span><strong>HDROP</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-388">Ein Handle für eine interne Drop-Struktur.</span><span class="sxs-lookup"><span data-stu-id="db7a9-388">A handle to an internal drop structure.</span></span></p>
<p><span data-ttu-id="db7a9-389">Dieser Typ wird in "shellapi. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-389">This type is declared in ShellApi.h as follows:</span></span></p>
<p><code>typedef HANDLE HDROP;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-390"><span id="HDWP"></span><span id="hdwp"></span><strong>Hdwp</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-390"><span id="HDWP"></span><span id="hdwp"></span><strong>HDWP</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-391">Ein Handle für eine verzögerte Fenster Positions Struktur.</span><span class="sxs-lookup"><span data-stu-id="db7a9-391">A handle to a deferred window position structure.</span></span></p>
<p><span data-ttu-id="db7a9-392">Dieser Typ wird in winuser. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-392">This type is declared in WinUser.h as follows:</span></span></p>
<p><code>typedef HANDLE HDWP;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-393"><span id="HENHMETAFILE"></span><span id="henhmetafile"></span><strong>"HENHMETAFILE"</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-393"><span id="HENHMETAFILE"></span><span id="henhmetafile"></span><strong>HENHMETAFILE</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-394">Ein Handle für eine <a href="/windows/desktop/gdi/metafiles">Erweiterte Metadatei</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-394">A handle to an <a href="/windows/desktop/gdi/metafiles">enhanced metafile</a>.</span></span></p>
<p><span data-ttu-id="db7a9-395">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-395">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HENHMETAFILE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-396"><span id="HFILE"></span><span id="hfile"></span><strong>HFILE</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-396"><span id="HFILE"></span><span id="hfile"></span><strong>HFILE</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-397">Ein Handle für eine Datei, die von <a href="/windows/desktop/api/winbase/nf-winbase-openfile"><strong>OpenFile</strong></a>geöffnet wurde <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea"><strong>, nicht für</strong></a>"".</span><span class="sxs-lookup"><span data-stu-id="db7a9-397">A handle to a file opened by <a href="/windows/desktop/api/winbase/nf-winbase-openfile"><strong>OpenFile</strong></a>, not <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea"><strong>CreateFile</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-398">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-398">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef int HFILE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-399"><span id="HFONT"></span><span id="hfont"></span><strong>HFont</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-399"><span id="HFONT"></span><span id="hfont"></span><strong>HFONT</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-400">Ein Handle für eine <a href="/windows/desktop/gdi/about-fonts">Schriftart</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-400">A handle to a <a href="/windows/desktop/gdi/about-fonts">font</a>.</span></span></p>
<p><span data-ttu-id="db7a9-401">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-401">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HFONT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-402"><span id="HGDIOBJ"></span><span id="hgdiobj"></span><strong>Hgdiobj</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-402"><span id="HGDIOBJ"></span><span id="hgdiobj"></span><strong>HGDIOBJ</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-403">Ein Handle für ein GDI-Objekt.</span><span class="sxs-lookup"><span data-stu-id="db7a9-403">A handle to a GDI object.</span></span></p>
<p><span data-ttu-id="db7a9-404">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-404">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HGDIOBJ;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-405"><span id="HGLOBAL"></span><span id="hglobal"></span><strong>HGLOBAL</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-405"><span id="HGLOBAL"></span><span id="hglobal"></span><strong>HGLOBAL</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-406">Ein Handle für einen globalen Speicherblock.</span><span class="sxs-lookup"><span data-stu-id="db7a9-406">A handle to a global memory block.</span></span></p>
<p><span data-ttu-id="db7a9-407">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-407">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HGLOBAL;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-408"><span id="HHOOK"></span><span id="hhook"></span><strong>Hhook</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-408"><span id="HHOOK"></span><span id="hhook"></span><strong>HHOOK</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-409">Ein Handle für einen <a href="/windows/desktop/winmsg/hooks">Hook</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-409">A handle to a <a href="/windows/desktop/winmsg/hooks">hook</a>.</span></span></p>
<p><span data-ttu-id="db7a9-410">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-410">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HHOOK;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-411"><span id="HICON"></span><span id="hicon"></span><strong>HICON</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-411"><span id="HICON"></span><span id="hicon"></span><strong>HICON</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-412">Ein Handle für ein <a href="/windows/desktop/menurc/icons">Symbol</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-412">A handle to an <a href="/windows/desktop/menurc/icons">icon</a>.</span></span></p>
<p><span data-ttu-id="db7a9-413">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-413">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HICON;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-414"><span id="HINSTANCE"></span><span id="hinstance"></span><strong>HINSTANCE</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-414"><span id="HINSTANCE"></span><span id="hinstance"></span><strong>HINSTANCE</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-415">Ein Handle für eine-Instanz.</span><span class="sxs-lookup"><span data-stu-id="db7a9-415">A handle to an instance.</span></span> <span data-ttu-id="db7a9-416">Dies ist die Basisadresse des Moduls im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="db7a9-416">This is the base address of the module in memory.</span></span></p>
<p><span data-ttu-id="db7a9-417"><strong>HMODULE</strong> und <strong>HINSTANCE</strong> sind heute identisch, haben jedoch unterschiedliche Dinge in 16-Bit-Fenstern dargestellt.</span><span class="sxs-lookup"><span data-stu-id="db7a9-417"><strong>HMODULE</strong> and <strong>HINSTANCE</strong> are the same today, but represented different things in 16-bit Windows.</span></span></p>
<p><span data-ttu-id="db7a9-418">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-418">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HINSTANCE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-419"><span id="HKEY"></span><span id="hkey"></span><strong>HKEY</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-419"><span id="HKEY"></span><span id="hkey"></span><strong>HKEY</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-420">Ein Handle für einen Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="db7a9-420">A handle to a registry key.</span></span></p>
<p><span data-ttu-id="db7a9-421">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-421">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HKEY;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-422"><span id="HKL"></span><span id="hkl"></span><strong>HKL</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-422"><span id="HKL"></span><span id="hkl"></span><strong>HKL</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-423">Ein Eingabe Gebiets Schema Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="db7a9-423">An input locale identifier.</span></span></p>
<p><span data-ttu-id="db7a9-424">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-424">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HKL;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-425"><span id="HLOCAL"></span><span id="hlocal"></span><strong>Hlocal</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-425"><span id="HLOCAL"></span><span id="hlocal"></span><strong>HLOCAL</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-426">Ein Handle für einen lokalen Speicherblock.</span><span class="sxs-lookup"><span data-stu-id="db7a9-426">A handle to a local memory block.</span></span></p>
<p><span data-ttu-id="db7a9-427">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-427">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HLOCAL;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-428"><span id="HMENU"></span><span id="hmenu"></span><strong>HMENU</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-428"><span id="HMENU"></span><span id="hmenu"></span><strong>HMENU</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-429">Ein Handle für ein <a href="/windows/desktop/menurc/menus">Menü</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-429">A handle to a <a href="/windows/desktop/menurc/menus">menu</a>.</span></span></p>
<p><span data-ttu-id="db7a9-430">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-430">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HMENU;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-431"><span id="HMETAFILE"></span><span id="hmetafile"></span><strong>HMETAFILE</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-431"><span id="HMETAFILE"></span><span id="hmetafile"></span><strong>HMETAFILE</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-432">Ein Handle für eine <a href="/windows/desktop/gdi/metafiles">Metadatei</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-432">A handle to a <a href="/windows/desktop/gdi/metafiles">metafile</a>.</span></span></p>
<p><span data-ttu-id="db7a9-433">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-433">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HMETAFILE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-434"><span id="HMODULE"></span><span id="hmodule"></span><strong>HMODULE</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-434"><span id="HMODULE"></span><span id="hmodule"></span><strong>HMODULE</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-435">Ein Handle für ein Modul.</span><span class="sxs-lookup"><span data-stu-id="db7a9-435">A handle to a module.</span></span> <span data-ttu-id="db7a9-436">Die ist die Basisadresse des Moduls im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="db7a9-436">The is the base address of the module in memory.</span></span></p>
<p><span data-ttu-id="db7a9-437"><strong>HMODULE</strong> und <strong>HINSTANCE</strong> sind in den aktuellen Versionen von Windows identisch, haben jedoch unterschiedliche Dinge in 16-Bit-Fenstern dargestellt.</span><span class="sxs-lookup"><span data-stu-id="db7a9-437"><strong>HMODULE</strong> and <strong>HINSTANCE</strong> are the same in current versions of Windows, but represented different things in 16-bit Windows.</span></span></p>
<p><span data-ttu-id="db7a9-438">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-438">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HINSTANCE HMODULE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-439"><span id="HMONITOR"></span><span id="hmonitor"></span><strong>Hmonitor</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-439"><span id="HMONITOR"></span><span id="hmonitor"></span><strong>HMONITOR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-440">Ein Handle für einen Anzeige Monitor.</span><span class="sxs-lookup"><span data-stu-id="db7a9-440">A handle to a display monitor.</span></span></p>
<p><span data-ttu-id="db7a9-441">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-441">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>if(WINVER >= 0x0500) typedef HANDLE HMONITOR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-442"><span id="HPALETTE"></span><span id="hpalette"></span><strong>HPALETTE</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-442"><span id="HPALETTE"></span><span id="hpalette"></span><strong>HPALETTE</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-443">Ein Handle für eine Palette.</span><span class="sxs-lookup"><span data-stu-id="db7a9-443">A handle to a palette.</span></span></p>
<p><span data-ttu-id="db7a9-444">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-444">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HPALETTE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-445"><span id="HPEN"></span><span id="hpen"></span><strong>HPEN</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-445"><span id="HPEN"></span><span id="hpen"></span><strong>HPEN</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-446">Ein Handle für einen <a href="/windows/desktop/gdi/pens">Stift</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-446">A handle to a <a href="/windows/desktop/gdi/pens">pen</a>.</span></span></p>
<p><span data-ttu-id="db7a9-447">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-447">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HPEN;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-448"><span id="HRESULT"></span><span id="hresult"></span><strong>HRESULT</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-448"><span id="HRESULT"></span><span id="hresult"></span><strong>HRESULT</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-449">Die von COM-Schnittstellen verwendeten Rückgabecodes.</span><span class="sxs-lookup"><span data-stu-id="db7a9-449">The return codes used by COM interfaces.</span></span> <span data-ttu-id="db7a9-450">Weitere Informationen finden Sie unter <a href="/windows/desktop/com/structure-of-com-error-codes">Struktur der com-Fehler Codes</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-450">For more information, see <a href="/windows/desktop/com/structure-of-com-error-codes">Structure of the COM Error Codes</a>.</span></span> <span data-ttu-id="db7a9-451">Um einen <strong>HRESULT</strong> -Wert zu testen, verwenden Sie die Makros <a href="/windows/desktop/api/winerror/nf-winerror-failed"><strong>failed</strong></a> und <a href="/windows/desktop/api/winerror/nf-winerror-succeeded"><strong>war erfolgreich</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="db7a9-451">To test an <strong>HRESULT</strong> value, use the <a href="/windows/desktop/api/winerror/nf-winerror-failed"><strong>FAILED</strong></a> and <a href="/windows/desktop/api/winerror/nf-winerror-succeeded"><strong>SUCCEEDED</strong></a> macros.</span></span></p>
<p><span data-ttu-id="db7a9-452">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-452">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef LONG HRESULT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-453"><span id="HRGN"></span><span id="hrgn"></span><strong>Hrgn</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-453"><span id="HRGN"></span><span id="hrgn"></span><strong>HRGN</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-454">Ein Handle für einen <a href="/windows/desktop/gdi/regions">Bereich</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-454">A handle to a <a href="/windows/desktop/gdi/regions">region</a>.</span></span></p>
<p><span data-ttu-id="db7a9-455">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-455">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HRGN;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-456"><span id="HRSRC"></span><span id="hrsrc"></span><strong>Hrsrc</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-456"><span id="HRSRC"></span><span id="hrsrc"></span><strong>HRSRC</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-457">Ein Handle für eine Ressource.</span><span class="sxs-lookup"><span data-stu-id="db7a9-457">A handle to a resource.</span></span></p>
<p><span data-ttu-id="db7a9-458">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-458">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HRSRC;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-459"><span id="HSZ"></span><span id="hsz"></span><strong>Hsz</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-459"><span id="HSZ"></span><span id="hsz"></span><strong>HSZ</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-460">Ein Handle für eine DDE-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="db7a9-460">A handle to a DDE string.</span></span></p>
<p><span data-ttu-id="db7a9-461">Dieser Typ wird in "Ddeml. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-461">This type is declared in Ddeml.h as follows:</span></span></p>
<p><code>typedef HANDLE HSZ;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-462"><span id="HWINSTA"></span><span id="hwinsta"></span><strong>Hwinsta</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-462"><span id="HWINSTA"></span><span id="hwinsta"></span><strong>HWINSTA</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-463">Ein Handle für eine <a href="/windows/desktop/winstation/window-stations">Fenster Station</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-463">A handle to a <a href="/windows/desktop/winstation/window-stations">window station</a>.</span></span></p>
<p><span data-ttu-id="db7a9-464">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-464">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE WINSTA;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-465"><span id="HWND"></span><span id="hwnd"></span><strong>HWND</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-465"><span id="HWND"></span><span id="hwnd"></span><strong>HWND</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-466">Ein Handle für ein <a href="/windows/desktop/winmsg/windows">Fenster</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-466">A handle to a <a href="/windows/desktop/winmsg/windows">window</a>.</span></span></p>
<p><span data-ttu-id="db7a9-467">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-467">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HWND;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-468"><span id="INT"></span><span id="int"></span><strong>Wartenden</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-468"><span id="INT"></span><span id="int"></span><strong>INT</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-469">Eine 32-Bit-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-469">A 32-bit signed integer.</span></span> <span data-ttu-id="db7a9-470">Der Bereich liegt zwischen-2147483648 und 2147483647 Decimal.</span><span class="sxs-lookup"><span data-stu-id="db7a9-470">The range is -2147483648 through 2147483647 decimal.</span></span></p>
<p><span data-ttu-id="db7a9-471">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-471">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef int INT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-472"><span id="INT_PTR"></span><span id="int_ptr"></span><strong>INT_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-472"><span id="INT_PTR"></span><span id="int_ptr"></span><strong>INT_PTR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-473">Ein ganzzahliger Typ mit Vorzeichen für die Zeiger Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="db7a9-473">A signed integer type for pointer precision.</span></span> <span data-ttu-id="db7a9-474">Verwenden Sie, wenn Sie einen Zeiger in eine ganze Zahl umwandeln, um Zeigerarithmetik auszuführen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-474">Use when casting a pointer to an integer to perform pointer arithmetic.</span></span></p>
<p><span data-ttu-id="db7a9-475">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-475">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db7a9-476">C++</span><span class="sxs-lookup"><span data-stu-id="db7a9-476">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64) 
 typedef __int64 INT_PTR; 
#else 
 typedef int INT_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-477"><span id="INT8"></span><span id="int8"></span><strong>Int8</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-477"><span id="INT8"></span><span id="int8"></span><strong>INT8</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-478">Eine 8-Bit-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-478">An 8-bit signed integer.</span></span></p>
<p><span data-ttu-id="db7a9-479">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-479">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed char INT8;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-480"><span id="INT16"></span><span id="int16"></span><strong>INT16</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-480"><span id="INT16"></span><span id="int16"></span><strong>INT16</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-481">Eine 16-Bit-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-481">A 16-bit signed integer.</span></span></p>
<p><span data-ttu-id="db7a9-482">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-482">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed short INT16;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-483"><span id="INT32"></span><span id="int32"></span><strong>Int32</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-483"><span id="INT32"></span><span id="int32"></span><strong>INT32</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-484">Eine 32-Bit-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-484">A 32-bit signed integer.</span></span> <span data-ttu-id="db7a9-485">Der Bereich liegt zwischen-2147483648 und 2147483647 Decimal.</span><span class="sxs-lookup"><span data-stu-id="db7a9-485">The range is -2147483648 through 2147483647 decimal.</span></span></p>
<p><span data-ttu-id="db7a9-486">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-486">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed int INT32;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-487"><span id="INT64"></span><span id="int64"></span><strong>Int64</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-487"><span id="INT64"></span><span id="int64"></span><strong>INT64</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-488">Eine 64-Bit-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-488">A 64-bit signed integer.</span></span> <span data-ttu-id="db7a9-489">Der Bereich ist-9.223.372.036.854.775.808 bis 9223372036854775807 Decimal.</span><span class="sxs-lookup"><span data-stu-id="db7a9-489">The range is -9223372036854775808 through 9223372036854775807 decimal.</span></span></p>
<p><span data-ttu-id="db7a9-490">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-490">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed __int64 INT64;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-491"><span id="LANGID"></span><span id="langid"></span><strong>LANGID</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-491"><span id="LANGID"></span><span id="langid"></span><strong>LANGID</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-492">Eine Sprach-ID.</span><span class="sxs-lookup"><span data-stu-id="db7a9-492">A language identifier.</span></span> <span data-ttu-id="db7a9-493">Weitere Informationen finden Sie unter <a href="/windows/desktop/Intl/language-identifiers">sprach</a>Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="db7a9-493">For more information, see <a href="/windows/desktop/Intl/language-identifiers">Language Identifiers</a>.</span></span></p>
<p><span data-ttu-id="db7a9-494">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-494">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef WORD LANGID;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-495"><span id="LCID"></span><span id="lcid"></span><strong>LCID</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-495"><span id="LCID"></span><span id="lcid"></span><strong>LCID</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-496">Ein Gebiets Schema Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="db7a9-496">A locale identifier.</span></span> <span data-ttu-id="db7a9-497">Weitere Informationen finden Sie unter <a href="/windows/desktop/Intl/locale-identifiers"></a>Gebiets Schema Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="db7a9-497">For more information, see <a href="/windows/desktop/Intl/locale-identifiers">Locale Identifiers</a>.</span></span></p>
<p><span data-ttu-id="db7a9-498">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-498">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef DWORD LCID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-499"><span id="LCTYPE"></span><span id="lctype"></span><strong>LCTYPE</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-499"><span id="LCTYPE"></span><span id="lctype"></span><strong>LCTYPE</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-500">Ein Gebiets Schema Informationstyp.</span><span class="sxs-lookup"><span data-stu-id="db7a9-500">A locale information type.</span></span> <span data-ttu-id="db7a9-501">Eine Liste finden Sie unter Gebiets Schema- <a href="/windows/desktop/Intl/locale-information-constants">Informations Konstanten</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-501">For a list, see <a href="/windows/desktop/Intl/locale-information-constants">Locale Information Constants</a>.</span></span></p>
<p><span data-ttu-id="db7a9-502">Dieser Typ wird in winnls. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-502">This type is declared in WinNls.h as follows:</span></span></p>
<p><code>typedef DWORD LCTYPE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-503"><span id="LGRPID"></span><span id="lgrpid"></span><strong>Lgrpid</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-503"><span id="LGRPID"></span><span id="lgrpid"></span><strong>LGRPID</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-504">Ein Bezeichner für die Sprachgruppe.</span><span class="sxs-lookup"><span data-stu-id="db7a9-504">A language group identifier.</span></span> <span data-ttu-id="db7a9-505">Eine Liste finden Sie unter <a href="/windows/desktop/api/winnls/nf-winnls-enumlanguagegrouplocalesa"><strong>enumlanguagegroupgebiets</strong></a>Schemas.</span><span class="sxs-lookup"><span data-stu-id="db7a9-505">For a list, see <a href="/windows/desktop/api/winnls/nf-winnls-enumlanguagegrouplocalesa"><strong>EnumLanguageGroupLocales</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-506">Dieser Typ wird in winnls. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-506">This type is declared in WinNls.h as follows:</span></span></p>
<p><code>typedef DWORD LGRPID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-507"><span id="LONG"></span><span id="long"></span><strong>Lange</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-507"><span id="LONG"></span><span id="long"></span><strong>LONG</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-508">Eine 32-Bit-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-508">A 32-bit signed integer.</span></span> <span data-ttu-id="db7a9-509">Der Bereich liegt zwischen-2147483648 und 2147483647 Decimal.</span><span class="sxs-lookup"><span data-stu-id="db7a9-509">The range is -2147483648 through 2147483647 decimal.</span></span></p>
<p><span data-ttu-id="db7a9-510">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-510">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef long LONG;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-511"><span id="LONGLONG"></span><span id="longlong"></span><strong>LONGLONG</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-511"><span id="LONGLONG"></span><span id="longlong"></span><strong>LONGLONG</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-512">Eine 64-Bit-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-512">A 64-bit signed integer.</span></span> <span data-ttu-id="db7a9-513">Der Bereich ist-9.223.372.036.854.775.808 bis 9223372036854775807 Decimal.</span><span class="sxs-lookup"><span data-stu-id="db7a9-513">The range is -9223372036854775808 through 9223372036854775807 decimal.</span></span></p>
<p><span data-ttu-id="db7a9-514">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-514">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db7a9-515">C++</span><span class="sxs-lookup"><span data-stu-id="db7a9-515">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if !defined(_M_IX86)
 typedef __int64 LONGLONG; 
#else
 typedef double LONGLONG;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-516"><span id="LONG_PTR"></span><span id="long_ptr"></span><strong>LONG_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-516"><span id="LONG_PTR"></span><span id="long_ptr"></span><strong>LONG_PTR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-517">Ein Long-Typ mit Vorzeichen für die Zeiger Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="db7a9-517">A signed long type for pointer precision.</span></span> <span data-ttu-id="db7a9-518">Verwenden Sie, wenn Sie einen Zeiger in eine Länge umwandeln, um Zeigerarithmetik auszuführen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-518">Use when casting a pointer to a long to perform pointer arithmetic.</span></span></p>
<p><span data-ttu-id="db7a9-519">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-519">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db7a9-520">C++</span><span class="sxs-lookup"><span data-stu-id="db7a9-520">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64)
 typedef __int64 LONG_PTR; 
#else
 typedef long LONG_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-521"><span id="LONG32"></span><span id="long32"></span><strong>LONG32</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-521"><span id="LONG32"></span><span id="long32"></span><strong>LONG32</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-522">Eine 32-Bit-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-522">A 32-bit signed integer.</span></span> <span data-ttu-id="db7a9-523">Der Bereich liegt zwischen-2147483648 und 2147483647 Decimal.</span><span class="sxs-lookup"><span data-stu-id="db7a9-523">The range is -2147483648 through 2147483647 decimal.</span></span></p>
<p><span data-ttu-id="db7a9-524">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-524">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed int LONG32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-525"><span id="LONG64"></span><span id="long64"></span><strong>LONG64</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-525"><span id="LONG64"></span><span id="long64"></span><strong>LONG64</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-526">Eine 64-Bit-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-526">A 64-bit signed integer.</span></span> <span data-ttu-id="db7a9-527">Der Bereich ist-9.223.372.036.854.775.808 bis 9223372036854775807 Decimal.</span><span class="sxs-lookup"><span data-stu-id="db7a9-527">The range is -9223372036854775808 through 9223372036854775807 decimal.</span></span></p>
<p><span data-ttu-id="db7a9-528">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-528">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef __int64 LONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-529"><span id="LPARAM"></span><span id="lparam"></span><strong>LParam</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-529"><span id="LPARAM"></span><span id="lparam"></span><strong>LPARAM</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-530">Ein Meldungs Parameter.</span><span class="sxs-lookup"><span data-stu-id="db7a9-530">A message parameter.</span></span></p>
<p><span data-ttu-id="db7a9-531">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-531">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef LONG_PTR LPARAM;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-532"><span id="LPBOOL"></span><span id="lpbool"></span><strong>LPBOOL</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-532"><span id="LPBOOL"></span><span id="lpbool"></span><strong>LPBOOL</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-533">Ein Zeiger auf einen <a href="#bool"><strong>bool</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-533">A pointer to a <a href="#bool"><strong>BOOL</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-534">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-534">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef BOOL far *LPBOOL;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-535"><span id="LPBYTE"></span><span id="lpbyte"></span><strong>LPBYTE</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-535"><span id="LPBYTE"></span><span id="lpbyte"></span><strong>LPBYTE</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-536">Ein Zeiger auf ein <a href="#byte"><strong>Byte</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-536">A pointer to a <a href="#byte"><strong>BYTE</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-537">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-537">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef BYTE far *LPBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-538"><span id="LPCOLORREF"></span><span id="lpcolorref"></span><strong>Lpcolorref</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-538"><span id="LPCOLORREF"></span><span id="lpcolorref"></span><strong>LPCOLORREF</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-539">Ein Zeiger auf einen <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> -Wert.</span><span class="sxs-lookup"><span data-stu-id="db7a9-539">A pointer to a <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> value.</span></span></p>
<p><span data-ttu-id="db7a9-540">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-540">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef DWORD *LPCOLORREF;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-541"><span id="LPCSTR"></span><span id="lpcstr"></span><strong>LPCSTR</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-541"><span id="LPCSTR"></span><span id="lpcstr"></span><strong>LPCSTR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-542">Ein Zeiger auf eine Konstante mit NULL endende Zeichenfolge von 8-Bit-Windows-Zeichen (ANSI).</span><span class="sxs-lookup"><span data-stu-id="db7a9-542">A pointer to a constant null-terminated string of 8-bit Windows (ANSI) characters.</span></span> <span data-ttu-id="db7a9-543">Weitere Informationen finden Sie unter <a href="/windows/desktop/gdi/character-sets-used-by-fonts">von Schriftarten verwendete Zeichensätze</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-543">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="db7a9-544">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-544">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef __nullterminated CONST CHAR *LPCSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-545"><span id="LPCTSTR"></span><span id="lpctstr"></span><strong>LPCTSTR</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-545"><span id="LPCTSTR"></span><span id="lpctstr"></span><strong>LPCTSTR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-546">Ein <a href="#lpcwstr"><strong>LPCWSTR</strong></a> , wenn <strong>Unicode</strong> definiert ist, andernfalls ein <a href="#lpcstr"><strong>LPCSTR</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="db7a9-546">An <a href="#lpcwstr"><strong>LPCWSTR</strong></a> if <strong>UNICODE</strong> is defined, an <a href="#lpcstr"><strong>LPCSTR</strong></a> otherwise.</span></span> <span data-ttu-id="db7a9-547">Weitere Informationen finden Sie unter <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows-Datentypen für</a>Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-547">For more information, see <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Data Types for Strings</a>.</span></span></p>
<p><span data-ttu-id="db7a9-548">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-548">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db7a9-549">C++</span><span class="sxs-lookup"><span data-stu-id="db7a9-549">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef LPCWSTR LPCTSTR; 
#else
 typedef LPCSTR LPCTSTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-550"><span id="LPCVOID"></span><span id="lpcvoid"></span><strong>Lpcvoid</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-550"><span id="LPCVOID"></span><span id="lpcvoid"></span><strong>LPCVOID</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-551">Ein Zeiger auf eine Konstante eines beliebigen Typs.</span><span class="sxs-lookup"><span data-stu-id="db7a9-551">A pointer to a constant of any type.</span></span></p>
<p><span data-ttu-id="db7a9-552">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-552">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef CONST void *LPCVOID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-553"><span id="LPCWSTR"></span><span id="lpcwstr"></span><strong>LPCWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-553"><span id="LPCWSTR"></span><span id="lpcwstr"></span><strong>LPCWSTR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-554">Ein Zeiger auf eine Konstante mit NULL endenden Zeichenfolge aus 16-Bit-Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-554">A pointer to a constant null-terminated string of 16-bit Unicode characters.</span></span> <span data-ttu-id="db7a9-555">Weitere Informationen finden Sie unter <a href="/windows/desktop/gdi/character-sets-used-by-fonts">von Schriftarten verwendete Zeichensätze</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-555">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="db7a9-556">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-556">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CONST WCHAR *LPCWSTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-557"><span id="LPDWORD"></span><span id="lpdword"></span><strong>LPDWORD</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-557"><span id="LPDWORD"></span><span id="lpdword"></span><strong>LPDWORD</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-558">Ein Zeiger auf ein <a href="#dword"><strong>DWORD</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-558">A pointer to a <a href="#dword"><strong>DWORD</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-559">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-559">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef DWORD *LPDWORD;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-560"><span id="LPHANDLE"></span><span id="lphandle"></span><strong>Lphandle</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-560"><span id="LPHANDLE"></span><span id="lphandle"></span><strong>LPHANDLE</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-561">Ein Zeiger auf ein <a href="#handle"><strong>handle</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-561">A pointer to a <a href="#handle"><strong>HANDLE</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-562">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-562">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE *LPHANDLE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-563"><span id="LPINT"></span><span id="lpint"></span><strong>Lpint</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-563"><span id="LPINT"></span><span id="lpint"></span><strong>LPINT</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-564">Ein Zeiger auf einen <a href="#int"><strong>int</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-564">A pointer to an <a href="#int"><strong>INT</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-565">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-565">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef int *LPINT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-566"><span id="LPLONG"></span><span id="lplong"></span><strong>Lplong</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-566"><span id="LPLONG"></span><span id="lplong"></span><strong>LPLONG</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-567">Ein Zeiger auf einen <a href="#long"><strong>Long</strong></a>-.</span><span class="sxs-lookup"><span data-stu-id="db7a9-567">A pointer to a <a href="#long"><strong>LONG</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-568">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-568">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef long *LPLONG;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-569"><span id="LPSTR"></span><span id="lpstr"></span><strong>LPSTR</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-569"><span id="LPSTR"></span><span id="lpstr"></span><strong>LPSTR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-570">Ein Zeiger auf eine auf NULL endende Zeichenfolge von 8-Bit-Windows-Zeichen (ANSI).</span><span class="sxs-lookup"><span data-stu-id="db7a9-570">A pointer to a null-terminated string of 8-bit Windows (ANSI) characters.</span></span> <span data-ttu-id="db7a9-571">Weitere Informationen finden Sie unter <a href="/windows/desktop/gdi/character-sets-used-by-fonts">von Schriftarten verwendete Zeichensätze</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-571">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="db7a9-572">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-572">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CHAR *LPSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-573"><span id="LPTSTR"></span><span id="lptstr"></span><strong>LPTSTR</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-573"><span id="LPTSTR"></span><span id="lptstr"></span><strong>LPTSTR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-574">Ein <a href="#lpwstr"><strong>LPWSTR</strong></a> , wenn <strong>Unicode</strong> definiert ist, andernfalls ein <a href="#lpstr"><strong>LPSTR</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="db7a9-574">An <a href="#lpwstr"><strong>LPWSTR</strong></a> if <strong>UNICODE</strong> is defined, an <a href="#lpstr"><strong>LPSTR</strong></a> otherwise.</span></span> <span data-ttu-id="db7a9-575">Weitere Informationen finden Sie unter <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows-Datentypen für</a>Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-575">For more information, see <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Data Types for Strings</a>.</span></span></p>
<p><span data-ttu-id="db7a9-576">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-576">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db7a9-577">C++</span><span class="sxs-lookup"><span data-stu-id="db7a9-577">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef LPWSTR LPTSTR;
#else
 typedef LPSTR LPTSTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-578"><span id="LPVOID"></span><span id="lpvoid"></span><strong>LPVOID</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-578"><span id="LPVOID"></span><span id="lpvoid"></span><strong>LPVOID</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-579">Ein Zeiger auf einen beliebigen Typ.</span><span class="sxs-lookup"><span data-stu-id="db7a9-579">A pointer to any type.</span></span></p>
<p><span data-ttu-id="db7a9-580">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-580">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef void *LPVOID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-581"><span id="LPWORD"></span><span id="lpword"></span><strong>Lpword</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-581"><span id="LPWORD"></span><span id="lpword"></span><strong>LPWORD</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-582">Ein Zeiger auf ein <a href="#word"><strong>Wort</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-582">A pointer to a <a href="#word"><strong>WORD</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-583">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-583">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef WORD *LPWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-584"><span id="LPWSTR"></span><span id="lpwstr"></span><strong>LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-584"><span id="LPWSTR"></span><span id="lpwstr"></span><strong>LPWSTR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-585">Ein Zeiger auf eine NULL-terminierte Zeichenfolge aus 16-Bit-Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-585">A pointer to a null-terminated string of 16-bit Unicode characters.</span></span> <span data-ttu-id="db7a9-586">Weitere Informationen finden Sie unter <a href="/windows/desktop/gdi/character-sets-used-by-fonts">von Schriftarten verwendete Zeichensätze</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-586">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="db7a9-587">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-587">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef WCHAR *LPWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-588"><span id="LRESULT"></span><span id="lresult"></span><strong>LRESULT</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-588"><span id="LRESULT"></span><span id="lresult"></span><strong>LRESULT</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-589">Signiertes Ergebnis der Nachrichtenverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="db7a9-589">Signed result of message processing.</span></span></p>
<p><span data-ttu-id="db7a9-590">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-590">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef LONG_PTR LRESULT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-591"><span id="PBOOL"></span><span id="pbool"></span><strong>Pbool</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-591"><span id="PBOOL"></span><span id="pbool"></span><strong>PBOOL</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-592">Ein Zeiger auf einen <a href="#bool"><strong>bool</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-592">A pointer to a <a href="#bool"><strong>BOOL</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-593">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-593">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef BOOL *PBOOL;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-594"><span id="PBOOLEAN"></span><span id="pboolean"></span><strong>Pboolescher Wert</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-594"><span id="PBOOLEAN"></span><span id="pboolean"></span><strong>PBOOLEAN</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-595">Ein Zeiger auf einen <a href="#boolean"><strong>booleschen</strong></a>Wert.</span><span class="sxs-lookup"><span data-stu-id="db7a9-595">A pointer to a <a href="#boolean"><strong>BOOLEAN</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-596">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-596">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef BOOLEAN *PBOOLEAN;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-597"><span id="PBYTE"></span><span id="pbyte"></span><strong>PBYTE</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-597"><span id="PBYTE"></span><span id="pbyte"></span><strong>PBYTE</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-598">Ein Zeiger auf ein <a href="#byte"><strong>Byte</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-598">A pointer to a <a href="#byte"><strong>BYTE</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-599">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-599">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef BYTE *PBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-600"><span id="PCHAR"></span><span id="pchar"></span><strong>PChar</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-600"><span id="PCHAR"></span><span id="pchar"></span><strong>PCHAR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-601">Ein Zeiger auf ein <a href="#char"><strong>char</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-601">A pointer to a <a href="#char"><strong>CHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-602">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-602">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CHAR *PCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-603"><span id="PCSTR"></span><span id="pcstr"></span><strong>Pcstr</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-603"><span id="PCSTR"></span><span id="pcstr"></span><strong>PCSTR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-604">Ein Zeiger auf eine Konstante mit NULL endende Zeichenfolge von 8-Bit-Windows-Zeichen (ANSI).</span><span class="sxs-lookup"><span data-stu-id="db7a9-604">A pointer to a constant null-terminated string of 8-bit Windows (ANSI) characters.</span></span> <span data-ttu-id="db7a9-605">Weitere Informationen finden Sie unter <a href="/windows/desktop/gdi/character-sets-used-by-fonts">von Schriftarten verwendete Zeichensätze</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-605">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="db7a9-606">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-606">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CONST CHAR *PCSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-607"><span id="PCTSTR"></span><span id="pctstr"></span><strong>Pctstr</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-607"><span id="PCTSTR"></span><span id="pctstr"></span><strong>PCTSTR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-608">Ein <a href="#pcwstr"><strong>pcwstr</strong></a> , wenn <strong>Unicode</strong> definiert ist, andernfalls ein <a href="#pcstr"><strong>pcstr</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="db7a9-608">A <a href="#pcwstr"><strong>PCWSTR</strong></a> if <strong>UNICODE</strong> is defined, a <a href="#pcstr"><strong>PCSTR</strong></a> otherwise.</span></span> <span data-ttu-id="db7a9-609">Weitere Informationen finden Sie unter <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows-Datentypen für</a>Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-609">For more information, see <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Data Types for Strings</a>.</span></span></p>
<p><span data-ttu-id="db7a9-610">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-610">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db7a9-611">C++</span><span class="sxs-lookup"><span data-stu-id="db7a9-611">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef LPCWSTR PCTSTR;
#else
 typedef LPCSTR PCTSTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-612"><span id="PCWSTR"></span><span id="pcwstr"></span><strong>PCWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-612"><span id="PCWSTR"></span><span id="pcwstr"></span><strong>PCWSTR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-613">Ein Zeiger auf eine Konstante mit NULL endenden Zeichenfolge aus 16-Bit-Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-613">A pointer to a constant null-terminated string of 16-bit Unicode characters.</span></span> <span data-ttu-id="db7a9-614">Weitere Informationen finden Sie unter <a href="/windows/desktop/gdi/character-sets-used-by-fonts">von Schriftarten verwendete Zeichensätze</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-614">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="db7a9-615">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-615">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CONST WCHAR *PCWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-616"><span id="PDWORD"></span><span id="pdword"></span><strong>PDWORD</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-616"><span id="PDWORD"></span><span id="pdword"></span><strong>PDWORD</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-617">Ein Zeiger auf ein <a href="#dword"><strong>DWORD</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-617">A pointer to a <a href="#dword"><strong>DWORD</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-618">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-618">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef DWORD *PDWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-619"><span id="PDWORDLONG"></span><span id="pdwordlong"></span><strong>Pdwordlong</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-619"><span id="PDWORDLONG"></span><span id="pdwordlong"></span><strong>PDWORDLONG</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-620">Ein Zeiger auf <a href="#dwordlong"><strong>dwordlong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-620">A pointer to a <a href="#dwordlong"><strong>DWORDLONG</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-621">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-621">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef DWORDLONG *PDWORDLONG;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-622"><span id="PDWORD_PTR"></span><span id="pdword_ptr"></span><strong>PDWORD_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-622"><span id="PDWORD_PTR"></span><span id="pdword_ptr"></span><strong>PDWORD_PTR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-623">Ein Zeiger auf einen <a href="#dword_ptr"><strong>DWORD_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-623">A pointer to a <a href="#dword_ptr"><strong>DWORD_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-624">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-624">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef DWORD_PTR *PDWORD_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-625"><span id="PDWORD32"></span><span id="pdword32"></span><strong>PDWORD32</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-625"><span id="PDWORD32"></span><span id="pdword32"></span><strong>PDWORD32</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-626">Ein Zeiger auf eine <a href="#dword32"><strong>DWORD32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-626">A pointer to a <a href="#dword32"><strong>DWORD32</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-627">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-627">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef DWORD32 *PDWORD32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-628"><span id="PDWORD64"></span><span id="pdword64"></span><strong>PDWORD64</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-628"><span id="PDWORD64"></span><span id="pdword64"></span><strong>PDWORD64</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-629">Ein Zeiger auf eine <a href="#dword64"><strong>DWORD64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-629">A pointer to a <a href="#dword64"><strong>DWORD64</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-630">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-630">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef DWORD64 *PDWORD64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-631"><span id="PFLOAT"></span><span id="pfloat"></span><strong>Pfloat</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-631"><span id="PFLOAT"></span><span id="pfloat"></span><strong>PFLOAT</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-632">Ein Zeiger auf einen <a href="#float"><strong>float</strong></a>-Wert.</span><span class="sxs-lookup"><span data-stu-id="db7a9-632">A pointer to a <a href="#float"><strong>FLOAT</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-633">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-633">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef FLOAT *PFLOAT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-634"><span id="PHALF_PTR"></span><span id="phalf_ptr"></span><strong>PHALF_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-634"><span id="PHALF_PTR"></span><span id="phalf_ptr"></span><strong>PHALF_PTR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-635">Ein Zeiger auf einen <a href="#half_ptr"><strong>HALF_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-635">A pointer to a <a href="#half_ptr"><strong>HALF_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-636">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-636">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db7a9-637">C++</span><span class="sxs-lookup"><span data-stu-id="db7a9-637">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef _WIN64
 typedef HALF_PTR *PHALF_PTR;
#else
 typedef HALF_PTR *PHALF_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-638"><span id="PHANDLE"></span><span id="phandle"></span><strong>Phandle</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-638"><span id="PHANDLE"></span><span id="phandle"></span><strong>PHANDLE</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-639">Ein Zeiger auf ein <a href="#handle"><strong>handle</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-639">A pointer to a <a href="#handle"><strong>HANDLE</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-640">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-640">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef HANDLE *PHANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-641"><span id="PHKEY"></span><span id="phkey"></span><strong>Phkey</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-641"><span id="PHKEY"></span><span id="phkey"></span><strong>PHKEY</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-642">Ein Zeiger auf einen <a href="#hkey"><strong>HKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-642">A pointer to an <a href="#hkey"><strong>HKEY</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-643">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-643">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HKEY *PHKEY;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-644"><span id="PINT"></span><span id="pint"></span><strong>Zeigen</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-644"><span id="PINT"></span><span id="pint"></span><strong>PINT</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-645">Ein Zeiger auf einen <a href="#int"><strong>int</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-645">A pointer to an <a href="#int"><strong>INT</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-646">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-646">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef int *PINT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-647"><span id="PINT_PTR"></span><span id="pint_ptr"></span><strong>PINT_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-647"><span id="PINT_PTR"></span><span id="pint_ptr"></span><strong>PINT_PTR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-648">Ein Zeiger auf einen <a href="#int_ptr"><strong>INT_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-648">A pointer to an <a href="#int_ptr"><strong>INT_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-649">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-649">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT_PTR *PINT_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-650"><span id="PINT8"></span><span id="pint8"></span><strong>PINT8</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-650"><span id="PINT8"></span><span id="pint8"></span><strong>PINT8</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-651">Ein Zeiger auf eine <a href="#int8"><strong>int8</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-651">A pointer to an <a href="#int8"><strong>INT8</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-652">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-652">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT8 *PINT8;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-653"><span id="PINT16"></span><span id="pint16"></span><strong>PINT16</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-653"><span id="PINT16"></span><span id="pint16"></span><strong>PINT16</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-654">Ein Zeiger auf eine <a href="#int16"><strong>INT16</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-654">A pointer to an <a href="#int16"><strong>INT16</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-655">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-655">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT16 *PINT16;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-656"><span id="PINT32"></span><span id="pint32"></span><strong>PINT32</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-656"><span id="PINT32"></span><span id="pint32"></span><strong>PINT32</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-657">Ein Zeiger auf eine <a href="#int32"><strong>Int32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-657">A pointer to an <a href="#int32"><strong>INT32</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-658">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-658">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT32 *PINT32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-659"><span id="PINT64"></span><span id="pint64"></span><strong>PINT64</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-659"><span id="PINT64"></span><span id="pint64"></span><strong>PINT64</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-660">Ein Zeiger auf eine <a href="#int64"><strong>Int64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-660">A pointer to an <a href="#int64"><strong>INT64</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-661">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-661">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT64 *PINT64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-662"><span id="PLCID"></span><span id="plcid"></span><strong>Plcid</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-662"><span id="PLCID"></span><span id="plcid"></span><strong>PLCID</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-663">Ein Zeiger auf eine <a href="#lcid"><strong>LCID</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-663">A pointer to an <a href="#lcid"><strong>LCID</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-664">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-664">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef PDWORD PLCID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-665"><span id="PLONG"></span><span id="plong"></span><strong>Plong</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-665"><span id="PLONG"></span><span id="plong"></span><strong>PLONG</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-666">Ein Zeiger auf einen <a href="#long"><strong>Long</strong></a>-.</span><span class="sxs-lookup"><span data-stu-id="db7a9-666">A pointer to a <a href="#long"><strong>LONG</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-667">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-667">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef LONG *PLONG;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-668"><span id="PLONGLONG"></span><span id="plonglong"></span><strong>Plonglong</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-668"><span id="PLONGLONG"></span><span id="plonglong"></span><strong>PLONGLONG</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-669">Ein Zeiger auf einen <a href="#longlong"><strong>Longlong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-669">A pointer to a <a href="#longlong"><strong>LONGLONG</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-670">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-670">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef LONGLONG *PLONGLONG;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-671"><span id="PLONG_PTR"></span><span id="plong_ptr"></span><strong>PLONG_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-671"><span id="PLONG_PTR"></span><span id="plong_ptr"></span><strong>PLONG_PTR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-672">Ein Zeiger auf einen <a href="#long_ptr"><strong>LONG_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-672">A pointer to a <a href="#long_ptr"><strong>LONG_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-673">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-673">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef LONG_PTR *PLONG_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-674"><span id="PLONG32"></span><span id="plong32"></span><strong>PLONG32</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-674"><span id="PLONG32"></span><span id="plong32"></span><strong>PLONG32</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-675">Ein Zeiger auf eine <a href="#long32"><strong>LONG32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-675">A pointer to a <a href="#long32"><strong>LONG32</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-676">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-676">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef LONG32 *PLONG32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-677"><span id="PLONG64"></span><span id="plong64"></span><strong>PLONG64</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-677"><span id="PLONG64"></span><span id="plong64"></span><strong>PLONG64</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-678">Ein Zeiger auf eine <a href="#long64"><strong>LONG64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-678">A pointer to a <a href="#long64"><strong>LONG64</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-679">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-679">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef LONG64 *PLONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-680"><span id="POINTER_32"></span><span id="pointer_32"></span><strong>POINTER_32</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-680"><span id="POINTER_32"></span><span id="pointer_32"></span><strong>POINTER_32</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-681">Ein 32-Bit-Zeiger.</span><span class="sxs-lookup"><span data-stu-id="db7a9-681">A 32-bit pointer.</span></span> <span data-ttu-id="db7a9-682">Bei einem 32-Bit-System handelt es sich hierbei um einen nativen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="db7a9-682">On a 32-bit system, this is a native pointer.</span></span> <span data-ttu-id="db7a9-683">Bei einem 64-Bit-System handelt es sich hierbei um einen abgeschnittene 64-Bit-Zeiger.</span><span class="sxs-lookup"><span data-stu-id="db7a9-683">On a 64-bit system, this is a truncated 64-bit pointer.</span></span></p>
<p><span data-ttu-id="db7a9-684">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-684">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db7a9-685">C++</span><span class="sxs-lookup"><span data-stu-id="db7a9-685">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64)
#define POINTER_32 __ptr32
#else
#define POINTER_32
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-686"><span id="POINTER_64"></span><span id="pointer_64"></span><strong>POINTER_64</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-686"><span id="POINTER_64"></span><span id="pointer_64"></span><strong>POINTER_64</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-687">Ein 64-Bit-Zeiger.</span><span class="sxs-lookup"><span data-stu-id="db7a9-687">A 64-bit pointer.</span></span> <span data-ttu-id="db7a9-688">Bei einem 64-Bit-System handelt es sich hierbei um einen nativen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="db7a9-688">On a 64-bit system, this is a native pointer.</span></span> <span data-ttu-id="db7a9-689">Auf einem 32-Bit-System ist dies ein mit Vorzeichen erweiterter 32-Bit-Zeiger.</span><span class="sxs-lookup"><span data-stu-id="db7a9-689">On a 32-bit system, this is a sign-extended 32-bit pointer.</span></span></p>
<p><span data-ttu-id="db7a9-690">Beachten Sie, dass es nicht sicher ist, dass der Status des hohen Zeiger Bits angenommen wird.</span><span class="sxs-lookup"><span data-stu-id="db7a9-690">Note that it is not safe to assume the state of the high pointer bit.</span></span></p>
<p><span data-ttu-id="db7a9-691">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-691">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db7a9-692">C++</span><span class="sxs-lookup"><span data-stu-id="db7a9-692">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if (_MSC_VER >= 1300)
#define POINTER_64 __ptr64
#else
#define POINTER_64
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-693"><span id="POINTER_SIGNED"></span><span id="pointer_signed"></span><strong>POINTER_SIGNED</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-693"><span id="POINTER_SIGNED"></span><span id="pointer_signed"></span><strong>POINTER_SIGNED</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-694">Ein Zeiger mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-694">A signed pointer.</span></span></p>
<p><span data-ttu-id="db7a9-695">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-695">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>#define POINTER_SIGNED __sptr</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-696"><span id="POINTER_UNSIGNED"></span><span id="pointer_unsigned"></span><strong>POINTER_UNSIGNED</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-696"><span id="POINTER_UNSIGNED"></span><span id="pointer_unsigned"></span><strong>POINTER_UNSIGNED</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-697">Ein Zeiger ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-697">An unsigned pointer.</span></span></p>
<p><span data-ttu-id="db7a9-698">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-698">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>#define POINTER_UNSIGNED __uptr</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-699"><span id="PSHORT"></span><span id="pshort"></span><strong>Pshort</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-699"><span id="PSHORT"></span><span id="pshort"></span><strong>PSHORT</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-700">Ein Zeiger auf einen <a href="#short"><strong>kurzen</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-700">A pointer to a <a href="#short"><strong>SHORT</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-701">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-701">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef SHORT *PSHORT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-702"><span id="PSIZE_T"></span><span id="psize_t"></span><strong>PSIZE_T</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-702"><span id="PSIZE_T"></span><span id="psize_t"></span><strong>PSIZE_T</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-703">Ein Zeiger auf einen <a href="#size_t"><strong>size_t</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-703">A pointer to a <a href="#size_t"><strong>SIZE_T</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-704">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-704">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef SIZE_T *PSIZE_T;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-705"><span id="PSSIZE_T"></span><span id="pssize_t"></span><strong>PSSIZE_T</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-705"><span id="PSSIZE_T"></span><span id="pssize_t"></span><strong>PSSIZE_T</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-706">Ein Zeiger auf einen <a href="#ssize_t"><strong>SSIZE_T</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-706">A pointer to a <a href="#ssize_t"><strong>SSIZE_T</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-707">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-707">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef SSIZE_T *PSSIZE_T;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-708"><span id="PSTR"></span><span id="pstr"></span><strong>Pstr</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-708"><span id="PSTR"></span><span id="pstr"></span><strong>PSTR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-709">Ein Zeiger auf eine auf NULL endende Zeichenfolge von 8-Bit-Windows-Zeichen (ANSI).</span><span class="sxs-lookup"><span data-stu-id="db7a9-709">A pointer to a null-terminated string of 8-bit Windows (ANSI) characters.</span></span> <span data-ttu-id="db7a9-710">Weitere Informationen finden Sie unter <a href="/windows/desktop/gdi/character-sets-used-by-fonts">von Schriftarten verwendete Zeichensätze</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-710">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="db7a9-711">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-711">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CHAR *PSTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-712"><span id="PTBYTE"></span><span id="ptbyte"></span><strong>Ptbyte</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-712"><span id="PTBYTE"></span><span id="ptbyte"></span><strong>PTBYTE</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-713">Ein Zeiger auf ein <a href="#tbyte"><strong>TByte</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-713">A pointer to a <a href="#tbyte"><strong>TBYTE</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-714">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-714">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef TBYTE *PTBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-715"><span id="PTCHAR"></span><span id="ptchar"></span><strong>Ptchar</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-715"><span id="PTCHAR"></span><span id="ptchar"></span><strong>PTCHAR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-716">Ein Zeiger auf einen <a href="#tchar"><strong>TCHAR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-716">A pointer to a <a href="#tchar"><strong>TCHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-717">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-717">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef TCHAR *PTCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-718"><span id="PTSTR"></span><span id="ptstr"></span><strong>Ptstr</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-718"><span id="PTSTR"></span><span id="ptstr"></span><strong>PTSTR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-719">Ein <a href="#pwstr"><strong>pwstr</strong></a> , wenn <strong>Unicode</strong> definiert ist, andernfalls ein <a href="#pstr"><strong>Pstr</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="db7a9-719">A <a href="#pwstr"><strong>PWSTR</strong></a> if <strong>UNICODE</strong> is defined, a <a href="#pstr"><strong>PSTR</strong></a> otherwise.</span></span> <span data-ttu-id="db7a9-720">Weitere Informationen finden Sie unter <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows-Datentypen für</a>Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-720">For more information, see <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Data Types for Strings</a>.</span></span></p>
<p><span data-ttu-id="db7a9-721">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-721">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db7a9-722">C++</span><span class="sxs-lookup"><span data-stu-id="db7a9-722">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef LPWSTR PTSTR;
#else typedef LPSTR PTSTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-723"><span id="PUCHAR"></span><span id="puchar"></span><strong>Puchar</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-723"><span id="PUCHAR"></span><span id="puchar"></span><strong>PUCHAR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-724">Ein Zeiger auf einen <a href="#uchar"><strong>UCHAR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-724">A pointer to a <a href="#uchar"><strong>UCHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-725">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-725">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef UCHAR *PUCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-726"><span id="PUHALF_PTR"></span><span id="puhalf_ptr"></span><strong>PUHALF_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-726"><span id="PUHALF_PTR"></span><span id="puhalf_ptr"></span><strong>PUHALF_PTR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-727">Ein Zeiger auf einen <a href="#uhalf_ptr"><strong>UHALF_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-727">A pointer to a <a href="#uhalf_ptr"><strong>UHALF_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-728">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-728">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db7a9-729">C++</span><span class="sxs-lookup"><span data-stu-id="db7a9-729">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef _WIN64
 typedef UHALF_PTR *PUHALF_PTR;
#else
 typedef UHALF_PTR *PUHALF_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-730"><span id="PUINT"></span><span id="puint"></span><strong>Puint</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-730"><span id="PUINT"></span><span id="puint"></span><strong>PUINT</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-731">Ein Zeiger auf einen <a href="#uint"><strong>uint</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-731">A pointer to a <a href="#uint"><strong>UINT</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-732">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-732">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef UINT *PUINT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-733"><span id="PUINT_PTR"></span><span id="puint_ptr"></span><strong>PUINT_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-733"><span id="PUINT_PTR"></span><span id="puint_ptr"></span><strong>PUINT_PTR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-734">Ein Zeiger auf einen <a href="#uint_ptr"><strong>UINT_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-734">A pointer to a <a href="#uint_ptr"><strong>UINT_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-735">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-735">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT_PTR *PUINT_PTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-736"><span id="PUINT8"></span><span id="puint8"></span><strong>PUINT8</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-736"><span id="PUINT8"></span><span id="puint8"></span><strong>PUINT8</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-737">Ein Zeiger auf eine <a href="#uint8"><strong>Uint8</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-737">A pointer to a <a href="#uint8"><strong>UINT8</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-738">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-738">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT8 *PUINT8;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-739"><span id="PUINT16"></span><span id="puint16"></span><strong>PUINT16</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-739"><span id="PUINT16"></span><span id="puint16"></span><strong>PUINT16</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-740">Ein Zeiger auf eine <a href="#uint16"><strong>UInt16</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-740">A pointer to a <a href="#uint16"><strong>UINT16</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-741">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-741">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT16 *PUINT16;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-742"><span id="PUINT32"></span><span id="puint32"></span><strong>PUINT32</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-742"><span id="PUINT32"></span><span id="puint32"></span><strong>PUINT32</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-743">Ein Zeiger auf eine <a href="#uint32"><strong>UInt32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-743">A pointer to a <a href="#uint32"><strong>UINT32</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-744">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-744">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT32 *PUINT32;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-745"><span id="PUINT64"></span><span id="puint64"></span><strong>PUINT64</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-745"><span id="PUINT64"></span><span id="puint64"></span><strong>PUINT64</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-746">Ein Zeiger auf eine <a href="#uint64"><strong>UINT64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-746">A pointer to a <a href="#uint64"><strong>UINT64</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-747">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-747">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT64 *PUINT64;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-748"><span id="PULONG"></span><span id="pulong"></span><strong>Pulong</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-748"><span id="PULONG"></span><span id="pulong"></span><strong>PULONG</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-749">Ein Zeiger auf einen <a href="#ulong"><strong>ulong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-749">A pointer to a <a href="#ulong"><strong>ULONG</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-750">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-750">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef ULONG *PULONG;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-751"><span id="PULONGLONG"></span><span id="pulonglong"></span><strong>Pulonglong</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-751"><span id="PULONGLONG"></span><span id="pulonglong"></span><strong>PULONGLONG</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-752">Ein Zeiger auf einen <a href="#ulonglong"><strong>ULONGLONG</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-752">A pointer to a <a href="#ulonglong"><strong>ULONGLONG</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-753">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-753">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef ULONGLONG *PULONGLONG;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-754"><span id="PULONG_PTR"></span><span id="pulong_ptr"></span><strong>PULONG_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-754"><span id="PULONG_PTR"></span><span id="pulong_ptr"></span><strong>PULONG_PTR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-755">Ein Zeiger auf einen <a href="#ulong_ptr"><strong>ULONG_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-755">A pointer to a <a href="#ulong_ptr"><strong>ULONG_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-756">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-756">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef ULONG_PTR *PULONG_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-757"><span id="PULONG32"></span><span id="pulong32"></span><strong>PULONG32</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-757"><span id="PULONG32"></span><span id="pulong32"></span><strong>PULONG32</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-758">Ein Zeiger auf eine <a href="#ulong32"><strong>ULONG32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-758">A pointer to a <a href="#ulong32"><strong>ULONG32</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-759">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-759">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef ULONG32 *PULONG32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-760"><span id="PULONG64"></span><span id="pulong64"></span><strong>PULONG64</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-760"><span id="PULONG64"></span><span id="pulong64"></span><strong>PULONG64</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-761">Ein Zeiger auf eine <a href="#ulong64"><strong>ULONG64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-761">A pointer to a <a href="#ulong64"><strong>ULONG64</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-762">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-762">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef ULONG64 *PULONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-763"><span id="PUSHORT"></span><span id="pushort"></span><strong>Pushort</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-763"><span id="PUSHORT"></span><span id="pushort"></span><strong>PUSHORT</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-764">Ein Zeiger auf einen <a href="#ushort"><strong>UShort</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-764">A pointer to a <a href="#ushort"><strong>USHORT</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-765">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-765">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef USHORT *PUSHORT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-766"><span id="PVOID"></span><span id="pvoid"></span><strong>PVoid</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-766"><span id="PVOID"></span><span id="pvoid"></span><strong>PVOID</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-767">Ein Zeiger auf einen beliebigen Typ.</span><span class="sxs-lookup"><span data-stu-id="db7a9-767">A pointer to any type.</span></span></p>
<p><span data-ttu-id="db7a9-768">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-768">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef void *PVOID;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-769"><span id="PWCHAR"></span><span id="pwchar"></span><strong>Pwchar</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-769"><span id="PWCHAR"></span><span id="pwchar"></span><strong>PWCHAR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-770">Ein Zeiger auf ein <a href="#wchar"><strong>WCHAR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-770">A pointer to a <a href="#wchar"><strong>WCHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-771">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-771">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef WCHAR *PWCHAR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-772"><span id="PWORD"></span><span id="pword"></span><strong>PWORD</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-772"><span id="PWORD"></span><span id="pword"></span><strong>PWORD</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-773">Ein Zeiger auf ein <a href="#word"><strong>Wort</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-773">A pointer to a <a href="#word"><strong>WORD</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-774">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-774">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef WORD *PWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-775"><span id="PWSTR"></span><span id="pwstr"></span><strong>Pwstr</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-775"><span id="PWSTR"></span><span id="pwstr"></span><strong>PWSTR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-776">Ein Zeiger auf eine NULL-terminierte Zeichenfolge aus 16-Bit-Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-776">A pointer to a null-terminated string of 16-bit Unicode characters.</span></span> <span data-ttu-id="db7a9-777">Weitere Informationen finden Sie unter <a href="/windows/desktop/gdi/character-sets-used-by-fonts">von Schriftarten verwendete Zeichensätze</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-777">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="db7a9-778">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-778">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef WCHAR *PWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-779"><span id="QWORD"></span><span id="qword"></span><strong>QWord</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-779"><span id="QWORD"></span><span id="qword"></span><strong>QWORD</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-780">Eine 64-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-780">A 64-bit unsigned integer.</span></span></p>
<p><span data-ttu-id="db7a9-781">Dieser Typ wird wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-781">This type is declared as follows:</span></span></p>
<p><code>typedef unsigned __int64 QWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-782"><span id="SC_HANDLE"></span><span id="sc_handle"></span><strong>SC_HANDLE</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-782"><span id="SC_HANDLE"></span><span id="sc_handle"></span><strong>SC_HANDLE</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-783">Ein Handle für eine Dienststeuerungs-Manager-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="db7a9-783">A handle to a service control manager database.</span></span> <span data-ttu-id="db7a9-784">Weitere Informationen finden Sie unter <a href="/windows/desktop/Services/scm-handles">SCM-Handles</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-784">For more information, see <a href="/windows/desktop/Services/scm-handles">SCM Handles</a>.</span></span></p>
<p><span data-ttu-id="db7a9-785">Dieser Typ wird in winsvc. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-785">This type is declared in WinSvc.h as follows:</span></span></p>
<p><code>typedef HANDLE SC_HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-786"><span id="SC_LOCK"></span><span id="sc_lock"></span><strong>SC_LOCK</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-786"><span id="SC_LOCK"></span><span id="sc_lock"></span><strong>SC_LOCK</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-787">Eine Sperre für eine Dienststeuerungs-Manager-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="db7a9-787">A lock to a service control manager database.</span></span> <span data-ttu-id="db7a9-788">Weitere Informationen finden Sie unter <a href="/windows/desktop/Services/scm-handles">SCM-Handles</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-788">For more information, see <a href="/windows/desktop/Services/scm-handles">SCM Handles</a>.</span></span></p>
<p><span data-ttu-id="db7a9-789">Dieser Typ wird in winsvc. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-789">This type is declared in WinSvc.h as follows:</span></span></p>
<p><code>typedef LPVOID SC_LOCK;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-790"><span id="SERVICE_STATUS_HANDLE"></span><span id="service_status_handle"></span><strong>SERVICE_STATUS_HANDLE</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-790"><span id="SERVICE_STATUS_HANDLE"></span><span id="service_status_handle"></span><strong>SERVICE_STATUS_HANDLE</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-791">Ein Handle für einen Dienststatus Wert.</span><span class="sxs-lookup"><span data-stu-id="db7a9-791">A handle to a service status value.</span></span> <span data-ttu-id="db7a9-792">Weitere Informationen finden Sie unter <a href="/windows/desktop/Services/scm-handles">SCM-Handles</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-792">For more information, see <a href="/windows/desktop/Services/scm-handles">SCM Handles</a>.</span></span></p>
<p><span data-ttu-id="db7a9-793">Dieser Typ wird in winsvc. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-793">This type is declared in WinSvc.h as follows:</span></span></p>
<p><code>typedef HANDLE SERVICE_STATUS_HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-794"><span id="SHORT"></span><span id="short"></span><strong>Kurzem</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-794"><span id="SHORT"></span><span id="short"></span><strong>SHORT</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-795">Eine 16-Bit-Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="db7a9-795">A 16-bit integer.</span></span> <span data-ttu-id="db7a9-796">Der Bereich liegt zwischen-32768 und 32767 Decimal.</span><span class="sxs-lookup"><span data-stu-id="db7a9-796">The range is -32768 through 32767 decimal.</span></span></p>
<p><span data-ttu-id="db7a9-797">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-797">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef short SHORT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-798"><span id="SIZE_T"></span><span id="size_t"></span><strong>SIZE_T</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-798"><span id="SIZE_T"></span><span id="size_t"></span><strong>SIZE_T</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-799">Die maximale Anzahl von Bytes, auf die ein Zeiger verweisen kann.</span><span class="sxs-lookup"><span data-stu-id="db7a9-799">The maximum number of bytes to which a pointer can point.</span></span> <span data-ttu-id="db7a9-800">Verwenden Sie für einen Zähler, der den vollständigen Bereich eines Zeigers umfassen muss.</span><span class="sxs-lookup"><span data-stu-id="db7a9-800">Use for a count that must span the full range of a pointer.</span></span></p>
<p><span data-ttu-id="db7a9-801">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-801">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef ULONG_PTR SIZE_T;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-802"><span id="SSIZE_T"></span><span id="ssize_t"></span><strong>SSIZE_T</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-802"><span id="SSIZE_T"></span><span id="ssize_t"></span><strong>SSIZE_T</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-803">Eine signierte Version von <a href="#size_t"><strong>size_t</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-803">A signed version of <a href="#size_t"><strong>SIZE_T</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-804">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-804">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef LONG_PTR SSIZE_T;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-805"><span id="TBYTE"></span><span id="tbyte"></span><strong>TByte</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-805"><span id="TBYTE"></span><span id="tbyte"></span><strong>TBYTE</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-806">Ein <a href="#wchar"><strong>WCHAR</strong></a> , wenn <strong>Unicode</strong> definiert ist, andernfalls ein <a href="#char"><strong>char</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="db7a9-806">A <a href="#wchar"><strong>WCHAR</strong></a> if <strong>UNICODE</strong> is defined, a <a href="#char"><strong>CHAR</strong></a> otherwise.</span></span></p>
<p><span data-ttu-id="db7a9-807">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-807">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db7a9-808">C++</span><span class="sxs-lookup"><span data-stu-id="db7a9-808">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef WCHAR TBYTE;
#else
 typedef unsigned char TBYTE;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-809"><span id="TCHAR"></span><span id="tchar"></span><strong>Tchar</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-809"><span id="TCHAR"></span><span id="tchar"></span><strong>TCHAR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-810">Ein <a href="#wchar"><strong>WCHAR</strong></a> , wenn <strong>Unicode</strong> definiert ist, andernfalls ein <a href="#char"><strong>char</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="db7a9-810">A <a href="#wchar"><strong>WCHAR</strong></a> if <strong>UNICODE</strong> is defined, a <a href="#char"><strong>CHAR</strong></a> otherwise.</span></span></p>
<p><span data-ttu-id="db7a9-811">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-811">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db7a9-812">C++</span><span class="sxs-lookup"><span data-stu-id="db7a9-812">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef WCHAR TCHAR;
#else
 typedef char TCHAR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-813"><span id="UCHAR"></span><span id="uchar"></span><strong>UCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-813"><span id="UCHAR"></span><span id="uchar"></span><strong>UCHAR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-814">Ein Zeichen ohne <a href="#char"><strong>Vorzeichen.</strong></a></span><span class="sxs-lookup"><span data-stu-id="db7a9-814">An unsigned <a href="#char"><strong>CHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-815">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-815">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned char UCHAR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-816"><span id="UHALF_PTR"></span><span id="uhalf_ptr"></span><strong>UHALF_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-816"><span id="UHALF_PTR"></span><span id="uhalf_ptr"></span><strong>UHALF_PTR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-817">Ein nicht signiertes <a href="#half_ptr"><strong>HALF_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-817">An unsigned <a href="#half_ptr"><strong>HALF_PTR</strong></a>.</span></span> <span data-ttu-id="db7a9-818">Verwenden Sie innerhalb einer-Struktur, die einen Zeiger und zwei kleine Felder enthält.</span><span class="sxs-lookup"><span data-stu-id="db7a9-818">Use within a structure that contains a pointer and two small fields.</span></span></p>
<p><span data-ttu-id="db7a9-819">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-819">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db7a9-820">C++</span><span class="sxs-lookup"><span data-stu-id="db7a9-820">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef _WIN64
 typedef unsigned int UHALF_PTR;
#else
 typedef unsigned short UHALF_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-821"><span id="UINT"></span><span id="uint"></span><strong>UINT</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-821"><span id="UINT"></span><span id="uint"></span><strong>UINT</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-822">Ein <a href="#int"><strong>int</strong></a>-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-822">An unsigned <a href="#int"><strong>INT</strong></a>.</span></span> <span data-ttu-id="db7a9-823">Der Bereich liegt zwischen 0 und 4294967295 Decimal.</span><span class="sxs-lookup"><span data-stu-id="db7a9-823">The range is 0 through 4294967295 decimal.</span></span></p>
<p><span data-ttu-id="db7a9-824">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-824">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned int UINT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-825"><span id="UINT_PTR"></span><span id="uint_ptr"></span><strong>UINT_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-825"><span id="UINT_PTR"></span><span id="uint_ptr"></span><strong>UINT_PTR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-826">Ein nicht signiertes <a href="#int_ptr"><strong>INT_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-826">An unsigned <a href="#int_ptr"><strong>INT_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-827">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-827">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db7a9-828">C++</span><span class="sxs-lookup"><span data-stu-id="db7a9-828">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64)
 typedef unsigned __int64 UINT_PTR;
#else
 typedef unsigned int UINT_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-829"><span id="UINT8"></span><span id="uint8"></span><strong>Uint8</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-829"><span id="UINT8"></span><span id="uint8"></span><strong>UINT8</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-830">Ein <a href="#int8"><strong>int8</strong></a>ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-830">An unsigned <a href="#int8"><strong>INT8</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-831">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-831">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned  char UINT8;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-832"><span id="UINT16"></span><span id="uint16"></span><strong>UInt16</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-832"><span id="UINT16"></span><span id="uint16"></span><strong>UINT16</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-833">Ein <a href="#int16"><strong>INT16</strong></a>ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-833">An unsigned <a href="#int16"><strong>INT16</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-834">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-834">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned  short UINT16;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-835"><span id="UINT32"></span><span id="uint32"></span><strong>UInt32</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-835"><span id="UINT32"></span><span id="uint32"></span><strong>UINT32</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-836">Ein <a href="#int32"><strong>Int32</strong></a>ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-836">An unsigned <a href="#int32"><strong>INT32</strong></a>.</span></span> <span data-ttu-id="db7a9-837">Der Bereich liegt zwischen 0 und 4294967295 Decimal.</span><span class="sxs-lookup"><span data-stu-id="db7a9-837">The range is 0 through 4294967295 decimal.</span></span></p>
<p><span data-ttu-id="db7a9-838">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-838">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned int UINT32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-839"><span id="UINT64"></span><span id="uint64"></span><strong>UINT64</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-839"><span id="UINT64"></span><span id="uint64"></span><strong>UINT64</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-840">Ein <a href="#int64"><strong>Int64</strong></a>ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-840">An unsigned <a href="#int64"><strong>INT64</strong></a>.</span></span> <span data-ttu-id="db7a9-841">Der Bereich liegt zwischen 0 und 18446744073709551615 Decimal.</span><span class="sxs-lookup"><span data-stu-id="db7a9-841">The range is 0 through 18446744073709551615 decimal.</span></span></p>
<p><span data-ttu-id="db7a9-842">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-842">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef usigned __int 64 UINT64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-843"><span id="ULONG"></span><span id="ulong"></span><strong>ULONG</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-843"><span id="ULONG"></span><span id="ulong"></span><strong>ULONG</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-844">Ein <a href="#long"><strong>Long</strong></a>-Typ ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-844">An unsigned <a href="#long"><strong>LONG</strong></a>.</span></span> <span data-ttu-id="db7a9-845">Der Bereich liegt zwischen 0 und 4294967295 Decimal.</span><span class="sxs-lookup"><span data-stu-id="db7a9-845">The range is 0 through 4294967295 decimal.</span></span></p>
<p><span data-ttu-id="db7a9-846">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-846">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned long ULONG;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-847"><span id="ULONGLONG"></span><span id="ulonglong"></span><strong>ULONGLONG</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-847"><span id="ULONGLONG"></span><span id="ulonglong"></span><strong>ULONGLONG</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-848">Eine 64-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-848">A 64-bit unsigned integer.</span></span> <span data-ttu-id="db7a9-849">Der Bereich liegt zwischen 0 und 18446744073709551615 Decimal.</span><span class="sxs-lookup"><span data-stu-id="db7a9-849">The range is 0 through 18446744073709551615 decimal.</span></span></p>
<p><span data-ttu-id="db7a9-850">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-850">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db7a9-851">C++</span><span class="sxs-lookup"><span data-stu-id="db7a9-851">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if !defined(_M_IX86)
 typedef unsigned __int64 ULONGLONG;
#else
 typedef double ULONGLONG;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-852"><span id="ULONG_PTR"></span><span id="ulong_ptr"></span><strong>ULONG_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-852"><span id="ULONG_PTR"></span><span id="ulong_ptr"></span><strong>ULONG_PTR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-853">Ein nicht signiertes <a href="#long_ptr"><strong>LONG_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-853">An unsigned <a href="#long_ptr"><strong>LONG_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="db7a9-854">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-854">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db7a9-855">C++</span><span class="sxs-lookup"><span data-stu-id="db7a9-855">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64)
 typedef unsigned __int64 ULONG_PTR;
#else
 typedef unsigned long ULONG_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-856"><span id="ULONG32"></span><span id="ulong32"></span><strong>ULONG32</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-856"><span id="ULONG32"></span><span id="ulong32"></span><strong>ULONG32</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-857">Ein <a href="#long32"><strong>LONG32</strong></a>ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-857">An unsigned <a href="#long32"><strong>LONG32</strong></a>.</span></span> <span data-ttu-id="db7a9-858">Der Bereich liegt zwischen 0 und 4294967295 Decimal.</span><span class="sxs-lookup"><span data-stu-id="db7a9-858">The range is 0 through 4294967295 decimal.</span></span></p>
<p><span data-ttu-id="db7a9-859">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-859">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned int ULONG32;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-860"><span id="ULONG64"></span><span id="ulong64"></span><strong>ULONG64</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-860"><span id="ULONG64"></span><span id="ulong64"></span><strong>ULONG64</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-861">Ein <a href="#long64"><strong>LONG64</strong></a>ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-861">An unsigned <a href="#long64"><strong>LONG64</strong></a>.</span></span> <span data-ttu-id="db7a9-862">Der Bereich liegt zwischen 0 und 18446744073709551615 Decimal.</span><span class="sxs-lookup"><span data-stu-id="db7a9-862">The range is 0 through 18446744073709551615 decimal.</span></span></p>
<p><span data-ttu-id="db7a9-863">Dieser Typ wird in basetsd. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-863">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned __int64 ULONG64;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-864"><span id="UNICODE_STRING"></span><span id="unicode_string"></span><strong>UNICODE_STRING</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-864"><span id="UNICODE_STRING"></span><span id="unicode_string"></span><strong>UNICODE_STRING</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-865">Eine Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="db7a9-865">A Unicode string.</span></span></p>
<p><span data-ttu-id="db7a9-866">Dieser Typ wird in winternl. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-866">This type is declared in Winternl.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db7a9-867">C++</span><span class="sxs-lookup"><span data-stu-id="db7a9-867">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>typedef struct _UNICODE_STRING {
  USHORT  Length;
  USHORT  MaximumLength;
  PWSTR  Buffer;
} UNICODE_STRING;
typedef UNICODE_STRING *PUNICODE_STRING;
typedef const UNICODE_STRING *PCUNICODE_STRING;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-868"><span id="USHORT"></span><span id="ushort"></span><strong>USHORT</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-868"><span id="USHORT"></span><span id="ushort"></span><strong>USHORT</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-869">Ein <a href="#short"><strong>Kurzschluss</strong></a>ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-869">An unsigned <a href="#short"><strong>SHORT</strong></a>.</span></span> <span data-ttu-id="db7a9-870">Der Bereich liegt zwischen 0 und 65535 Decimal.</span><span class="sxs-lookup"><span data-stu-id="db7a9-870">The range is 0 through 65535 decimal.</span></span></p>
<p><span data-ttu-id="db7a9-871">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-871">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned short USHORT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-872"><span id="USN"></span><span id="usn"></span><strong>USN</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-872"><span id="USN"></span><span id="usn"></span><strong>USN</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-873">Eine Update Sequenznummer (Update Sequence Number, US).</span><span class="sxs-lookup"><span data-stu-id="db7a9-873">An update sequence number (USN).</span></span></p>
<p><span data-ttu-id="db7a9-874">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-874">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef LONGLONG USN;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-875"><span id="VOID"></span><span id="void"></span><strong>Blutung</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-875"><span id="VOID"></span><span id="void"></span><strong>VOID</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-876">Beliebiger Typ</span><span class="sxs-lookup"><span data-stu-id="db7a9-876">Any type.</span></span></p>
<p><span data-ttu-id="db7a9-877">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-877">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>#define VOID void</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-878"><span id="WCHAR"></span><span id="wchar"></span><strong>WCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-878"><span id="WCHAR"></span><span id="wchar"></span><strong>WCHAR</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-879">Ein 16-Bit-Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-879">A 16-bit Unicode character.</span></span> <span data-ttu-id="db7a9-880">Weitere Informationen finden Sie unter <a href="/windows/desktop/gdi/character-sets-used-by-fonts">von Schriftarten verwendete Zeichensätze</a>.</span><span class="sxs-lookup"><span data-stu-id="db7a9-880">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="db7a9-881">Dieser Typ wird in "Winnt. h" wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-881">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef wchar_t WCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-882"><span id="WINAPI"></span><span id="winapi"></span><strong>WinAPI</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-882"><span id="WINAPI"></span><span id="winapi"></span><strong>WINAPI</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-883">Die Aufruf Konvention für Systemfunktionen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-883">The calling convention for system functions.</span></span></p>
<p><span data-ttu-id="db7a9-884">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-884">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>#define WINAPI __stdcall</code></p>
<p><span data-ttu-id="db7a9-885"><strong>Callback</strong>, <strong>WinAPI</strong>und <strong>apientry</strong> werden verwendet, um Funktionen mit der __stdcall-Aufruf Konvention zu definieren.</span><span class="sxs-lookup"><span data-stu-id="db7a9-885"><strong>CALLBACK</strong>, <strong>WINAPI</strong>, and <strong>APIENTRY</strong> are all used to define functions with the __stdcall calling convention.</span></span> <span data-ttu-id="db7a9-886">Die meisten Funktionen in der Windows-API werden mithilfe von <strong>WinAPI</strong>deklariert.</span><span class="sxs-lookup"><span data-stu-id="db7a9-886">Most functions in the Windows API are declared using <strong>WINAPI</strong>.</span></span> <span data-ttu-id="db7a9-887">Möglicherweise möchten Sie den <strong>Rückruf</strong> für die von Ihnen implementierten Rückruf Funktionen verwenden, um die Funktion als Rückruffunktion zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="db7a9-887">You may wish to use <strong>CALLBACK</strong> for the callback functions that you implement to help identify the function as a callback function.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db7a9-888"><span id="WORD"></span><span id="word"></span><strong>Wort</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-888"><span id="WORD"></span><span id="word"></span><strong>WORD</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-889">Eine 16-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="db7a9-889">A 16-bit unsigned integer.</span></span> <span data-ttu-id="db7a9-890">Der Bereich liegt zwischen 0 und 65535 Decimal.</span><span class="sxs-lookup"><span data-stu-id="db7a9-890">The range is 0 through 65535 decimal.</span></span></p>
<p><span data-ttu-id="db7a9-891">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-891">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned short WORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db7a9-892"><span id="WPARAM"></span><span id="wparam"></span><strong>WParam</strong></span><span class="sxs-lookup"><span data-stu-id="db7a9-892"><span id="WPARAM"></span><span id="wparam"></span><strong>WPARAM</strong></span></span></td>
<td><p><span data-ttu-id="db7a9-893">Ein Meldungs Parameter.</span><span class="sxs-lookup"><span data-stu-id="db7a9-893">A message parameter.</span></span></p>
<p><span data-ttu-id="db7a9-894">Dieser Typ wird in WINDEF. h wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="db7a9-894">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef UINT_PTR WPARAM;</code></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="db7a9-895">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db7a9-895">Requirements</span></span>



| <span data-ttu-id="db7a9-896">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db7a9-896">Requirement</span></span> | <span data-ttu-id="db7a9-897">Wert</span><span class="sxs-lookup"><span data-stu-id="db7a9-897">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db7a9-898">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="db7a9-898">Minimum supported client</span></span><br/> | <span data-ttu-id="db7a9-899">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db7a9-899">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="db7a9-900">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="db7a9-900">Minimum supported server</span></span><br/> | <span data-ttu-id="db7a9-901">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db7a9-901">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                |
| <span data-ttu-id="db7a9-902">Header</span><span class="sxs-lookup"><span data-stu-id="db7a9-902">Header</span></span><br/>                   | <dl> <span data-ttu-id="db7a9-903"><dt>Basetsd. h; </dt> <dt>WINDEF. h; </dt> <dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="db7a9-903"><dt>BaseTsd.h; </dt> <dt>WinDef.h; </dt> <dt>WinNT.h</dt></span></span> </dl> |
