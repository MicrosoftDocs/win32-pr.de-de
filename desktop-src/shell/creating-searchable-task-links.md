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
# <a name="creating-searchable-task-links-for-a-control-panel-item"></a>Erstellen von durchsuchbaren Aufgaben Verknüpfungen für ein System Steuerungselement

Ab Windows Vista enthält die Kategorieansicht "Systemsteuerung" unter jedem Symbol der System Steuerungselemente Aufgaben Verknüpfungen, wie hier gezeigt.

![Aufgaben Verknüpfungen auf der Kategorieseite "System und Wartung"](images/controlpaneltasklinks.png)

Wenn ein Benutzer Text in das **Suchfeld** in der oberen rechten Ecke des Fensters eingibt, enthalten die Suchergebnisse diese Aufgaben Verknüpfungen, wie hier für eine Suche nach dem Wort "Display" gezeigt.

![Aufgaben Verknüpfungen in den Suchergebnissen der Systemsteuerung](images/controlpanelsearchresults.png)

In diesem Thema wird Folgendes erörtert:

-   [Bewährte Methoden zum Verknüpfen von Aufgaben](#task-link-best-practices)
-   [Erstellen einer Task-XML-Datei](#creating-a-task-xml-file)
-   [Lokalisieren von Aufgaben Verknüpfungen](#localizing-task-links)
-   [Schlüsselwörter und suchen](#keywords-and-searching)
-   [Zugehörige Themen](#related-topics)

## <a name="task-link-best-practices"></a>Bewährte Methoden zum Verknüpfen von Aufgaben

Es wird empfohlen, dass Sie Aufgaben Verknüpfungen für Ihre System Steuerungselemente als Hilfe für Benutzer bereitstellen, die nach Funktionen suchen. Es ist auch möglich, den Aufgaben Verknüpfungen Schlüsselwörter hinzuzufügen, damit ein Benutzer Sie finden kann, auch ohne den Titel oder die Terminologie einer Aufgabe zu kennen.

Die besten Aufgaben Verknüpfungen dienen drei Zwecken:

1.  Stellen Sie eine Verknüpfung mit der Funktionalität des System Steuerungs Elements bereit.
2.  Geben Sie Schlüsselwörter an, damit Benutzer in ihrer eigenen Sprache suchen können. Ein Benutzer möchte möglicherweise "compaction" eingeben, weil er den technischen Begriff kennt. Ein Benutzer darf "DB Too Big" oder "Database FileSize" eingeben. Das Hinzufügen geeigneter Schlüsselwörter zur Aufgabe bedeutet, dass Benutzer das System Steuerungselement finden können.
3.  Geben Sie Hinweise zur Funktionsweise des System Steuerungs Elements an. Wenn ein Benutzer die Links unterhalb des Symbols eines System Steuerungs Elements sieht, kann er mehr Informationen darüber erhalten, wie das System Steuerungselement verwendet wird, wenn der Name und das Symbol alleine bereitgestellt werden können.

Bei Aufgaben Verknüpfungen sollte es sich um einen Endbenutzer mit Fokus handeln, nicht um Technologie oder Features. Beispielsweise wäre "Enable Database compaction" eine ungültige Formulierung, da es sich um technische Fachjargon handelt, die den meisten Benutzern nicht vertraut sind. Die Möglichkeit, die Datenbankdatei kleiner zu machen, ist besser, da Sie das tatsächliche Endziel des Benutzers und nicht den Mechanismus zum Erreichen der Methode erwähnt. Das Ziel ist nicht, eine übermäßige mplifizierung durchzuführen, sondern die Aufgabe in Bezug auf das, was der Benutzer erreichen möchte, zu formulieren.

## <a name="creating-a-task-xml-file"></a>Erstellen einer Task-XML-Datei

Aufgaben Verknüpfungen werden in einer XML-Datei definiert. Dieser Abschnitt enthält die Details einer XML-Beispieldatei, die drei Aufgaben Verknüpfungen für ein System Steuerungselement namens **Notepad** definiert. Er definiert Titel, Schlüsselwörter und die Befehlszeilen für die Aufgaben Verknüpfungen. Außerdem wird veranschaulicht, wie Sie angeben, welche Aufgaben Verknüpfungen unter welcher Kategorie angezeigt werden. Ein System Steuerungselement, das für die Anzeige in mehr als einer Kategorie registriert ist, kann abhängig von der Kategorie verschiedene Links anzeigen. Erläuterungen zu den verschiedenen Elementen und bereitgestellten Informationen werden als Kommentare in der XML-Datei selbst angegeben.


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
> Ab Windows 7 kann ein System Steuerungselement anhand seines kanonischen Namens anstelle seines ausführbaren Namens identifiziert werden: das **<sh: ControlPanel->** Element kann anstelle von **<sh: Command->** verwendet werden. Das **<sh: ControlPanel->** Element stellt auch ein Attribut bereit, um die Seite des Elements anzugeben, auf dem es geöffnet werden soll. Im folgenden finden Sie ein Beispiel für das **<sh: ControlPanel>** -Element:

 


```
<sh:controlpanel name="Microsoft.Presentation" page="pageWallpaper"/>
```



## <a name="localizing-task-links"></a>Lokalisieren von Aufgaben Verknüpfungen

Der Text für die Titel und Schlüsselwörter der Aufgaben Verknüpfungen kann in einer Zeichen folgen Tabelle im Modul des System Steuerungs Elements gespeichert werden. In diesem Fall wird in der XML-Datei das folgende Format verwendet:


```
<sh:task id="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"> 
    <!-- This is a generated GUID, specific to this task link -->
    <sh:name>@myTextResources.dll,-100</sh:name>
    <sh:keywords>@myTextResources.dll,-101</sh:keywords>
    <sh:command>%ProgramFiles%\Microsoft Games\Solitaire\solitaire.exe</sh:command>
</sh:task>
```



In diesem Beispiel wird der Text für den Namen der Aufgabe in der Zeichen folgen Ressourcen-ID 100 in myTextResources.dll angezeigt, und der Text für die Schlüsselwörter wird in der Zeichen folgen Ressourcen-ID 101 angezeigt.

## <a name="keywords-and-searching"></a>Schlüsselwörter und suchen

Die System Steuerungs Suche findet Aufgaben Verknüpfungen basierend auf dem Namen und den zugehörigen Schlüsselwörtern. Sie entspricht jedem Wort in der Suche mit dem Präfix von Wörtern im Namen und in den Schlüsselwörtern. Beispielsweise entspricht die Abfrage Zeichenfolge "CPU" der Aufgabe "siehe laufende Prozesse" im vorherigen Beispiel, weil "CPU" in der Liste der Schlüsselwörter enthalten ist. Die Abfrage Zeichenfolge "pro" würde das Ergebnis ebenfalls finden, da das Titelwort "Processes" mit dieser Zeichenfolge beginnt. Beachten Sie, dass die Abfrage nur mit Präfixen übereinstimmt. Die Abfrage Zeichenfolge "rocess" stimmt nicht mit einem Ergebnis, weil diese Zeichenfolge, während der Teil des titelworts "Process", nicht mit diesem Wort beginnt.

Wenn eine Suchabfrage mehrere Token enthält, müssen alle Token mit dem Präfix eines Schlüssel Worts oder eines Teils des Aufgaben Titels für ein Ergebnis identisch sein. Die Abfrage "CPU-Ebene" stimmt nicht, da "Level" nicht im Schlüsselwort festgelegt ist. Die Abfrage "CPU Run" führt zu einem Ergebnis, da "CPU" mit einem Schlüsselwort übereinstimmt, und "Run" ist das Präfix des Worts "Running" im Titel der Aufgabe.

Die Systemsteuerung stellt nicht automatisch Rechtschreibprüfung oder Variationen wie plurale oder Bindestriche bereit. Bei Übereinstimmungen wird die Groß-/Kleinschreibung nicht beachtet Um eine erfolgreiche Schlüsselwort Liste zu gewährleisten, wird empfohlen, Variationen selbst anzugeben, z. b. für diesen Aufgaben Link, der Bildschirmschoner umfasst: "Screensaver; Bildschirmschoner; Bildschirmschoner;"

Es ist nicht erforderlich, den Singular "Bildschirmschoner" hinzuzufügen, da eine Abfrage, die "Screensaver" findet, aufgrund der Präfix Übereinstimmung auch "Bildschirmschoner" findet. Ein Benutzer, der sogar einen Teil des Worts eingibt, wie z. b. "Screensa", sieht weiterhin eine Entsprechung für einen Aufgaben Link, der "Screensaver" als Schlüsselwort hat. Für Sprachen, in denen das Wort in Plural Formularen geändert wird, müssen alle Formulare eingefügt werden, die ein Benutzer in den Schlüsselwörtern erwartet.

Als Konvention hat Microsoft kleine Wörter wie "Gewusst wie" oder "Ich will" aus dem Satz von Schlüsselwörtern ausgelassen. Es wird erwartet, dass die meisten Benutzer einfach die wichtigsten Wörter eingeben, z. b. "Maus", "hoher Kontrast" oder "Videotreiber", um Ergebnisse zu erhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System Steuerungselemente](control-panel-applications.md)
</dt> <dt>

[Richtlinien zur Benutzerfreundlichkeit](user-experience-guidelines.md)
</dt> <dt>

[System Steuerungselemente werden registriert](registering-control-panel-items.md)
</dt> <dt>

[Verwenden von CPlApplet](using-cplapplet.md)
</dt> <dt>

[Nachrichtenverarbeitung in der Systemsteuerung](message-processing.md)
</dt> <dt>

[Ausführen von System Steuerungselementen](executing-control-panel-items.md)
</dt> <dt>

[Erweitern von System Steuerungselementen](extending-system-control-panel-items.md)
</dt> <dt>

[Zuweisen von System Steuerungs Kategorien](assigning-control-panel-categories.md)
</dt> <dt>

[Zugreifen auf die Systemsteuerung im abgesicherten Modus unter Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



