---
description: Das SelectionTree-Steuerelement verwendet das selectionnoitems-Ereignis, um veralteten Element Beschreibungstext zu löschen oder um Schaltflächen zu deaktivieren, die unbrauchbar werden. Dieses Ereignis sollte in der Tabelle EventMapping erstellt werden.
ms.assetid: a79abd77-a6e5-4a1f-8a63-51644151404a
title: Selectionnoitems ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6544dfcaad3d22b63d71703ea95d1aa4f09a1efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363005"
---
# <a name="selectionnoitems-controlevent"></a><span data-ttu-id="e4132-104">Selectionnoitems ControlEvent</span><span class="sxs-lookup"><span data-stu-id="e4132-104">SelectionNoItems ControlEvent</span></span>

<span data-ttu-id="e4132-105">Das [SelectionTree-Steuer](selectiontree-control.md) Element verwendet das selectionnoitems-Ereignis, um veralteten Element Beschreibungstext zu löschen oder um Schaltflächen zu deaktivieren, die unbrauchbar werden.</span><span class="sxs-lookup"><span data-stu-id="e4132-105">The [SelectionTree control](selectiontree-control.md) uses the SelectionNoItems event to delete obsolete item description text or to disable buttons that have become useless.</span></span> <span data-ttu-id="e4132-106">Dieses Ereignis sollte in der [Tabelle EventMapping](eventmapping-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e4132-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="e4132-107">Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e4132-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="e4132-108">Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e4132-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="e4132-109">Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="e4132-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="e4132-110">Dieses Ereignis kann sich nur auf Steuerelemente auswirken, die sich im gleichen Dialogfeld wie das SelectionTree-Steuerelement befinden.</span><span class="sxs-lookup"><span data-stu-id="e4132-110">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

## <a name="published-by"></a><span data-ttu-id="e4132-111">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="e4132-111">Published By</span></span>

<span data-ttu-id="e4132-112">[SelectionTree-Steuer](selectiontree-control.md) Element, wenn die Auswahl keine Knoten aufweist.</span><span class="sxs-lookup"><span data-stu-id="e4132-112">[SelectionTree control](selectiontree-control.md) if the selection has no nodes.</span></span>

## <a name="argument"></a><span data-ttu-id="e4132-113">Argument</span><span class="sxs-lookup"><span data-stu-id="e4132-113">Argument</span></span>

<span data-ttu-id="e4132-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="e4132-114">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="e4132-115">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="e4132-115">Action on Subscribers</span></span>

<span data-ttu-id="e4132-116">Löscht veraltete Element Beschreibungstext oder deaktiviert veraltete Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="e4132-116">Deletes obsolete item description text or disables obsolete buttons.</span></span>

## <a name="typical-use"></a><span data-ttu-id="e4132-117">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="e4132-117">Typical Use</span></span>

<span data-ttu-id="e4132-118">Kann verwendet werden, um die Schaltflächen "Next", "Reset" und "diskcost" im [Auswahl Dialogfeld](selection-dialog.md) zu deaktivieren, wenn eine Auswahl keine Knoten aufweist und diese Schaltflächen unbrauchbar werden</span><span class="sxs-lookup"><span data-stu-id="e4132-118">May be used to disable the Next, Reset, and DiskCost buttons on the [Selection Dialog](selection-dialog.md) when a selection has no nodes and these buttons become useless.</span></span>

 

 



