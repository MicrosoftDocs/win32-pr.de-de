---
description: Das SelectionTree-Steuerelement verwendet das selectionsize-Ereignis, um die Größe des hervorgehobenen Elements zu veröffentlichen.
ms.assetid: 1ef161b6-f127-45ad-a312-d2adcb5124ef
title: Selectionsize-ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c11829661f0120fa5906a04f081e6c979b37180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216353"
---
# <a name="selectionsize-controlevent"></a><span data-ttu-id="82f79-103">Selectionsize-ControlEvent</span><span class="sxs-lookup"><span data-stu-id="82f79-103">SelectionSize ControlEvent</span></span>

<span data-ttu-id="82f79-104">Das [SelectionTree-Steuer](selectiontree-control.md) Element verwendet das selectionsize-Ereignis, um die Größe des hervorgehobenen Elements zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="82f79-104">The [SelectionTree control](selectiontree-control.md) uses the SelectionSize event to publish the size of the highlighted item.</span></span> <span data-ttu-id="82f79-105">Wenn es sich um ein übergeordnetes Element handelt, wird auch die Anzahl der ausgewählten untergeordneten Elemente veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="82f79-105">If it is a parent item, then the number of children selected is also published.</span></span> <span data-ttu-id="82f79-106">Die Zeichenfolge ist eine der Zeichen folgen **selchildcostpos**, **selchildcostneg**, **selbientcostpospos**, **selbientcostposneg**, **selbientcostnegpos** oder **selparameentcostnegneg** aus der [UIText-Tabelle](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="82f79-106">The string is one of the **SelChildCostPos**, **SelChildCostNeg**, **SelParentCostPosPos**, **SelParentCostPosNeg**, **SelParentCostNegPos** or **SelParentCostNegNeg** strings from the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="82f79-107">Dieses Ereignis sollte in der [Tabelle EventMapping](eventmapping-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="82f79-107">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="82f79-108">Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="82f79-108">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="82f79-109">Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="82f79-109">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="82f79-110">Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="82f79-110">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="82f79-111">Dieses Ereignis kann sich nur auf Steuerelemente auswirken, die sich im gleichen Dialogfeld wie das SelectionTree-Steuerelement befinden.</span><span class="sxs-lookup"><span data-stu-id="82f79-111">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

## <a name="published-by"></a><span data-ttu-id="82f79-112">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="82f79-112">Published By</span></span>

[<span data-ttu-id="82f79-113">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="82f79-113">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="82f79-114">Argument</span><span class="sxs-lookup"><span data-stu-id="82f79-114">Argument</span></span>

<span data-ttu-id="82f79-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="82f79-115">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="82f79-116">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="82f79-116">Action on Subscribers</span></span>

<span data-ttu-id="82f79-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="82f79-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="82f79-118">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="82f79-118">Typical Use</span></span>

<span data-ttu-id="82f79-119">Ein [Text](text-control.md) Steuerelement im gleichen modalen Dialogfeld wie das SelectionTree-Steuerelement über die [EventMapping-Tabelle](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="82f79-119">A [Text](text-control.md) control on the same modal dialog as the SelectionTree Control via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="82f79-120">Das Text Steuerelement verwendet dieses Ereignis, um die Größe des hervorgehobenen Elements anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="82f79-120">The Text Control uses this event to display the size of the highlighted item.</span></span>

 

 



