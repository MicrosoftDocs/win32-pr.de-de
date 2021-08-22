---
title: EM_GETEDITSTYLE Nachricht (Richedit.h)
description: Ruft die aktuellen Bearbeitungsformatflags ab.
ms.assetid: 568e51a4-0767-4a59-bf34-bc0281b5fe65
keywords:
- EM_GETEDITSTYLE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_GETEDITSTYLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb34e4912ff00d76abf8db4c631296836ad9adaf83853aa064c34b11e7f71e20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019708"
---
# <a name="em_geteditstyle-message"></a>EM \_ GETEDITSTYLE-Nachricht

Ruft die aktuellen Bearbeitungsformatflags ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die aktuellen Bearbeitungsformatflags zurück, die einen oder mehrere der folgenden Werte enthalten können:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rückgabecode</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>SES_BEEPONMAXTEXT</strong></dt> </dl></td>
<td>Rich Edit ruft den Systembeeper auf, wenn der Benutzer versucht, mehr als die maximalen Zeichen einzugeben.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_BIDI</strong></dt> </dl></td>
<td>Aktiviert die bidirektionale Verarbeitung. Dies wird von Rich Edit automatisch aktiviert, wenn einer der folgenden Fensterstile aktiv ist: <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RIGHT</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RTLREADING</strong></a> <a href="/windows/desktop/winmsg/extended-window-styles"><strong>, WS_EX_LEFTSCROLLBAR</strong></a>. Diese Einstellung ist jedoch nützlich für die Verarbeitung dieser Fensterstile bei Verwendung einer benutzerdefinierten Implementierung von <a href="/windows/desktop/api/Textserv/nl-textserv-itexthost"><strong>ITextHost</strong></a> (Standardwert: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_CTFALLOWEMBED</strong></dt> </dl></td>
<td><strong>Windows XP mit SP1:</strong>Einfügen eingebetteter Objekte mit TSF zulassen (Standardeinstellung: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_CTFALLOWPROOFING</strong></dt> </dl></td>
<td><strong>Windows XP mit SP1:</strong>Ermöglicht TSF-Korrekturtipps (Standard: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_CTFALLOWSMARTTAG</strong></dt> </dl></td>
<td><strong>Windows XP mit SP1:</strong>Ermöglicht TSF SmartTag-Tipps (Standardwert: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_CTFNOLOCK</strong></dt> </dl></td>
<td><strong>Windows 8:</strong>Erlauben Sie den Lese-/Schreibzugriff der TSF-Sperre nicht. Dadurch wird die TSF-Eingabe angehalten. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_DEFAULTLATINLIGA</strong></dt> </dl></td>
<td><strong>Windows 8:</strong>Schriftarten mit einer Filigatur werden mit OpenType-Standardfeatures angezeigt, was zu einer verbesserten Typografie führt (Standardeinstellung: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_DRAFTMODE</strong></dt> </dl></td>
<td><strong>Windows XP mit SP1:</strong>Verwenden Sie Schriftarten im Entwurfsmodus, um Text anzuzeigen. Der Entwurfsmodus ist eine Barrierefreiheitsoption, bei der das -Steuerelement den Text mit einer einzelnen Schriftart anzeigt. Die Schriftart wird durch die Systemeinstellung für die schriftart bestimmt, die in Meldungsfeldern verwendet wird. Beispielsweise können benutzerfreundliche Benutzer Text einfacher lesen, wenn er einheitlich ist, anstatt eine Mischung aus Schriftarten und Stilen (Standard: 0). <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_EMULATE10</strong></dt> </dl></td>
<td><strong>Windows 8:</strong>Emulieren des RichEdit 1.0-Verhaltens. <br/>
<blockquote>
[!Note]<br />
Wenn Sie dieses Verhalten wirklich wünschen, verwenden Sie die Windows riched32.dll anstelle von riched20.dll oder msftedit.dll. Riched32.dll verfügten über mehr Funktionalität.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_EMULATESYSEDIT</strong></dt> </dl></td>
<td>Wenn dieses Bit aktiviert ist, versucht Rich Edit, das Bearbeitungssteuerelement des Systems zu emulieren (Standardwert: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_EXTENDBACKCOLOR</strong></dt> </dl></td>
<td>Erweitert die Hintergrundfarbe bis zu den Rändern des Clientrechtecks (Standardwert: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_HIDEGRIDLINES</strong></dt> </dl></td>
<td><strong>Windows XP mit SP1:</strong>Wenn die Breite der Tabellenrasterlinien 0 (null) ist, werden keine Gitternetzlinien angezeigt. Dies entspricht dem Feature Gitternetzlinien ausblenden im Tabellenmenü von Word (Standard: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_HYPERLINKTOOLTIPS</strong></dt> </dl></td>
<td><strong>Windows 8:</strong>Wenn sich der Cursor über einem Link befindet, zeigen Sie eine QuickInfo mit der Ziellinkadresse an (Standard: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_LOGICALCARET</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: Geben Sie logische Caret-Informationen anstelle einer Caretbitmap an, wie in <a href="/windows/desktop/api/Textserv/nf-textserv-itexthost-txsetcaretpos"><strong>ITextHost::TxSetCaretPos</strong></a> (Standard: 0) beschrieben. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_LOWERCASE</strong></dt> </dl></td>
<td>Konvertiert alle Eingabezeichen in Kleinbuchstaben (Standardwert: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_MAPCPS</strong></dt> </dl></td>
<td>Veraltet. Darf nicht verwendet werden.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_MULTISELECT</strong></dt> </dl></td>
<td><strong>Windows 8:</strong>Aktivieren Sie die Mehrfachauswahl mit einzelner Mausauswahl, während die STRG-TASTE gedrückt wird (Standardeinstellung: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_NOEALINEHEIGHTADJUST</strong></dt> </dl></td>
<td><strong>Windows 8:</strong>Passen Sie die Linienhöhe nicht für ostasiatischen Text an (Standard: 0, wodurch die Zeilenhöhe um 15 % angepasst wird). <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_NOFOCUSLINKNOTIFY</strong></dt> </dl></td>
<td>Sendet <a href="en-link.md">EN_LINK</a> Benachrichtigung von Links, die keinen Fokus haben.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_NOIME</strong></dt> </dl></td>
<td>ImEs werden für diese Instanz des Rich Edit-Steuerelements nicht verwendet (Standardeinstellung: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_NOINPUTSEQUENCECHK</strong></dt> </dl></td>
<td>Wenn dieses Bit eingeschaltet ist, überprüft rich edit nicht die Sequenz des typisierten Texts. Einige Sprachen (z. B. Thai und Chinesisch) erfordern die Überprüfung der Eingabereihenfolgereihenfolge, bevor sie an den Sicherungsspeicher übermittelt werden (Standard: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_SCROLLONKILLFOCUS</strong></dt> </dl></td>
<td>Wenn KillFocus auftritt, scrollen Sie zum Anfang des Texts (Zeichenposition gleich 0) (Standardwert: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_SMARTDRAGDROP</strong></dt> </dl></td>
<td><strong>Windows 8:</strong>Fügen Sie beim Löschen von Text ein Leerzeichen entsprechend dem Kontext hinzu, oder löschen Sie es (Standardwert: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_USECRLF</strong></dt> </dl></td>
<td>Veraltet. Darf nicht verwendet werden.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_WORDDRAGDROP</strong></dt> </dl></td>
<td><strong>Windows 8:</strong>Wenn die Wortauswahl aktiv ist, stellen Sie sicher, dass sich die Ablageposition an einer Wortgrenze befindet (Standardwert: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_UPPERCASE</strong></dt> </dl></td>
<td>Konvertiert alle Eingabezeichen in Großbuchstaben (Standardwert: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_USEAIMM</strong></dt> </dl></td>
<td>Verwendet die Active IMM-Eingabemethodenkomponente, die mit Internet Explorer 4.0 oder höher ausgeliefert wird (Standardwert: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_USEATFONT</strong></dt> </dl></td>
<td><strong>Windows XP mit SP1:</strong>Verwendet eine @-Schriftart, die für vertikalen Text konzipiert ist. wird mit dem <a href="rich-edit-control-styles.md"><strong></strong></a> ES_VERTICAL-Fensterstil verwendet. Der Name einer @-Schriftart beginnt z. B. mit dem @-Symbol &quot; @Batang &quot; (Standardwert: 0, wird jedoch automatisch für vertikales Textlayout aktiviert). <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_USECTF</strong></dt> </dl></td>
<td><strong>Windows XP mit SP1:</strong>Aktiviert die TSF-Unterstützung. (Standard: 0)<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_XLTCRCRLFTOCR</strong></dt> </dl></td>
<td>Aktiviert die Übersetzung von CRCRLFs in CRs. Wenn dieses Bit eingeschaltet ist und eine Datei eingelesen wird, werden alle Crcrlf-Instanzen intern in harte CRs konvertiert. Dies wirkt sich auf den Textumbruch aus. Beachten Sie, dass die CRs durch CRLFs ersetzt werden, wenn eine solche Datei als Nur-Text gespeichert wird. Dies ist der .txt Standard für Nur-Text (Standardwert: 0, wodurch CRCRLFs bei der Eingabe gelöscht wird). <br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | Rich Edit 3.0<br/>                                                              |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ SETEDITSTYLE**](em-seteditstyle.md)
</dt> </dl>

 

