---
title: EM_GETEDITSTYLE Meldung (RichEdit. h)
description: Ruft die aktuellen Flags für Bearbeitungs Stile ab.
ms.assetid: 568e51a4-0767-4a59-bf34-bc0281b5fe65
keywords:
- Windows-Steuerelemente für EM_GETEDITSTYLE Meldung
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
ms.openlocfilehash: 9264338ea525cc0165e1ed942d90654b95357b17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040723"
---
# <a name="em_geteditstyle-message"></a>EM \_ GetEditStyle-Nachricht

Ruft die aktuellen Flags für Bearbeitungs Stile ab.

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

Gibt die aktuellen Flags für den Bearbeitungs Stil zurück, die einen oder mehrere der folgenden Werte enthalten können:



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
<td>Durch die umfassende Bearbeitung wird der System Bearbeiter aufgerufen, wenn der Benutzer versucht, mehr als die maximal zulässige Anzahl von Zeichen einzugeben.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_BIDI</strong></dt> </dl></td>
<td>Schaltet die bidirektionale Verarbeitung ein. Dies wird automatisch durch eine umfangreiche Bearbeitung aktiviert, wenn eines der folgenden Fenster Stile aktiv ist: <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RIGHT</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RTLREADING</strong></a> <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_LEFTSCROLLBAR</strong></a>. Diese Einstellung ist jedoch nützlich, wenn diese Fenster Stile verwendet werden, wenn eine benutzerdefinierte Implementierung von <a href="/windows/desktop/api/Textserv/nl-textserv-itexthost"><strong>itexthost</strong></a> verwendet wird (Standard: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_CTFALLOWEMBED</strong></dt> </dl></td>
<td><strong>Windows XP mit SP1</strong>: zulassen, dass eingebettete Objekte mithilfe von TSF eingefügt werden (Standard: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_CTFALLOWPROOFING</strong></dt> </dl></td>
<td><strong>Windows XP mit SP1</strong>: ermöglicht TSF-Korrektur Tipps (Standard: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_CTFALLOWSMARTTAG</strong></dt> </dl></td>
<td><strong>Windows XP mit SP1</strong>: ermöglicht TSF Smarttag-Tipps (Standard: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_CTFNOLOCK</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: lassen Sie den TSF-Sperr Lese-/Schreibzugriff nicht zu. Dadurch wird TSF-Eingabe angehalten. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_DEFAULTLATINLIGA</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: Schriftarten mit einer fi Ligaturen werden mit OpenType-Standard Features angezeigt, die zu einer verbesserten Typografie führen (Standard: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_DRAFTMODE</strong></dt> </dl></td>
<td><strong>Windows XP mit SP1</strong>: Verwenden Sie den Entwurfs Modus-Schriftarten, um Text anzuzeigen. Der Entwurfs Modus ist eine Barrierefreiheits Option, bei der das Steuerelement den Text mit einer einzelnen Schriftart anzeigt. die Schriftart wird durch die Systemeinstellung für die in Meldungs Feldern verwendete Schriftart festgelegt. Barrierefreie Benutzer können z. b. Text leichter lesen, wenn er einheitlich ist, anstatt eine Mischung aus Schriftarten und Stilen (Standard: 0) zu verwenden. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_EMULATE10</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: Emulieren Sie das RichEdit 1,0-Verhalten. <br/>
<blockquote>
[!Note]<br />
Wenn Sie dieses Verhalten wirklich wünschen, verwenden Sie die Windows-riched32.dll anstelle von riched20.dll oder msftedit.dll. Riched32.dll verfügten über mehr Funktionalität.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_EMULATESYSEDIT</strong></dt> </dl></td>
<td>Wenn dieses Bit aktiviert ist, versucht Rich Edit, das System Bearbeitungs Steuerelement zu emulieren (Standard: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_EXTENDBACKCOLOR</strong></dt> </dl></td>
<td>Erweitert die Hintergrundfarbe auf die Ränder des Client Rechtecks (Standard: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_HIDEGRIDLINES</strong></dt> </dl></td>
<td><strong>Windows XP mit SP1</strong>: Wenn die Breite der Tabellen Gitternetz Linien 0 (null) ist, werden keine Gitternetz Linien angezeigt. Dies entspricht der Funktion Gitternetz Linien ausblenden im Menü Tabelle von Word (Standard: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_HYPERLINKTOOLTIPS</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: Wenn sich der Cursor über einem Link befindet, zeigen Sie eine QuickInfo mit der Ziel Linkadresse an (Standard: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_LOGICALCARET</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: Stellen Sie logische einfügeinformationen anstelle einer Caretzeichen-Bitmap bereit, wie in <a href="/windows/desktop/api/Textserv/nf-textserv-itexthost-txsetcaretpos"><strong>itexthost:: txsetcaretpos</strong></a> (Standard: 0) beschrieben. <br/></td>
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
<td><strong>Windows 8</strong>: Aktivieren Sie die Mehrfachauswahl mit einzelner Maus Auswahl, die beim Drücken der STRG-Taste getroffen wird (Standard: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_NOEALINEHEIGHTADJUST</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: passen Sie die Zeilenhöhe nicht für ostasiatischen Text an (Standardwert: 0, wodurch die Zeilenhöhe um 15%) angepasst wird. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_NOFOCUSLINKNOTIFY</strong></dt> </dl></td>
<td>Sendet <a href="en-link.md">EN_LINK</a> Benachrichtigung von Links, die keinen Fokus haben.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_NOIME</strong></dt> </dl></td>
<td>Lässt keine IMEs für diese Instanz des Rich Edit-Steuer Elements zu (Standard: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_NOINPUTSEQUENCECHK</strong></dt> </dl></td>
<td>Wenn dieses Bit eingeschaltet ist, wird die Sequenz von typisiertem Text von Rich Edit nicht überprüft. Einige Sprachen (z. b. Thai und Vietnamese) erfordern die Überprüfung der Eingabe Sequenz Reihenfolge vor der Übermittlung an den Sicherungs Speicher (Standard: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_SCROLLONKILLFOCUS</strong></dt> </dl></td>
<td>Wenn "killfocus" auftritt, führen Sie einen Bildlauf zum Anfang des Texts durch (Zeichenposition gleich 0) (Standardwert: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_SMARTDRAGDROP</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: Hinzufügen oder Löschen eines leer Zeichens entsprechend dem Kontext beim Ablegen von Text (Standard: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_USECRLF</strong></dt> </dl></td>
<td>Veraltet. Darf nicht verwendet werden.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_WORDDRAGDROP</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: Wenn Word Select aktiviert ist, stellen Sie sicher, dass sich der Ablageort an einer Wort Grenze befindet (Standardwert: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_UPPERCASE</strong></dt> </dl></td>
<td>Konvertiert alle Eingabezeichen in Großbuchstaben (Standardwert: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_USEAIMM</strong></dt> </dl></td>
<td>Verwendet die Komponente der Active imm-Eingabemethode, die im Lieferumfang von Internet Explorer 4,0 oder höher (Standard: 0) enthalten ist.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_USEATFONT</strong></dt> </dl></td>
<td><strong>Windows XP mit SP1</strong>: verwendet ein @ Font-Zeichen, das für vertikalen Text konzipiert ist. Dies wird mit dem Fenster Stil des <a href="rich-edit-control-styles.md"><strong>ES_VERTICAL</strong></a> verwendet. Der Name von @ Font beginnt mit dem @-Symbol, z. b &quot; @Batang &quot; . (Standard: 0, wird jedoch für das vertikale Text Layout automatisch aktiviert). <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_USECTF</strong></dt> </dl></td>
<td><strong>Windows XP mit SP1</strong>: schaltet TSF-Unterstützung ein. (Standardwert: 0)<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_XLTCRCRLFTOCR</strong></dt> </dl></td>
<td>Schaltet die Übersetzung von crcrlfs in CRS ein. Wenn dieses Bit eingeschaltet ist und eine Datei eingelesen wird, werden alle Instanzen von crcrlf intern in Hard CRS konvertiert. Dies wirkt sich auf das Umwickeln von Text aus. Beachten Sie Folgendes: Wenn eine solche Datei als nur-Text gespeichert wird, wird der CRS durch CRLFs ersetzt. Dies ist der TXT-Standard für Klartext (Standardwert: 0, wodurch crcrlfs bei der Eingabe gelöscht wird). <br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | Rich Edit 3,0<br/>                                                              |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM-Einstellungs \_ Stil**](em-seteditstyle.md)
</dt> </dl>

 

