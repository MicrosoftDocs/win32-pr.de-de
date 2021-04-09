---
description: ControlEvents entsprechen Microsoft Windows-Meldungen in Win32-basierten Anwendungen.
ms.assetid: ac62bb94-0605-4145-996a-e91fb1a42a77
title: ControlEvent (Übersicht)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b92f8662a87bf9040b6a811fc170c25a5cf62ad7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868464"
---
# <a name="controlevent-overview"></a><span data-ttu-id="d9842-103">ControlEvent (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="d9842-103">ControlEvent Overview</span></span>

<span data-ttu-id="d9842-104">ControlEvents entsprechen Microsoft Windows-Meldungen in Win32-basierten Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="d9842-104">ControlEvents are analogous to Microsoft Windows messages in Win32-based applications.</span></span> <span data-ttu-id="d9842-105">Anstatt jedoch eine Rückruffunktion zu erstellen, um Windows-Meldungen zu empfangen und Windows-Meldungen mit der [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) -Funktion zu senden, veröffentlichen die Benutzeroberflächen-Installationsprogramme und Steuerelemente die [ControlEvents](control-events.md).</span><span class="sxs-lookup"><span data-stu-id="d9842-105">However, rather than creating a callback function to receive Windows messages and sending Windows messages with the [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) function, the user interface (UI) installer and controls publish [ControlEvents](control-events.md).</span></span> <span data-ttu-id="d9842-106">Andere Steuerelemente und das Installationsprogramm können angegeben werden, um bestimmte ControlEvents zu abonnieren, die dann die Attribute des abonnierenden Steuer Elements ändern.</span><span class="sxs-lookup"><span data-stu-id="d9842-106">Other controls and the installer can be specified to subscribe to particular ControlEvents that will then change attributes of the subscribing control.</span></span> <span data-ttu-id="d9842-107">Zum Hinzufügen von Arbeits Steuerelementen zu Dialogfeldern gibt der Autor der Benutzeroberfläche die Veröffentlichung von ControlEvents in der [Tabelle ControlEvent](controlevent-table.md) an und abonniert Steuerelemente für ControlEvents in der [Tabelle EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="d9842-107">To add working controls to dialog boxes, the author of the UI specifies the publication of ControlEvents in the [ControlEvent table](controlevent-table.md) and subscribes controls to ControlEvents in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="d9842-108">Das Installationsprogramm veröffentlicht die folgenden Ereignisse für Abonnierungs Steuerelemente, die in der [Tabelle EventMapping](eventmapping-table.md)aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="d9842-108">The installer will publish the following events to subscribing controls listed in the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="d9842-109">Ein [ProgressBar-Steuer](progressbar-control.md) Element oder ein [Billboard-Steuer](billboard-control.md) Element abonniert in der Regel setProgress. der Rest wird von [Text Steuerelementen](text-control.md)abonniert.</span><span class="sxs-lookup"><span data-stu-id="d9842-109">A [ProgressBar control](progressbar-control.md) or [Billboard control](billboard-control.md) typically subscribes to SetProgress, the rest are subscribed to by [Text controls](text-control.md).</span></span>

[<span data-ttu-id="d9842-110">Aktions Daten-ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-110">ActionData ControlEvent</span></span>](actiondata-controlevent.md)

[<span data-ttu-id="d9842-111">Action Text ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-111">ActionText ControlEvent</span></span>](actiontext-controlevent.md)

[<span data-ttu-id="d9842-112">SetProgress ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-112">SetProgress ControlEvent</span></span>](setprogress-controlevent.md)

[<span data-ttu-id="d9842-113">Timeremainung ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-113">TimeRemaining ControlEvent</span></span>](timeremaining-controlevent.md)

[<span data-ttu-id="d9842-114">Scriptinprogress ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-114">ScriptInProgress ControlEvent</span></span>](scriptinprogress-controlevent.md)

<span data-ttu-id="d9842-115">Die folgenden Ereignisse werden vom-Steuerelement veröffentlicht, wenn die Elementauswahl in einem [SelectionTree-Steuer](selectiontree-control.md) Element oder einem [directerylist-Steuer](directorylist-control.md)Element verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="d9842-115">The following events are published by the control when the item selection is moved in a [SelectionTree control](selectiontree-control.md) or [DirectoryList Control](directorylist-control.md).</span></span> <span data-ttu-id="d9842-116">Abonniere Steuerelemente müssen sich im gleichen Dialogfeld befinden und in der Tabelle EventMapping aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d9842-116">Subscribing controls must be located on the same dialog box and listed in the EventMapping table.</span></span>

[<span data-ttu-id="d9842-117">Ignorechange ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-117">IgnoreChange ControlEvent</span></span>](ignorechange-controlevent.md)

[<span data-ttu-id="d9842-118">Selectiondescription ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-118">SelectionDescription ControlEvent</span></span>](selectiondescription-controlevent.md)

[<span data-ttu-id="d9842-119">Selectionsize-ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-119">SelectionSize ControlEvent</span></span>](selectionsize-controlevent.md)

[<span data-ttu-id="d9842-120">Selectionpath ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-120">SelectionPath ControlEvent</span></span>](selectionpath-controlevent.md)

[<span data-ttu-id="d9842-121">Selectionaction ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-121">SelectionAction ControlEvent</span></span>](selectionaction-controlevent.md)

[<span data-ttu-id="d9842-122">Selectionnoitems ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-122">SelectionNoItems ControlEvent</span></span>](selectionnoitems-controlevent.md)

<span data-ttu-id="d9842-123">Die folgenden ControlEvents können nach dem Ermessen eines Benutzers veröffentlicht werden, indem Sie mit einem [PUSHBUTTON-Steuer](pushbutton-control.md) Element oder [CheckBox-Steuer](checkbox-control.md) Element in einem Dialogfeld interagieren.</span><span class="sxs-lookup"><span data-stu-id="d9842-123">The following ControlEvents can be published at the discretion of a user by interacting with a [PushButton control](pushbutton-control.md) or [CheckBox control](checkbox-control.md) on a dialog box.</span></span> <span data-ttu-id="d9842-124">Das CheckBox-Steuerelement kann nur die Ereignisse ADDLOCAL, addsource, Remove, doaction und SetProperty veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="d9842-124">The Checkbox control can only publish the AddLocal, AddSource, Remove, DoAction, and SetProperty events.</span></span> <span data-ttu-id="d9842-125">Bei Windows Installer Versionen, die mit Windows Server 2003 und höher ausgeliefert wurden, kann das [SelectionTree-Steuer](selectiontree-control.md) Element die ControlEvents doaction, ControlEvent und SetProperty veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="d9842-125">With Windows Installer versions that shipped with Windows Server 2003 and later, the [SelectionTree control](selectiontree-control.md) can publish the DoAction, ControlEvent and SetProperty ControlEvents.</span></span> <span data-ttu-id="d9842-126">Der Autor der Benutzeroberfläche sollte das ControlEvent in der [ControlEvent-Tabelle](controlevent-table.md)auflisten.</span><span class="sxs-lookup"><span data-stu-id="d9842-126">The author of the UI should list the ControlEvent in the [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="d9842-127">Der Benutzeroberflächen Handler des Installers ist der Abonnent dieser Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="d9842-127">The UI handler of the installer is the subscriber to these events.</span></span>

[<span data-ttu-id="d9842-128">ADDLOCAL-ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-128">AddLocal ControlEvent</span></span>](addlocal-controlevent.md)

[<span data-ttu-id="d9842-129">Addsource-ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-129">AddSource ControlEvent</span></span>](addsource-controlevent.md)

[<span data-ttu-id="d9842-130">Checkexistingtargetpath ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-130">CheckExistingTargetPath ControlEvent</span></span>](checkexistingtargetpath-controlevent.md)

[<span data-ttu-id="d9842-131">Checktargetpath ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-131">CheckTargetPath ControlEvent</span></span>](checktargetpath-controlevent.md)

[<span data-ttu-id="d9842-132">Doaction ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-132">DoAction ControlEvent</span></span>](doaction-controlevent.md)

[<span data-ttu-id="d9842-133">Enablerollback-ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-133">EnableRollback ControlEvent</span></span>](enablerollback-controlevent.md)

[<span data-ttu-id="d9842-134">EndDialog-ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-134">EndDialog ControlEvent</span></span>](enddialog-controlevent.md)

[<span data-ttu-id="d9842-135">Newdialog-ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-135">NewDialog ControlEvent</span></span>](newdialog-controlevent.md)

[<span data-ttu-id="d9842-136">ControlEvent neu installieren</span><span class="sxs-lookup"><span data-stu-id="d9842-136">Reinstall ControlEvent</span></span>](reinstall-controlevent.md)

[<span data-ttu-id="d9842-137">REINSTALLMODE-ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-137">ReinstallMode ControlEvent</span></span>](reinstallmode-controlevent.md)

[<span data-ttu-id="d9842-138">ControlEvent entfernen</span><span class="sxs-lookup"><span data-stu-id="d9842-138">Remove ControlEvent</span></span>](remove-controlevent.md)

[<span data-ttu-id="d9842-139">ControlEvent zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="d9842-139">Reset ControlEvent</span></span>](reset-controlevent.md)

[<span data-ttu-id="d9842-140">Setinstalllevel ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-140">SetInstallLevel ControlEvent</span></span>](setinstalllevel-controlevent.md)

[<span data-ttu-id="d9842-141">SetProperty-ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-141">SetProperty ControlEvent</span></span>](setproperty-controlevent.md)

[<span data-ttu-id="d9842-142">Settargetpath ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-142">SetTargetPath ControlEvent</span></span>](settargetpath-controlevent.md)

[<span data-ttu-id="d9842-143">Spawndialog-ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-143">SpawnDialog ControlEvent</span></span>](spawndialog-controlevent.md)

[<span data-ttu-id="d9842-144">Spawnwaitdialog ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-144">SpawnWaitDialog ControlEvent</span></span>](spawnwaitdialog-controlevent.md)

[<span data-ttu-id="d9842-145">ValidateProductID ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-145">ValidateProductID ControlEvent</span></span>](validateproductid-controlevent.md)

<span data-ttu-id="d9842-146">Ein [PUSHBUTTON-Steuer](pushbutton-control.md) Element kann die folgenden Ereignisse in einem Abonnierung [SelectionTree-Steuer](selectiontree-control.md) Element oder [directerylist-Steuer](directorylist-control.md) Element veröffentlichen, das sich im gleichen Dialogfeld befindet.</span><span class="sxs-lookup"><span data-stu-id="d9842-146">A [PushButton control](pushbutton-control.md) can publish the following events to a subscribing [SelectionTree control](selectiontree-control.md) or [DirectoryList control](directorylist-control.md) located in the same dialog box.</span></span> <span data-ttu-id="d9842-147">Das PUSHBUTTON-Steuerelement sollte in der Tabelle ControlEvent aufgeführt werden, und die Abonnierungs Steuerelemente sollten in der Tabelle EventMapping aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d9842-147">The PushButton Control should be listed in the ControlEvent table and the subscribing controls should be listed in the EventMapping table.</span></span>

[<span data-ttu-id="d9842-148">Selectionbrowse-ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-148">SelectionBrowse ControlEvent</span></span>](selectionbrowse-controlevent.md)

[<span data-ttu-id="d9842-149">Director-listup-ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-149">DirectoryListUp ControlEvent</span></span>](directorylistup-controlevent.md)

[<span data-ttu-id="d9842-150">Director-listnew ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-150">DirectoryListNew ControlEvent</span></span>](directorylistnew-controlevent.md)

[<span data-ttu-id="d9842-151">Director-listopen ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d9842-151">DirectoryListOpen ControlEvent</span></span>](directorylistopen-controlevent.md)

<span data-ttu-id="d9842-152">Steuerungs Ereignisse erfordern im Allgemeinen, dass die Benutzeroberfläche auf der [*vollständigen Benutzeroberfläche*](f-gly.md) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d9842-152">Control events generally require that the UI be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="d9842-153">Die meisten ControlEvents können nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegenden Benutzeroberfläche*](b-gly.md) verwendet werden, da auf diesen Ebenen nur modaldialogfelder angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d9842-153">Most ControlEvents will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md) because these levels only display modeless dialog boxes.</span></span> <span data-ttu-id="d9842-154">Die Ereignisse "Aktions Text", "addsource", "setProgress", "timeremaineing" und "scriptinprogress" sind Ausnahmen und funktionieren in reduzierter oder grundlegender Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="d9842-154">The ActionText, AddSource, SetProgress, TimeRemaining, and ScriptInProgress events are exceptions and will work in reduced or basic UI.</span></span> <span data-ttu-id="d9842-155">Weitere Informationen zu UI-Ebenen finden Sie unter [Benutzeroberflächen](user-interface-levels.md)Ebenen.</span><span class="sxs-lookup"><span data-stu-id="d9842-155">For more information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="d9842-156">Sie können [benutzerdefinierte Aktionen](custom-actions.md) ausführen, indem Sie ein ControlEvent über ein [PUSHBUTTON-Steuer](pushbutton-control.md) Element oder ein [CheckBox-Steuer](checkbox-control.md)Element veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="d9842-156">You can run [custom actions](custom-actions.md) by publishing a ControlEvent from a [PushButton control](pushbutton-control.md) or [Checkbox control](checkbox-control.md).</span></span> <span data-ttu-id="d9842-157">Fügen Sie der [Tabelle ControlEvent](controlevent-table.md) einen Datensatz mit den Namen des Dialog Felds und dem Steuerelement hinzu, das ControlEvent veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="d9842-157">Add a record to the [ControlEvent table](controlevent-table.md) with the names of the dialog and the control publishing the ControlEvent.</span></span> <span data-ttu-id="d9842-158">Dieses Steuerelement sollte ein [doaction-ControlEvent](doaction-controlevent.md) veröffentlichen, das den Installer benachrichtigt, um die benutzerdefinierte Aktion auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d9842-158">This control should publish a [DoAction ControlEvent](doaction-controlevent.md) notifying the installer to run the custom action.</span></span> <span data-ttu-id="d9842-159">Auf Systemen unter Windows XP oder früher können Sie eine benutzerdefinierte Aktion nicht ausführen, indem Sie ein ControlEvent von einem [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="d9842-159">On Windows XP or earlier systems, you cannot run a custom action by publishing a ControlEvent from a [SelectionTree control](selectiontree-control.md).</span></span>

<span data-ttu-id="d9842-160">Weitere Informationen zu bestimmten ControlEvents finden Sie in der Liste der standardmäßigen [ControlEvents](control-events.md) in der [Benutzeroberflächen Referenz](user-interface-reference.md).</span><span class="sxs-lookup"><span data-stu-id="d9842-160">For a more information about particular ControlEvents, see the list of standard [ControlEvents](control-events.md) in [User Interface Reference](user-interface-reference.md).</span></span>

 

 
