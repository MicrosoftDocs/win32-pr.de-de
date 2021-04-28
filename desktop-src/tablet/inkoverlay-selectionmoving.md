---
description: 'InkOverlay.SelectionMoving-Ereignis: Tritt ein, wenn sich die Position der aktuellen Auswahl ändert, z. B. durch Änderungen an der Benutzeroberfläche, Ausschneide- und Einfügeprozessen oder die Selection-Eigenschaft.'
ms.assetid: 7cd7a5b1-4ae6-4038-afd0-6ef9d0700938
title: InkOverlay.SelectionMoving-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ee4784e6b4c475c30d9b2a3ab30fe166ea3d67d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086698"
---
# <a name="inkoverlayselectionmoving-event"></a><span data-ttu-id="0119e-103">InkOverlay.SelectionMoving-Ereignis</span><span class="sxs-lookup"><span data-stu-id="0119e-103">InkOverlay.SelectionMoving event</span></span>

<span data-ttu-id="0119e-104">Tritt ein, wenn sich die Position der aktuellen Auswahl ändert, z. B. durch Änderungen [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) an der Benutzeroberfläche, Prozeduren zum Ausschneiden und Einfügen oder die Selection-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0119e-104">Occurs when the position of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="0119e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0119e-105">Syntax</span></span>


```C++
void SelectionMoving(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="0119e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0119e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0119e-107">*CurSelectionRect* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="0119e-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0119e-108">Das Rechteck, in das die Auswahl nach dem **SelectionMoving-Ereignis** verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="0119e-108">The rectangle to which the selection is moved after the **SelectionMoving** event.</span></span>

> [!Note]  
> <span data-ttu-id="0119e-109">Dieses Rechteck wird in Clientfensterkoordinaten angegeben, was Szenarien wie die Beibehaltung des Seitenverhältnisses bei der Größenänderung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="0119e-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0119e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0119e-110">Return value</span></span>

<span data-ttu-id="0119e-111">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0119e-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0119e-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0119e-112">Remarks</span></span>

<span data-ttu-id="0119e-113">Diese Ereignismethode wird in den \_ Dispatch-only-Schnittstellen IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit einer ID aus DISPID \_ IOESelectionMoving definiert.</span><span class="sxs-lookup"><span data-stu-id="0119e-113">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID off DISPID\_IOESelectionMoving.</span></span>

## <a name="requirements"></a><span data-ttu-id="0119e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0119e-114">Requirements</span></span>



| <span data-ttu-id="0119e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0119e-115">Requirement</span></span> | <span data-ttu-id="0119e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0119e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0119e-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0119e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0119e-118">Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0119e-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="0119e-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0119e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0119e-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0119e-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="0119e-121">Header</span><span class="sxs-lookup"><span data-stu-id="0119e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0119e-122"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="0119e-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0119e-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0119e-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="0119e-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0119e-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="0119e-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0119e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0119e-126">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0119e-126">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="0119e-127">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0119e-127">**InkOverlay Class**</span></span>
</dt> <dt>

[<span data-ttu-id="0119e-128">**Selection-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="0119e-128">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="0119e-129">**InkRectangle-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0119e-129">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 




