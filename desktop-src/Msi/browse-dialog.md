---
description: Das Dialogfeld Durchsuchen ermöglicht dem Benutzer die Auswahl eines Verzeichnisses. Das Verzeichnis muss nicht vorhanden sein und kann mit diesem Steuerelement erstellt werden.
ms.assetid: 35b991b8-d291-44ef-b1c0-8128bed3c3c8
title: Dialog Feld durchsuchen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f6d3c3d95caec7e9a439621f6741b0dceb0c83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393609"
---
# <a name="browse-dialog"></a><span data-ttu-id="4adc4-104">Dialog Feld durchsuchen</span><span class="sxs-lookup"><span data-stu-id="4adc4-104">Browse Dialog</span></span>

<span data-ttu-id="4adc4-105">Das Dialogfeld Durchsuchen ermöglicht dem Benutzer die Auswahl eines Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="4adc4-105">A Browse dialog box enables the user to select a directory.</span></span> <span data-ttu-id="4adc4-106">Das Verzeichnis muss nicht vorhanden sein und kann mit diesem Steuerelement erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4adc4-106">The directory does not have to exist and may be created by using this control.</span></span>

<span data-ttu-id="4adc4-107">Diese Art von Dialogfeld enthält im Allgemeinen die folgenden drei Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="4adc4-107">This type of dialog box commonly contains the following three controls.</span></span> <span data-ttu-id="4adc4-108">Diese Steuerelemente sind mit derselben Eigenschaft verbunden.</span><span class="sxs-lookup"><span data-stu-id="4adc4-108">These controls are connected to the same property.</span></span> <span data-ttu-id="4adc4-109">Diese Eigenschaft ist der Pfad, der ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="4adc4-109">That property is the path being selected.</span></span>

-   <span data-ttu-id="4adc4-110">Ein [pathedit-Steuer](pathedit-control.md) Element, um den Endabschnitt des Pfads auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="4adc4-110">A [PathEdit control](pathedit-control.md) to select the tail section of the path.</span></span> <span data-ttu-id="4adc4-111">Dieses Steuerelement kann den Fokus nicht verlieren, wenn das eingegebene Ende auf dem aktuellen Volume nicht gültig ist.</span><span class="sxs-lookup"><span data-stu-id="4adc4-111">This control cannot lose focus if the entered tail is not valid on the present volume.</span></span>
-   <span data-ttu-id="4adc4-112">Ein [directoriycombo-Steuer](directorycombo-control.md) Element, um den derzeit ausgewählten Pfad anzuzeigen, der vom Steuerelement "pathedit" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4adc4-112">A [DirectoryCombo control](directorycombo-control.md) to show the presently selected path that is displayed by the PathEdit control.</span></span> <span data-ttu-id="4adc4-113">Dieses Steuerelement zeigt nicht das letzte Segment des Pfads an.</span><span class="sxs-lookup"><span data-stu-id="4adc4-113">This control does not show the last segment of the path.</span></span>
-   <span data-ttu-id="4adc4-114">Ein [Director List-Steuer](directorylist-control.md) Element, das die Ordner unterhalb des Verzeichnisses anzeigt, das zurzeit von directoriycombo angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4adc4-114">A [DirectoryList control](directorylist-control.md) to show the folders below the directory currently displayed by the DirectoryCombo.</span></span> <span data-ttu-id="4adc4-115">Dadurch kann auch ein Ordner angezeigt werden, der noch nicht erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4adc4-115">This can also show a folder that is not yet created.</span></span>

<span data-ttu-id="4adc4-116">Das Dialogfeld Durchsuchen enthält normalerweise auch ein [directoriycombo-Steuer](directorycombo-control.md) Element, das die anzuzeigenden Volumetypen angibt.</span><span class="sxs-lookup"><span data-stu-id="4adc4-116">A Browse dialog box also usually contains a [DirectoryCombo control](directorycombo-control.md) that specifies the volume types to display.</span></span> <span data-ttu-id="4adc4-117">Es ist üblich, dass alle Volumetypen im Dialogfeld Durchsuchen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4adc4-117">It is common for all volume types to be displayed on a Browse dialog box.</span></span>

<span data-ttu-id="4adc4-118">Dialogfelder durchsuchen enthalten in der Regel drei [PUSHBUTTON](pushbutton-control.md)-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="4adc4-118">Browse dialog boxes commonly contain three [PushButton controls](pushbutton-control.md).</span></span> <span data-ttu-id="4adc4-119">Diese Schaltflächen sind mit ihren jeweiligen ControlEvents in der [ControlEvent-Tabelle](controlevent-table.md)verknüpft.</span><span class="sxs-lookup"><span data-stu-id="4adc4-119">These buttons are linked to their respective ControlEvents in [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="4adc4-120">Diese Schaltflächen werden zum Aktivieren der folgenden Steuerelement Optionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="4adc4-120">These buttons are used for activating the following control options.</span></span>



| <span data-ttu-id="4adc4-121">Control-Option</span><span class="sxs-lookup"><span data-stu-id="4adc4-121">Control option</span></span> | <span data-ttu-id="4adc4-122">ControlEvent</span><span class="sxs-lookup"><span data-stu-id="4adc4-122">ControlEvent</span></span>                                            |
|----------------|---------------------------------------------------------|
| <span data-ttu-id="4adc4-123">Eine Ebene nach oben</span><span class="sxs-lookup"><span data-stu-id="4adc4-123">Up One Level</span></span>   | [<span data-ttu-id="4adc4-124">Directoren</span><span class="sxs-lookup"><span data-stu-id="4adc4-124">DirectoryListUp</span></span>](directorylistup-controlevent.md)     |
| <span data-ttu-id="4adc4-125">Neuer Ordner</span><span class="sxs-lookup"><span data-stu-id="4adc4-125">New Folder</span></span>     | [<span data-ttu-id="4adc4-126">Directoriylistnew</span><span class="sxs-lookup"><span data-stu-id="4adc4-126">DirectoryListNew</span></span>](directorylistnew-controlevent.md)   |
| <span data-ttu-id="4adc4-127">Öffnen</span><span class="sxs-lookup"><span data-stu-id="4adc4-127">Open</span></span>           | [<span data-ttu-id="4adc4-128">Directoriylistopen</span><span class="sxs-lookup"><span data-stu-id="4adc4-128">DirectoryListOpen</span></span>](directorylistopen-controlevent.md) |



 

<span data-ttu-id="4adc4-129">Damit die Option neuer Ordner mit einem nicht standardmäßigen Ordnernamen funktioniert, muss der Pfad des neuen Ordners in der [UIText-Tabelle](uitext-table.md)angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4adc4-129">For the New Folder option to work with a non-default folder name, the new folder's path must be specified in the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="4adc4-130">Die Pfad Zeichenfolge sollte das \| Formular "kurzdateiname Long Dateiname" für den Dateinamen verwenden.</span><span class="sxs-lookup"><span data-stu-id="4adc4-130">The path string should use the "short file name\|long file name" form for the file name.</span></span> <span data-ttu-id="4adc4-131">Verwenden Sie z. b. einen Dateinamen wie "myprod ~ 1 \| My Fabulous Product".</span><span class="sxs-lookup"><span data-stu-id="4adc4-131">For example, use a file name such as "MyProd~1\|My Fabulous Product".</span></span> <span data-ttu-id="4adc4-132">Weitere Informationen zum Format des Datei namens finden Sie unter Datentyp der [Dateiname](filename.md) -Spalte.</span><span class="sxs-lookup"><span data-stu-id="4adc4-132">See the [Filename](filename.md) column data type for more information about the file name format.</span></span> <span data-ttu-id="4adc4-133">Wenn der Pfad in der UIText-Tabelle nicht vorhanden ist oder wenn er auf einen ungültigen Wert festgelegt ist, wird er standardmäßig auf den Wert "fldr \| New Folder" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4adc4-133">If the path is not present in the UIText table, or if it is set to an invalid value, then it is set to a value of "Fldr\|New Folder" by default.</span></span> <span data-ttu-id="4adc4-134">Die Schaltfläche **neuer Ordner** kann weggelassen werden, wenn das Dialogfeld nur vorhandene Ordner suchen muss.</span><span class="sxs-lookup"><span data-stu-id="4adc4-134">The **New Folder** button can be omitted if the dialog box only need to search for existing folders.</span></span>

 

 



