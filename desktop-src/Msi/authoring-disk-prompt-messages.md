---
description: Verwenden Sie die folgenden Richtlinien, um eine Windows Installer Installation zu erstellen, die ein Meldungs Feld anzeigt, in dem der Benutzer zum Einfügen eines Datenträgers
ms.assetid: 8b53a490-921f-4d89-83b7-dbc62231ef92
title: Erstellen von Datenträger Aufforderungs Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f536a27c2adb5896992eb19a86bff64b9498d83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349169"
---
# <a name="authoring-disk-prompt-messages"></a><span data-ttu-id="2e65f-103">Erstellen von Datenträger Aufforderungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="2e65f-103">Authoring Disk Prompt Messages</span></span>

<span data-ttu-id="2e65f-104">Verwenden Sie die folgenden Richtlinien, um eine Windows Installer Installation zu erstellen, die ein Meldungs Feld anzeigt, in dem der Benutzer zum Einfügen eines Datenträgers</span><span class="sxs-lookup"><span data-stu-id="2e65f-104">Use the following guidelines to author a Windows Installer installation that displays a message box prompting the user to insert a disk.</span></span>

<span data-ttu-id="2e65f-105">**So zeigen Sie ein Meldungs Feld an, das den Benutzer auffordert, einen Datenträger einzufügen**</span><span class="sxs-lookup"><span data-stu-id="2e65f-105">**To display a message box prompting the user to insert a disk**</span></span>

1.  <span data-ttu-id="2e65f-106">Verwenden Sie die Erstellungs Funktionen des Installers, um die Zeichenfolge der [**diskprompt**](diskprompt.md) -Eigenschaft in der [Eigenschaften](property-table.md) Tabelle festzulegen.</span><span class="sxs-lookup"><span data-stu-id="2e65f-106">Use the authoring capabilities of the installer to set the [**DiskPrompt**](diskprompt.md) property string in the [Property](property-table.md) table.</span></span> <span data-ttu-id="2e65f-107">Dies sollte den Namen des installierten Produkts und einen Platzhalter Parameter innerhalb der Zeichenfolge für den auf dem Datenträger gedruckten Titel einschließen.</span><span class="sxs-lookup"><span data-stu-id="2e65f-107">This should include the name of the product being installed and a placeholder parameter within the string for the title printed on the disk.</span></span> <span data-ttu-id="2e65f-108">Für Microsoft Publisher könnte die **diskprompt** -Eigenschaft z. b. "Microsoft Publisher: Disk \[ 1 \] " lauten, wobei " \[ 1" \] der Platzhalter für den Datenträger Titel ist.</span><span class="sxs-lookup"><span data-stu-id="2e65f-108">For example, for Microsoft Publisher the **DiskPrompt** property could be "Microsoft Publisher: Disk \[1\]", where \[1\] is the placeholder for the disk title.</span></span>
2.  <span data-ttu-id="2e65f-109">Geben Sie die Titel der einzelnen Datenträger ein, für die in separate Zeilen der Spalte "diskprompt" der [Medien](media-table.md) Tabelle aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="2e65f-109">Enter the titles of each of the disks being prompted for into separate rows of the DiskPrompt column of the [Media](media-table.md) table.</span></span> <span data-ttu-id="2e65f-110">Der erste und einzige Eintrag in der Medien Tabelle könnte z. b. "1 – install" lauten.</span><span class="sxs-lookup"><span data-stu-id="2e65f-110">For example, the first and only entry into the Media table could be "1–Install."</span></span>
3.  <span data-ttu-id="2e65f-111">Während der [InstallFiles](installfiles-action.md) -Aktion wird der Wert aus der diskprompt-Spalte der [Medien](media-table.md) Tabelle durch den Platzhalter in der Zeichenfolge der [**diskprompt**](diskprompt.md) -Eigenschaft ersetzt.</span><span class="sxs-lookup"><span data-stu-id="2e65f-111">During the [InstallFiles](installfiles-action.md) action the value from the DiskPrompt column of the [Media](media-table.md) table is substituted for the placeholder in the string of the [**DiskPrompt**](diskprompt.md) property.</span></span>
4.  <span data-ttu-id="2e65f-112">Die Meldung, die im Meldungs Feld angezeigt wird, wird aus einer integrierten Vorlagen Zeichenfolge in der [Fehler Tabelle](error-table.md)erstellt.</span><span class="sxs-lookup"><span data-stu-id="2e65f-112">The message displayed by the message box is created from a built-in template string in the [Error table](error-table.md).</span></span> <span data-ttu-id="2e65f-113">Dies ist der Fehler 1302, und die Vorlagen Zeichenfolge lautet: "Bitte legen Sie den Datenträger \[ ein: 2 \] " und \[ 2 \] steht für einen Platzhalter für die [**diskprompt**](diskprompt.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="2e65f-113">This is Error 1302 and the template string is: "Please insert the disk: \[2\]", and the \[2\] represents a placeholder for the [**DiskPrompt**](diskprompt.md) property.</span></span>

<span data-ttu-id="2e65f-114">Im Beispiel wird dem Benutzer die folgende Meldung angezeigt: "legen Sie den Datenträger ein: Microsoft Publisher: Disk 1 – install".</span><span class="sxs-lookup"><span data-stu-id="2e65f-114">The example displays the following message to the user: "Please insert the disk: Microsoft Publisher: Disk 1 – Install."</span></span>

<span data-ttu-id="2e65f-115">Beachten Sie, dass Datenträger-prompt-Meldungen von allen [Benutzeroberflächen Ebenen](user-interface-levels.md) angezeigt werden, ausgenommen keine.</span><span class="sxs-lookup"><span data-stu-id="2e65f-115">Note that disk prompt messages get displayed by all [User Interface Levels](user-interface-levels.md) except None.</span></span>

 

 



