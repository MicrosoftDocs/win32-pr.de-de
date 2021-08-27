---
title: Verwenden von Rich Edit-Steuerelementen
description: Dieser Abschnitt enthält Themen, in denen das Erstellen und Verwenden von Rich-Edit-Steuerelementen veranschaulicht wird.
ms.assetid: 2c4717c9-3257-42d5-9c36-89b7e524e788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce4d6565160babc896ea9affe2d5c0c772c5b77e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466177"
---
# <a name="using-rich-edit-controls"></a>Verwenden von Rich Edit-Steuerelementen

Dieser Abschnitt enthält Themen, in denen das Erstellen und Verwenden von Rich-Edit-Steuerelementen veranschaulicht wird.

## <a name="in-this-section"></a>In diesem Abschnitt




| Thema | BESCHREIBUNG | 
|-------|-------------|
| <a href="create-rich-edit-controls.md">Erstellen von Rich Edit-Steuerelementen</a><br /> | Rufen Sie zum Erstellen eines Rich-Edit-Steuerelements die <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>CreateWindowEx-Funktion</strong></a> auf, und geben Sie dabei die Rich Edit Window-Klasse an. Geben Sie für Microsoft Rich Edit 4.1 (Msftedit.dll) MSFTEDIT_CLASS Fensterklasse an. Geben Sie für alle vorherigen Versionen RICHEDIT_CLASS. Weitere Informationen finden Sie unter <a href="about-rich-edit-controls.md">Versionen von Rich Edit.</a> <br /> Umfangreiche Bearbeitungssteuerelemente unterstützen die meisten Fensterstile, die mit Bearbeitungssteuerelementen verwendet werden, sowie zusätzliche Stile. Sie sollten die <a href="edit-control-styles.md"><strong>ES_MULTILINE</strong></a> angeben, wenn Sie mehr als eine Textzeile im Steuerelement zulassen möchten. Weitere Informationen finden Sie unter <a href="rich-edit-control-styles.md">Rich Edit Control Styles</a>. <br /> | 
| <a href="format-text-in-rich-edit-controls.md">Formatieren von Text in Rich Edit-Steuerelementen</a><br /> | Eine Anwendung kann Nachrichten an ein umfangreiches Bearbeitungssteuerzeichen senden, um Zeichen und Absätze zu formatieren und Formatierungsinformationen abzurufen. Absatzformatierungsattribute umfassen Ausrichtung, Registerkarten, Einzüge, Nummerierung und einfache Tabellen. Für Zeichen können Sie Schriftartname, Schriftgrad, Farbe und Effekte angeben, z. B. fett, italisch und geschützt. <br /> | 
| <a href="interact-with-the-current-selection.md">Interagieren mit der aktuellen Auswahl</a><br /> | Der Benutzer kann Text in einem Rich-Edit-Steuerelement auswählen, indem er die Maus oder die Tastatur verwendet. Die <em>aktuelle Auswahl</em> ist der Bereich der ausgewählten Zeichen oder die Position der Einfügemarke, wenn keine Zeichen ausgewählt sind. Eine Anwendung kann Informationen über die aktuelle Auswahl erhalten, festlegen, bestimmen, wann sie sich ändert, und die Markierung der Auswahl ein- oder ausblenden. <br /> | 
| <a href="use-rich-edit-text-operations.md">Verwenden von Rich-Edit-Text-Vorgängen</a><br /> | Eine Anwendung kann Nachrichten senden, um Text in einem Rich-Edit-Steuerelement abzurufen oder zu suchen. Sie können entweder den ausgewählten Text oder einen angegebenen Textbereich abrufen. <br /> | 
| <a href="use-word-and-line-break-information.md">Verwenden von Informationen zu Wörtern und Zeilenumbrüchen</a><br /> | Ein umfangreiches Bearbeitungssteuerwort ruft eine Funktion auf, die als Wörterumbruchprozedur bezeichnet wird, um Brüche zwischen Wörtern zu finden und zu bestimmen, wo Zeilen durchbrechen werden können. Das -Steuerelement verwendet diese Informationen beim Ausführen von Zeilenumbruchvorgängen und bei der Verarbeitung von TASTENKOMBINATIONEN STRG+NACH-LINKS-TASTE und STRG+NACH-RECHTS-TASTE. Eine Anwendung kann Nachrichten an ein umfangreiches Bearbeitungssteuerzeichen senden, um die Standardprozedur für Die Wortumbruch zu ersetzen, Wörterumbruchinformationen abzurufen und zu bestimmen, auf welche Zeile ein bestimmtes Zeichen fällt. <br /> | 
| <a href="use-rich-edit-clipboard-operations.md">Verwenden von Rich Edit-Zwischenablagevorgängen</a><br /> | Eine Anwendung kann den Inhalt der Zwischenablage mithilfe des besten verfügbaren Zwischenablageformats oder eines bestimmten Zwischenablageformats in ein rich-Edit-Steuerelement einfügen. Sie können auch bestimmen, ob ein Rich-Edit-Steuerelement ein Zwischenablageformat eingefügt werden kann. <br /> | 
| <a href="use-streams.md">Verwenden von Streams</a><br /> | Sie können Datenströme verwenden, um Daten in ein oder aus einem Rich-Edit-Steuerelement zu übertragen. Ein Stream wird durch eine <a href="/windows/desktop/api/Richedit/ns-richedit-editstream"><strong>EDITSTREAM-Struktur</strong></a> definiert, die einen Puffer und eine anwendungsdefinierte Rückruffunktion angibt. <br /> | 
| <a href="automatically-resize-rich-edit-controls.md">Automatisches Ändern der Größe von Rich Edit-Steuerelementen</a><br /> | Eine Anwendung kann die Größe eines Rich-Edit-Steuerelements nach Bedarf ändern, sodass es immer die gleiche Größe wie der Inhalt hat. Ein umfassendes Bearbeitungssteuer steuerelement unterstützt diese so genannte <a href="en-requestresize.md"></a> <em>bottomless-Funktionalität,</em> indem es dem übergeordneten Fenster einen EN_REQUESTRESIZE-Benachrichtigungscode sendet, wenn sich die Größe des Inhalts des Steuerelements ändert. <br /> | 
| <a href="use-rich-edit-control-notification-codes.md">Verwenden von Rich Edit-Steuerelement-Benachrichtigungscodes</a><br /> | Das übergeordnete Fenster eines Rich-Edit-Steuerelements kann Benachrichtigungscodes verarbeiten, um Ereignisse zu überwachen, die sich auf das Steuerelement auswirken. Umfangreiche Bearbeitungssteuerelemente unterstützen alle Benachrichtigungscodes, die mit Bearbeitungssteuerelementen verwendet werden, sowie mehrere zusätzliche. <br /> | 
| <a href="use-font-binding-in-rich-edit-controls.md">Verwenden der Schriftartbindung in Rich Edit-Steuerelementen</a><br /> | Microsoft Rich Edit 3.0 weist Je nach Kontext Nur-Text-Zeichen einen Zeichensatz zu. Beispiele: <br /><ul><li>Griechisch-Zeichen werden als <strong>GREEK_CHARSET.</strong></li><li>Hangul-Symbole werden <strong>HANGUL_CHARSET.</strong></li><li>Chinesische Zeichen werden zugewiesen SHIFTJIS_CHARSET <strong>wenn</strong> Kanazeichen in <strong></strong> der Nähe gefunden werden, oder GB2312_CHARSET, wenn in der Nähe kein Kana gefunden wird.</li><li>Nicht neutrale ANSI-Zeichen werden <strong>in jedem ANSI_CHARSET</strong> zugewiesen.</li></ul> | 
| <a href="using-rich-edit-com.md">Verwenden von OLE in Rich Edit-Steuerelementen</a><br /> | Dieser Abschnitt enthält Informationen zur Verwendung von Objektverknüpfung und -einbettung (OLE) in Rich-Edit-Steuerelementen. <br /> | 
| <a href="printing-rich-edit-controls.md">Drucken des Inhalts von Rich Edit-Steuerelementen</a><br /> | Dieser Abschnitt enthält Informationen zum Drucken des Inhalts von Rich-Edit-Steuerelementen. <br /> | 




 

 

