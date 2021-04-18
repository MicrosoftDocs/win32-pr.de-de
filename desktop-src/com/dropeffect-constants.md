---
title: Dropffect-Konstanten (oleidl. h)
description: Stellt Informationen zu den Auswirkungen eines Drag & Drop-Vorgangs dar.
ms.assetid: d8e46899-3fbf-4012-8dd3-67fa627526d5
topic_type:
- apiref
api_name:
- DROPEFFECT_NONE
- DROPEFFECT_COPY
- DROPEFFECT_MOVE
- DROPEFFECT_LINK
- DROPEFFECT_SCROLL
api_location:
- OleIdl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2b1888aa028d4e047a9a8ec1f54e2497fa28ce4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343481"
---
# <a name="dropeffect-constants"></a><span data-ttu-id="16cc6-103">Dropffect-Konstanten</span><span class="sxs-lookup"><span data-stu-id="16cc6-103">DROPEFFECT Constants</span></span>

<span data-ttu-id="16cc6-104">Stellt Informationen zu den Auswirkungen eines Drag & Drop-Vorgangs dar.</span><span class="sxs-lookup"><span data-stu-id="16cc6-104">Represents information about the effects of a drag-and-drop operation.</span></span> <span data-ttu-id="16cc6-105">Die [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) -Funktion und viele der Methoden in [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) und [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) verwenden die Werte dieser Enumeration.</span><span class="sxs-lookup"><span data-stu-id="16cc6-105">The [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) function and many of the methods in the [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) and [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) use the values of this enumeration.</span></span>



| <span data-ttu-id="16cc6-106">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="16cc6-106">Constant/value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="16cc6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16cc6-107">Description</span></span>                                                                                                                         |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DROPEFFECT_NONE"></span><span id="dropeffect_none"></span><dl> <span data-ttu-id="16cc6-108"><dt>**Dropffect \_ Keine**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="16cc6-108"><dt>**DROPEFFECT\_NONE**</dt> <dt>0</dt></span></span> </dl>                | <span data-ttu-id="16cc6-109">Das Ablage Ziel kann die Daten nicht akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="16cc6-109">Drop target cannot accept the data.</span></span><br/>                                                                                      |
| <span id="DROPEFFECT_COPY"></span><span id="dropeffect_copy"></span><dl> <span data-ttu-id="16cc6-110"><dt>**Dropffect \_ Kopieren**</dt> Sie <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="16cc6-110"><dt>**DROPEFFECT\_COPY**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="16cc6-111">Löschen Sie die Ergebnisse in einer Kopie.</span><span class="sxs-lookup"><span data-stu-id="16cc6-111">Drop results in a copy.</span></span> <span data-ttu-id="16cc6-112">Die ursprünglichen Daten sind von der Zieh Quelle unberührt.</span><span class="sxs-lookup"><span data-stu-id="16cc6-112">The original data is untouched by the drag source.</span></span><br/>                                               |
| <span id="DROPEFFECT_MOVE"></span><span id="dropeffect_move"></span><dl> <span data-ttu-id="16cc6-113"><dt>**Dropffect \_ Verschieben**</dt> von <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="16cc6-113"><dt>**DROPEFFECT\_MOVE**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="16cc6-114">Ziehen Sie die Quelle, um die Daten zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="16cc6-114">Drag source should remove the data.</span></span> <br/>                                                                                     |
| <span id="DROPEFFECT_LINK"></span><span id="dropeffect_link"></span><dl> <span data-ttu-id="16cc6-115"><dt>**Dropffect \_ Link**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="16cc6-115"><dt>**DROPEFFECT\_LINK**</dt> <dt>4</dt></span></span> </dl>                | <span data-ttu-id="16cc6-116">Mit Drag Source sollte ein Link zu den ursprünglichen Daten erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="16cc6-116">Drag source should create a link to the original data.</span></span><br/>                                                                   |
| <span id="DROPEFFECT_SCROLL"></span><span id="dropeffect_scroll"></span><dl> <span data-ttu-id="16cc6-117"><dt>**Dropffect \_**</dt>Bildlauf <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="16cc6-117"><dt>**DROPEFFECT\_SCROLL**</dt> <dt>0x80000000</dt></span></span> </dl> | <span data-ttu-id="16cc6-118">Der Bildlauf wird gerade gestartet oder ist gegenwärtig im Ziel.</span><span class="sxs-lookup"><span data-stu-id="16cc6-118">Scrolling is about to start or is currently occurring in the target.</span></span> <span data-ttu-id="16cc6-119">Dieser Wert wird zusätzlich zu den anderen Werten verwendet.</span><span class="sxs-lookup"><span data-stu-id="16cc6-119">This value is used in addition to the other values.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="16cc6-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16cc6-120">Remarks</span></span>

<span data-ttu-id="16cc6-121">Die Anwendung sollte immer Werte aus der **drompffect** -Enumeration maskieren, um die Kompatibilität mit zukünftigen Implementierungen sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="16cc6-121">Your application should always mask values from the **DROPEFFECT** enumeration to ensure compatibility with future implementations.</span></span> <span data-ttu-id="16cc6-122">Zurzeit haben nur einige der Positionen in einem **dropeer ffect** -Wert Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="16cc6-122">Presently, only some of the positions in a **DROPEFFECT** value have meaning.</span></span> <span data-ttu-id="16cc6-123">In Zukunft werden weitere Interpretationen für die Bits hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="16cc6-123">In the future, more interpretations for the bits will be added.</span></span> <span data-ttu-id="16cc6-124">Drag Sources und Drop Targets sollten diese Werte vor dem Vergleich sorgfältig maskieren.</span><span class="sxs-lookup"><span data-stu-id="16cc6-124">Drag sources and drop targets should carefully mask these values appropriately before comparing.</span></span> <span data-ttu-id="16cc6-125">Sie sollten einen **dropeer-ect** -Vorgang nicht \_ mit dem folgenden Vorgang vergleichen:</span><span class="sxs-lookup"><span data-stu-id="16cc6-125">They should never compare a **DROPEFFECT** against, say, DROPEFFECT\_COPY by doing the following:</span></span>

``` syntax
if (dwDropEffect == DROPEFFECT_COPY)... 
```

<span data-ttu-id="16cc6-126">Stattdessen sollte die Anwendung immer für den Wert oder die Werte maskiert werden, die mit einem der folgenden Verfahren gesucht werden:</span><span class="sxs-lookup"><span data-stu-id="16cc6-126">Instead, the application should always mask for the value or values being sought as using one of the following techniques:</span></span>

``` syntax
if (dwDropEffect & DROPEFFECT_COPY) == DROPEFFECT_COPY)...

if (dwDropEffect & DROPEFFECT_COPY)... 
```

<span data-ttu-id="16cc6-127">Dies ermöglicht die Definition von neuen Drop-Effekten, wobei die Abwärtskompatibilität mit vorhandenem Code beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="16cc6-127">This allows for the definition of new drop effects, while preserving backward compatibility with existing code.</span></span>

## <a name="requirements"></a><span data-ttu-id="16cc6-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16cc6-128">Requirements</span></span>



| <span data-ttu-id="16cc6-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16cc6-129">Requirement</span></span> | <span data-ttu-id="16cc6-130">Wert</span><span class="sxs-lookup"><span data-stu-id="16cc6-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="16cc6-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="16cc6-131">Minimum supported client</span></span><br/> | <span data-ttu-id="16cc6-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16cc6-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="16cc6-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="16cc6-133">Minimum supported server</span></span><br/> | <span data-ttu-id="16cc6-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16cc6-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="16cc6-135">Header</span><span class="sxs-lookup"><span data-stu-id="16cc6-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="16cc6-136"><dt>Oleidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="16cc6-136"><dt>OleIdl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16cc6-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16cc6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16cc6-138">**DoDragDrop**</span><span class="sxs-lookup"><span data-stu-id="16cc6-138">**DoDragDrop**</span></span>](/windows/desktop/api/Ole2/nf-ole2-dodragdrop)
</dt> <dt>

[<span data-ttu-id="16cc6-139">**IDropSource**</span><span class="sxs-lookup"><span data-stu-id="16cc6-139">**IDropSource**</span></span>](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)
</dt> <dt>

[<span data-ttu-id="16cc6-140">**IDropTarget**</span><span class="sxs-lookup"><span data-stu-id="16cc6-140">**IDropTarget**</span></span>](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)
</dt> </dl>

 

 





