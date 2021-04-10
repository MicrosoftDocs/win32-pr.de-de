---
description: Das Installationsprogramm verwendet dieses Ereignis, um den Namen der aktuellen Aktion zu veröffentlichen. Der Name kann in einem Dialogfeld durch ein Text Steuerelement angezeigt werden, das diese ControlEvent abonniert. Dieses Ereignis sollte in der Tabelle EventMapping erstellt werden.
ms.assetid: 2b4928fe-2d5c-46c1-8a31-cbebbc78d304
title: Action Text ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caf03829818ea7ce7732ca5f51f1710a11e8d07f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959551"
---
# <a name="actiontext-controlevent"></a><span data-ttu-id="6a319-105">Action Text ControlEvent</span><span class="sxs-lookup"><span data-stu-id="6a319-105">ActionText ControlEvent</span></span>

<span data-ttu-id="6a319-106">Das Installationsprogramm verwendet dieses Ereignis, um den Namen der aktuellen Aktion zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="6a319-106">The installer uses this event to publish the name of the present action.</span></span> <span data-ttu-id="6a319-107">Der Name kann in einem Dialogfeld durch ein [Text Steuer](text-control.md) Element angezeigt werden, das diese ControlEvent abonniert.</span><span class="sxs-lookup"><span data-stu-id="6a319-107">The name can be displayed on a dialog box by a [Text Control](text-control.md) that subscribes to this ControlEvent.</span></span> <span data-ttu-id="6a319-108">Dieses Ereignis sollte in der [Tabelle EventMapping](eventmapping-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6a319-108">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="6a319-109">Diese ControlEvent kann von einer Benutzeroberfläche verarbeitet werden, die auf der [*grundlegenden*](b-gly.md)Benutzeroberfläche, der [*reduzierten*](r-gly.md)Benutzeroberfläche oder der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6a319-109">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="6a319-110">Weitere Informationen zu UI-Ebenen finden Sie unter [Benutzeroberflächen](user-interface-levels.md)Ebenen.</span><span class="sxs-lookup"><span data-stu-id="6a319-110">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="6a319-111">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="6a319-111">Published By</span></span>

<span data-ttu-id="6a319-112">Diese ControlEvent wird vom Installationsprogramm veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="6a319-112">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="6a319-113">Argument</span><span class="sxs-lookup"><span data-stu-id="6a319-113">Argument</span></span>

<span data-ttu-id="6a319-114">Dieses ControlEvent verwendet kein Argument.</span><span class="sxs-lookup"><span data-stu-id="6a319-114">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="6a319-115">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="6a319-115">Action on Subscribers</span></span>

<span data-ttu-id="6a319-116">Die Abonnenten werden angezeigt, wenn eine neue Fortschritts Daten vom Installationsprogramm empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="6a319-116">The subscribers are shown when a new progress data arrives from the installer.</span></span>

## <a name="typical-use"></a><span data-ttu-id="6a319-117">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="6a319-117">Typical Use</span></span>

<span data-ttu-id="6a319-118">Ein [Text Steuer](text-control.md) Element in einem nicht modalem Dialogfeld abonniert dieses Ereignis über die [EventMapping-Tabelle](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="6a319-118">A [Text Control](text-control.md) on a modeless dialog subscribes to this event through the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="6a319-119">Das [Text Steuer](text-control-attribute.md) Element-Attribut sollte im Feld Attribute der Tabelle aufgelistet werden, um den Namen der aktuellen Aktion zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6a319-119">The [Text Control Attribute](text-control-attribute.md) should be listed in the Attributes field of this table to receive the name of the current action.</span></span>

 

 



