---
description: 'InkOverlay.SelectionResized-Ereignis: Tritt auf, wenn sich die Größe der aktuellen Auswahl geändert hat, z. B. durch Änderungen an der Benutzeroberfläche, durch Ausschneide- und Einfügevorgänge oder durch die Selection-Eigenschaft.'
ms.assetid: 606d4bdf-b02e-459f-a4cf-050daac6c309
title: InkOverlay.SelectionResized-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f3dd3cf1bdda004733dde99bb66150710044310
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116878"
---
# <a name="inkoverlayselectionresized-event"></a><span data-ttu-id="25bfc-103">InkOverlay.SelectionResized-Ereignis</span><span class="sxs-lookup"><span data-stu-id="25bfc-103">InkOverlay.SelectionResized event</span></span>

<span data-ttu-id="25bfc-104">Tritt ein, wenn sich die Größe der aktuellen Auswahl geändert hat, z. B. durch Änderungen an der Benutzeroberfläche, durch Ausschneide- und Einfügevorgänge oder durch die [**Selection-Eigenschaft.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)</span><span class="sxs-lookup"><span data-stu-id="25bfc-104">Occurs when the size of the current selection has changed, for example through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="25bfc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="25bfc-105">Syntax</span></span>


```C++
void SelectionResized(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="25bfc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="25bfc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25bfc-107">*OldSelectionRect* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="25bfc-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25bfc-108">Das umgebundene Rechteck der ausgewählten [InkStrokes-Auflistung,](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) wie es vor dem **Ausgelösten SelectionResized-Ereignis vorhanden** war.</span><span class="sxs-lookup"><span data-stu-id="25bfc-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionResized** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="25bfc-109">Dieses Rechteck wird in Freiraumkoordinaten angegeben, was Rückgängig-Szenarien ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="25bfc-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25bfc-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="25bfc-110">Return value</span></span>

<span data-ttu-id="25bfc-111">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="25bfc-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="25bfc-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="25bfc-112">Remarks</span></span>

<span data-ttu-id="25bfc-113">Diese Ereignismethode wird in den \_ \_ dispatch-only-Schnittstellen (dispinterfaces) von IInkOverlayEvents und IInkPictureEvents mit der ID DISPID \_ IOESelectionResized definiert.</span><span class="sxs-lookup"><span data-stu-id="25bfc-113">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResized.</span></span>

## <a name="requirements"></a><span data-ttu-id="25bfc-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25bfc-114">Requirements</span></span>



| <span data-ttu-id="25bfc-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25bfc-115">Requirement</span></span> | <span data-ttu-id="25bfc-116">Wert</span><span class="sxs-lookup"><span data-stu-id="25bfc-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25bfc-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="25bfc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="25bfc-118">Nur Desktop-Apps für Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="25bfc-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="25bfc-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="25bfc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="25bfc-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="25bfc-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="25bfc-121">Header</span><span class="sxs-lookup"><span data-stu-id="25bfc-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="25bfc-122"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="25bfc-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="25bfc-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="25bfc-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="25bfc-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25bfc-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="25bfc-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="25bfc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25bfc-126">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="25bfc-126">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="25bfc-127">**Selection-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="25bfc-127">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="25bfc-128">**InkRectangle-Klasse**</span><span class="sxs-lookup"><span data-stu-id="25bfc-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

