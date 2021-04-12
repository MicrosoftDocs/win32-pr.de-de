---
description: Dieses Ereignis benachrichtigt das Installationsprogramm, ein modales Dialogfeld zu entfernen. In jedem Fall entfernt das Installationsprogramm das vorhandene Dialogfeld.
ms.assetid: 74a28696-6387-4d62-8955-4708ba5872bb
title: EndDialog-ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08449bffe29093e32066e92e1b8fc739efa02d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216374"
---
# <a name="enddialog-controlevent"></a><span data-ttu-id="1adf5-104">EndDialog-ControlEvent</span><span class="sxs-lookup"><span data-stu-id="1adf5-104">EndDialog ControlEvent</span></span>

<span data-ttu-id="1adf5-105">Dieses Ereignis benachrichtigt das Installationsprogramm, ein modales Dialogfeld zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="1adf5-105">This event notifies the installer to remove a modal dialog box.</span></span> <span data-ttu-id="1adf5-106">In jedem Fall entfernt das Installationsprogramm das vorhandene Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="1adf5-106">In all cases the installer removes the present dialog box.</span></span>

<span data-ttu-id="1adf5-107">Dieses Ereignis kann von einem [PUSHBUTTON-Steuer](pushbutton-control.md)Element oder einem [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="1adf5-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="1adf5-108">Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1adf5-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="1adf5-109">Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1adf5-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="1adf5-110">Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1adf5-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="1adf5-111">Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="1adf5-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="1adf5-112">In der folgenden Tabelle wird die Aktion des-Ereignisses aufgelistet, das sich aus verschiedenen in der [ControlEvent-Tabelle](controlevent-table.md)eingegebenen Argumenten ergibt.</span><span class="sxs-lookup"><span data-stu-id="1adf5-112">The following table lists the action of the event resulting from different arguments entered into the [ControlEvent table](controlevent-table.md).</span></span>



| <span data-ttu-id="1adf5-113">Argument</span><span class="sxs-lookup"><span data-stu-id="1adf5-113">Argument</span></span> | <span data-ttu-id="1adf5-114">Aktion durch das Installationsprogramm</span><span class="sxs-lookup"><span data-stu-id="1adf5-114">Action by the installer</span></span>                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1adf5-115">Beenden</span><span class="sxs-lookup"><span data-stu-id="1adf5-115">Exit</span></span>     | <span data-ttu-id="1adf5-116">Die Assistenten Sequenz ist geschlossen, und das Steuerelement wird mit dem Userexit-Wert an das Installationsprogramm zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1adf5-116">The wizard sequence is closed and the control returns to the installer with the UserExit value.</span></span> <span data-ttu-id="1adf5-117">Dieses Argument kann nicht in einem Dialogfeld verwendet werden, das einem anderen Dialogfeld untergeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1adf5-117">This argument cannot be used in a dialog box that is a child of another dialog box.</span></span> |
| <span data-ttu-id="1adf5-118">Erneut versuchen</span><span class="sxs-lookup"><span data-stu-id="1adf5-118">Retry</span></span>    | <span data-ttu-id="1adf5-119">Die Assistenten Sequenz ist geschlossen, und das Steuerelement wird mit dem Suspend-Wert an das Installationsprogramm zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1adf5-119">The wizard sequence is closed and the control returns to the installer with the Suspend value.</span></span> <span data-ttu-id="1adf5-120">Dieses Argument kann nicht in einem Dialogfeld verwendet werden, das einem anderen Dialogfeld untergeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1adf5-120">This argument cannot be used in a dialog box that is a child of another dialog box.</span></span>  |
| <span data-ttu-id="1adf5-121">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="1adf5-121">Ignore</span></span>   | <span data-ttu-id="1adf5-122">Die Assistenten Sequenz ist geschlossen, und das Steuerelement wird mit dem fertigen Wert an das Installationsprogramm zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1adf5-122">The wizard sequence is closed and the control returns to the installer with the Finished value.</span></span> <span data-ttu-id="1adf5-123">Dieses Argument kann nicht in einem Dialogfeld verwendet werden, das einem anderen Dialogfeld untergeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1adf5-123">This argument cannot be used in a dialog box that is a child of another dialog box.</span></span> |
| <span data-ttu-id="1adf5-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1adf5-124">Return</span></span>   | <span data-ttu-id="1adf5-125">Das Steuerelement wird an das übergeordnete Element des aktuellen Dialog Felds zurückgegeben, oder, wenn kein übergeordnetes Element vorhanden ist, wird das Steuerelement mit dem Wert Erfolg an das Installationsprogramm zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="1adf5-125">The control returns to the parent of the present dialog box, or if there is no parent, the control returns to the installer with the Success value.</span></span>                                 |



 

## <a name="published-by"></a><span data-ttu-id="1adf5-126">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="1adf5-126">Published By</span></span>

<span data-ttu-id="1adf5-127">Diese ControlEvent wird vom Installationsprogramm veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="1adf5-127">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="1adf5-128">Argument</span><span class="sxs-lookup"><span data-stu-id="1adf5-128">Argument</span></span>

<span data-ttu-id="1adf5-129">In regulären Dialogfeldern kann die Argument-Spalte der [ControlEvent-Tabelle](controlevent-table.md) "Return", "Exit", "Retry" oder "Ignore" lauten.</span><span class="sxs-lookup"><span data-stu-id="1adf5-129">On regular dialog boxes the Argument column of the [ControlEvent table](controlevent-table.md) can be "Return", "Exit", "Retry", or "Ignore".</span></span>

<span data-ttu-id="1adf5-130">Im Dialogfeld Fehler kann die Argument-Spalte der [ControlEvent-Tabelle](controlevent-table.md) "errorok", "errorcancel", "errorabort", "errorretry", "errorignore", "erroryes" oder "errorno" lauten.</span><span class="sxs-lookup"><span data-stu-id="1adf5-130">On error dialog boxes the Argument column of the [ControlEvent table](controlevent-table.md) can be "ErrorOk", "ErrorCancel", "ErrorAbort", "ErrorRetry", "ErrorIgnore", "ErrorYes", or "ErrorNo".</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="1adf5-131">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="1adf5-131">Action on Subscribers</span></span>

<span data-ttu-id="1adf5-132">Keine.</span><span class="sxs-lookup"><span data-stu-id="1adf5-132">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="1adf5-133">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="1adf5-133">Typical Use</span></span>

<span data-ttu-id="1adf5-134">Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement in einem modalen Dialogfeld ist an dieses Ereignis in der Tabelle [ControlEvent](controlevent-table.md) gebunden, um ein Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="1adf5-134">A [PushButton](pushbutton-control.md) control on a modal dialog is tied to this event in the [ControlEvent](controlevent-table.md) table to close a dialog box.</span></span>

 

 



