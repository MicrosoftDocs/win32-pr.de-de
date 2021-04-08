---
description: Das SelectionTree-Steuerelement verwendet das selectionpath-Ereignis, um den Pfad für das hervorgehobene Element zu veröffentlichen.
ms.assetid: 755e5bf2-42c4-4213-9bb7-4f15ad22041f
title: Selectionpath ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8314b12d14e10ccf96c7db9db32e63172050c0bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959925"
---
# <a name="selectionpath-controlevent"></a><span data-ttu-id="e954f-103">Selectionpath ControlEvent</span><span class="sxs-lookup"><span data-stu-id="e954f-103">SelectionPath ControlEvent</span></span>

<span data-ttu-id="e954f-104">Das [SelectionTree-Steuer](selectiontree-control.md) Element verwendet das selectionpath-Ereignis, um den Pfad für das hervorgehobene Element zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="e954f-104">The [SelectionTree control](selectiontree-control.md) uses the SelectionPath event to publish the path for the highlighted item.</span></span> <span data-ttu-id="e954f-105">Wenn das Element zum Ausführen aus der Quelle ausgewählt ist, ist dies der Pfad der Quelle.</span><span class="sxs-lookup"><span data-stu-id="e954f-105">If the item is selected to run from source, then this is the path of the source.</span></span> <span data-ttu-id="e954f-106">Wenn das Element als nicht vorhanden ausgewählt wird, ist die Zeichenfolge die **absentpath** -Zeichenfolge aus der [UIText-Tabelle](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="e954f-106">If the item is selected to be absent, then the string is the **AbsentPath** string from the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="e954f-107">Dieses Ereignis sollte in der [Tabelle EventMapping](eventmapping-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e954f-107">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="e954f-108">Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e954f-108">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="e954f-109">Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e954f-109">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="e954f-110">Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="e954f-110">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="e954f-111">Dieses Ereignis kann sich nur auf Steuerelemente auswirken, die sich im gleichen Dialogfeld wie das SelectionTree-Steuerelement befinden.</span><span class="sxs-lookup"><span data-stu-id="e954f-111">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

## <a name="published-by"></a><span data-ttu-id="e954f-112">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="e954f-112">Published By</span></span>

[<span data-ttu-id="e954f-113">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="e954f-113">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="e954f-114">Argument</span><span class="sxs-lookup"><span data-stu-id="e954f-114">Argument</span></span>

<span data-ttu-id="e954f-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="e954f-115">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="e954f-116">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="e954f-116">Action on Subscribers</span></span>

<span data-ttu-id="e954f-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="e954f-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="e954f-118">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="e954f-118">Typical Use</span></span>

<span data-ttu-id="e954f-119">Ein [Text](text-control.md) Steuerelement im gleichen modalen Dialogfeld wie die SelectionTree sollte das Ereignis über die [EventMapping-Tabelle](eventmapping-table.md)abonnieren.</span><span class="sxs-lookup"><span data-stu-id="e954f-119">A [Text](text-control.md) control on the same modal dialog as the SelectionTree should subscribe to the event via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="e954f-120">Das Text Steuerelement zeigt den Pfad des hervorgehobenen Elements an.</span><span class="sxs-lookup"><span data-stu-id="e954f-120">The Text Control displays the path of the highlighted item.</span></span>

 

 



