---
description: Diese ControlEvent kann zum Aktivieren oder Deaktivieren der Rollback-Funktionen des Installers verwendet werden.
ms.assetid: 5279151c-a7cd-4f66-8d1b-d688b3b1cf82
title: Enablerollback-ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc651ef90b46c87431453f50c7ee5a28953e4d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345830"
---
# <a name="enablerollback-controlevent"></a><span data-ttu-id="f62cb-103">Enablerollback-ControlEvent</span><span class="sxs-lookup"><span data-stu-id="f62cb-103">EnableRollback ControlEvent</span></span>

<span data-ttu-id="f62cb-104">Diese ControlEvent kann zum Aktivieren oder Deaktivieren der Rollback-Funktionen des Installers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f62cb-104">This ControlEvent can be used to turn on or turn off the installer's rollback capabilities.</span></span>

<span data-ttu-id="f62cb-105">Dieses Ereignis kann von einem [PUSHBUTTON-Steuer](pushbutton-control.md)Element oder einem [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="f62cb-105">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="f62cb-106">Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f62cb-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="f62cb-107">Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f62cb-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="f62cb-108">Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f62cb-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="f62cb-109">Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="f62cb-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="f62cb-110">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="f62cb-110">Published By</span></span>

<span data-ttu-id="f62cb-111">Diese ControlEvent wird vom Installationsprogramm veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="f62cb-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="f62cb-112">Argument</span><span class="sxs-lookup"><span data-stu-id="f62cb-112">Argument</span></span>

<span data-ttu-id="f62cb-113">False deaktiviert die Rollback-Funktionen des Installers.</span><span class="sxs-lookup"><span data-stu-id="f62cb-113">False turns off the installer's rollback capabilities.</span></span> <span data-ttu-id="f62cb-114">True schaltet die Rollback-Funktionen des Installers um.</span><span class="sxs-lookup"><span data-stu-id="f62cb-114">True turns on the installer's rollback capabilities.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="f62cb-115">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="f62cb-115">Action on Subscribers</span></span>

<span data-ttu-id="f62cb-116">Diese ControlEvent führt keine Aktion für Abonnenten aus.</span><span class="sxs-lookup"><span data-stu-id="f62cb-116">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="f62cb-117">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="f62cb-117">Typical Use</span></span>

<span data-ttu-id="f62cb-118">Kann verwendet werden, um die Rollback-Funktionen zu deaktivieren, wenn der Installer erkennt, dass nicht genügend Speicherplatz vorhanden ist, um die Installation abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="f62cb-118">Can be used to turn off rollback capabilities if the installer detects that there is insufficient disk space available to complete the installation.</span></span> <span data-ttu-id="f62cb-119">In diesem Fall sollte ControlEvent mit den Eigenschaften [**ouesfdiskspace**](outofdiskspace.md), [**outo fnorbdiskspace**](outofnorbdiskspace.md)und [**promptrollbackcost**](promptrollbackcost.md) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f62cb-119">For this case, the ControlEvent should be used with the [**OutOfDiskSpace**](outofdiskspace.md), [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md), and the [**PROMPTROLLBACKCOST**](promptrollbackcost.md) properties.</span></span>

 

 



