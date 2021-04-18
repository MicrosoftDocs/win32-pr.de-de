---
title: List-View Element Zustände (kommstrg. h)
description: Der Zustandswert eines Elements besteht aus dem Zustand des Elements, einem optionalen Überlagerungs Masken Index und einem optionalen Status Bildmasken Index.
ms.assetid: 21827f4a-f133-489b-bbd2-6979d1928b40
topic_type:
- apiref
api_name:
- LVIS_ACTIVATING
- LVIS_CUT
- LVIS_DROPHILITED
- LVIS_FOCUSED
- LVIS_OVERLAYMASK
- LVIS_SELECTED
- LVIS_STATEIMAGEMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8432760dd4cc7efde30700f837864ddcf04aac31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351314"
---
# <a name="list-view-item-states"></a><span data-ttu-id="0c8a9-103">List-View Element Zustände</span><span class="sxs-lookup"><span data-stu-id="0c8a9-103">List-View Item States</span></span>

<span data-ttu-id="0c8a9-104">Der Zustandswert eines Elements besteht aus dem Zustand des Elements, einem optionalen Überlagerungs Masken Index und einem optionalen Status Bildmasken Index.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-104">An item's state value consists of the item's state, an optional overlay mask index, and an optional state image mask index.</span></span>

<span data-ttu-id="0c8a9-105">Der Zustand eines Elements bestimmt seine Darstellung und Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-105">An item's state determines its appearance and functionality.</span></span> <span data-ttu-id="0c8a9-106">Der Status kann NULL oder mindestens einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="0c8a9-106">The state can be zero or one or more of the following values:</span></span>



| <span data-ttu-id="0c8a9-107">Konstante</span><span class="sxs-lookup"><span data-stu-id="0c8a9-107">Constant</span></span>                                                                                                                                                                        | <span data-ttu-id="0c8a9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c8a9-108">Description</span></span>                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_ACTIVATING"></span><span id="lvis_activating"></span><dl> <span data-ttu-id="0c8a9-109"><dt>**Aktivieren von LVIS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0c8a9-109"><dt>**LVIS\_ACTIVATING**</dt></span></span> </dl>             | <span data-ttu-id="0c8a9-110">Wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-110">Not currently supported.</span></span><br/>                                                                                                                                  |
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <span data-ttu-id="0c8a9-111"><dt>**LVIS- \_ Ausschneiden**</dt></span><span class="sxs-lookup"><span data-stu-id="0c8a9-111"><dt>**LVIS\_CUT**</dt></span></span> </dl>                                  | <span data-ttu-id="0c8a9-112">Das Element ist für einen Ausschneide-und Einfügevorgang gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-112">The item is marked for a cut-and-paste operation.</span></span><br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <span data-ttu-id="0c8a9-113"><dt>**LVIS wurde \_ beendet.**</dt></span><span class="sxs-lookup"><span data-stu-id="0c8a9-113"><dt>**LVIS\_DROPHILITED**</dt></span></span> </dl>          | <span data-ttu-id="0c8a9-114">Das Element wird als Drag & Drop-Ziel hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-114">The item is highlighted as a drag-and-drop target.</span></span><br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <span data-ttu-id="0c8a9-115"><dt>**LVIS \_ fokussiert**</dt></span><span class="sxs-lookup"><span data-stu-id="0c8a9-115"><dt>**LVIS\_FOCUSED**</dt></span></span> </dl>                      | <span data-ttu-id="0c8a9-116">Das Element besitzt den Fokus, sodass es von einem Standard Fokus Rechteck umgeben ist.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-116">The item has the focus, so it is surrounded by a standard focus rectangle.</span></span> <span data-ttu-id="0c8a9-117">Obwohl mehr als ein Element ausgewählt werden kann, kann nur ein Element den Fokus haben.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-117">Although more than one item may be selected, only one item can have the focus.</span></span><br/> |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <span data-ttu-id="0c8a9-118"><dt>**LVIS \_ overlaymask**</dt></span><span class="sxs-lookup"><span data-stu-id="0c8a9-118"><dt>**LVIS\_OVERLAYMASK**</dt></span></span> </dl>          | <span data-ttu-id="0c8a9-119">Der Index des Überlagerungs Bilds des Elements wird von einer Maske abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-119">The item's overlay image index is retrieved by a mask.</span></span><br/>                                                                                                    |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <span data-ttu-id="0c8a9-120"><dt>**LVIS \_ ausgewählt**</dt></span><span class="sxs-lookup"><span data-stu-id="0c8a9-120"><dt>**LVIS\_SELECTED**</dt></span></span> </dl>                   | <span data-ttu-id="0c8a9-121">Das Element ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-121">The item is selected.</span></span> <span data-ttu-id="0c8a9-122">Die Darstellung eines ausgewählten Elements hängt davon ab, ob es den Fokus und die für die Auswahl verwendeten Systemfarben besitzt.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-122">The appearance of a selected item depends on whether it has the focus and also on the system colors used for selection.</span></span><br/>             |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <span data-ttu-id="0c8a9-123"><dt>**LVIS- \_ Status-magemask**</dt></span><span class="sxs-lookup"><span data-stu-id="0c8a9-123"><dt>**LVIS\_STATEIMAGEMASK**</dt></span></span> </dl> | <span data-ttu-id="0c8a9-124">Der Status Bild Index des Elements wird von einer Maske abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-124">The item's state image index is retrieved by a mask.</span></span><br/>                                                                                                      |



## <a name="remarks"></a><span data-ttu-id="0c8a9-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c8a9-125">Remarks</span></span>

<span data-ttu-id="0c8a9-126">Sie können die **LVIS \_ overlaymask** -Maske verwenden, um den 1-basierten Index des Überlagerungs Bilds zu isolieren.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-126">You can use the **LVIS\_OVERLAYMASK** mask to isolate the one-based index of the overlay image.</span></span> <span data-ttu-id="0c8a9-127">Sie können den 1-basierten Index des Zustands Bilds mithilfe der **LVIS- \_ stateimagemask** -Maske isolieren.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-127">You can use the **LVIS\_STATEIMAGEMASK** mask to isolate the one-based index of the state image.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c8a9-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c8a9-128">Requirements</span></span>



| <span data-ttu-id="0c8a9-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c8a9-129">Requirement</span></span> | <span data-ttu-id="0c8a9-130">Wert</span><span class="sxs-lookup"><span data-stu-id="0c8a9-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0c8a9-131">Header</span><span class="sxs-lookup"><span data-stu-id="0c8a9-131">Header</span></span><br/> | <dl> <span data-ttu-id="0c8a9-132"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c8a9-132"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





