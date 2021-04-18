---
description: Das SelectionTree-Steuerelement verwendet das selectiondescription-Ereignis, um eine Zeichenfolge zu veröffentlichen, die die Beschreibung für das hervorgehobene Element enthält. Diese Zeichenfolge ist das Beschreibungsfeld der Feature-Tabelle. Dieses Ereignis sollte in der Tabelle EventMapping erstellt werden.
ms.assetid: 29ae9aec-764f-4ff2-9c08-805538130cb1
title: Selectiondescription ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901db4efbed03341243d1b978dab0b8759fbc02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357815"
---
# <a name="selectiondescription-controlevent"></a><span data-ttu-id="9b280-105">Selectiondescription ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9b280-105">SelectionDescription ControlEvent</span></span>

<span data-ttu-id="9b280-106">Das [SelectionTree-Steuer](selectiontree-control.md) Element verwendet das selectiondescription-Ereignis, um eine Zeichenfolge zu veröffentlichen, die die Beschreibung für das hervorgehobene Element enthält.</span><span class="sxs-lookup"><span data-stu-id="9b280-106">The [SelectionTree control](selectiontree-control.md) uses the SelectionDescription event to publish a string that contains the description for the highlighted item.</span></span> <span data-ttu-id="9b280-107">Diese Zeichenfolge ist das **Beschreibungs** Feld der [Feature-Tabelle](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="9b280-107">This string is the **Description** field of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="9b280-108">Dieses Ereignis sollte in der [Tabelle EventMapping](eventmapping-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9b280-108">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="9b280-109">Dieses Ereignis kann sich nur auf Steuerelemente auswirken, die sich im gleichen Dialogfeld wie das [SelectionTree-Steuer](selectiontree-control.md)Element befinden.</span><span class="sxs-lookup"><span data-stu-id="9b280-109">This event can only affect controls that are located on the same dialog box as the [SelectionTree control](selectiontree-control.md).</span></span>

<span data-ttu-id="9b280-110">Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9b280-110">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="9b280-111">Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="9b280-111">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="9b280-112">Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="9b280-112">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="9b280-113">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="9b280-113">Published By</span></span>

[<span data-ttu-id="9b280-114">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="9b280-114">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="9b280-115">Argument</span><span class="sxs-lookup"><span data-stu-id="9b280-115">Argument</span></span>

<span data-ttu-id="9b280-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="9b280-116">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="9b280-117">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="9b280-117">Action on Subscribers</span></span>

<span data-ttu-id="9b280-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="9b280-118">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="9b280-119">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="9b280-119">Typical Use</span></span>

<span data-ttu-id="9b280-120">Ein [Text](text-control.md) Steuerelement im gleichen modalen Dialogfeld wie SelectionTree abonniert dieses ControlEvent über die [EventMapping-Tabelle](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="9b280-120">A [Text](text-control.md) control on the same modal dialog as the SelectionTree subscribes to this ControlEvent via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="9b280-121">Das Text Steuerelement verwendet dieses Ereignis, um die Beschreibung des hervorgehobenen Elements anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9b280-121">The Text Control uses this event to display the description of the highlighted item.</span></span>

 

 



