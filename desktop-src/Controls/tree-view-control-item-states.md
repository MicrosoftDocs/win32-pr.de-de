---
title: Tree-View Steuerelement Zustände (kommstrg. h)
description: In diesem Abschnitt sind die elementstatusflags aufgeführt, mit denen der Zustand eines Elements in einem Strukturansicht-Steuerelement angegeben wird.
ms.assetid: 5b11d575-6dfd-47a8-b959-b19aaeeca70e
topic_type:
- apiref
api_name:
- TVIS_BOLD
- TVIS_CUT
- TVIS_DROPHILITED
- TVIS_EXPANDED
- TVIS_EXPANDEDONCE
- TVIS_EXPANDPARTIAL
- TVIS_SELECTED
- TVIS_OVERLAYMASK
- TVIS_STATEIMAGEMASK
- TVIS_USERMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef4a19306855b7f38d03aa00323b26407f108bfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352929"
---
# <a name="tree-view-control-item-states"></a><span data-ttu-id="d64fa-103">Status der Tree-View-Steuerelement Zustände</span><span class="sxs-lookup"><span data-stu-id="d64fa-103">Tree-View Control Item States</span></span>

<span data-ttu-id="d64fa-104">In diesem Abschnitt sind die elementstatusflags aufgeführt, mit denen der Zustand eines Elements in einem Strukturansicht-Steuerelement angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d64fa-104">This section lists the item state flags used to indicate the state of an item in a tree-view control.</span></span>



| <span data-ttu-id="d64fa-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="d64fa-105">Constant</span></span>                                                                                                                                                                        | <span data-ttu-id="d64fa-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d64fa-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVIS_BOLD"></span><span id="tvis_bold"></span><dl> <span data-ttu-id="d64fa-107"><dt>**Tvis \_ Fett**</dt></span><span class="sxs-lookup"><span data-stu-id="d64fa-107"><dt>**TVIS\_BOLD**</dt></span></span> </dl>                               | <span data-ttu-id="d64fa-108">Das Element ist fett formatiert.</span><span class="sxs-lookup"><span data-stu-id="d64fa-108">The item is bold.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_CUT"></span><span id="tvis_cut"></span><dl> <span data-ttu-id="d64fa-109"><dt>**Tvis- \_ Ausschneiden**</dt></span><span class="sxs-lookup"><span data-stu-id="d64fa-109"><dt>**TVIS\_CUT**</dt></span></span> </dl>                                  | <span data-ttu-id="d64fa-110">Das Element wird als Teil eines Ausschneide-und Einfügevorgangs ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="d64fa-110">The item is selected as part of a cut-and-paste operation.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TVIS_DROPHILITED"></span><span id="tvis_drophilited"></span><dl> <span data-ttu-id="d64fa-111"><dt>**Tvis wurde \_ beendet.**</dt></span><span class="sxs-lookup"><span data-stu-id="d64fa-111"><dt>**TVIS\_DROPHILITED**</dt></span></span> </dl>          | <span data-ttu-id="d64fa-112">Das Element ist als Drag & Drop-Ziel ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="d64fa-112">The item is selected as a drag-and-drop target.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_EXPANDED"></span><span id="tvis_expanded"></span><dl> <span data-ttu-id="d64fa-113"><dt>**Tvis \_ erweitert**</dt></span><span class="sxs-lookup"><span data-stu-id="d64fa-113"><dt>**TVIS\_EXPANDED**</dt></span></span> </dl>                   | <span data-ttu-id="d64fa-114">Die Liste der untergeordneten Elemente des Elements wird derzeit erweitert. Das heißt, dass die untergeordneten Elemente sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="d64fa-114">The item's list of child items is currently expanded; that is, the child items are visible.</span></span> <span data-ttu-id="d64fa-115">Dieser Wert gilt nur für übergeordnete Elemente.</span><span class="sxs-lookup"><span data-stu-id="d64fa-115">This value applies only to parent items.</span></span><br/>                                                                                                                                                                                                                                                                                                                  |
| <span id="TVIS_EXPANDEDONCE"></span><span id="tvis_expandedonce"></span><dl> <span data-ttu-id="d64fa-116"><dt>**Tvis \_ expandebug**</dt></span><span class="sxs-lookup"><span data-stu-id="d64fa-116"><dt>**TVIS\_EXPANDEDONCE**</dt></span></span> </dl>       | <span data-ttu-id="d64fa-117">Die Liste der untergeordneten Elemente des Elements wurde mindestens einmal erweitert.</span><span class="sxs-lookup"><span data-stu-id="d64fa-117">The item's list of child items has been expanded at least once.</span></span> <span data-ttu-id="d64fa-118">Die TVN-Benachrichtigungs Codes [ \_ itemexpandeing](tvn-itemexpanding.md) und [TVN \_ itemexpanded](tvn-itemexpanded.md) werden nicht für übergeordnete Elemente generiert, für die dieser Status als Reaktion auf eine [**TVM \_**](tvm-expand.md) -Erweiterungs Meldung festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="d64fa-118">The [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) and [TVN\_ITEMEXPANDED](tvn-itemexpanded.md) notification codes are not generated for parent items that have this state set in response to a [**TVM\_EXPAND**](tvm-expand.md) message.</span></span> <span data-ttu-id="d64fa-119">Durch die Verwendung von "TVE \_ Collapse" und "TVE \_ redusereset" mit der **\_ Erweiterung "TVM** " wird dieser Zustand zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="d64fa-119">Using TVE\_COLLAPSE and TVE\_COLLAPSERESET with **TVM\_EXPAND** will cause this state to be reset.</span></span> <span data-ttu-id="d64fa-120">Dieser Wert gilt nur für übergeordnete Elemente.</span><span class="sxs-lookup"><span data-stu-id="d64fa-120">This value applies only to parent items.</span></span> <br/> |
| <span id="TVIS_EXPANDPARTIAL"></span><span id="tvis_expandpartial"></span><dl> <span data-ttu-id="d64fa-121"><dt>**Tvis \_ expandpartial**</dt></span><span class="sxs-lookup"><span data-stu-id="d64fa-121"><dt>**TVIS\_EXPANDPARTIAL**</dt></span></span> </dl>    | <span data-ttu-id="d64fa-122">**Version 4,70**.</span><span class="sxs-lookup"><span data-stu-id="d64fa-122">**Version 4.70**.</span></span> <span data-ttu-id="d64fa-123">Ein teilweise erweitertes Struktur Ansichts Element.</span><span class="sxs-lookup"><span data-stu-id="d64fa-123">A partially expanded tree-view item.</span></span> <span data-ttu-id="d64fa-124">In diesem Zustand sind einige, jedoch nicht alle untergeordneten Elemente sichtbar, und das Pluszeichen des übergeordneten Elements wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d64fa-124">In this state, some, but not all, of the child items are visible and the parent item's plus symbol is displayed.</span></span> <br/>                                                                                                                                                                                                                                                                              |
| <span id="TVIS_SELECTED"></span><span id="tvis_selected"></span><dl> <span data-ttu-id="d64fa-125"><dt>**Tvis \_ ausgewählt**</dt></span><span class="sxs-lookup"><span data-stu-id="d64fa-125"><dt>**TVIS\_SELECTED**</dt></span></span> </dl>                   | <span data-ttu-id="d64fa-126">Das Element ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="d64fa-126">The item is selected.</span></span> <span data-ttu-id="d64fa-127">Das Aussehen hängt davon ab, ob es den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="d64fa-127">Its appearance depends on whether it has the focus.</span></span> <span data-ttu-id="d64fa-128">Das Element wird mithilfe der Systemfarben für die Auswahl gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d64fa-128">The item will be drawn using the system colors for selection.</span></span> <br/>                                                                                                                                                                                                                                                                                                              |
| <span id="TVIS_OVERLAYMASK"></span><span id="tvis_overlaymask"></span><dl> <span data-ttu-id="d64fa-129"><dt>**Tvis- \_ overlaymask**</dt></span><span class="sxs-lookup"><span data-stu-id="d64fa-129"><dt>**TVIS\_OVERLAYMASK**</dt></span></span> </dl>          | <span data-ttu-id="d64fa-130">Maske für die Bits, die zum Angeben des Überlagerungs Bilds des Elements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d64fa-130">Mask for the bits used to specify the item's overlay image index.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_STATEIMAGEMASK"></span><span id="tvis_stateimagemask"></span><dl> <span data-ttu-id="d64fa-131"><dt>**Tvis- \_ Status-magemask**</dt></span><span class="sxs-lookup"><span data-stu-id="d64fa-131"><dt>**TVIS\_STATEIMAGEMASK**</dt></span></span> </dl> | <span data-ttu-id="d64fa-132">Maske für die Bits, die verwendet werden, um den Status Bild Index des Elements anzugeben.</span><span class="sxs-lookup"><span data-stu-id="d64fa-132">Mask for the bits used to specify the item's state image index.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_USERMASK"></span><span id="tvis_usermask"></span><dl> <span data-ttu-id="d64fa-133"><dt>**Tvis- \_ USERMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="d64fa-133"><dt>**TVIS\_USERMASK**</dt></span></span> </dl>                   | <span data-ttu-id="d64fa-134">Identisch mit **Tvis- \_ Status-magemask**.</span><span class="sxs-lookup"><span data-stu-id="d64fa-134">Same as **TVIS\_STATEIMAGEMASK**.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |



## <a name="remarks"></a><span data-ttu-id="d64fa-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d64fa-135">Remarks</span></span>

<span data-ttu-id="d64fa-136">Wenn Sie den Überlagerungs Bild Index oder den Status Bild Index eines Elements festlegen oder abrufen, müssen Sie die folgenden Masken im **statemask** -Member der [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur angeben:</span><span class="sxs-lookup"><span data-stu-id="d64fa-136">When you set or retrieve an item's overlay image index or state image index, you must specify the following masks in the **stateMask** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure:</span></span>

-   <span data-ttu-id="d64fa-137">**Tvis- \_ overlaymask**</span><span class="sxs-lookup"><span data-stu-id="d64fa-137">**TVIS\_OVERLAYMASK**</span></span>
-   <span data-ttu-id="d64fa-138">**Tvis- \_ Status-magemask**</span><span class="sxs-lookup"><span data-stu-id="d64fa-138">**TVIS\_STATEIMAGEMASK**</span></span>
-   <span data-ttu-id="d64fa-139">**Tvis- \_ USERMASK**</span><span class="sxs-lookup"><span data-stu-id="d64fa-139">**TVIS\_USERMASK**</span></span>

<span data-ttu-id="d64fa-140">Diese Werte können auch zum Maskieren der Zustands Bits verwendet werden, die nicht von Interesse sind.</span><span class="sxs-lookup"><span data-stu-id="d64fa-140">These values can also be used to mask off the state bits that are not of interest.</span></span>

## <a name="requirements"></a><span data-ttu-id="d64fa-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d64fa-141">Requirements</span></span>



| <span data-ttu-id="d64fa-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d64fa-142">Requirement</span></span> | <span data-ttu-id="d64fa-143">Wert</span><span class="sxs-lookup"><span data-stu-id="d64fa-143">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d64fa-144">Header</span><span class="sxs-lookup"><span data-stu-id="d64fa-144">Header</span></span><br/> | <dl> <span data-ttu-id="d64fa-145"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d64fa-145"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





