---
description: Das Installationsprogramm verwendet dieses Ereignis, um Daten auf der neuesten Aktion zu veröffentlichen. Die Daten können in einem Dialogfeld durch ein Text Steuerelement angezeigt werden, das diese ControlEvent abonniert. Dieses Ereignis sollte in der Tabelle EventMapping erstellt werden.
ms.assetid: 3c0ab7d0-35f2-4966-8eff-f9f0419d8eed
title: Aktions Daten-ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13bbfe27a59dbe0eda27e7a24e654711d1999188
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367886"
---
# <a name="actiondata-controlevent"></a><span data-ttu-id="a1f8f-105">Aktions Daten-ControlEvent</span><span class="sxs-lookup"><span data-stu-id="a1f8f-105">ActionData ControlEvent</span></span>

<span data-ttu-id="a1f8f-106">Das Installationsprogramm verwendet dieses Ereignis, um Daten auf der neuesten Aktion zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="a1f8f-106">The installer uses this event to publish data on the latest action.</span></span> <span data-ttu-id="a1f8f-107">Die Daten können in einem Dialogfeld durch ein [Text Steuer](text-control.md) Element angezeigt werden, das diese ControlEvent abonniert.</span><span class="sxs-lookup"><span data-stu-id="a1f8f-107">The data can be displayed on a dialog box by a [Text Control](text-control.md) that subscribes to this ControlEvent.</span></span> <span data-ttu-id="a1f8f-108">Dieses Ereignis sollte in der [Tabelle EventMapping](eventmapping-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a1f8f-108">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="a1f8f-109">Diese ControlEvent kann von einer Benutzeroberfläche verarbeitet werden, die auf der [*grundlegenden*](b-gly.md)Benutzeroberfläche, der [*reduzierten*](r-gly.md)Benutzeroberfläche oder der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a1f8f-109">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="a1f8f-110">Weitere Informationen zu UI-Ebenen finden Sie unter [Benutzeroberflächen](user-interface-levels.md)Ebenen.</span><span class="sxs-lookup"><span data-stu-id="a1f8f-110">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="a1f8f-111">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="a1f8f-111">Published By</span></span>

<span data-ttu-id="a1f8f-112">Diese ControlEvent wird vom Installationsprogramm veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="a1f8f-112">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="a1f8f-113">Argument</span><span class="sxs-lookup"><span data-stu-id="a1f8f-113">Argument</span></span>

<span data-ttu-id="a1f8f-114">Dieses ControlEvent verwendet kein Argument.</span><span class="sxs-lookup"><span data-stu-id="a1f8f-114">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="a1f8f-115">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="a1f8f-115">Action on Subscribers</span></span>

<span data-ttu-id="a1f8f-116">Die Abonnenten werden ausgeblendet, wenn eine neue Aktion startet und angezeigt wird, wenn neue Aktions Daten vom Installationsprogramm empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="a1f8f-116">The subscribers are hidden when a new action starts and shown when new action data arrives from the installer.</span></span>

## <a name="typical-use"></a><span data-ttu-id="a1f8f-117">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="a1f8f-117">Typical Use</span></span>

<span data-ttu-id="a1f8f-118">Ein [Text Steuer](text-control.md) Element in einem nicht modalem Dialogfeld abonniert dieses Ereignis über die [EventMapping-Tabelle](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="a1f8f-118">A [Text Control](text-control.md) on a modeless dialog box subscribes to this event through the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="a1f8f-119">Das [Text Steuer](text-control-attribute.md) Element-Attribut wird im Feld Attribute der Tabelle aufgelistet, um die aktuellen Aktions Daten zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="a1f8f-119">The [Text Control Attribute](text-control-attribute.md) is listed in the Attributes field of this table to receive the current action data.</span></span> <span data-ttu-id="a1f8f-120">Wird normalerweise verwendet, um die Namen der Dateien anzuzeigen, die beim Kopieren von Dateien kopiert wurden.</span><span class="sxs-lookup"><span data-stu-id="a1f8f-120">Typically used to display the names of the files copied during file copy.</span></span>

 

 



