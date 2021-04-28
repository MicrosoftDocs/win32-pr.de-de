---
description: 'InkPicture.SelectionMoved-Ereignis: Tritt auf, wenn sich die Position der aktuellen Auswahl geändert hat, z. B. durch Änderungen an der Benutzeroberfläche, Durchschneide- und Einfügevorgänge oder die Selection-Eigenschaft.'
ms.assetid: 669dc6c2-1620-40f3-b4b5-7ab8967e739a
title: InkPicture.SelectionMoved-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2006b2580e8732c90187b265576b217cdbad9b02
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086448"
---
# <a name="inkpictureselectionmoved-event"></a><span data-ttu-id="76d78-103">InkPicture.SelectionMoved-Ereignis</span><span class="sxs-lookup"><span data-stu-id="76d78-103">InkPicture.SelectionMoved event</span></span>

<span data-ttu-id="76d78-104">Tritt ein, wenn sich die Position der aktuellen Auswahl geändert hat, z. B. durch Änderungen an der Benutzeroberfläche, durch Ausschneide- und Einfügevorgänge oder durch [**die Selection-Eigenschaft.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="76d78-104">Occurs when the position of the current selection has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="76d78-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="76d78-105">Syntax</span></span>


```C++
void SelectionMoved(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="76d78-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="76d78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76d78-107">*OldSelectionRect* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="76d78-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76d78-108">Das umgebundene Rechteck der ausgewählten [InkStrokes-Auflistung,](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) wie es vor dem **Ausgelösten des SelectionMoved-Ereignisses vorhanden** war.</span><span class="sxs-lookup"><span data-stu-id="76d78-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionMoved** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="76d78-109">Dieses Rechteck wird in Freiraumkoordinaten angegeben, was Rückgängig-Szenarien ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="76d78-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76d78-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76d78-110">Return value</span></span>

<span data-ttu-id="76d78-111">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="76d78-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="76d78-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76d78-112">Remarks</span></span>

<span data-ttu-id="76d78-113">Diese Ereignismethode wird in den dispatch-only-Schnittstellen (dispinterfaces) **\_ von IInkOverlayEvents** und **\_ IInkPictureEvents** mit der ID DISPID \_ IOESelectionMoved definiert.</span><span class="sxs-lookup"><span data-stu-id="76d78-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionMoved.</span></span>

<span data-ttu-id="76d78-114">Um das neue umgebundene Rechteck der Auflistung der verschobenen Striche zu erhalten, rufen Sie die [**Selection.GetBoundingBox-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) auf.</span><span class="sxs-lookup"><span data-stu-id="76d78-114">To get the new bounding rectangle of the collection of strokes that have been moved, call the [**Selection.GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="76d78-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76d78-115">Requirements</span></span>



| <span data-ttu-id="76d78-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76d78-116">Requirement</span></span> | <span data-ttu-id="76d78-117">Wert</span><span class="sxs-lookup"><span data-stu-id="76d78-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76d78-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76d78-118">Minimum supported client</span></span><br/> | <span data-ttu-id="76d78-119">Nur Desktop-Apps für Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="76d78-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="76d78-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76d78-120">Minimum supported server</span></span><br/> | <span data-ttu-id="76d78-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="76d78-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="76d78-122">Header</span><span class="sxs-lookup"><span data-stu-id="76d78-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="76d78-123"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="76d78-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="76d78-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="76d78-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="76d78-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76d78-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="76d78-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="76d78-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76d78-127">Inkpicture</span><span class="sxs-lookup"><span data-stu-id="76d78-127">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="76d78-128">[**Selection Property \[ InkPicture-Steuerelement\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="76d78-128">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="76d78-129">**InkRectangle-Klasse**</span><span class="sxs-lookup"><span data-stu-id="76d78-129">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

