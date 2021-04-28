---
description: 'InkOverlay.SelectionMoved-Ereignis: Tritt auf, wenn sich die Position der aktuellen Auswahl geändert hat, z. B. durch Änderungen an der Benutzeroberfläche, Ausschneide- und Einfügeprozeduren oder die Selection-Eigenschaft.'
ms.assetid: 78b5ab11-01c0-4bdb-ae1f-ec55774abdce
title: InkOverlay.SelectionMoved-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27bf1600683b5258bf899692b692c8cdcabb359
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116868"
---
# <a name="inkoverlayselectionmoved-event"></a><span data-ttu-id="e9b54-103">InkOverlay.SelectionMoved-Ereignis</span><span class="sxs-lookup"><span data-stu-id="e9b54-103">InkOverlay.SelectionMoved event</span></span>

<span data-ttu-id="e9b54-104">Tritt ein, wenn sich die Position der aktuellen Auswahl geändert hat, z. B. [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) durch Änderungen an der Benutzeroberfläche, Prozeduren zum Ausschneiden und Einfügen oder die Selection-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e9b54-104">Occurs when the position of the current selection has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9b54-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9b54-105">Syntax</span></span>


```C++
void SelectionMoved(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="e9b54-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9b54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9b54-107">*OldSelectionRect* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e9b54-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9b54-108">Das umschließende Rechteck der ausgewählten [InkStrokes-Auflistung,](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) wie es vor dem **Ausgelösten SelectionMoved-Ereignis** vorhanden war.</span><span class="sxs-lookup"><span data-stu-id="e9b54-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionMoved** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="e9b54-109">Dieses Rechteck wird in Freihandraumkoordinaten angegeben, was Rückgängig-Szenarien ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="e9b54-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9b54-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e9b54-110">Return value</span></span>

<span data-ttu-id="e9b54-111">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e9b54-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9b54-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9b54-112">Remarks</span></span>

<span data-ttu-id="e9b54-113">Diese Ereignismethode wird in den \_ Dispatch-Only-Schnittstellen IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ IOESelectionMoved definiert.</span><span class="sxs-lookup"><span data-stu-id="e9b54-113">TThis event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of of DISPID\_IOESelectionMoved.</span></span>

<span data-ttu-id="e9b54-114">Um das neue umgrenzende Rechteck der Auflistung der verschobenen Striche abzurufen, rufen Sie die [**Selection.GetBoundingBox-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) auf.</span><span class="sxs-lookup"><span data-stu-id="e9b54-114">To get the new bounding rectangle of the collection of strokes that have been moved, call the [**Selection.GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9b54-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9b54-115">Requirements</span></span>



| <span data-ttu-id="e9b54-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9b54-116">Requirement</span></span> | <span data-ttu-id="e9b54-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e9b54-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9b54-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e9b54-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e9b54-119">Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e9b54-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e9b54-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e9b54-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e9b54-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e9b54-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="e9b54-122">Header</span><span class="sxs-lookup"><span data-stu-id="e9b54-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9b54-123"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="e9b54-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e9b54-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e9b54-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="e9b54-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9b54-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="e9b54-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e9b54-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9b54-127">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e9b54-127">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="e9b54-128">**Selection-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="e9b54-128">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="e9b54-129">**InkRectangle-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e9b54-129">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

