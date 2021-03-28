---
description: Ab Windows Vista enthält die Kategorieansicht "Systemsteuerung" unter jedem Symbol der System Steuerungselemente Aufgaben Verknüpfungen, wie hier gezeigt.
ms.assetid: 54a03536-6fe6-4304-a555-58e5bca128b9
title: Erstellen von durchsuchbaren Aufgaben Verknüpfungen für ein System Steuerungselement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b4e98e8a6e07f84e8012b58cefe8e0d249fc069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862127"
---
# <a name="creating-searchable-task-links-for-a-control-panel-item"></a><span data-ttu-id="9ecc6-103">Erstellen von durchsuchbaren Aufgaben Verknüpfungen für ein System Steuerungselement</span><span class="sxs-lookup"><span data-stu-id="9ecc6-103">Creating Searchable Task Links for a Control Panel Item</span></span>

<span data-ttu-id="9ecc6-104">Ab Windows Vista enthält die Kategorieansicht "Systemsteuerung" unter jedem Symbol der System Steuerungselemente Aufgaben Verknüpfungen, wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-104">As of Windows Vista, the Control Panel category view provides task links beneath each Control Panel item's icon as shown here.</span></span>

![Aufgaben Verknüpfungen auf der Kategorieseite "System und Wartung"](images/controlpaneltasklinks.png)

<span data-ttu-id="9ecc6-106">Wenn ein Benutzer Text in das **Suchfeld** in der oberen rechten Ecke des Fensters eingibt, enthalten die Suchergebnisse diese Aufgaben Verknüpfungen, wie hier für eine Suche nach dem Wort "Display" gezeigt.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-106">When a user enters text in the **Search** box in the upper right of the window, the search results include these task links as shown here for a search on the word "display".</span></span>

![Aufgaben Verknüpfungen in den Suchergebnissen der Systemsteuerung](images/controlpanelsearchresults.png)

<span data-ttu-id="9ecc6-108">In diesem Thema wird Folgendes erörtert:</span><span class="sxs-lookup"><span data-stu-id="9ecc6-108">This topic discusses the following:</span></span>

-   [<span data-ttu-id="9ecc6-109">Bewährte Methoden zum Verknüpfen von Aufgaben</span><span class="sxs-lookup"><span data-stu-id="9ecc6-109">Task Link Best Practices</span></span>](#task-link-best-practices)
-   [<span data-ttu-id="9ecc6-110">Erstellen einer Task-XML-Datei</span><span class="sxs-lookup"><span data-stu-id="9ecc6-110">Creating a Task XML File</span></span>](#creating-a-task-xml-file)
-   [<span data-ttu-id="9ecc6-111">Lokalisieren von Aufgaben Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="9ecc6-111">Localizing Task Links</span></span>](#localizing-task-links)
-   [<span data-ttu-id="9ecc6-112">Schlüsselwörter und suchen</span><span class="sxs-lookup"><span data-stu-id="9ecc6-112">Keywords and Searching</span></span>](#keywords-and-searching)
-   [<span data-ttu-id="9ecc6-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9ecc6-113">Related topics</span></span>](#related-topics)

## <a name="task-link-best-practices"></a><span data-ttu-id="9ecc6-114">Bewährte Methoden zum Verknüpfen von Aufgaben</span><span class="sxs-lookup"><span data-stu-id="9ecc6-114">Task Link Best Practices</span></span>

<span data-ttu-id="9ecc6-115">Es wird empfohlen, dass Sie Aufgaben Verknüpfungen für Ihre System Steuerungselemente als Hilfe für Benutzer bereitstellen, die nach Funktionen suchen.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-115">It is recommended that you provide task links for your Control Panel items as an aid to users searching for functionality.</span></span> <span data-ttu-id="9ecc6-116">Es ist auch möglich, den Aufgaben Verknüpfungen Schlüsselwörter hinzuzufügen, damit ein Benutzer Sie finden kann, auch ohne den Titel oder die Terminologie einer Aufgabe zu kennen.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-116">It is also possible to add keywords to the task links so that a user can find them even without knowing a task's title or terminology.</span></span>

<span data-ttu-id="9ecc6-117">Die besten Aufgaben Verknüpfungen dienen drei Zwecken:</span><span class="sxs-lookup"><span data-stu-id="9ecc6-117">The best task links serve three purposes:</span></span>

1.  <span data-ttu-id="9ecc6-118">Stellen Sie eine Verknüpfung mit der Funktionalität des System Steuerungs Elements bereit.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-118">Provide a shortcut to the functionality of the Control Panel item.</span></span>
2.  <span data-ttu-id="9ecc6-119">Geben Sie Schlüsselwörter an, damit Benutzer in ihrer eigenen Sprache suchen können.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-119">Provide keywords so that users can search using their own language.</span></span> <span data-ttu-id="9ecc6-120">Ein Benutzer möchte möglicherweise "compaction" eingeben, weil er den technischen Begriff kennt.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-120">A user may want to type "compaction" because he or she knows the technical term.</span></span> <span data-ttu-id="9ecc6-121">Ein Benutzer darf "DB Too Big" oder "Database FileSize" eingeben.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-121">A user may type "DB too big", or "database filesize".</span></span> <span data-ttu-id="9ecc6-122">Das Hinzufügen geeigneter Schlüsselwörter zur Aufgabe bedeutet, dass Benutzer das System Steuerungselement finden können.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-122">Adding suitable keywords to the task means that users can find your Control Panel item.</span></span>
3.  <span data-ttu-id="9ecc6-123">Geben Sie Hinweise zur Funktionsweise des System Steuerungs Elements an.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-123">Provide hints about what the Control Panel item does.</span></span> <span data-ttu-id="9ecc6-124">Wenn ein Benutzer die Links unterhalb des Symbols eines System Steuerungs Elements sieht, kann er mehr Informationen darüber erhalten, wie das System Steuerungselement verwendet wird, wenn der Name und das Symbol alleine bereitgestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-124">When a user sees the links beneath a Control Panel item's icon, they can get more information about what the Control Panel item is used for than the name and icon alone can provide.</span></span>

<span data-ttu-id="9ecc6-125">Bei Aufgaben Verknüpfungen sollte es sich um einen Endbenutzer mit Fokus handeln, nicht um Technologie oder Features.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-125">Task links should be end-user focused, not technology- or feature-focused.</span></span> <span data-ttu-id="9ecc6-126">Beispielsweise wäre "Enable Database compaction" eine ungültige Formulierung, da es sich um technische Fachjargon handelt, die den meisten Benutzern nicht vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-126">For example, "Enable database compaction" would be bad wording because it is technical jargon unfamiliar to the majority of users.</span></span> <span data-ttu-id="9ecc6-127">Die Möglichkeit, die Datenbankdatei kleiner zu machen, ist besser, da Sie das tatsächliche Endziel des Benutzers und nicht den Mechanismus zum Erreichen der Methode erwähnt.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-127">"Make my database file smaller" is better because it mentions the user's actual end goal rather than the mechanism to get there.</span></span> <span data-ttu-id="9ecc6-128">Das Ziel ist nicht, eine übermäßige mplifizierung durchzuführen, sondern die Aufgabe in Bezug auf das, was der Benutzer erreichen möchte, zu formulieren.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-128">The goal is not to oversimplify, but rather to phrase the task in terms of what the user wants to accomplish.</span></span>

## <a name="creating-a-task-xml-file"></a><span data-ttu-id="9ecc6-129">Erstellen einer Task-XML-Datei</span><span class="sxs-lookup"><span data-stu-id="9ecc6-129">Creating a Task XML File</span></span>

<span data-ttu-id="9ecc6-130">Aufgaben Verknüpfungen werden in einer XML-Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-130">Task links are defined in an XML file.</span></span> <span data-ttu-id="9ecc6-131">Dieser Abschnitt enthält die Details einer XML-Beispieldatei, die drei Aufgaben Verknüpfungen für ein System Steuerungselement namens **Notepad** definiert.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-131">This section provides the details of an example .xml file that defines three task links for a Control Panel item called **Notepad**.</span></span> <span data-ttu-id="9ecc6-132">Er definiert Titel, Schlüsselwörter und die Befehlszeilen für die Aufgaben Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-132">It defines titles, keywords, and the command lines for the task links.</span></span> <span data-ttu-id="9ecc6-133">Außerdem wird veranschaulicht, wie Sie angeben, welche Aufgaben Verknüpfungen unter welcher Kategorie angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-133">It also illustrates how to specify which task links appear under which category.</span></span> <span data-ttu-id="9ecc6-134">Ein System Steuerungselement, das für die Anzeige in mehr als einer Kategorie registriert ist, kann abhängig von der Kategorie verschiedene Links anzeigen.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-134">A Control Panel item that is registered to appear in more than one category has the option of showing different links depending on the category.</span></span> <span data-ttu-id="9ecc6-135">Erläuterungen zu den verschiedenen Elementen und bereitgestellten Informationen werden als Kommentare in der XML-Datei selbst angegeben.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-135">Explanations of the various elements and information provided are given as comments in the XML itself.</span></span>


```
<?xml version="1.0" ?>
<applications xmlns="http://schemas.microsoft.com/windows/cpltasks/v1" 
              xmlns:sh="http://schemas.microsoft.com/windows/tasks/v1">
    
    <!-- Notepad -->
    <application id="{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}"> 
    <!-- This GUID must match the GUID you created for your Control Panel item,
         and registered in namespace -->
    
        <!-- Solitaire -->
        <sh:task id="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"> 
            <!-- This is a generated GUID, specific to this task link -->
            <sh:name>Play solitaire</sh:name>
            <sh:keywords>solitare;game;cards;ace;diamond;heart;club;single</sh:keywords>
            <sh:command>%ProgramFiles%\Microsoft Games\Solitaire\solitaire.exe</sh:command>
        </sh:task>

        <!-- Task Manager -->
        <sh:task id="{BF46D6AA-B5E6-4EE1-9E5B-ED017272B9F9}" needsElevation="true"> 
            <!-- This is a generated GUID, specific to this task link -->
            <!-- The needsElevation="true" attribute means that the task 
                 appears with a shield icon next to it. Adding this attribute 
                 does not cause the .exe to require elevation - it just adds an 
                 icon to tell users that the command already requires it -->
            <sh:name>See running processes</sh:name>
            <sh:keywords>taskmgr;taskman;running processes;threads;cpu;</sh:keywords>
            <sh:command>taskmgr.exe</sh:command>
        </sh:task>

        <!-- IE -->
        <sh:task id="{DE3A6DCC-C18A-4BBF-9227-11856D7B4422}">
            <sh:name>Open Internet Explorer</sh:name>
            <sh:keywords>IE;web;browser;net;Internet;ActiveX;plug-in;plugin</sh:keywords>
            <sh:command>iexplore.exe</sh:command>
        </sh:task>
        
        <!-- Category assignments -->

        <!-- Appearance and Personalization -->
        <category id="1"> 
        <!-- These idref attributes refer to the GUIDs of the tasks defined above. A maximum of five tasks are shown per category. -->
            <sh:task idref="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"/>   
            <sh:task idref="{BF46D6AA-B5E6-4EE1-9E5B-ED017272B9F9}"/>
            <sh:task idref="{DE3A6DCC-C18A-4BBF-9227-11856D7B4422}"/>
        </category>
        
        <!-- Programs -->
        <category id="8"> 
            <sh:task idref="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}">
                <sh:name>Click here to play</sh:name>
                <!-- This overrides the defined text. When the Notepad Control 
                     Panel item appears in the Programs category, it uses the 
                     "Click here to play" text for this Solitaire link, instead 
                     of "Play solitaire". -->
            </sh:task>
            <sh:task idref="{BF46D6AA-B5E6-4EE1-9E5B-ED017272B9F9}"/>
            <sh:task idref="{DE3A6DCC-C18A-4BBF-9227-11856D7B4422}"/>
       </category>
   </application>
</applications>
```



> [!Note]  
> <span data-ttu-id="9ecc6-136">Ab Windows 7 kann ein System Steuerungselement anhand seines kanonischen Namens anstelle seines ausführbaren Namens identifiziert werden: das **<sh: ControlPanel->** Element kann anstelle von **<sh: Command->** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-136">As of Windows 7, a Control Panel item can be identified by its canonical name rather than its executable name: the **<sh:controlpanel>** element can be used in place of **<sh:command>**.</span></span> <span data-ttu-id="9ecc6-137">Das **<sh: ControlPanel->** Element stellt auch ein Attribut bereit, um die Seite des Elements anzugeben, auf dem es geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-137">The **<sh:controlpanel>** element also provides an attribute to specify the page of the item to which it should open.</span></span> <span data-ttu-id="9ecc6-138">Im folgenden finden Sie ein Beispiel für das **<sh: ControlPanel>** -Element:</span><span class="sxs-lookup"><span data-stu-id="9ecc6-138">The following shows an example of the **<sh:controlpanel>** element:</span></span>

 


```
<sh:controlpanel name="Microsoft.Presentation" page="pageWallpaper"/>
```



## <a name="localizing-task-links"></a><span data-ttu-id="9ecc6-139">Lokalisieren von Aufgaben Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="9ecc6-139">Localizing Task Links</span></span>

<span data-ttu-id="9ecc6-140">Der Text für die Titel und Schlüsselwörter der Aufgaben Verknüpfungen kann in einer Zeichen folgen Tabelle im Modul des System Steuerungs Elements gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-140">The text for the task links' titles and keywords can be stored in a string table in the Control Panel item's module.</span></span> <span data-ttu-id="9ecc6-141">In diesem Fall wird in der XML-Datei das folgende Format verwendet:</span><span class="sxs-lookup"><span data-stu-id="9ecc6-141">In that case, the format used in the XML file becomes:</span></span>


```
<sh:task id="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"> 
    <!-- This is a generated GUID, specific to this task link -->
    <sh:name>@myTextResources.dll,-100</sh:name>
    <sh:keywords>@myTextResources.dll,-101</sh:keywords>
    <sh:command>%ProgramFiles%\Microsoft Games\Solitaire\solitaire.exe</sh:command>
</sh:task>
```



<span data-ttu-id="9ecc6-142">In diesem Beispiel wird der Text für den Namen der Aufgabe in der Zeichen folgen Ressourcen-ID 100 in myTextResources.dll angezeigt, und der Text für die Schlüsselwörter wird in der Zeichen folgen Ressourcen-ID 101 angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-142">In this example, the text for the task's name appears in string resource ID 100 in myTextResources.dll, and the text for the keywords appears in string resource ID 101.</span></span>

## <a name="keywords-and-searching"></a><span data-ttu-id="9ecc6-143">Schlüsselwörter und suchen</span><span class="sxs-lookup"><span data-stu-id="9ecc6-143">Keywords and Searching</span></span>

<span data-ttu-id="9ecc6-144">Die System Steuerungs Suche findet Aufgaben Verknüpfungen basierend auf dem Namen und den zugehörigen Schlüsselwörtern.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-144">The Control Panel search finds task links based on their name and also on their keywords.</span></span> <span data-ttu-id="9ecc6-145">Sie entspricht jedem Wort in der Suche mit dem Präfix von Wörtern im Namen und in den Schlüsselwörtern.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-145">It matches each word in the search with the prefix of words in the name and keywords.</span></span> <span data-ttu-id="9ecc6-146">Beispielsweise entspricht die Abfrage Zeichenfolge "CPU" der Aufgabe "siehe laufende Prozesse" im vorherigen Beispiel, weil "CPU" in der Liste der Schlüsselwörter enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-146">For example, the query string "cpu" would match the task "See running processes" in the earlier example because "cpu" is in the keyword list.</span></span> <span data-ttu-id="9ecc6-147">Die Abfrage Zeichenfolge "pro" würde das Ergebnis ebenfalls finden, da das Titelwort "Processes" mit dieser Zeichenfolge beginnt.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-147">The query string "pro" would also find that result because the title word "processes" begins with that string.</span></span> <span data-ttu-id="9ecc6-148">Beachten Sie, dass die Abfrage nur mit Präfixen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-148">Note that the query only matches prefixes.</span></span> <span data-ttu-id="9ecc6-149">Die Abfrage Zeichenfolge "rocess" stimmt nicht mit einem Ergebnis, weil diese Zeichenfolge, während der Teil des titelworts "Process", nicht mit diesem Wort beginnt.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-149">The query string "rocess" would not match a result because that string, while part of the title word "process", does not begin that word.</span></span>

<span data-ttu-id="9ecc6-150">Wenn eine Suchabfrage mehrere Token enthält, müssen alle Token mit dem Präfix eines Schlüssel Worts oder eines Teils des Aufgaben Titels für ein Ergebnis identisch sein.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-150">When a search query contains multiple tokens, all the tokens must match the prefix of some keyword or part of the task title for a result.</span></span> <span data-ttu-id="9ecc6-151">Die Abfrage "CPU-Ebene" stimmt nicht, da "Level" nicht im Schlüsselwort festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-151">The query "cpu level" would not match, because "level" is not in the keyword set.</span></span> <span data-ttu-id="9ecc6-152">Die Abfrage "CPU Run" führt zu einem Ergebnis, da "CPU" mit einem Schlüsselwort übereinstimmt, und "Run" ist das Präfix des Worts "Running" im Titel der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-152">The query "cpu run" would give a result, because "cpu" matches a keyword, and "run" is the prefix of the word "running" in the task's title.</span></span>

<span data-ttu-id="9ecc6-153">Die Systemsteuerung stellt nicht automatisch Rechtschreibprüfung oder Variationen wie plurale oder Bindestriche bereit.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-153">Control Panel does not automatically provide spelling correction or variations such as plurals or hyphenation.</span></span> <span data-ttu-id="9ecc6-154">Bei Übereinstimmungen wird die Groß-/Kleinschreibung nicht beachtet</span><span class="sxs-lookup"><span data-stu-id="9ecc6-154">Matches are also case-insensitive.</span></span> <span data-ttu-id="9ecc6-155">Um eine erfolgreiche Schlüsselwort Liste zu gewährleisten, wird empfohlen, Variationen selbst anzugeben, z. b. für diesen Aufgaben Link, der Bildschirmschoner umfasst: "Screensaver; Bildschirmschoner; Bildschirmschoner;"</span><span class="sxs-lookup"><span data-stu-id="9ecc6-155">To ensure a successful keyword list, it is recommended to provide variations yourself, such as for this task link that involves screen savers: "screensavers;screen-savers;screen savers;"</span></span>

<span data-ttu-id="9ecc6-156">Es ist nicht erforderlich, den Singular "Bildschirmschoner" hinzuzufügen, da eine Abfrage, die "Screensaver" findet, aufgrund der Präfix Übereinstimmung auch "Bildschirmschoner" findet.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-156">There is no need to add the singular "screensaver", because a query that finds "screensavers" will also find "screensaver" due to the prefix match.</span></span> <span data-ttu-id="9ecc6-157">Ein Benutzer, der sogar einen Teil des Worts eingibt, wie z. b. "Screensa", sieht weiterhin eine Entsprechung für einen Aufgaben Link, der "Screensaver" als Schlüsselwort hat.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-157">A user typing even part of the word, like "screensa" will still see a match on a task link that has "screensavers" as a keyword.</span></span> <span data-ttu-id="9ecc6-158">Für Sprachen, in denen das Wort in Plural Formularen geändert wird, müssen alle Formulare eingefügt werden, die ein Benutzer in den Schlüsselwörtern erwartet.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-158">For languages where plural forms change the word, it is necessary to put all the forms a user could reasonably be expected to type into the keywords.</span></span>

<span data-ttu-id="9ecc6-159">Als Konvention hat Microsoft kleine Wörter wie "Gewusst wie" oder "Ich will" aus dem Satz von Schlüsselwörtern ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-159">As a convention, Microsoft has omitted small words like "how do I" or "I want to" from the set of keywords.</span></span> <span data-ttu-id="9ecc6-160">Es wird erwartet, dass die meisten Benutzer einfach die wichtigsten Wörter eingeben, z. b. "Maus", "hoher Kontrast" oder "Videotreiber", um Ergebnisse zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-160">The expectation is that most users will simply type the most important words such as "mouse", "high contrast", or "video driver" to get results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ecc6-161">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9ecc6-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ecc6-162">System Steuerungselemente</span><span class="sxs-lookup"><span data-stu-id="9ecc6-162">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="9ecc6-163">Richtlinien zur Benutzerfreundlichkeit</span><span class="sxs-lookup"><span data-stu-id="9ecc6-163">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="9ecc6-164">System Steuerungselemente werden registriert</span><span class="sxs-lookup"><span data-stu-id="9ecc6-164">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="9ecc6-165">Verwenden von CPlApplet</span><span class="sxs-lookup"><span data-stu-id="9ecc6-165">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="9ecc6-166">Nachrichtenverarbeitung in der Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="9ecc6-166">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="9ecc6-167">Ausführen von System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="9ecc6-167">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="9ecc6-168">Erweitern von System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="9ecc6-168">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="9ecc6-169">Zuweisen von System Steuerungs Kategorien</span><span class="sxs-lookup"><span data-stu-id="9ecc6-169">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="9ecc6-170">Zugreifen auf die Systemsteuerung im abgesicherten Modus unter Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ecc6-170">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



