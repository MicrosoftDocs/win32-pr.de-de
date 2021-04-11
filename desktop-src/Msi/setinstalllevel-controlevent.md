---
description: Das setinstalllevel-Ereignis ändert die Installations Ebene in den durch das-Argument angegebenen Wert.
ms.assetid: 71cfd516-4a92-446c-bd8f-a3a04dba0bb2
title: Setinstalllevel ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 347f54cee1494b2ff91f7dc1701f0b7749d47e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214859"
---
# <a name="setinstalllevel-controlevent"></a><span data-ttu-id="585a0-103">Setinstalllevel ControlEvent</span><span class="sxs-lookup"><span data-stu-id="585a0-103">SetInstallLevel ControlEvent</span></span>

<span data-ttu-id="585a0-104">Das setinstalllevel-Ereignis ändert die Installations Ebene in den durch das-Argument angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="585a0-104">The SetInstallLevel event changes the installation level to the value specified by the argument.</span></span>

<span data-ttu-id="585a0-105">Dieses Ereignis kann von einem [PUSHBUTTON-Steuer](pushbutton-control.md)Element oder einem [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="585a0-105">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="585a0-106">Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="585a0-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="585a0-107">Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="585a0-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="585a0-108">Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="585a0-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="585a0-109">Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="585a0-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="585a0-110">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="585a0-110">Published By</span></span>

<span data-ttu-id="585a0-111">Diese ControlEvent wird vom Installationsprogramm veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="585a0-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="585a0-112">Argument</span><span class="sxs-lookup"><span data-stu-id="585a0-112">Argument</span></span>

<span data-ttu-id="585a0-113">Eine ganze Zahl, die den neuen Wert der-Installations Ebene ist.</span><span class="sxs-lookup"><span data-stu-id="585a0-113">An integer that is the new value of the installation level.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="585a0-114">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="585a0-114">Action on Subscribers</span></span>

<span data-ttu-id="585a0-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="585a0-115">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="585a0-116">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="585a0-116">Typical Use</span></span>

<span data-ttu-id="585a0-117">Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement in einem modalen Dialogfeld ist an dieses Ereignis in der Tabelle [ControlEvent](controlevent-table.md) gebunden, um die Installations Ebene zu ändern.</span><span class="sxs-lookup"><span data-stu-id="585a0-117">A [PushButton](pushbutton-control.md) control on a modal dialog box is tied to this event in the [ControlEvent](controlevent-table.md) table to change the installation level.</span></span>

 

 



