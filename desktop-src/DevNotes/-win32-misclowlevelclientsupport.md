---
description: Dieses Thema enthält Informationen über Low-Level-APIs, die von der Windows-Client Infrastruktur verwendet werden.
ms.assetid: 14a6e970-2032-420e-9930-a15909dbbb97
title: Sonstige Low-Level Client Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11558c9994a9c622f71e803521352d1073e68c05
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860566"
---
# <a name="miscellaneous-low-level-client-support"></a>Sonstige Low-Level Client Unterstützung

Dieses Thema enthält Informationen über Low-Level-APIs, die von der Windows-Client Infrastruktur verwendet werden.

### <a name="functions"></a>Functions



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Thema</th>
<th>Inhalte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/winbase/nf-winbase-_lclose"><strong>_lclose</strong></a></td>
<td>Die _lclose-Funktion schließt die angegebene Datei, sodass Sie nicht mehr zum Lesen oder schreiben verfügbar ist. Diese Funktion wird aus Gründen der Kompatibilität mit 16-Bit-Versionen von Windows bereitgestellt. Win32-basierte Anwendungen sollten die CloseHandle-Funktion verwenden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winbase/nf-winbase-_lopen"><strong>_lopen</strong></a></td>
<td>Die _lopen-Funktion öffnet eine vorhandene Datei und legt den Dateizeiger auf den Anfang der Datei fest. Diese Funktion wird aus Gründen der Kompatibilität mit 16-Bit-Versionen von Windows bereitgestellt. Win32-basierte Anwendungen sollten die Funktion "Up File" verwenden. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winbase/nf-winbase-_lread"><strong>_lread</strong></a></td>
<td>Die _lread-Funktion liest Daten aus der angegebenen Datei. Diese Funktion wird aus Gründen der Kompatibilität mit 16-Bit-Versionen von Windows bereitgestellt. Win32-basierte Anwendungen sollten die Funktion "Read File" verwenden. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-aredvdcodecsenabled"><strong>Aredvdcodecsenabled</strong></a></td>
<td>Gibt einen Wert zurück, der angibt, ob DVD-Codecs auf dem aktuellen Gerät aktiviert sind.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-disableprocesswindowsghosting"><strong>Disableprocesswindowsghosting</strong></a></td>
<td>Deaktiviert die Fenster-Ghosting-Funktion für den aufrufenden GUI-Prozess. Window Ghosting ist ein Windows-Manager-Feature, mit dem der Benutzer das Hauptfenster einer Anwendung, die nicht antwortet, minimieren, verschieben oder schließen kann.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediacomponentpackageinfo"><strong>Getmediacomponentpackageingefo</strong></a></td>
<td>Gibt eine Liste der Eigenschaften für alle auf dem System installierten Medien Codecs zurück, die die angegebenen Anforderungen erfüllen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediaextensioncommunicationfactory"><strong>Getmediaextensioncommunicationfactory</strong></a></td>
<td>Erstellt eine kommunikationfactory zum Registrieren einer medienerweiterung.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-instantiatecomponentfrompackage"><strong>Instantiatecomponentfrompackage</strong></a></td>
<td>Erstellt eine Instanz einer-Klasse in einem Anwendungspaket. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-ismediabehaviorenabled"><strong>Ismediaverhaloraktivierte</strong></a></td>
<td>Ruft einen Wert ab, der angibt, ob das mit der angegebenen GUID verknüpfte Medienverhalten aktiviert ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a></td>
<td>Veraltet. Diese Funktion wird verwendet, um das angegebene Handle zu schließen. <a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a> wird durch <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>abgelöst.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>Ntdeviceiocontrolfile</strong></a></td>
<td>Veraltet. Erstellt Deskriptoren für den angegebenen Puffer und übergibt die nicht typisierten Daten an den Gerätetreiber, der dem Datei Handle zugeordnet ist. <a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>Ntdeviceiocontrolfile</strong></a> wird von <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>abgelöst.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>Ntwaitforsingleobject</strong></a></td>
<td>Veraltet. Wartet, bis das angegebene Objekt den Zustand hat <code>signaled</code> . <a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>Ntwaitforsingleobject</strong></a> wird durch <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a>abgelöst.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>Rtlansistringdeunicodestring</strong></a></td>
<td>Konvertiert die angegebene ANSI-Quell Zeichenfolge in eine Unicode-Zeichenfolge. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlchartointeger"><strong>Rtlcharto Integer</strong></a></td>
<td>Konvertiert eine Zeichenfolge in eine ganze Zahl.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions//ff899322(v=vs.85)"><strong>Rtlformatcurrentuserkeypath</strong></a></td>
<td>Initialisiert den angegebenen Puffer mit einer Zeichen folgen Darstellung der sid für den aktuellen Benutzer. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeansistring"><strong>Rtlfreansistring</strong></a></td>
<td>Gibt den von <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>rtlunicodestringdeansistring</strong></a>zugewiesenen Zeichen folgen Puffer frei.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeoemstring"><strong>Rtlfreoemstring</strong></a></td>
<td>Gibt den von <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>rtlunicodestringdeoemstring</strong></a>zugewiesenen Zeichen folgen Puffer frei.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeunicodestring"><strong>Rtlfreunicodestring</strong></a></td>
<td>Gibt den von <a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>rtlansistringdeunicodestring</strong></a> oder <a href="https://msdn.microsoft.com/library/ms803011.aspx">rtlupcaseunicodestring</a>zugewiesenen Zeichen folgen Puffer frei.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitstring"><strong>Rtlinitstring</strong></a></td>
<td>Initialisiert eine gezählte Zeichenfolge. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitunicodestring"><strong>Rtlinitunicodestring</strong></a></td>
<td>Initialisiert eine gezählte Unicode-Zeichenfolge. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>Rtlunicodestringdeansistring</strong></a></td>
<td>Konvertiert die angegebene Unicode-Quell Zeichenfolge in eine ANSI-Zeichenfolge. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>Rtlunicodestringdeoemstring</strong></a></td>
<td>Diese Funktion konvertiert die angegebene Unicode-Quell Zeichenfolge in eine OEM-Zeichenfolge. Die Übersetzung erfolgt in Bezug auf die OEM-Codepage (OCP). <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodetomultibytesize"><strong>Rtlunicodetomultibytesize</strong></a></td>
<td>Bestimmt, wie viele Bytes erforderlich sind, um eine Unicode-Zeichenfolge als ANSI-Zeichenfolge darzustellen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a></td>
<td>Die <a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a> -Funktion übersetzt die angegebene Unicode-Zeichenfolge mithilfe der UTF-8-Codepage (8-Bit-Unicode Transformation Format) in eine neue Zeichenfolge.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a></td>
<td>Die <a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a> -Funktion übersetzt die angegebene Quell Zeichenfolge mithilfe der UTF-8-Codepage in eine Unicode-Zeichenfolge.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Ime/nf-ime-sendimemessageexa"><strong>Sendimemessageex</strong></a></td>
<td>Gibt eine Aktion oder Verarbeitung für den Eingabemethoden-Editor (IME) durch eine angegebene Unterfunktion an.
<blockquote>
[!Note]<br />
Diese Funktion ist veraltet und sollte nicht verwendet werden.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winnls32/nf-winnls32-winnlsenableime"><strong>Winnlsenableime</strong></a></td>
<td>Aktiviert oder deaktiviert vorübergehend einen IME und aktiviert oder deaktiviert die Anzeige aller Fenster, die im Besitz des IME sind.
<blockquote>
[!Note]<br />
Diese Funktion ist veraltet und sollte nicht verwendet werden.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="structures"></a>Strukturen



| Thema                                 | Inhalte                                                                                                                                                                                                                              |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Imestruct**](/windows/win32/api/ime/ns-ime-imestruct) | Wird von [**sendimemessageex**](/windows/desktop/api/Ime/nf-ime-sendimemessageexa) verwendet, um die Unterfunktion anzugeben, die in der IME-Nachricht und ihren Parametern ausgeführt werden soll. Diese Struktur wird auch zum Empfangen von Rückgabe Werten von diesen unter Funktionen verwendet.<br/> |
| [**Schnür**](/windows/desktop/api/Winternl/ns-winternl-string)       | Diese Struktur wird mit der [**rtlunicodestringdeoemstring**](/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring) -Funktion verwendet. <br/>                                                                                                              |



 

### <a name="compiler-routines"></a>Compilerroutinen



| Thema                                                             | Inhalte                                                                                                     |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**\_\_C- \_ spezifische \_ Handlerroutine**](--c-specific-handler2.md) | [**\_ \_ C- \_ spezifischer \_ Handler**](--c-specific-handler2.md) ist eine Hilfsroutine für den c-Compiler.<br/> |
| [\_alldiv-Routine](-win32-alldiv.md)                             | [ \_ alldiv Routine](-win32-alldiv.md) ist eine Hilfsroutine für den C-Compiler.<br/>                     |
| [\_allmul](-win32-allmul.md) | Multipliziert zwei **Longlong** oder **ULONGLONG**. |
| [\_aulldiv](-win32-aulldiv.md) | Dividiert zwei **ULONGLONG** -Ganzzahlen. |
| [\_chkstk-Routine](-win32-chkstk.md)                             | die [ \_ chkstk-Routine](-win32-chkstk.md) ist eine Hilfsroutine für den C-Compiler.<br/>                     |
