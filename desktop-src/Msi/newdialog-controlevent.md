---
description: Dieses Ereignis benachrichtigt den Installer, dass ein modales Dialogfeld in ein anderes Dialogfeld übergeht. Das Installationsprogramm entfernt das vorhandene Dialogfeld und erstellt das neue Dialogfeld mit dem Namen, der im-Argument angegeben ist.
ms.assetid: bd1aa465-55a0-4983-8c71-7e7075ee9dfb
title: Newdialog-ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 439c459bc5bfe061cc7f888d9c0a3374afa9098b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130673"
---
# <a name="newdialog-controlevent"></a><span data-ttu-id="2cd65-104">Newdialog-ControlEvent</span><span class="sxs-lookup"><span data-stu-id="2cd65-104">NewDialog ControlEvent</span></span>

<span data-ttu-id="2cd65-105">Dieses Ereignis benachrichtigt den Installer, dass ein modales Dialogfeld in ein anderes Dialogfeld übergeht.</span><span class="sxs-lookup"><span data-stu-id="2cd65-105">This event notifies the installer to transition a modal dialog box to another dialog box.</span></span> <span data-ttu-id="2cd65-106">Das Installationsprogramm entfernt das vorhandene Dialogfeld und erstellt das neue Dialogfeld mit dem Namen, der im-Argument angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="2cd65-106">The installer removes the present dialog box and creates the new one with the name indicated in the argument.</span></span>

<span data-ttu-id="2cd65-107">Dieses Ereignis kann von einem [PUSHBUTTON-Steuer](pushbutton-control.md)Element oder einem [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="2cd65-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="2cd65-108">Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2cd65-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="2cd65-109">Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2cd65-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="2cd65-110">Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2cd65-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="2cd65-111">Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="2cd65-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="2cd65-112">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="2cd65-112">Published By</span></span>

<span data-ttu-id="2cd65-113">Diese ControlEvent wird vom Installationsprogramm veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="2cd65-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="2cd65-114">Argument</span><span class="sxs-lookup"><span data-stu-id="2cd65-114">Argument</span></span>

<span data-ttu-id="2cd65-115">Eine Zeichenfolge, die den Namen des neuen Dialog Felds ist.</span><span class="sxs-lookup"><span data-stu-id="2cd65-115">A string that is the name of the new dialog.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="2cd65-116">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="2cd65-116">Action on Subscribers</span></span>

<span data-ttu-id="2cd65-117">Diese ControlEvent führt keine Aktion für Abonnenten aus.</span><span class="sxs-lookup"><span data-stu-id="2cd65-117">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="2cd65-118">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="2cd65-118">Typical Use</span></span>

<span data-ttu-id="2cd65-119">Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement in einem modalen Dialogfeld ist an dieses Ereignis in der Tabelle [ControlEvent](controlevent-table.md) gebunden, um einen Übergang zum nächsten oder vorherigen Dialogfeld der gleichen Assistenten Sequenz zu signalisieren.</span><span class="sxs-lookup"><span data-stu-id="2cd65-119">A [PushButton](pushbutton-control.md) control on a modal dialog box is tied to this event in the [ControlEvent](controlevent-table.md) table to signal a transition to the next or previous dialog box of the same wizard sequence.</span></span>

 

 



