---
title: Windows-Datentypen (BaseTsd.h)
description: Die datentyps, die von Windows werden verwendet, um Rückgabewerte, Funktions- und Meldungsparameter sowie Strukturmitglieder zu definieren.
ms.assetid: 4553cafc-450e-4493-a4d4-cb6e2f274d46
keywords:
- Datentypen
- Datentypen,Windows
- Windows-API
- Windows API, Datentypen
- APIENTRY
- ATOM
- BOOL
- BOOLEAN
- BYTE
- Rückruf
- CCHAR
- CHAR
- COLORREF
- Const
- DWORD
- DWORDLONG
- DWORD_PTR
- DWORD32
- DWORD64
- GLEITKOMMAZAHL
- HACCEL
- HALF_PTR
- HANDLE
- HBITMAP
- HBRUSH
- HCOLORSPACE
- HCONV
- HCONVLIST
- HCURSOR
- Hdc
- HDDEDATA
- HDESK
- HDROP
- HDWP
- HENHMETAFILE
- HFILE
- HFONT
- LKDIOBJ
- HGLOBAL
- HHOOK
- HICON
- Hinstance
- Hkey
- HKL
- HLOCAL
- Hmenu
- HMETAFILE
- HMODULE
- Hmonitor
- HPALETTE
- HPEN
- HRESULT
- HRGN
- HRSRC
- HSZ
- HWINSTA
- HWND
- INT
- INT_PTR
- INT8
- INT16
- INT32
- INT64
- Langid
- LCID
- LCTYPE
- LGRPID
- LONG
- LONGLONG
- LONG_PTR
- LONG32
- LONG64
- Lparam
- LPBOOL
- LPBYTE
- LPCOLORREF
- LPCSTR
- LPCTSTR
- LPCVOID
- LPCWSTR
- LPDWORD
- LPHANDLE
- LPINT
- LPLONG
- LPSTR
- LPTSTR
- LPVOID
- LPWORD
- LPWSTR
- LRESULT
- PBOOL
- PBOOLEAN
- PBYTE
- PCHAR
- PCSTR
- PCTSTR
- PCWSTR
- PDWORD
- PDWORDLONG
- PDWORD_PTR
- PDWORD32
- PDWORD64
- PFLOAT
- PHALF_PTR
- PHANDLE
- PHKEY
- Pint
- PINT_PTR
- PINT8
- PINT16
- PINT32
- PINT64
- PLCID
- PLONG
- PLONGLONG
- PLONG_PTR
- PLONG32
- PLONG64
- POINTER_32
- POINTER_64
- POINTER_SIGNED
- POINTER_UNSIGNED
- PSHORT
- PSIZE_T
- PSSIZE_T
- Pstr
- PTBYTE
- PTCHAR
- PTSTR
- PUCHAR
- PUHALF_PTR
- PUINT
- PUINT_PTR
- PUINT8
- PUINT16
- PUINT32
- PUINT64
- PULONG
- PULONGLONG
- PULONG_PTR
- PULONG32
- PULONG64
- PUSHORT
- PVOID
- PWCHAR
- PWORD
- PWSTR
- QWORD
- SC_HANDLE
- SC_LOCK
- SERVICE_STATUS_HANDLE
- SHORT
- Size_t
- SSIZE_T
- TBYTE
- TCHAR
- UCHAR
- UHALF_PTR
- UINT
- UINT_PTR
- UINT8
- UINT16
- UINT32
- UINT64
- ULONG
- ULONGLONG
- ULONG_PTR
- Ulong32
- ULONG64
- UNICODE_STRING
- Ushort
- USN
- Leere
- WCHAR
- WINAPI
- WORD
- Wparam
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6769b5d3fd7c65eab1eef5c408ebd2e905b9677a3580774a857c68431aabd3dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412950"
---
# <a name="windows-data-types"></a>Windows-Datentypen

Die von Windows unterstützten Datentypen werden verwendet, um Funktionsrückgabewerte, Funktions- und Nachrichtenparameter sowie Strukturmember zu definieren. Sie definieren die Größe und Bedeutung dieser Elemente. Weitere Informationen zu den zugrunde liegenden C/C++-Datentypen finden Sie unter [Datentypbereiche.](/cpp/cpp/data-type-ranges?view=vs-2019)

Die folgende Tabelle enthält die folgenden Typen: character, integer, Boolean, pointer und handle. Die Zeichen-, Integer- und booleschen Typen sind für die meisten C-Compiler üblich. Die meisten Zeigertypnamen beginnen mit dem Präfix P oder LP. Handles verweisen auf eine Ressource, die in den Arbeitsspeicher geladen wurde.

Weitere Informationen zur Behandlung von 64-Bit-Ganzzahlen finden Sie unter [Große ganze Zahlen.](large-integers.md)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Datentyp</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="APIENTRY"></span><span id="apientry"></span><strong>APIENTRY</strong></td>
<td>Die Aufrufkonvention für Systemfunktionen.<br/> Dieser Typ wird in WinDef.h wie folgt deklariert:<br/> <code>#define APIENTRY WINAPI</code><br/></td>
</tr>
<tr class="even">
<td><span id="ATOM"></span><span id="atom"></span><strong>Atom</strong></td>
<td>Ein Atom. Weitere Informationen finden Sie unter <a href="/windows/desktop/dataxchg/about-atom-tables">Informationen zu Atom-Tabellen.</a><br/> Dieser Typ wird in WinDef.h wie folgt deklariert:<br/> <code>typedef WORD ATOM;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="BOOL"></span><span id="bool"></span><strong>Bool</strong></td>
<td>Eine boolesche Variable (sollte <strong>TRUE</strong> oder <strong>FALSE sein).</strong><br/> Dieser Typ wird in WinDef.h wie folgt deklariert:<br/> <code>typedef int BOOL;</code><br/></td>
</tr>
<tr class="even">
<td><span id="BOOLEAN"></span><span id="boolean"></span><strong>Boolean</strong></td>
<td>Eine boolesche Variable (muss <strong>TRUE</strong> oder <strong>FALSE sein).</strong><br/> Dieser Typ wird in WinNT.h wie folgt deklariert:<br/> <code>typedef BYTE BOOLEAN;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="BYTE"></span><span id="byte"></span><strong>Byte</strong></td>
<td>Ein Byte (8 Bits).<br/> Dieser Typ wird in WinDef.h wie folgt deklariert:<br/> <code>typedef unsigned char BYTE;</code><br/></td>
</tr>
<tr class="even">
<td><span id="CALLBACK"></span><span id="callback"></span><strong>Rückruf</strong></td>
<td>Die Aufrufkonvention für Rückruffunktionen.<br/> Dieser Typ wird in WinDef.h wie folgt deklariert:<br/> <code>#define CALLBACK __stdcall</code><br/> <strong>CALLBACK,</strong> <strong>WINAPI</strong>und <strong>APIENTRY</strong> werden alle zum Definieren von Funktionen mit der __stdcall verwendet. Die meisten Funktionen in der Windows-API werden mit <strong>winapi deklariert.</strong> Sie können <strong>CALLBACK</strong> für die Rückruffunktionen verwenden, die Sie implementieren, um die Funktion als Rückruffunktion zu identifizieren.<br/></td>
</tr>
<tr class="odd">
<td><span id="CCHAR"></span><span id="cchar"></span><strong>CCHAR</strong></td>
<td>Ein 8-Bit-Windows (ANSI)<br/> Dieser Typ wird in WinNT.h wie folgt deklariert:<br/> <code>typedef char CCHAR;</code><br/></td>
</tr>
<tr class="even">
<td><span id="CHAR"></span><span id="char"></span><strong>Char</strong></td>
<td>Ein 8-Bit-Windows (ANSI) Weitere Informationen finden Sie unter <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Von Schriftarten verwendete Zeichensätze.</a><br/> Dieser Typ wird in WinNT.h wie folgt deklariert:<br/> <code>typedef char CHAR;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="COLORREF"></span><span id="colorref"></span><strong>COLORREF</strong></td>
<td>Der Farbwert rot, grün, blau (RGB) (32 Bits). Informationen zu diesem Typ finden Sie unter <a href="/windows/desktop/gdi/colorref"><strong>COLORREF.</strong></a><br/> Dieser Typ wird in WinDef.h wie folgt deklariert:<br/> <code>typedef DWORD COLORREF;</code><br/></td>
</tr>
<tr class="even">
<td><span id="CONST"></span><span id="const"></span><strong>Const</strong></td>
<td>Eine Variable, deren Wert während der Ausführung konstant bleiben soll. <br/> Dieser Typ wird in WinDef.h wie folgt deklariert:<br/> <code>#define CONST const</code><br/></td>
</tr>
<tr class="odd">
<td><span id="DWORD"></span><span id="dword"></span><strong>Dword</strong></td>
<td>Eine 32-Bit-Ganzzahl ohne Vorzeichen. Der Bereich ist 0 bis 4294967295 Dezimalzahl.<br/> Dieser Typ wird in IntSafe.h wie folgt deklariert:<br/> <code>typedef unsigned long DWORD;</code><br/></td>
</tr>
<tr class="even">
<td><span id="DWORDLONG"></span><span id="dwordlong"></span><strong>DWORDLONG</strong></td>
<td>Eine 64-Bit-Ganzzahl ohne Vorzeichen. Der Bereich ist 0 bis 18446744073709551615 Dezimalzahl.<br/> Dieser Typ wird in IntSafe.h wie folgt deklariert:<br/> <code>typedef unsigned __int64 DWORDLONG;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="DWORD_PTR"></span><span id="dword_ptr"></span><strong>DWORD_PTR</strong></td>
<td>Ein long-Typ ohne Vorzeichen für Zeigergenauigkeit. Verwenden Sie beim Umwandlung eines Zeigers in einen langen Typ, um Zeigerarithmetik durchzuführen. (Wird auch häufig für allgemeine 32-Bit-Parameter verwendet, die auf 64 Bit in 64-Bit-Windows.)<br/> Dieser Typ wird in BaseTsd.h wie folgt deklariert:<br/> <code>typedef ULONG_PTR DWORD_PTR;</code><br/></td>
</tr>
<tr class="even">
<td><span id="DWORD32"></span><span id="dword32"></span><strong>DWORD32</strong></td>
<td>Eine 32-Bit-Ganzzahl ohne Vorzeichen.<br/> Dieser Typ wird in BaseTsd.h wie folgt deklariert:<br/> <code>typedef unsigned int DWORD32;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="DWORD64"></span><span id="dword64"></span><strong>DWORD64</strong></td>
<td>Eine 64-Bit-Ganzzahl ohne Vorzeichen.<br/> Dieser Typ wird in BaseTsd.h wie folgt deklariert:<br/> <code>typedef unsigned __int64 DWORD64;</code><br/></td>
</tr>
<tr class="even">
<td><span id="FLOAT"></span><span id="float"></span><strong>schweben</strong></td>
<td>Eine Gleitkommavariable.<br/> Dieser Typ wird in WinDef.h wie folgt deklariert:<br/> <code>typedef float FLOAT;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="HACCEL"></span><span id="haccel"></span><strong>HACCEL</strong></td>
<td>Ein Handle für eine <a href="/windows/desktop/menurc/keyboard-accelerators">Zugriffstastentabelle.</a><br/> Dieser Typ wird in WinDef.h wie folgt deklariert:<br/> <code>typedef HANDLE HACCEL;</code><br/></td>
</tr>
<tr class="even">
<td><span id="HALF_PTR"></span><span id="half_ptr"></span><strong>HALF_PTR</strong></td>
<td>Die Hälfte der Größe eines Zeigers. Verwenden Sie in einer -Struktur, die einen Zeiger und zwei kleine Felder enthält.<br/> Dieser Typ wird in BaseTsd.h wie folgt deklariert:<br/> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="HANDLE"></span><span id="handle"></span><strong>Behandeln</strong></td>
<td><p>Ein Handle für ein Objekt.</p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<p><code>typedef PVOID HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span id="HBITMAP"></span><span id="hbitmap"></span><strong>HBITMAP</strong></td>
<td><p>Ein Handle für eine <a href="/windows/desktop/gdi/bitmaps">Bitmap.</a></p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef HANDLE HBITMAP;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HBRUSH"></span><span id="hbrush"></span><strong>HBRUSH</strong></td>
<td><p>Ein Handle für einen <a href="/windows/desktop/gdi/brushes">Pinsel.</a></p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef HANDLE HBRUSH;</code></p></td>
</tr>
<tr class="even">
<td><span id="HCOLORSPACE"></span><span id="hcolorspace"></span><strong>HCOLORSPACE</strong></td>
<td><p>Ein Handle für einen <a href="/previous-versions//dd316799(v=vs.85)">Farbraum.</a></p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef HANDLE HCOLORSPACE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HCONV"></span><span id="hconv"></span><strong>HCONV</strong></td>
<td><p>Ein Handle für eine DDE-Konversation (Dynamic Data Exchange).</p>
<p>Dieser Typ wird in Ddeml.h wie folgt deklariert:</p>
<p><code>typedef HANDLE HCONV;</code></p></td>
</tr>
<tr class="even">
<td><span id="HCONVLIST"></span><span id="hconvlist"></span><strong>HCONVLIST</strong></td>
<td><p>Ein Handle für eine DDE-Konversationsliste.</p>
<p>Dieser Typ wird in Ddeml.h wie folgt deklariert:</p>
<p><code>typedef HANDLE HCONVLIST;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HCURSOR"></span><span id="hcursor"></span><strong>HCURSOR</strong></td>
<td><p>Ein Handle für einen <a href="/windows/desktop/menurc/cursors">Cursor.</a></p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef HICON HCURSOR;</code></p></td>
</tr>
<tr class="even">
<td><span id="HDC"></span><span id="hdc"></span><strong>Hdc</strong></td>
<td><p>Ein Handle für einen <a href="/windows/desktop/gdi/device-context-types">Gerätekontext</a> (DC).</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef HANDLE HDC;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HDDEDATA"></span><span id="hddedata"></span><strong>HDDEDATA</strong></td>
<td><p>Ein Handle für DDE-Daten.</p>
<p>Dieser Typ wird in Ddeml.h wie folgt deklariert:</p>
<p><code>typedef HANDLE HDDEDATA;</code></p></td>
</tr>
<tr class="even">
<td><span id="HDESK"></span><span id="hdesk"></span><strong>HDESK</strong></td>
<td><p>Ein Handle für einen <a href="/windows/desktop/winstation/desktops">Desktop.</a></p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef HANDLE HDESK;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HDROP"></span><span id="hdrop"></span><strong>HDROP</strong></td>
<td><p>Ein Handle für eine interne Absturzstruktur.</p>
<p>Dieser Typ wird in ShellApi.h wie folgt deklariert:</p>
<p><code>typedef HANDLE HDROP;</code></p></td>
</tr>
<tr class="even">
<td><span id="HDWP"></span><span id="hdwp"></span><strong>HDWP</strong></td>
<td><p>Ein Handle für eine verzögerte Fensterpositionsstruktur.</p>
<p>Dieser Typ wird in WinUser.h wie folgt deklariert:</p>
<p><code>typedef HANDLE HDWP;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HENHMETAFILE"></span><span id="henhmetafile"></span><strong>HENHMETAFILE</strong></td>
<td><p>Ein Handle für eine <a href="/windows/desktop/gdi/metafiles">erweiterte Metadatei.</a></p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef HANDLE HENHMETAFILE;</code></p></td>
</tr>
<tr class="even">
<td><span id="HFILE"></span><span id="hfile"></span><strong>HFILE</strong></td>
<td><p>Ein Handle für eine Datei, die von <a href="/windows/desktop/api/winbase/nf-winbase-openfile"><strong>OpenFile geöffnet wurde,</strong></a>nicht <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea"><strong>CreateFile</strong></a>.</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef int HFILE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HFONT"></span><span id="hfont"></span><strong>HFONT</strong></td>
<td><p>Ein Handle für eine <a href="/windows/desktop/gdi/about-fonts">Schriftart.</a></p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef HANDLE HFONT;</code></p></td>
</tr>
<tr class="even">
<td><span id="HGDIOBJ"></span><span id="hgdiobj"></span><strong>LKDIOBJ</strong></td>
<td><p>Ein Handle für ein GDI-Objekt.</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef HANDLE HGDIOBJ;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HGLOBAL"></span><span id="hglobal"></span><strong>HGLOBAL</strong></td>
<td><p>Ein Handle für einen globalen Speicherblock.</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef HANDLE HGLOBAL;</code></p></td>
</tr>
<tr class="even">
<td><span id="HHOOK"></span><span id="hhook"></span><strong>HHOOK</strong></td>
<td><p>Ein Handle für einen <a href="/windows/desktop/winmsg/hooks">Hook.</a></p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef HANDLE HHOOK;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HICON"></span><span id="hicon"></span><strong>HICON</strong></td>
<td><p>Ein Handle für ein <a href="/windows/desktop/menurc/icons">Symbol.</a></p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef HANDLE HICON;</code></p></td>
</tr>
<tr class="even">
<td><span id="HINSTANCE"></span><span id="hinstance"></span><strong>Hinstance</strong></td>
<td><p>Ein Handle für eine Instanz. Dies ist die Basisadresse des Moduls im Arbeitsspeicher.</p>
<p><strong>HMODULE</strong> und <strong>HINSTANCE</strong> sind heute identisch, repräsentierten aber in 16-Bit-Windows.</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef HANDLE HINSTANCE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HKEY"></span><span id="hkey"></span><strong>Hkey</strong></td>
<td><p>Ein Handle für einen Registrierungsschlüssel.</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef HANDLE HKEY;</code></p></td>
</tr>
<tr class="even">
<td><span id="HKL"></span><span id="hkl"></span><strong>HKL</strong></td>
<td><p>Ein Eingabe-Locale Identifier.</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef HANDLE HKL;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HLOCAL"></span><span id="hlocal"></span><strong>HLOCAL</strong></td>
<td><p>Ein Handle für einen lokalen Speicherblock.</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef HANDLE HLOCAL;</code></p></td>
</tr>
<tr class="even">
<td><span id="HMENU"></span><span id="hmenu"></span><strong>Hmenu</strong></td>
<td><p>Ein Handle für ein <a href="/windows/desktop/menurc/menus">Menü.</a></p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef HANDLE HMENU;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HMETAFILE"></span><span id="hmetafile"></span><strong>HMETAFILE</strong></td>
<td><p>Ein Handle für eine <a href="/windows/desktop/gdi/metafiles">Metadatei.</a></p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef HANDLE HMETAFILE;</code></p></td>
</tr>
<tr class="even">
<td><span id="HMODULE"></span><span id="hmodule"></span><strong>HMODULE</strong></td>
<td><p>Ein Handle für ein Modul. ist die Basisadresse des Moduls im Arbeitsspeicher.</p>
<p><strong>HMODULE</strong> und <strong>HINSTANCE</strong> sind in aktuellen Versionen von Windows identisch, repräsentierten jedoch unterschiedliche Dinge in 16-Bit-Windows.</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef HINSTANCE HMODULE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HMONITOR"></span><span id="hmonitor"></span><strong>Hmonitor</strong></td>
<td><p>Ein Handle für einen Anzeigemonitor.</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>if(WINVER >= 0x0500) typedef HANDLE HMONITOR;</code></p></td>
</tr>
<tr class="even">
<td><span id="HPALETTE"></span><span id="hpalette"></span><strong>HPALETTE</strong></td>
<td><p>Ein Handle für eine Palette.</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef HANDLE HPALETTE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HPEN"></span><span id="hpen"></span><strong>HPEN</strong></td>
<td><p>Ein Handle für einen <a href="/windows/desktop/gdi/pens">Stift</a>.</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef HANDLE HPEN;</code></p></td>
</tr>
<tr class="even">
<td><span id="HRESULT"></span><span id="hresult"></span><strong>Hresult</strong></td>
<td><p>Die von COM-Schnittstellen verwendeten Rückgabecodes. Weitere Informationen finden Sie unter <a href="/windows/desktop/com/structure-of-com-error-codes">Struktur der COM-Fehlercodes</a>. Verwenden Sie zum <strong>Testen eines HRESULT-Werts</strong> die <a href="/windows/desktop/api/winerror/nf-winerror-failed"><strong>Makros FAILED</strong></a> und <a href="/windows/desktop/api/winerror/nf-winerror-succeeded"><strong>SUCCEEDED.</strong></a></p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<p><code>typedef LONG HRESULT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HRGN"></span><span id="hrgn"></span><strong>HRGN</strong></td>
<td><p>Ein Handle für einen <a href="/windows/desktop/gdi/regions">Bereich.</a></p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef HANDLE HRGN;</code></p></td>
</tr>
<tr class="even">
<td><span id="HRSRC"></span><span id="hrsrc"></span><strong>HRSRC</strong></td>
<td><p>Ein Handle für eine Ressource.</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef HANDLE HRSRC;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HSZ"></span><span id="hsz"></span><strong>HSZ</strong></td>
<td><p>Ein Handle für eine DDE-Zeichenfolge.</p>
<p>Dieser Typ wird in Ddeml.h wie folgt deklariert:</p>
<p><code>typedef HANDLE HSZ;</code></p></td>
</tr>
<tr class="even">
<td><span id="HWINSTA"></span><span id="hwinsta"></span><strong>HWINSTA</strong></td>
<td><p>Ein Handle für eine <a href="/windows/desktop/winstation/window-stations">Fensterstation.</a></p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef HANDLE WINSTA;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HWND"></span><span id="hwnd"></span><strong>Hwnd</strong></td>
<td><p>Ein Handle für ein <a href="/windows/desktop/winmsg/windows">Fenster.</a></p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef HANDLE HWND;</code></p></td>
</tr>
<tr class="even">
<td><span id="INT"></span><span id="int"></span><strong>Int</strong></td>
<td><p>Eine 32-Bit-Ganzzahl mit Vorzeichen. Der Bereich ist -2147483648 bis 2147483647 Dezimalzahl.</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef int INT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="INT_PTR"></span><span id="int_ptr"></span><strong>INT_PTR</strong></td>
<td><p>Ein Ganzzahltyp mit Vorzeichen für Zeigergenauigkeit. Verwenden Sie beim Konvertieren eines Zeigers in eine ganze Zahl, um Zeigerarithmetik durchzuführen.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="INT8"></span><span id="int8"></span><strong>INT8</strong></td>
<td><p>Eine 8-Bit-Ganzzahl mit Vorzeichen.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef signed char INT8;</code></p></td>
</tr>
<tr class="odd">
<td><span id="INT16"></span><span id="int16"></span><strong>INT16</strong></td>
<td><p>Eine 16-Bit-Ganzzahl mit Vorzeichen.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef signed short INT16;</code></p></td>
</tr>
<tr class="even">
<td><span id="INT32"></span><span id="int32"></span><strong>INT32</strong></td>
<td><p>Eine 32-Bit-Ganzzahl mit Vorzeichen. Der Bereich ist -2147483648 bis 2147483647 Dezimalzahl.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef signed int INT32;</code></p></td>
</tr>
<tr class="odd">
<td><span id="INT64"></span><span id="int64"></span><strong>INT64</strong></td>
<td><p>Eine 64-Bit-Ganzzahl mit Vorzeichen. Der Bereich ist -9223372036854775808 bis 9223372036854775807 Dezimalzahl.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef signed __int64 INT64;</code></p></td>
</tr>
<tr class="even">
<td><span id="LANGID"></span><span id="langid"></span><strong>Langid</strong></td>
<td><p>Ein Sprachbezeichner. Weitere Informationen finden Sie unter <a href="/windows/desktop/Intl/language-identifiers">Sprachbezeichner.</a></p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<p><code>typedef WORD LANGID;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LCID"></span><span id="lcid"></span><strong>Lcid</strong></td>
<td><p>Ein -Locale-Bezeichner. Weitere Informationen finden Sie unter <a href="/windows/desktop/Intl/locale-identifiers">Locale Identifiers</a>.</p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<p><code>typedef DWORD LCID;</code></p></td>
</tr>
<tr class="even">
<td><span id="LCTYPE"></span><span id="lctype"></span><strong>LCTYPE</strong></td>
<td><p>Ein Locale Information-Typ. Eine Liste finden Sie unter <a href="/windows/desktop/Intl/locale-information-constants">Gebietsschemainformationskonstanten.</a></p>
<p>Dieser Typ wird in WinNls.h wie folgt deklariert:</p>
<p><code>typedef DWORD LCTYPE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LGRPID"></span><span id="lgrpid"></span><strong>LGRPID</strong></td>
<td><p>Ein Sprachgruppenbezeichner. Eine Liste finden Sie unter <a href="/windows/desktop/api/winnls/nf-winnls-enumlanguagegrouplocalesa"><strong>EnumLanguageGroupLocales</strong></a>.</p>
<p>Dieser Typ wird in WinNls.h wie folgt deklariert:</p>
<p><code>typedef DWORD LGRPID;</code></p></td>
</tr>
<tr class="even">
<td><span id="LONG"></span><span id="long"></span><strong>Lange</strong></td>
<td><p>Eine 32-Bit-Ganzzahl mit Vorzeichen. Der Bereich wird bis 2147483647 Dezimalzahl 2147483648.</p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<p><code>typedef long LONG;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LONGLONG"></span><span id="longlong"></span><strong>LONGLONG</strong></td>
<td><p>Eine 64-Bit-Ganzzahl mit Vorzeichen. Der Bereich ist bis 9223372036854775807 Dezimalzahl 9223372036854775808.</p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="LONG_PTR"></span><span id="long_ptr"></span><strong>LONG_PTR</strong></td>
<td><p>Ein long-Typ mit Vorzeichen für Zeigergenauigkeit. Verwenden Sie , wenn Sie einen Zeiger in einen long umwandeln, um Zeigerarithmetik auszuführen.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="LONG32"></span><span id="long32"></span><strong>LONG32</strong></td>
<td><p>Eine 32-Bit-Ganzzahl mit Vorzeichen. Der Bereich wird bis 2147483647 Dezimalzahl 2147483648.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef signed int LONG32;</code></p></td>
</tr>
<tr class="even">
<td><span id="LONG64"></span><span id="long64"></span><strong>LONG64</strong></td>
<td><p>Eine 64-Bit-Ganzzahl mit Vorzeichen. Der Bereich ist bis 9223372036854775807 Dezimalzahl 9223372036854775808.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef __int64 LONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPARAM"></span><span id="lparam"></span><strong>Lparam</strong></td>
<td><p>Ein Nachrichtenparameter.</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef LONG_PTR LPARAM;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPBOOL"></span><span id="lpbool"></span><strong>LPBOOL</strong></td>
<td><p>Ein Zeiger auf eine <a href="#bool"><strong>BOOL-</strong></a>.</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef BOOL far *LPBOOL;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPBYTE"></span><span id="lpbyte"></span><strong>LPBYTE</strong></td>
<td><p>Ein Zeiger auf ein <a href="#byte"><strong>BYTE.</strong></a></p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef BYTE far *LPBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPCOLORREF"></span><span id="lpcolorref"></span><strong>LPCOLORREF</strong></td>
<td><p>Ein Zeiger auf einen <a href="/windows/desktop/gdi/colorref"><strong>COLORREF-Wert.</strong></a></p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef DWORD *LPCOLORREF;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPCSTR"></span><span id="lpcstr"></span><strong>LPCSTR</strong></td>
<td><p>Ein Zeiger auf eine konstante NULL-endende Zeichenfolge mit 8-Bit-Windows (ANSI)-Zeichen. Weitere Informationen finden Sie unter <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Von Schriftarten verwendete Zeichensätze.</a></p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<p><code>typedef __nullterminated CONST CHAR *LPCSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPCTSTR"></span><span id="lpctstr"></span><strong>LPCTSTR</strong></td>
<td><p>Ein <a href="#lpcwstr"><strong>LPCWSTR,</strong></a> wenn <strong>UNICODE</strong> definiert ist, andernfalls <a href="#lpcstr"><strong>ein LPCSTR.</strong></a> Weitere Informationen finden Sie unter <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Datentypen für Zeichenfolgen.</a></p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="LPCVOID"></span><span id="lpcvoid"></span><strong>LPCVOID</strong></td>
<td><p>Ein Zeiger auf eine Konstante eines beliebigen Typs.</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef CONST void *LPCVOID;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPCWSTR"></span><span id="lpcwstr"></span><strong>LPCWSTR</strong></td>
<td><p>Ein Zeiger auf eine konstante NULL-endende Zeichenfolge mit 16-Bit-Unicode-Zeichen. Weitere Informationen finden Sie unter <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Von Schriftarten verwendete Zeichensätze.</a></p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<p><code>typedef CONST WCHAR *LPCWSTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPDWORD"></span><span id="lpdword"></span><strong>LPDWORD</strong></td>
<td><p>Ein Zeiger auf eine <a href="#dword"><strong>DWORD-.</strong></a></p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef DWORD *LPDWORD;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPHANDLE"></span><span id="lphandle"></span><strong>LPHANDLE</strong></td>
<td><p>Ein Zeiger auf ein <a href="#handle"><strong>HANDLE.</strong></a></p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef HANDLE *LPHANDLE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPINT"></span><span id="lpint"></span><strong>LPINT</strong></td>
<td><p>Ein Zeiger auf einen <a href="#int"><strong>INT.</strong></a></p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef int *LPINT;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPLONG"></span><span id="lplong"></span><strong>LPLONG</strong></td>
<td><p>Ein Zeiger auf eine <a href="#long"><strong>LONG-.</strong></a></p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef long *LPLONG;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPSTR"></span><span id="lpstr"></span><strong>Lpstr</strong></td>
<td><p>Ein Zeiger auf eine auf NULL endende Zeichenfolge mit 8-Bit-Windows(ANSI)-Zeichen. Weitere Informationen finden Sie unter <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Von Schriftarten verwendete Zeichensätze.</a></p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<p><code>typedef CHAR *LPSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPTSTR"></span><span id="lptstr"></span><strong>Lptstr</strong></td>
<td><p>Ein <a href="#lpwstr"><strong>LPWSTR,</strong></a> wenn <strong>UNICODE</strong> definiert ist, andernfalls ein <a href="#lpstr"><strong>LPSTR.</strong></a> Weitere Informationen finden Sie unter <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Datentypen für Zeichenfolgen.</a></p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="LPVOID"></span><span id="lpvoid"></span><strong>LPVOID</strong></td>
<td><p>Ein Zeiger auf einen beliebigen Typ.</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef void *LPVOID;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPWORD"></span><span id="lpword"></span><strong>LPWORD</strong></td>
<td><p>Ein Zeiger auf eine <a href="#word"><strong>WORD-.</strong></a></p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef WORD *LPWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPWSTR"></span><span id="lpwstr"></span><strong>Lpwstr</strong></td>
<td><p>Ein Zeiger auf eine auf NULL endende Zeichenfolge mit 16-Bit-Unicode-Zeichen. Weitere Informationen finden Sie unter <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Von Schriftarten verwendete Zeichensätze.</a></p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<p><code>typedef WCHAR *LPWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="LRESULT"></span><span id="lresult"></span><strong>Lresult</strong></td>
<td><p>Signiertes Ergebnis der Nachrichtenverarbeitung.</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef LONG_PTR LRESULT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PBOOL"></span><span id="pbool"></span><strong>PBOOL</strong></td>
<td><p>Ein Zeiger auf eine <a href="#bool"><strong>BOOL-</strong></a>.</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef BOOL *PBOOL;</code></p></td>
</tr>
<tr class="even">
<td><span id="PBOOLEAN"></span><span id="pboolean"></span><strong>PBOOLEAN</strong></td>
<td><p>Ein Zeiger auf einen <a href="#boolean"><strong>BOOLESCHEN</strong></a>Wert.</p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<p><code>typedef BOOLEAN *PBOOLEAN;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PBYTE"></span><span id="pbyte"></span><strong>PBYTE</strong></td>
<td><p>Ein Zeiger auf ein <a href="#byte"><strong>BYTE.</strong></a></p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef BYTE *PBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span id="PCHAR"></span><span id="pchar"></span><strong>PCHAR</strong></td>
<td><p>Ein Zeiger auf eine <a href="#char"><strong>CHAR-.</strong></a></p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<p><code>typedef CHAR *PCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PCSTR"></span><span id="pcstr"></span><strong>PCSTR</strong></td>
<td><p>Ein Zeiger auf eine konstante NULL-terminierte Zeichenfolge mit 8-Bit-Windows Zeichen (ANSI). Weitere Informationen finden Sie unter <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Von Schriftarten verwendete Zeichensätze.</a></p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<p><code>typedef CONST CHAR *PCSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="PCTSTR"></span><span id="pctstr"></span><strong>PCTSTR</strong></td>
<td><p>Ein <a href="#pcwstr"><strong>PCWSTR,</strong></a> wenn <strong>UNICODE</strong> definiert ist, andernfalls ein <a href="#pcstr"><strong>PCSTR.</strong></a> Weitere Informationen finden Sie unter <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Datentypen für Zeichenfolgen.</a></p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="PCWSTR"></span><span id="pcwstr"></span><strong>PCWSTR</strong></td>
<td><p>Ein Zeiger auf eine konstante NULL-endende Zeichenfolge mit 16-Bit-Unicode-Zeichen. Weitere Informationen finden Sie unter <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Von Schriftarten verwendete Zeichensätze.</a></p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<p><code>typedef CONST WCHAR *PCWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="PDWORD"></span><span id="pdword"></span><strong>PDWORD</strong></td>
<td><p>Ein Zeiger auf eine <a href="#dword"><strong>DWORD-.</strong></a></p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef DWORD *PDWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PDWORDLONG"></span><span id="pdwordlong"></span><strong>PDWORDLONG</strong></td>
<td><p>Ein Zeiger auf eine <a href="#dwordlong"><strong>DWORDLONG -Datei.</strong></a></p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<p><code>typedef DWORDLONG *PDWORDLONG;</code></p></td>
</tr>
<tr class="even">
<td><span id="PDWORD_PTR"></span><span id="pdword_ptr"></span><strong>PDWORD_PTR</strong></td>
<td><p>Ein Zeiger auf eine <a href="#dword_ptr"><strong>DWORD_PTR</strong></a>.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef DWORD_PTR *PDWORD_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PDWORD32"></span><span id="pdword32"></span><strong>PDWORD32</strong></td>
<td><p>Ein Zeiger auf ein <a href="#dword32"><strong>DWORD32-</strong></a>.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef DWORD32 *PDWORD32;</code></p></td>
</tr>
<tr class="even">
<td><span id="PDWORD64"></span><span id="pdword64"></span><strong>PDWORD64</strong></td>
<td><p>Ein Zeiger auf ein <a href="#dword64"><strong>DWORD64-.</strong></a></p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef DWORD64 *PDWORD64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PFLOAT"></span><span id="pfloat"></span><strong>PFLOAT</strong></td>
<td><p>Ein Zeiger auf eine <a href="#float"><strong>FLOAT-.</strong></a></p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef FLOAT *PFLOAT;</code></p></td>
</tr>
<tr class="even">
<td><span id="PHALF_PTR"></span><span id="phalf_ptr"></span><strong>PHALF_PTR</strong></td>
<td><p>Ein Zeiger auf einen <a href="#half_ptr"><strong>HALF_PTR</strong></a>.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="PHANDLE"></span><span id="phandle"></span><strong>PHANDLE</strong></td>
<td><p>Ein Zeiger auf ein <a href="#handle"><strong>HANDLE.</strong></a></p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<p><code>typedef HANDLE *PHANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span id="PHKEY"></span><span id="phkey"></span><strong>PHKEY</strong></td>
<td><p>Ein Zeiger auf einen <a href="#hkey"><strong>HKEY.</strong></a></p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef HKEY *PHKEY;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PINT"></span><span id="pint"></span><strong>Pint</strong></td>
<td><p>Ein Zeiger auf einen <a href="#int"><strong>INT.</strong></a></p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef int *PINT;</code></p></td>
</tr>
<tr class="even">
<td><span id="PINT_PTR"></span><span id="pint_ptr"></span><strong>PINT_PTR</strong></td>
<td><p>Ein Zeiger auf eine <a href="#int_ptr"><strong>INT_PTR</strong></a>.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef INT_PTR *PINT_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PINT8"></span><span id="pint8"></span><strong>PINT8</strong></td>
<td><p>Ein Zeiger auf eine <a href="#int8"><strong>INT8-.</strong></a></p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef INT8 *PINT8;</code></p></td>
</tr>
<tr class="even">
<td><span id="PINT16"></span><span id="pint16"></span><strong>PINT16</strong></td>
<td><p>Ein Zeiger auf ein <a href="#int16"><strong>INT16</strong></a>-.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef INT16 *PINT16;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PINT32"></span><span id="pint32"></span><strong>PINT32</strong></td>
<td><p>Ein Zeiger auf eine <a href="#int32"><strong>INT32-.</strong></a></p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef INT32 *PINT32;</code></p></td>
</tr>
<tr class="even">
<td><span id="PINT64"></span><span id="pint64"></span><strong>PINT64</strong></td>
<td><p>Ein Zeiger auf ein <a href="#int64"><strong>INT64-.</strong></a></p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef INT64 *PINT64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PLCID"></span><span id="plcid"></span><strong>PLCID</strong></td>
<td><p>Ein Zeiger auf eine <a href="#lcid"><strong>LCID.</strong></a></p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<p><code>typedef PDWORD PLCID;</code></p></td>
</tr>
<tr class="even">
<td><span id="PLONG"></span><span id="plong"></span><strong>PLONG</strong></td>
<td><p>Ein Zeiger auf eine <a href="#long"><strong>LONG-.</strong></a></p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<p><code>typedef LONG *PLONG;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PLONGLONG"></span><span id="plonglong"></span><strong>PLONGLONG</strong></td>
<td><p>Ein Zeiger auf eine <a href="#longlong"><strong>LONGLONG-.</strong></a></p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<p><code>typedef LONGLONG *PLONGLONG;</code></p></td>
</tr>
<tr class="even">
<td><span id="PLONG_PTR"></span><span id="plong_ptr"></span><strong>PLONG_PTR</strong></td>
<td><p>Ein Zeiger auf eine <a href="#long_ptr"><strong>LONG_PTR</strong></a>.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef LONG_PTR *PLONG_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PLONG32"></span><span id="plong32"></span><strong>PLONG32</strong></td>
<td><p>Ein Zeiger auf eine <a href="#long32"><strong>LONG32-.</strong></a></p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef LONG32 *PLONG32;</code></p></td>
</tr>
<tr class="even">
<td><span id="PLONG64"></span><span id="plong64"></span><strong>PLONG64</strong></td>
<td><p>Ein Zeiger auf eine <a href="#long64"><strong>LONG64-.</strong></a></p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef LONG64 *PLONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="POINTER_32"></span><span id="pointer_32"></span><strong>POINTER_32</strong></td>
<td><p>Ein 32-Bit-Zeiger. Auf einem 32-Bit-System ist dies ein nativer Zeiger. Auf einem 64-Bit-System ist dies ein abgeschnittener 64-Bit-Zeiger.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="POINTER_64"></span><span id="pointer_64"></span><strong>POINTER_64</strong></td>
<td><p>Ein 64-Bit-Zeiger. Auf einem 64-Bit-System ist dies ein nativer Zeiger. Auf einem 32-Bit-System ist dies ein 32-Bit-Zeiger mit Vorzeichenerweiterung.</p>
<p>Beachten Sie, dass es nicht sicher ist, den Zustand des hohen Zeigerbits anzunehmen.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="POINTER_SIGNED"></span><span id="pointer_signed"></span><strong>POINTER_SIGNED</strong></td>
<td><p>Ein Zeiger mit Vorzeichen.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>#define POINTER_SIGNED __sptr</code></p></td>
</tr>
<tr class="even">
<td><span id="POINTER_UNSIGNED"></span><span id="pointer_unsigned"></span><strong>POINTER_UNSIGNED</strong></td>
<td><p>Ein Zeiger ohne Vorzeichen.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>#define POINTER_UNSIGNED __uptr</code></p></td>
</tr>
<tr class="odd">
<td><span id="PSHORT"></span><span id="pshort"></span><strong>PSHORT</strong></td>
<td><p>Ein Zeiger auf eine <a href="#short"><strong>KURZE</strong></a>.</p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<p><code>typedef SHORT *PSHORT;</code></p></td>
</tr>
<tr class="even">
<td><span id="PSIZE_T"></span><span id="psize_t"></span><strong>PSIZE_T</strong></td>
<td><p>Ein Zeiger auf eine <a href="#size_t"><strong>SIZE_T</strong></a>.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef SIZE_T *PSIZE_T;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PSSIZE_T"></span><span id="pssize_t"></span><strong>PSSIZE_T</strong></td>
<td><p>Ein Zeiger auf eine <a href="#ssize_t"><strong>SSIZE_T</strong></a>.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef SSIZE_T *PSSIZE_T;</code></p></td>
</tr>
<tr class="even">
<td><span id="PSTR"></span><span id="pstr"></span><strong>Pstr</strong></td>
<td><p>Ein Zeiger auf eine nullbeendte Zeichenfolge mit 8-Bit-Windows Zeichen (ANSI). Weitere Informationen finden Sie unter <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Von Schriftarten verwendete Zeichensätze.</a></p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<p><code>typedef CHAR *PSTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PTBYTE"></span><span id="ptbyte"></span><strong>PTBYTE</strong></td>
<td><p>Ein Zeiger auf eine <a href="#tbyte"><strong>TBYTE-.</strong></a></p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<p><code>typedef TBYTE *PTBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span id="PTCHAR"></span><span id="ptchar"></span><strong>PTCHAR</strong></td>
<td><p>Ein Zeiger auf eine <a href="#tchar"><strong>TCHAR-</strong></a>.</p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<p><code>typedef TCHAR *PTCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PTSTR"></span><span id="ptstr"></span><strong>PTSTR</strong></td>
<td><p>Ein <a href="#pwstr"><strong>PWSTR,</strong></a> wenn <strong>UNICODE</strong> definiert ist, <a href="#pstr"><strong>andernfalls ein PSTR.</strong></a> Weitere Informationen finden Sie unter <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Datentypen für Zeichenfolgen.</a></p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="PUCHAR"></span><span id="puchar"></span><strong>PUCHAR</strong></td>
<td><p>Ein Zeiger auf eine <a href="#uchar"><strong>UCHAR-</strong></a>.</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef UCHAR *PUCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUHALF_PTR"></span><span id="puhalf_ptr"></span><strong>PUHALF_PTR</strong></td>
<td><p>Ein Zeiger auf eine <a href="#uhalf_ptr"><strong>UHALF_PTR</strong></a>.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="PUINT"></span><span id="puint"></span><strong>PUINT</strong></td>
<td><p>Ein Zeiger auf einen <a href="#uint"><strong>UINT.</strong></a></p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef UINT *PUINT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUINT_PTR"></span><span id="puint_ptr"></span><strong>PUINT_PTR</strong></td>
<td><p>Ein Zeiger auf eine <a href="#uint_ptr"><strong>UINT_PTR</strong></a>.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef UINT_PTR *PUINT_PTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="PUINT8"></span><span id="puint8"></span><strong>PUINT8</strong></td>
<td><p>Ein Zeiger auf einen <a href="#uint8"><strong>UINT8-</strong></a>.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef UINT8 *PUINT8;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUINT16"></span><span id="puint16"></span><strong>PUINT16</strong></td>
<td><p>Ein Zeiger auf einen <a href="#uint16"><strong>UINT16.</strong></a></p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef UINT16 *PUINT16;</code></p></td>
</tr>
<tr class="even">
<td><span id="PUINT32"></span><span id="puint32"></span><strong>PUINT32</strong></td>
<td><p>Ein Zeiger auf einen <a href="#uint32"><strong>UINT32.</strong></a></p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef UINT32 *PUINT32;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUINT64"></span><span id="puint64"></span><strong>PUINT64</strong></td>
<td><p>Ein Zeiger auf einen <a href="#uint64"><strong>UINT64.</strong></a></p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef UINT64 *PUINT64;</code></p></td>
</tr>
<tr class="even">
<td><span id="PULONG"></span><span id="pulong"></span><strong>PULONG</strong></td>
<td><p>Ein Zeiger auf eine <a href="#ulong"><strong>ULONG-</strong></a>.</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef ULONG *PULONG;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PULONGLONG"></span><span id="pulonglong"></span><strong>PULONGLONG</strong></td>
<td><p>Ein Zeiger auf einen <a href="#ulonglong"><strong>ULONGLONG-.</strong></a></p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef ULONGLONG *PULONGLONG;</code></p></td>
</tr>
<tr class="even">
<td><span id="PULONG_PTR"></span><span id="pulong_ptr"></span><strong>PULONG_PTR</strong></td>
<td><p>Ein Zeiger auf eine <a href="#ulong_ptr"><strong>ULONG_PTR</strong></a>.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef ULONG_PTR *PULONG_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PULONG32"></span><span id="pulong32"></span><strong>PULONG32</strong></td>
<td><p>Ein Zeiger auf einen <a href="#ulong32"><strong>ULONG32.</strong></a></p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef ULONG32 *PULONG32;</code></p></td>
</tr>
<tr class="even">
<td><span id="PULONG64"></span><span id="pulong64"></span><strong>PULONG64</strong></td>
<td><p>Ein Zeiger auf einen <a href="#ulong64"><strong>ULONG64-</strong></a>.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef ULONG64 *PULONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUSHORT"></span><span id="pushort"></span><strong>PUSHORT</strong></td>
<td><p>Ein Zeiger auf eine <a href="#ushort"><strong>USHORT-</strong></a>.</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef USHORT *PUSHORT;</code></p></td>
</tr>
<tr class="even">
<td><span id="PVOID"></span><span id="pvoid"></span><strong>PVOID</strong></td>
<td><p>Ein Zeiger auf einen beliebigen Typ.</p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<p><code>typedef void *PVOID;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PWCHAR"></span><span id="pwchar"></span><strong>PWCHAR</strong></td>
<td><p>Ein Zeiger auf eine <a href="#wchar"><strong>WCHAR-</strong></a>.</p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<p><code>typedef WCHAR *PWCHAR;</code></p></td>
</tr>
<tr class="even">
<td><span id="PWORD"></span><span id="pword"></span><strong>PWORD</strong></td>
<td><p>Ein Zeiger auf eine <a href="#word"><strong>WORD-.</strong></a></p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef WORD *PWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PWSTR"></span><span id="pwstr"></span><strong>PWSTR</strong></td>
<td><p>Ein Zeiger auf eine auf NULL beendete Zeichenfolge mit 16-Bit-Unicode-Zeichen. Weitere Informationen finden Sie unter <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Von Schriftarten verwendete Zeichensätze.</a></p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<p><code>typedef WCHAR *PWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="QWORD"></span><span id="qword"></span><strong>Qword</strong></td>
<td><p>Eine 64-Bit-Ganzzahl ohne Vorzeichen.</p>
<p>Dieser Typ wird wie folgt deklariert:</p>
<p><code>typedef unsigned __int64 QWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="SC_HANDLE"></span><span id="sc_handle"></span><strong>SC_HANDLE</strong></td>
<td><p>Ein Handle für eine Dienststeuerungs-Manager-Datenbank. Weitere Informationen finden Sie unter <a href="/windows/desktop/Services/scm-handles">SCM-Handles.</a></p>
<p>Dieser Typ wird in WinSvc.h wie folgt deklariert:</p>
<p><code>typedef HANDLE SC_HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span id="SC_LOCK"></span><span id="sc_lock"></span><strong>SC_LOCK</strong></td>
<td><p>Eine Sperre für eine Dienststeuerungs-Manager-Datenbank. Weitere Informationen finden Sie unter <a href="/windows/desktop/Services/scm-handles">SCM-Handles.</a></p>
<p>Dieser Typ wird in WinSvc.h wie folgt deklariert:</p>
<p><code>typedef LPVOID SC_LOCK;</code></p></td>
</tr>
<tr class="odd">
<td><span id="SERVICE_STATUS_HANDLE"></span><span id="service_status_handle"></span><strong>SERVICE_STATUS_HANDLE</strong></td>
<td><p>Ein Handle für einen Dienststatuswert. Weitere Informationen finden Sie unter <a href="/windows/desktop/Services/scm-handles">SCM-Handles.</a></p>
<p>Dieser Typ wird in WinSvc.h wie folgt deklariert:</p>
<p><code>typedef HANDLE SERVICE_STATUS_HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span id="SHORT"></span><span id="short"></span><strong>kurz</strong></td>
<td><p>Eine 16-Bit-Ganzzahl. Der Bereich ist -32768 bis 32767 dezimal.</p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<p><code>typedef short SHORT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="SIZE_T"></span><span id="size_t"></span><strong>Size_t</strong></td>
<td><p>Die maximale Anzahl von Bytes, auf die ein Zeiger zeigen kann. Verwenden Sie für eine Anzahl, die den gesamten Bereich eines Zeigers umfassen muss.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef ULONG_PTR SIZE_T;</code></p></td>
</tr>
<tr class="even">
<td><span id="SSIZE_T"></span><span id="ssize_t"></span><strong>SSIZE_T</strong></td>
<td><p>Eine signierte Version von <a href="#size_t"><strong>SIZE_T</strong></a>.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef LONG_PTR SSIZE_T;</code></p></td>
</tr>
<tr class="odd">
<td><span id="TBYTE"></span><span id="tbyte"></span><strong>Tbyte</strong></td>
<td><p>Ein <a href="#wchar"><strong>WCHAR,</strong></a> wenn <strong>UNICODE</strong> definiert ist, andernfalls ein <a href="#char"><strong>CHAR.</strong></a></p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="TCHAR"></span><span id="tchar"></span><strong>Tchar</strong></td>
<td><p>Ein <a href="#wchar"><strong>WCHAR,</strong></a> wenn <strong>UNICODE</strong> definiert ist, andernfalls ein <a href="#char"><strong>CHAR.</strong></a></p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="UCHAR"></span><span id="uchar"></span><strong>UCHAR</strong></td>
<td><p>Ein <a href="#char"><strong>char-Zeichen</strong></a>ohne Vorzeichen.</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef unsigned char UCHAR;</code></p></td>
</tr>
<tr class="even">
<td><span id="UHALF_PTR"></span><span id="uhalf_ptr"></span><strong>UHALF_PTR</strong></td>
<td><p>Ein HALF_PTR <a href="#half_ptr"><strong>ohne</strong></a>Vorzeichen. Verwenden Sie in einer -Struktur, die einen Zeiger und zwei kleine Felder enthält.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="UINT"></span><span id="uint"></span><strong>Uint</strong></td>
<td><p>Ein <a href="#int"><strong>int-Zeichen</strong></a>ohne Vorzeichen. Der Bereich ist 0 bis 4294967295 Dezimalzahl.</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef unsigned int UINT;</code></p></td>
</tr>
<tr class="even">
<td><span id="UINT_PTR"></span><span id="uint_ptr"></span><strong>UINT_PTR</strong></td>
<td><p>Ein nicht signierter <a href="#int_ptr"><strong>INT_PTR</strong></a>.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="UINT8"></span><span id="uint8"></span><strong>UINT8</strong></td>
<td><p>Ein <a href="#int8"><strong>int8-Zeichen</strong></a>ohne Vorzeichen.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef unsigned  char UINT8;</code></p></td>
</tr>
<tr class="even">
<td><span id="UINT16"></span><span id="uint16"></span><strong>UINT16</strong></td>
<td><p>Ein nicht signierter <a href="#int16"><strong>INT16</strong></a>.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef unsigned  short UINT16;</code></p></td>
</tr>
<tr class="odd">
<td><span id="UINT32"></span><span id="uint32"></span><strong>UINT32</strong></td>
<td><p>Ein <a href="#int32"><strong>int32</strong></a>ohne Vorzeichen. Der Bereich ist 0 bis 4294967295 Dezimalzahl.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef unsigned int UINT32;</code></p></td>
</tr>
<tr class="even">
<td><span id="UINT64"></span><span id="uint64"></span><strong>UINT64</strong></td>
<td><p>Ein <a href="#int64"><strong>int64-Zeichen</strong></a>ohne Vorzeichen. Der Bereich ist 0 bis 18446744073709551615 Dezimalzahl.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef usigned __int 64 UINT64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="ULONG"></span><span id="ulong"></span><strong>Ulong</strong></td>
<td><p>Ein unsigned <a href="#long"><strong>LONG</strong></a>. Der Bereich ist 0 bis 4294967295 Dezimalzahl.</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef unsigned long ULONG;</code></p></td>
</tr>
<tr class="even">
<td><span id="ULONGLONG"></span><span id="ulonglong"></span><strong>ULONGLONG</strong></td>
<td><p>Eine 64-Bit-Ganzzahl ohne Vorzeichen. Der Bereich ist 0 bis 18446744073709551615 Dezimalzahl.</p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="ULONG_PTR"></span><span id="ulong_ptr"></span><strong>ULONG_PTR</strong></td>
<td><p>Ein LONG_PTR <a href="#long_ptr"><strong>ohne</strong></a>Vorzeichen.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="ULONG32"></span><span id="ulong32"></span><strong>Ulong32</strong></td>
<td><p>Ein <a href="#long32"><strong>long32-Zeichen</strong></a>ohne Vorzeichen. Der Bereich ist 0 bis 4294967295 Dezimalzahl.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef unsigned int ULONG32;</code></p></td>
</tr>
<tr class="odd">
<td><span id="ULONG64"></span><span id="ulong64"></span><strong>ULONG64</strong></td>
<td><p>Ein <a href="#long64"><strong>long64-Zeichen</strong></a>ohne Vorzeichen. Der Bereich ist 0 bis 18446744073709551615 Dezimalzahl.</p>
<p>Dieser Typ wird in BaseTsd.h wie folgt deklariert:</p>
<p><code>typedef unsigned __int64 ULONG64;</code></p></td>
</tr>
<tr class="even">
<td><span id="UNICODE_STRING"></span><span id="unicode_string"></span><strong>UNICODE_STRING</strong></td>
<td><p>Eine Unicode-Zeichenfolge.</p>
<p>Dieser Typ wird in Derl.h wie folgt deklariert:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="USHORT"></span><span id="ushort"></span><strong>Ushort</strong></td>
<td><p>Ein <a href="#short"><strong>short-Zeichen</strong></a>ohne Vorzeichen. Der Bereich ist 0 bis 65535 dezimal.</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef unsigned short USHORT;</code></p></td>
</tr>
<tr class="even">
<td><span id="USN"></span><span id="usn"></span><strong>Usn</strong></td>
<td><p>Eine Updatesequenznummer (USN).</p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<p><code>typedef LONGLONG USN;</code></p></td>
</tr>
<tr class="odd">
<td><span id="VOID"></span><span id="void"></span><strong>Leere</strong></td>
<td><p>Beliebiger Typ</p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<p><code>#define VOID void</code></p></td>
</tr>
<tr class="even">
<td><span id="WCHAR"></span><span id="wchar"></span><strong>Wchar</strong></td>
<td><p>Ein 16-Bit-Unicode-Zeichen. Weitere Informationen finden Sie unter <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Von Schriftarten verwendete Zeichensätze.</a></p>
<p>Dieser Typ wird in WinNT.h wie folgt deklariert:</p>
<p><code>typedef wchar_t WCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="WINAPI"></span><span id="winapi"></span><strong>Winapi</strong></td>
<td><p>Die Aufrufkonvention für Systemfunktionen.</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>#define WINAPI __stdcall</code></p>
<p><strong>CALLBACK,</strong> <strong>WINAPI</strong>und <strong>APIENTRY</strong> werden alle verwendet, um Funktionen mit der __stdcall Aufrufkonvention zu definieren. Die meisten Funktionen in der Windows-API werden mit <strong>winapi</strong>deklariert. Möglicherweise möchten Sie <strong>CALLBACK</strong> für die Rückruffunktionen verwenden, die Sie implementieren, um die Funktion als Rückruffunktion zu identifizieren.</p></td>
</tr>
<tr class="even">
<td><span id="WORD"></span><span id="word"></span><strong>Wort</strong></td>
<td><p>Eine 16-Bit-Ganzzahl ohne Vorzeichen. Der Bereich ist 0 bis 65535 dezimal.</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef unsigned short WORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="WPARAM"></span><span id="wparam"></span><strong>Wparam</strong></td>
<td><p>Ein Nachrichtenparameter.</p>
<p>Dieser Typ wird in WinDef.h wie folgt deklariert:</p>
<p><code>typedef UINT_PTR WPARAM;</code></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                                                                                                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                                                                                                                                |
| Header<br/>                   | <dl> <dt>BaseTsd.h; </dt> <dt>WinDef.h; </dt> <dt>WinNT.h</dt> </dl> |
