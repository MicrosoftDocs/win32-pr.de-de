---
description: Das SelectionTree-Steuerelement verwendet das selectionpathon-Ereignis, um einen booleschen Wert zu veröffentlichen, der angibt, ob dem aktuell ausgewählten Feature ein Auswahl Pfad zugeordnet ist. Dieses Ereignis sollte in der Tabelle EventMapping erstellt werden.
ms.assetid: 441b9416-066a-429b-92d2-555584a20fa2
title: Selectionpathon ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9882ea534a0d4c91a0107ce3949363350a17fbea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359601"
---
# <a name="selectionpathon-controlevent"></a><span data-ttu-id="2f5b9-104">Selectionpathon ControlEvent</span><span class="sxs-lookup"><span data-stu-id="2f5b9-104">SelectionPathOn ControlEvent</span></span>

<span data-ttu-id="2f5b9-105">Das [SelectionTree-Steuer](selectiontree-control.md) Element verwendet das selectionpathon-Ereignis, um einen booleschen Wert zu veröffentlichen, der angibt, ob dem aktuell ausgewählten Feature ein Auswahl Pfad zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2f5b9-105">The [SelectionTree control](selectiontree-control.md) uses the SelectionPathOn event to publish a Boolean value indicating whether there is a selection path associated with the currently selected feature.</span></span> <span data-ttu-id="2f5b9-106">Dieses Ereignis sollte in der [Tabelle EventMapping](eventmapping-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2f5b9-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="2f5b9-107">Dieses Ereignis kann sich nur auf Steuerelemente auswirken, die sich im gleichen Dialogfeld wie das SelectionTree-Steuerelement befinden.</span><span class="sxs-lookup"><span data-stu-id="2f5b9-107">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

<span data-ttu-id="2f5b9-108">Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2f5b9-108">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="2f5b9-109">Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2f5b9-109">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="2f5b9-110">Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="2f5b9-110">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="2f5b9-111">Der seleclevent "selectionpathon" wird nie während einer [Wartungs Installation](maintenance-installation.md)veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="2f5b9-111">The SelectionPathOn ControlEvent is never published during a [Maintenance Installation](maintenance-installation.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="2f5b9-112">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="2f5b9-112">Published By</span></span>

[<span data-ttu-id="2f5b9-113">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="2f5b9-113">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="2f5b9-114">Argument</span><span class="sxs-lookup"><span data-stu-id="2f5b9-114">Argument</span></span>

<span data-ttu-id="2f5b9-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="2f5b9-115">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="2f5b9-116">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="2f5b9-116">Action on Subscribers</span></span>

<span data-ttu-id="2f5b9-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="2f5b9-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="2f5b9-118">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="2f5b9-118">Typical Use</span></span>

<span data-ttu-id="2f5b9-119">Ein [Text](text-control.md) Steuerelement im gleichen modalen Dialogfeld wie die SelectionTree sollte das Ereignis über die [EventMapping-Tabelle](eventmapping-table.md)abonnieren.</span><span class="sxs-lookup"><span data-stu-id="2f5b9-119">A [Text](text-control.md) control on the same modal dialog as the SelectionTree should subscribe to the event via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="2f5b9-120">Das Text Steuerelement zeigt die Beschriftung des Auswahl Pfads an.</span><span class="sxs-lookup"><span data-stu-id="2f5b9-120">The Text Control displays the caption of the selection path.</span></span> <span data-ttu-id="2f5b9-121">Dieses Text Steuerelement ist abhängig vom Ereignis sichtbar oder ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="2f5b9-121">This text control is visible or hidden depending on the event.</span></span>

 

 



