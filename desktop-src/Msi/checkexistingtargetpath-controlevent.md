---
description: Mit diesem Ereignis wird das Installationsprogramm benachrichtigt, dass überprüft werden muss, ob der ausgewählte Pfad beschreibbar ist. Wenn der Pfad nicht geschrieben werden kann, blockiert das Ereignis weitere ControlEvents, die dem Steuerelement zugeordnet sind.
ms.assetid: 4672e2e4-a789-4050-81b9-92ec491745ac
title: Checkexistingtargetpath ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1117de57c5474d196da1f40da6fda3cce60b8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347120"
---
# <a name="checkexistingtargetpath-controlevent"></a><span data-ttu-id="e6dac-104">Checkexistingtargetpath ControlEvent</span><span class="sxs-lookup"><span data-stu-id="e6dac-104">CheckExistingTargetPath ControlEvent</span></span>

<span data-ttu-id="e6dac-105">Mit diesem Ereignis wird das Installationsprogramm benachrichtigt, dass überprüft werden muss, ob der ausgewählte Pfad beschreibbar ist.</span><span class="sxs-lookup"><span data-stu-id="e6dac-105">This event notifies the installer that it has to verify that the selected path is writable.</span></span> <span data-ttu-id="e6dac-106">Wenn der Pfad nicht geschrieben werden kann, blockiert das Ereignis weitere ControlEvents, die dem Steuerelement zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e6dac-106">If the path is cannot be written, then the event blocks further ControlEvents associated with the control.</span></span>

<span data-ttu-id="e6dac-107">Dieses Ereignis kann von einem [PUSHBUTTON-Steuer](pushbutton-control.md)Element oder einem [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="e6dac-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="e6dac-108">Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e6dac-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="e6dac-109">Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e6dac-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="e6dac-110">Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e6dac-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="e6dac-111">Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="e6dac-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="e6dac-112">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="e6dac-112">Published By</span></span>

<span data-ttu-id="e6dac-113">Diese ControlEvent wird vom Installationsprogramm veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="e6dac-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="e6dac-114">Argument</span><span class="sxs-lookup"><span data-stu-id="e6dac-114">Argument</span></span>

<span data-ttu-id="e6dac-115">Der Name der Eigenschaft, die den Pfad enthält.</span><span class="sxs-lookup"><span data-stu-id="e6dac-115">The name of the property containing the path.</span></span> <span data-ttu-id="e6dac-116">Wenn die Eigenschaft deretendiert ist, wird der Eigenschaftsname in eckige Klammern eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="e6dac-116">If the property is indirected, then the property name is enclosed in square brackets.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="e6dac-117">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="e6dac-117">Action on Subscribers</span></span>

<span data-ttu-id="e6dac-118">Diese ControlEvent führt keine Aktion für Abonnenten aus.</span><span class="sxs-lookup"><span data-stu-id="e6dac-118">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="e6dac-119">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="e6dac-119">Typical Use</span></span>

<span data-ttu-id="e6dac-120">Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement in einem Dialogfeld zum Durchsuchen ist an dieses Ereignis in der Tabelle [ControlEvent](controlevent-table.md) gebunden, um den ausgewählten Pfad vor der Rückgabe zum Auswahl Dialogfeld zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e6dac-120">A [PushButton](pushbutton-control.md) control on a browse dialog is tied to this event in the [ControlEvent](controlevent-table.md) table to check the selected path before returning to the selection dialog.</span></span>

 

 



