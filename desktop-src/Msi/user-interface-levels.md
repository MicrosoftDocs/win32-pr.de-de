---
description: Windows Installer bietet Paket Entwicklern die Möglichkeit, eine interne Benutzeroberfläche zu erstellen, die über mehrere Funktionsebenen verfügt.
ms.assetid: 9f5796a7-e244-4fc8-af85-52a147bb2c0b
title: Benutzeroberflächen Ebenen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a835d1b11a4db4393041e83c1b1dc885018610f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218516"
---
# <a name="user-interface-levels"></a><span data-ttu-id="5032e-103">Benutzeroberflächen Ebenen</span><span class="sxs-lookup"><span data-stu-id="5032e-103">User Interface Levels</span></span>

<span data-ttu-id="5032e-104">Windows Installer bietet Paket Entwicklern die Möglichkeit, eine interne Benutzeroberfläche zu erstellen, die über mehrere Funktionsebenen verfügt.</span><span class="sxs-lookup"><span data-stu-id="5032e-104">Windows Installer provides package developers the capability to author an internal user interface that has multiple levels of functionality.</span></span> <span data-ttu-id="5032e-105">Da die interne Benutzeroberfläche vom Autor des Pakets erstellt werden muss, hängt das Verhalten der vollständigen Benutzeroberfläche, der reduzierten Benutzeroberfläche, der Standardbenutzer Oberfläche und der Ebene "None" vom Installationspaket ab.</span><span class="sxs-lookup"><span data-stu-id="5032e-105">Because the internal UI must be created by the author of the package, the behavior of the full UI, reduced UI, basic UI, and None levels depends on the installation package.</span></span> <span data-ttu-id="5032e-106">In der folgenden Tabelle werden die Funktionen beschrieben, die häufig für UI-Ebenen bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="5032e-106">The following table describes the functionality commonly ascribed to UI levels.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5032e-107">UI-Ebene</span><span class="sxs-lookup"><span data-stu-id="5032e-107">UI Level</span></span></th>
<th><span data-ttu-id="5032e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5032e-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5032e-109">Vollständige Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="5032e-109">Full UI</span></span></td>
<td><span data-ttu-id="5032e-110">Zeigt modale und nicht modale Dialogfelder an, die in der internen Benutzeroberfläche erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="5032e-110">Displays modal and modeless dialog boxes that have been authored into the internal UI.</span></span> <span data-ttu-id="5032e-111">Zeigt die <a href="error-dialog.md">Dialog</a> Felder der erstellten Fehler an.</span><span class="sxs-lookup"><span data-stu-id="5032e-111">Displays authored <a href="error-dialog.md">Error Dialog</a> boxes.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="5032e-112">Modale Dialogfelder erfordern Benutzereingaben, bevor die Installation fortgesetzt werden kann. Sie werden durch Festlegen des <a href="modal-dialog-style-bit.md">modalen Dialog Felds Bit</a> in der Spalte Attribute der <a href="dialog-table.md">Dialog</a> Tabelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="5032e-112">Modal dialog boxes require user input before the installation can continue and are specified by setting the <a href="modal-dialog-style-bit.md">Modal Dialog Style Bit</a> in the Attributes column of the <a href="dialog-table.md">Dialog</a> table.</span></span> <span data-ttu-id="5032e-113">Für ein nicht modalem Dialogfeld sind keine Benutzereingaben erforderlich, damit die Installation fortgesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5032e-113">A modeless dialog box does not require user input for the installation to continue.</span></span>
</blockquote>
<br/> <span data-ttu-id="5032e-114">Eine vollständige Benutzeroberfläche zeigt im Allgemeinen das <a href="user-interface-wizard-behavior.md">Verhalten der Benutzeroberfläche</a>an.</span><span class="sxs-lookup"><span data-stu-id="5032e-114">A full UI commonly exhibits <a href="user-interface-wizard-behavior.md">User Interface Wizard Behavior</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5032e-115">Reduzierte Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="5032e-115">Reduced UI</span></span></td>
<td><span data-ttu-id="5032e-116">Zeigt alle nicht modalem Dialogfelder an, die in der Benutzeroberfläche erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="5032e-116">Displays any modeless dialog boxes that have been authored into the UI.</span></span> <span data-ttu-id="5032e-117">In werden keine erstellten modalen Dialogfelder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5032e-117">Does not display any authored modal dialog boxes.</span></span> <span data-ttu-id="5032e-118">Zeigt die <a href="error-dialog.md">Dialog</a> Felder der erstellten Fehler an.</span><span class="sxs-lookup"><span data-stu-id="5032e-118">Displays authored <a href="error-dialog.md">Error Dialog</a> boxes.</span></span> <span data-ttu-id="5032e-119">Zeigt <a href="authoring-disk-prompt-messages.md">Eingabe</a> Aufforderungs Meldungen an.</span><span class="sxs-lookup"><span data-stu-id="5032e-119">Displays <a href="authoring-disk-prompt-messages.md">Disk Prompt</a> messages.</span></span> <span data-ttu-id="5032e-120">Zeigt <a href="filesinuse-dialog.md">FilesInUse-Dialog</a> Felder an.</span><span class="sxs-lookup"><span data-stu-id="5032e-120">Displays <a href="filesinuse-dialog.md">FilesInUse Dialog</a> boxes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5032e-121">Standardbenutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="5032e-121">Basic UI</span></span></td>
<td><span data-ttu-id="5032e-122">Zeigt die integrierten Dialogfelder ohne Modus an, in denen Statusmeldungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5032e-122">Displays the built-in modeless dialog boxes that show progress messages.</span></span> <span data-ttu-id="5032e-123">Zeigt integrierte Fehler Dialogfelder an.</span><span class="sxs-lookup"><span data-stu-id="5032e-123">Displays built-in error dialog boxes.</span></span> <span data-ttu-id="5032e-124">In werden keine erstellten Dialogfelder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5032e-124">Does not display any authored dialog boxes.</span></span> <span data-ttu-id="5032e-125">Fordert Benutzer auf, einen Datenträger einzufügen, indem ein Dialogfeld mit dem Wert der <a href="diskprompt.md"><strong>diskprompt</strong></a> -Eigenschaft angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5032e-125">Prompts users to insert a disk by displaying a dialog box containing the <a href="diskprompt.md"><strong>DiskPrompt</strong></a> property value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5032e-126">Keine</span><span class="sxs-lookup"><span data-stu-id="5032e-126">None</span></span></td>
<td><span data-ttu-id="5032e-127">None bedeutet eine unbeaufsichtigte Installation, die keine Benutzeroberfläche anzeigt.</span><span class="sxs-lookup"><span data-stu-id="5032e-127">None means a silent installation that displays no UI.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5032e-128">Die Ebene der internen Benutzeroberfläche kann mithilfe von " [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5032e-128">The level of the internal UI can be set using [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span></span> <span data-ttu-id="5032e-129">Der Installer legt die [**uilevel**](uilevel.md) -Eigenschaft auf die aktuelle Ebene der Benutzeroberfläche fest.</span><span class="sxs-lookup"><span data-stu-id="5032e-129">The installer sets the [**UILevel**](uilevel.md) property to the current level of the UI.</span></span>

<span data-ttu-id="5032e-130">Wenn die [**limitui**](limitui.md) -Eigenschaft festgelegt ist, ist die Benutzeroberflächen Ebene, die bei der Installation des Pakets verwendet wird, auf Basic beschränkt.</span><span class="sxs-lookup"><span data-stu-id="5032e-130">If the [**LIMITUI**](limitui.md) property is set, the user interface (UI) level used when installing the package is restricted to Basic.</span></span>

<span data-ttu-id="5032e-131">Ein Beispiel für die Benutzeroberflächen Erstellung finden Sie unter [einem Installations Beispiel](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="5032e-131">For an example of UI authoring, see [An Installation Example](an-installation-example.md).</span></span>

 

 




