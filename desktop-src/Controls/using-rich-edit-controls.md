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
# <a name="using-rich-edit-controls"></a><span data-ttu-id="8c74c-103">Verwenden von Rich Edit-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="8c74c-103">Using Rich Edit Controls</span></span>

<span data-ttu-id="8c74c-104">Dieser Abschnitt enthält Themen, die veranschaulichen, wie Sie Rich Edit-Steuerelemente erstellen und verwenden.</span><span class="sxs-lookup"><span data-stu-id="8c74c-104">This section contains topics that demonstrate how to create and use rich edit controls.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8c74c-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="8c74c-105">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c74c-106">Thema</span><span class="sxs-lookup"><span data-stu-id="8c74c-106">Topic</span></span></th>
<th><span data-ttu-id="8c74c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8c74c-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8c74c-108"><a href="create-rich-edit-controls.md">Erstellen von Rich-Edit-Steuerelementen</a></span><span class="sxs-lookup"><span data-stu-id="8c74c-108"><a href="create-rich-edit-controls.md">How to Create Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="8c74c-109">Zum Erstellen eines Rich-Edit-Steuer Elements rufen Sie die Funktion " <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>kreatewindowex</strong></a> " auf, und geben Sie die Rich-Bearbeitungsfenster Klasse an</span><span class="sxs-lookup"><span data-stu-id="8c74c-109">To create a rich edit control, call the <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>CreateWindowEx</strong></a> function, specifying the rich edit window class.</span></span> <span data-ttu-id="8c74c-110">Geben Sie für Microsoft Rich Edit 4,1 (Msftedit.dll) MSFTEDIT_CLASS als Fenster Klasse an.</span><span class="sxs-lookup"><span data-stu-id="8c74c-110">For Microsoft Rich Edit 4.1 (Msftedit.dll), specify MSFTEDIT_CLASS as the window class.</span></span> <span data-ttu-id="8c74c-111">Geben Sie für alle früheren Versionen RICHEDIT_CLASS an.</span><span class="sxs-lookup"><span data-stu-id="8c74c-111">For all previous versions, specify RICHEDIT_CLASS.</span></span> <span data-ttu-id="8c74c-112">Weitere Informationen finden Sie unter <a href="about-rich-edit-controls.md">Versionen von Rich Edit</a>.</span><span class="sxs-lookup"><span data-stu-id="8c74c-112">For more information, see <a href="about-rich-edit-controls.md">Versions of Rich Edit</a>.</span></span> <br/> <span data-ttu-id="8c74c-113">Rich Edit-Steuerelemente unterstützen die meisten Fenster Stile, die mit Bearbeitungs Steuerelementen und zusätzlichen Stilen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c74c-113">Rich edit controls support most of the window styles used with edit controls as well as additional styles.</span></span> <span data-ttu-id="8c74c-114">Sie sollten den Stil des <a href="edit-control-styles.md"><strong>ES_MULTILINE</strong></a> Fensters angeben, wenn Sie mehr als eine Textzeile im Steuerelement zulassen möchten.</span><span class="sxs-lookup"><span data-stu-id="8c74c-114">You should specify the <a href="edit-control-styles.md"><strong>ES_MULTILINE</strong></a> window style if you want to allow more than one line of text in the control.</span></span> <span data-ttu-id="8c74c-115">Weitere Informationen finden Sie unter <a href="rich-edit-control-styles.md">Rich Edit-Steuerelement Stile</a>.</span><span class="sxs-lookup"><span data-stu-id="8c74c-115">For more information, see <a href="rich-edit-control-styles.md">Rich Edit Control Styles</a>.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c74c-116"><a href="format-text-in-rich-edit-controls.md">Formatieren von Text in Rich Edit-Steuerelementen</a></span><span class="sxs-lookup"><span data-stu-id="8c74c-116"><a href="format-text-in-rich-edit-controls.md">How to Format Text in Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="8c74c-117">Eine Anwendung kann Nachrichten an ein Rich Edit-Steuerelement senden, um Zeichen und Absätze zu formatieren und Formatierungsinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8c74c-117">An application can send messages to a rich edit control in order to format characters and paragraphs and retrieve formatting information.</span></span> <span data-ttu-id="8c74c-118">Die Attribute für die Absatz Formatierung umfassen Ausrichtung, Tabstopps, Einzüge, Nummerierungen und einfache Tabellen.</span><span class="sxs-lookup"><span data-stu-id="8c74c-118">Paragraph formatting attributes include alignment, tabs, indents, numbering, and simple tables.</span></span> <span data-ttu-id="8c74c-119">Für Zeichen können Sie Schriftart Name, Größe, Farbe und Effekte angeben, z. b. Fett, kursiv und geschützt.</span><span class="sxs-lookup"><span data-stu-id="8c74c-119">For characters, you can specify font name, size, color, and effects such as bold, italic, and protected.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c74c-120"><a href="interact-with-the-current-selection.md">Interagieren mit der aktuellen Auswahl</a></span><span class="sxs-lookup"><span data-stu-id="8c74c-120"><a href="interact-with-the-current-selection.md">How to Interact with the Current Selection</a></span></span><br/></td>
<td><span data-ttu-id="8c74c-121">Der Benutzer kann Text in einem Rich-Edit-Steuerelement mit der Maus oder der Tastatur auswählen.</span><span class="sxs-lookup"><span data-stu-id="8c74c-121">The user can select text in a rich edit control by using the mouse or the keyboard.</span></span> <span data-ttu-id="8c74c-122">Bei der <em>aktuellen Auswahl</em> handelt es sich um den Bereich der ausgewählten Zeichen oder um die Position der Einfügemarke, wenn keine Zeichen ausgewählt sind.</span><span class="sxs-lookup"><span data-stu-id="8c74c-122">The <em>current selection</em> is the range of selected characters, or the position of the insertion point if no characters are selected.</span></span> <span data-ttu-id="8c74c-123">Eine Anwendung kann Informationen über die aktuelle Auswahl, die Festlegung, den Zeitpunkt der Änderung und das Anzeigen oder Ausblenden der Auswahl Markierung erhalten.</span><span class="sxs-lookup"><span data-stu-id="8c74c-123">An application can get information about the current selection, set it, determine when it changes, and show or hide the selection highlight.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c74c-124"><a href="use-rich-edit-text-operations.md">Verwenden von Rich-Text-Bearbeitungsvorgängen</a></span><span class="sxs-lookup"><span data-stu-id="8c74c-124"><a href="use-rich-edit-text-operations.md">How to Use Rich Edit Text Operations</a></span></span><br/></td>
<td><span data-ttu-id="8c74c-125">Eine Anwendung kann Nachrichten senden, um Text in einem Rich-Edit-Steuerelement abzurufen oder zu suchen.</span><span class="sxs-lookup"><span data-stu-id="8c74c-125">An application can send messages to retrieve or find text in a rich edit control.</span></span> <span data-ttu-id="8c74c-126">Sie können entweder den ausgewählten Text oder einen angegebenen Textbereich abrufen.</span><span class="sxs-lookup"><span data-stu-id="8c74c-126">You can retrieve either the selected text or a specified range of text.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c74c-127"><a href="use-word-and-line-break-information.md">Verwenden von Wort-und Zeilenumbruch Informationen</a></span><span class="sxs-lookup"><span data-stu-id="8c74c-127"><a href="use-word-and-line-break-information.md">How to Use Word and Line Break Information</a></span></span><br/></td>
<td><span data-ttu-id="8c74c-128">Ein Rich-Edit-Steuerelement ruft eine Funktion auf, die als Wort Umbruch Prozedur bezeichnet wird, um Unterbrechungen zwischen Wörtern zu finden und zu bestimmen, wo Zeilen unterbrochen werden können</span><span class="sxs-lookup"><span data-stu-id="8c74c-128">A rich edit control calls a function called a word-break procedure to find breaks between words and to determine where it can break lines.</span></span> <span data-ttu-id="8c74c-129">Das-Steuerelement verwendet diese Informationen beim Ausführen von Zeilenumbruch Vorgängen und bei der Verarbeitung von STRG + nach-links-Pfeiltaste und STRG + nach-rechts-Taste.</span><span class="sxs-lookup"><span data-stu-id="8c74c-129">The control uses this information when performing word-wrap operations and when processing CTRL+LEFT ARROW key and CTRL+RIGHT ARROW key combinations.</span></span> <span data-ttu-id="8c74c-130">Eine Anwendung kann Nachrichten an ein Rich-Edit-Steuerelement senden, um die Standardprozedur für das Wort Umbruch zu ersetzen, Informationen zum Wort Umbruch abzurufen und zu bestimmen, auf welche Zeile ein bestimmtes Zeichen fällt.</span><span class="sxs-lookup"><span data-stu-id="8c74c-130">An application can send messages to a rich edit control to replace the default word-break procedure, to retrieve word-break information, and to determine what line a given character falls on.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c74c-131"><a href="use-rich-edit-clipboard-operations.md">So verwenden Sie Rich-Edit-Zwischenablage Vorgänge</a></span><span class="sxs-lookup"><span data-stu-id="8c74c-131"><a href="use-rich-edit-clipboard-operations.md">How to Use Rich Edit Clipboard Operations</a></span></span><br/></td>
<td><span data-ttu-id="8c74c-132">Eine Anwendung kann den Inhalt der Zwischenablage in ein Rich-Edit-Steuerelement einfügen, indem Sie entweder das beste verfügbare Zwischenablage Format oder ein bestimmtes Zwischenablage Format verwendet.</span><span class="sxs-lookup"><span data-stu-id="8c74c-132">An application can paste the contents of the clipboard into a rich edit control by using either the best available clipboard format or a specific clipboard format.</span></span> <span data-ttu-id="8c74c-133">Sie können auch bestimmen, ob ein Rich-Edit-Steuerelement in der Lage ist, ein Zwischenablage Format einzufügen.</span><span class="sxs-lookup"><span data-stu-id="8c74c-133">You can also determine whether a rich edit control is capable of pasting a clipboard format.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c74c-134"><a href="use-streams.md">Verwenden von Streams</a></span><span class="sxs-lookup"><span data-stu-id="8c74c-134"><a href="use-streams.md">How to Use Streams</a></span></span><br/></td>
<td><span data-ttu-id="8c74c-135">Sie können Datenströme verwenden, um Daten in ein oder aus einem Rich-Edit-Steuerelement zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="8c74c-135">You can use streams to transfer data into or out of a rich edit control.</span></span> <span data-ttu-id="8c74c-136">Ein Stream wird durch eine <a href="/windows/desktop/api/Richedit/ns-richedit-editstream"><strong>editstream</strong></a> -Struktur definiert, die einen Puffer und eine Anwendungs definierte Rückruffunktion angibt.</span><span class="sxs-lookup"><span data-stu-id="8c74c-136">A stream is defined by an <a href="/windows/desktop/api/Richedit/ns-richedit-editstream"><strong>EDITSTREAM</strong></a> structure, which specifies a buffer and an application-defined callback function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c74c-137"><a href="automatically-resize-rich-edit-controls.md">Automatisches Ändern der Größe von Rich-Edit-Steuerelementen</a></span><span class="sxs-lookup"><span data-stu-id="8c74c-137"><a href="automatically-resize-rich-edit-controls.md">How to Automatically Resize Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="8c74c-138">Eine Anwendung kann die Größe eines Rich-Edit-Steuer Elements nach Bedarf ändern, sodass es immer dieselbe Größe wie der Inhalt hat.</span><span class="sxs-lookup"><span data-stu-id="8c74c-138">An application can resize a rich edit control as needed so that it is always the same size as its contents.</span></span> <span data-ttu-id="8c74c-139">Ein Rich-Edit-Steuerelement unterstützt diese so genannte, nicht <em>aufgerufene Funktion</em> , indem es das übergeordnete Fenster an einen <a href="en-requestresize.md">EN_REQUESTRESIZE</a> Benachrichtigungs Code sendet, wenn sich die Größe des Inhalts des Steuer Elements ändert.</span><span class="sxs-lookup"><span data-stu-id="8c74c-139">A rich edit control supports this so-called <em>bottomless</em> functionality by sending its parent window an <a href="en-requestresize.md">EN_REQUESTRESIZE</a> notification code whenever the size of the control's content changes.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c74c-140"><a href="use-rich-edit-control-notification-codes.md">Verwenden von Benachrichtigungs Codes für Rich-Edit-Steuerelemente</a></span><span class="sxs-lookup"><span data-stu-id="8c74c-140"><a href="use-rich-edit-control-notification-codes.md">How to Use Rich Edit Control Notification Codes</a></span></span><br/></td>
<td><span data-ttu-id="8c74c-141">Das übergeordnete Fenster eines Rich-Edit-Steuer Elements kann Benachrichtigungs Codes verarbeiten, um Ereignisse zu überwachen, die das Steuerelement</span><span class="sxs-lookup"><span data-stu-id="8c74c-141">A rich edit control's parent window can process notification codes to monitor events that affect the control.</span></span> <span data-ttu-id="8c74c-142">Rich Edit-Steuerelemente unterstützen alle Benachrichtigungs Codes, die mit Bearbeitungs Steuerelementen verwendet werden, sowie mehrere zusätzliche.</span><span class="sxs-lookup"><span data-stu-id="8c74c-142">Rich edit controls support all of the notification codes that are used with edit controls, as well as several additional ones.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c74c-143"><a href="use-font-binding-in-rich-edit-controls.md">Verwenden der Schriftart Bindung in Rich Edit-Steuerelementen</a></span><span class="sxs-lookup"><span data-stu-id="8c74c-143"><a href="use-font-binding-in-rich-edit-controls.md">How to Use Font Binding in Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="8c74c-144">Microsoft Rich Edit 3,0 weist in Abhängigkeit von ihrem Kontext einen Zeichensatz für einfache Textzeichen zu.</span><span class="sxs-lookup"><span data-stu-id="8c74c-144">Microsoft Rich Edit 3.0 assigns a character set to plain-text characters depending on their context.</span></span> <span data-ttu-id="8c74c-145">Hier einige Beispiele:</span><span class="sxs-lookup"><span data-stu-id="8c74c-145">Some examples are:</span></span> <br/>
<ul>
<li><span data-ttu-id="8c74c-146">Griechischen Zeichen werden <strong>GREEK_CHARSET</strong>zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="8c74c-146">Greek characters are assigned <strong>GREEK_CHARSET</strong>.</span></span></li>
<li><span data-ttu-id="8c74c-147">Hangul-Symbole werden <strong>HANGUL_CHARSET</strong>zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="8c74c-147">Hangul symbols are assigned <strong>HANGUL_CHARSET</strong>.</span></span></li>
<li><span data-ttu-id="8c74c-148">Chinesische Zeichen werden <strong>SHIFTJIS_CHARSET</strong> zugewiesen, wenn Kana-Zeichen in der Nähe gefunden werden, oder <strong>GB2312_CHARSET</strong> , wenn in der Nähe keine Kana gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="8c74c-148">Chinese characters are assigned <strong>SHIFTJIS_CHARSET</strong> if kana characters are found nearby, or <strong>GB2312_CHARSET</strong> if no kana are found nearby.</span></span></li>
<li><span data-ttu-id="8c74c-149">Nicht neutrale ANSI-Zeichen werden <strong>ANSI_CHARSET</strong> in einem beliebigen Ereignis zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="8c74c-149">Non-neutral ANSI characters are assigned <strong>ANSI_CHARSET</strong> in any event.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c74c-150"><a href="using-rich-edit-com.md">Verwenden von OLE in Rich Edit-Steuerelementen</a></span><span class="sxs-lookup"><span data-stu-id="8c74c-150"><a href="using-rich-edit-com.md">How to Use OLE in Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="8c74c-151">Dieser Abschnitt enthält Informationen zur Verwendung von Object Linking and Embedding (OLE) in Rich Edit-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="8c74c-151">This section contains information about using object linking and embedding (OLE) in rich edit controls.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c74c-152"><a href="printing-rich-edit-controls.md">Drucken des Inhalts der Rich Edit-Steuerelemente</a></span><span class="sxs-lookup"><span data-stu-id="8c74c-152"><a href="printing-rich-edit-controls.md">How to Print the Contents of Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="8c74c-153">Dieser Abschnitt enthält Informationen zum Drucken der Inhalte der Rich Edit-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="8c74c-153">This section contains information about how to print the contents of rich edit controls.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

 

