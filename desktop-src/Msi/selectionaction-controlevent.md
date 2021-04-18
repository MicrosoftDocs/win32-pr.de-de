---
description: Das SelectionTree-Steuerelement verwendet dieses Ereignis, um eine Zeichenfolge zu veröffentlichen, die das markierte Element beschreibt. Die Zeichenfolge ist einer der &\# 0034; SEL \* & \# 0034; Zeichen folgen aus der UIText-Tabelle. Dieses Ereignis sollte in der Tabelle EventMapping erstellt werden.
ms.assetid: 7770b46f-21c7-459f-9778-a86de70d467f
title: Selectionaction ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eda06826f6ac649e2278441c944cdea0332689af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354848"
---
# <a name="selectionaction-controlevent"></a><span data-ttu-id="ca0cb-105">Selectionaction ControlEvent</span><span class="sxs-lookup"><span data-stu-id="ca0cb-105">SelectionAction ControlEvent</span></span>

<span data-ttu-id="ca0cb-106">Das [SelectionTree-Steuer](selectiontree-control.md) Element verwendet dieses Ereignis, um eine Zeichenfolge zu veröffentlichen, die das markierte Element beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ca0cb-106">The [SelectionTree control](selectiontree-control.md) uses this event to publish a string describing the highlighted item.</span></span> <span data-ttu-id="ca0cb-107">Die Zeichenfolge ist eine der "SEL"-Zeichen folgen \* aus der [UIText-Tabelle](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="ca0cb-107">The string is one of the "Sel\*" strings from the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="ca0cb-108">Dieses Ereignis sollte in der [Tabelle EventMapping](eventmapping-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ca0cb-108">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="ca0cb-109">Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ca0cb-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="ca0cb-110">Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ca0cb-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="ca0cb-111">Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="ca0cb-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="ca0cb-112">Dieses Ereignis kann sich nur auf Steuerelemente auswirken, die sich im gleichen Dialogfeld wie das SelectionTree-Steuerelement befinden.</span><span class="sxs-lookup"><span data-stu-id="ca0cb-112">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

## <a name="published-by"></a><span data-ttu-id="ca0cb-113">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="ca0cb-113">Published By</span></span>

[<span data-ttu-id="ca0cb-114">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="ca0cb-114">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="ca0cb-115">Argument</span><span class="sxs-lookup"><span data-stu-id="ca0cb-115">Argument</span></span>

<span data-ttu-id="ca0cb-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="ca0cb-116">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="ca0cb-117">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="ca0cb-117">Action on Subscribers</span></span>

<span data-ttu-id="ca0cb-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="ca0cb-118">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="ca0cb-119">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="ca0cb-119">Typical Use</span></span>

<span data-ttu-id="ca0cb-120">Ein [Text](text-control.md) Steuerelement im gleichen modalen Dialogfeld wie SelectionTree sollte dieses Ereignis über die [EventMapping-Tabelle](eventmapping-table.md)abonnieren.</span><span class="sxs-lookup"><span data-stu-id="ca0cb-120">A [Text](text-control.md) control in the same modal dialog box as the SelectionTree should subscribe to this event via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="ca0cb-121">Das Text Steuerelement zeigt die Erläuterung des ausgewählten Elements an.</span><span class="sxs-lookup"><span data-stu-id="ca0cb-121">The Text Control displays the explanation of the selected item.</span></span>

 

 



