---
description: 'InkOverlay.SelectionResizing-Ereignis: Tritt ein, wenn sich die Größe der aktuellen Auswahl ändert, z. B. durch Änderungen an der Benutzeroberfläche, Ausschneide- und Einfügeprozessen oder die Selection-Eigenschaft.'
ms.assetid: 7fe0249c-c43d-498b-9029-cf5969201d96
title: InkOverlay.SelectionResizing-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b5577f83c14ccc2e998fb4257344729e2219a2d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086678"
---
# <a name="inkoverlayselectionresizing-event"></a><span data-ttu-id="039fe-103">InkOverlay.SelectionResizing-Ereignis</span><span class="sxs-lookup"><span data-stu-id="039fe-103">InkOverlay.SelectionResizing event</span></span>

<span data-ttu-id="039fe-104">Tritt ein, wenn sich die Größe der aktuellen Auswahl ändert, z. B. durch Änderungen [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) an der Benutzeroberfläche, Prozeduren zum Ausschneiden und Einfügen oder die Selection-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="039fe-104">Occurs when the size of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="039fe-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="039fe-105">Syntax</span></span>


```C++
void SelectionResizing(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="039fe-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="039fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="039fe-107">*CurSelectionRect* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="039fe-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="039fe-108">Das umgrenzende Rechteck der Auswahl nach dem **SelectionResizing-Ereignis.**</span><span class="sxs-lookup"><span data-stu-id="039fe-108">The bounding rectangle of the selection after the **SelectionResizing** event.</span></span>

> [!Note]  
> <span data-ttu-id="039fe-109">Dieses Rechteck wird in Clientfensterkoordinaten angegeben, was Szenarien wie das Beibehalten des Seitenverhältnisses bei der Größenänderung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="039fe-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="039fe-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="039fe-110">Return value</span></span>

<span data-ttu-id="039fe-111">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="039fe-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="039fe-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="039fe-112">Remarks</span></span>

<span data-ttu-id="039fe-113">Diese Ereignismethode wird in den \_ Dispatch-only-Schnittstellen IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ IOESelectionResizing definiert.</span><span class="sxs-lookup"><span data-stu-id="039fe-113">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResizing.</span></span>

## <a name="requirements"></a><span data-ttu-id="039fe-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="039fe-114">Requirements</span></span>



| <span data-ttu-id="039fe-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="039fe-115">Requirement</span></span> | <span data-ttu-id="039fe-116">Wert</span><span class="sxs-lookup"><span data-stu-id="039fe-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="039fe-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="039fe-117">Minimum supported client</span></span><br/> | <span data-ttu-id="039fe-118">Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="039fe-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="039fe-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="039fe-119">Minimum supported server</span></span><br/> | <span data-ttu-id="039fe-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="039fe-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="039fe-121">Header</span><span class="sxs-lookup"><span data-stu-id="039fe-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="039fe-122"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="039fe-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="039fe-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="039fe-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="039fe-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="039fe-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="039fe-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="039fe-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="039fe-126">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="039fe-126">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="039fe-127">**Selection-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="039fe-127">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="039fe-128">**InkRectangle-Klasse**</span><span class="sxs-lookup"><span data-stu-id="039fe-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 




