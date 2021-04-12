---
description: Tritt auf, wenn sich die Position der aktuellen Auswahl geändert hat, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und einfügeprozeduren oder von der Selection-Eigenschaft.
ms.assetid: 78b5ab11-01c0-4bdb-ae1f-ec55774abdce
title: InkOverlay. selectionverschodas Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f254b5e3ae3c23f50b12c097608946aad3b3c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348668"
---
# <a name="inkoverlayselectionmoved-event"></a><span data-ttu-id="67f3a-103">InkOverlay. selectionverschodas Ereignis</span><span class="sxs-lookup"><span data-stu-id="67f3a-103">InkOverlay.SelectionMoved event</span></span>

<span data-ttu-id="67f3a-104">Tritt auf, wenn sich die Position der aktuellen Auswahl geändert hat, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und einfügeprozeduren oder von der [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="67f3a-104">Occurs when the position of the current selection has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="67f3a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="67f3a-105">Syntax</span></span>


```C++
void SelectionMoved(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="67f3a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="67f3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67f3a-107">*Oldselectionrect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67f3a-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67f3a-108">Das umschließende Rechteck der ausgewählten [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung, wie es vor dem Auslösen des **selectionverschochereignisses** vorhanden war.</span><span class="sxs-lookup"><span data-stu-id="67f3a-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionMoved** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="67f3a-109">Dieses Rechteck wird in Freihand Raumkoordinaten angegeben, die rückgängig-Szenarien ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="67f3a-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67f3a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="67f3a-110">Return value</span></span>

<span data-ttu-id="67f3a-111">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="67f3a-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="67f3a-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67f3a-112">Remarks</span></span>

<span data-ttu-id="67f3a-113">TDiese Ereignismethode wird in den \_ Dispatch-only-Schnittstellen iinkoverlayevents und \_ iinkpictureevents (Dispinterfaces) mit der ID DISPID \_ ioeselectionverschot definiert.</span><span class="sxs-lookup"><span data-stu-id="67f3a-113">TThis event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of of DISPID\_IOESelectionMoved.</span></span>

<span data-ttu-id="67f3a-114">Zum Abrufen des neuen umgebenden Rechtecks der Auflistung von Strichen, die verschoben wurden, müssen Sie die [**Selection. GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="67f3a-114">To get the new bounding rectangle of the collection of strokes that have been moved, call the [**Selection.GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="67f3a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67f3a-115">Requirements</span></span>



| <span data-ttu-id="67f3a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67f3a-116">Requirement</span></span> | <span data-ttu-id="67f3a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="67f3a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67f3a-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="67f3a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="67f3a-119">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67f3a-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="67f3a-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="67f3a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="67f3a-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="67f3a-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="67f3a-122">Header</span><span class="sxs-lookup"><span data-stu-id="67f3a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="67f3a-123"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="67f3a-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="67f3a-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="67f3a-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="67f3a-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67f3a-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="67f3a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67f3a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67f3a-127">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="67f3a-127">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="67f3a-128">**Auswahl Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="67f3a-128">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="67f3a-129">**Inkrechteck-Klasse**</span><span class="sxs-lookup"><span data-stu-id="67f3a-129">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

