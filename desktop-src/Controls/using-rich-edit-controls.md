---
title: Verwenden von Rich Edit-Steuerelementen
description: Dieser Abschnitt enthält Themen, die veranschaulichen, wie Sie Rich Edit-Steuerelemente erstellen und verwenden.
ms.assetid: 2c4717c9-3257-42d5-9c36-89b7e524e788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0489660bb6849d0de76ae7fc2f4e21ca931662a8
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104474517"
---
# <a name="using-rich-edit-controls"></a>Verwenden von Rich Edit-Steuerelementen

Dieser Abschnitt enthält Themen, die veranschaulichen, wie Sie Rich Edit-Steuerelemente erstellen und verwenden.

## <a name="in-this-section"></a>In diesem Abschnitt



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Thema</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="create-rich-edit-controls.md">Erstellen von Rich-Edit-Steuerelementen</a><br/></td>
<td>Zum Erstellen eines Rich-Edit-Steuer Elements rufen Sie die Funktion " <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>kreatewindowex</strong></a> " auf, und geben Sie die Rich-Bearbeitungsfenster Klasse an Geben Sie für Microsoft Rich Edit 4,1 (Msftedit.dll) MSFTEDIT_CLASS als Fenster Klasse an. Geben Sie für alle früheren Versionen RICHEDIT_CLASS an. Weitere Informationen finden Sie unter <a href="about-rich-edit-controls.md">Versionen von Rich Edit</a>. <br/> Rich Edit-Steuerelemente unterstützen die meisten Fenster Stile, die mit Bearbeitungs Steuerelementen und zusätzlichen Stilen verwendet werden. Sie sollten den Stil des <a href="edit-control-styles.md"><strong>ES_MULTILINE</strong></a> Fensters angeben, wenn Sie mehr als eine Textzeile im Steuerelement zulassen möchten. Weitere Informationen finden Sie unter <a href="rich-edit-control-styles.md">Rich Edit-Steuerelement Stile</a>. <br/></td>
</tr>
<tr class="even">
<td><a href="format-text-in-rich-edit-controls.md">Formatieren von Text in Rich Edit-Steuerelementen</a><br/></td>
<td>Eine Anwendung kann Nachrichten an ein Rich Edit-Steuerelement senden, um Zeichen und Absätze zu formatieren und Formatierungsinformationen abzurufen. Die Attribute für die Absatz Formatierung umfassen Ausrichtung, Tabstopps, Einzüge, Nummerierungen und einfache Tabellen. Für Zeichen können Sie Schriftart Name, Größe, Farbe und Effekte angeben, z. b. Fett, kursiv und geschützt. <br/></td>
</tr>
<tr class="odd">
<td><a href="interact-with-the-current-selection.md">Interagieren mit der aktuellen Auswahl</a><br/></td>
<td>Der Benutzer kann Text in einem Rich-Edit-Steuerelement mit der Maus oder der Tastatur auswählen. Bei der <em>aktuellen Auswahl</em> handelt es sich um den Bereich der ausgewählten Zeichen oder um die Position der Einfügemarke, wenn keine Zeichen ausgewählt sind. Eine Anwendung kann Informationen über die aktuelle Auswahl, die Festlegung, den Zeitpunkt der Änderung und das Anzeigen oder Ausblenden der Auswahl Markierung erhalten. <br/></td>
</tr>
<tr class="even">
<td><a href="use-rich-edit-text-operations.md">Verwenden von Rich-Text-Bearbeitungsvorgängen</a><br/></td>
<td>Eine Anwendung kann Nachrichten senden, um Text in einem Rich-Edit-Steuerelement abzurufen oder zu suchen. Sie können entweder den ausgewählten Text oder einen angegebenen Textbereich abrufen. <br/></td>
</tr>
<tr class="odd">
<td><a href="use-word-and-line-break-information.md">Verwenden von Wort-und Zeilenumbruch Informationen</a><br/></td>
<td>Ein Rich-Edit-Steuerelement ruft eine Funktion auf, die als Wort Umbruch Prozedur bezeichnet wird, um Unterbrechungen zwischen Wörtern zu finden und zu bestimmen, wo Zeilen unterbrochen werden können Das-Steuerelement verwendet diese Informationen beim Ausführen von Zeilenumbruch Vorgängen und bei der Verarbeitung von STRG + nach-links-Pfeiltaste und STRG + nach-rechts-Taste. Eine Anwendung kann Nachrichten an ein Rich-Edit-Steuerelement senden, um die Standardprozedur für das Wort Umbruch zu ersetzen, Informationen zum Wort Umbruch abzurufen und zu bestimmen, auf welche Zeile ein bestimmtes Zeichen fällt. <br/></td>
</tr>
<tr class="even">
<td><a href="use-rich-edit-clipboard-operations.md">So verwenden Sie Rich-Edit-Zwischenablage Vorgänge</a><br/></td>
<td>Eine Anwendung kann den Inhalt der Zwischenablage in ein Rich-Edit-Steuerelement einfügen, indem Sie entweder das beste verfügbare Zwischenablage Format oder ein bestimmtes Zwischenablage Format verwendet. Sie können auch bestimmen, ob ein Rich-Edit-Steuerelement in der Lage ist, ein Zwischenablage Format einzufügen. <br/></td>
</tr>
<tr class="odd">
<td><a href="use-streams.md">Verwenden von Streams</a><br/></td>
<td>Sie können Datenströme verwenden, um Daten in ein oder aus einem Rich-Edit-Steuerelement zu übertragen. Ein Stream wird durch eine <a href="/windows/desktop/api/Richedit/ns-richedit-editstream"><strong>editstream</strong></a> -Struktur definiert, die einen Puffer und eine Anwendungs definierte Rückruffunktion angibt. <br/></td>
</tr>
<tr class="even">
<td><a href="automatically-resize-rich-edit-controls.md">Automatisches Ändern der Größe von Rich-Edit-Steuerelementen</a><br/></td>
<td>Eine Anwendung kann die Größe eines Rich-Edit-Steuer Elements nach Bedarf ändern, sodass es immer dieselbe Größe wie der Inhalt hat. Ein Rich-Edit-Steuerelement unterstützt diese so genannte, nicht <em>aufgerufene Funktion</em> , indem es das übergeordnete Fenster an einen <a href="en-requestresize.md">EN_REQUESTRESIZE</a> Benachrichtigungs Code sendet, wenn sich die Größe des Inhalts des Steuer Elements ändert. <br/></td>
</tr>
<tr class="odd">
<td><a href="use-rich-edit-control-notification-codes.md">Verwenden von Benachrichtigungs Codes für Rich-Edit-Steuerelemente</a><br/></td>
<td>Das übergeordnete Fenster eines Rich-Edit-Steuer Elements kann Benachrichtigungs Codes verarbeiten, um Ereignisse zu überwachen, die das Steuerelement Rich Edit-Steuerelemente unterstützen alle Benachrichtigungs Codes, die mit Bearbeitungs Steuerelementen verwendet werden, sowie mehrere zusätzliche. <br/></td>
</tr>
<tr class="even">
<td><a href="use-font-binding-in-rich-edit-controls.md">Verwenden der Schriftart Bindung in Rich Edit-Steuerelementen</a><br/></td>
<td>Microsoft Rich Edit 3,0 weist in Abhängigkeit von ihrem Kontext einen Zeichensatz für einfache Textzeichen zu. Hier einige Beispiele: <br/>
<ul>
<li>Griechischen Zeichen werden <strong>GREEK_CHARSET</strong>zugewiesen.</li>
<li>Hangul-Symbole werden <strong>HANGUL_CHARSET</strong>zugewiesen.</li>
<li>Chinesische Zeichen werden <strong>SHIFTJIS_CHARSET</strong> zugewiesen, wenn Kana-Zeichen in der Nähe gefunden werden, oder <strong>GB2312_CHARSET</strong> , wenn in der Nähe keine Kana gefunden werden.</li>
<li>Nicht neutrale ANSI-Zeichen werden <strong>ANSI_CHARSET</strong> in einem beliebigen Ereignis zugewiesen.</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="using-rich-edit-com.md">Verwenden von OLE in Rich Edit-Steuerelementen</a><br/></td>
<td>Dieser Abschnitt enthält Informationen zur Verwendung von Object Linking and Embedding (OLE) in Rich Edit-Steuerelementen. <br/></td>
</tr>
<tr class="even">
<td><a href="printing-rich-edit-controls.md">Drucken des Inhalts der Rich Edit-Steuerelemente</a><br/></td>
<td>Dieser Abschnitt enthält Informationen zum Drucken der Inhalte der Rich Edit-Steuerelemente. <br/></td>
</tr>
</tbody>
</table>



 

 

