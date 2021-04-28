---
description: 'InkPicture.SelectionResized-Ereignis: Tritt auf, wenn sich die Größe der aktuellen Auswahl geändert hat, z. B. durch Änderungen an der Benutzeroberfläche, Ausschneide- und Einfügeprozeduren oder die Selection-Eigenschaft.'
ms.assetid: 4e7f461f-2909-40ab-98d8-b763d489eb62
title: InkPicture.SelectionResized-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dcad4b84cd21ee9b4d385f24033c56913765810
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086468"
---
# <a name="inkpictureselectionresized-event"></a><span data-ttu-id="878e5-103">InkPicture.SelectionResized-Ereignis</span><span class="sxs-lookup"><span data-stu-id="878e5-103">InkPicture.SelectionResized event</span></span>

<span data-ttu-id="878e5-104">Tritt ein, wenn sich die Größe der aktuellen Auswahl geändert hat, z. B. [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) durch Änderungen an der Benutzeroberfläche, Prozeduren zum Ausschneiden und Einfügen oder die Selection-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="878e5-104">Occurs when the size of the current selection has changed, for example through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="878e5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="878e5-105">Syntax</span></span>


```C++
void SelectionResized(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="878e5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="878e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="878e5-107">*OldSelectionRect* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="878e5-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="878e5-108">Das umschließende Rechteck der ausgewählten [InkStrokes-Auflistung,](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) wie es vor dem **Ausgelösten SelectionResized-Ereignis** vorhanden war.</span><span class="sxs-lookup"><span data-stu-id="878e5-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionResized** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="878e5-109">Dieses Rechteck wird in Freihandraumkoordinaten angegeben, was Rückgängig-Szenarien ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="878e5-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="878e5-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="878e5-110">Return value</span></span>

<span data-ttu-id="878e5-111">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="878e5-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="878e5-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="878e5-112">Remarks</span></span>

<span data-ttu-id="878e5-113">Diese Ereignismethode wird in den Dispatch-only-Schnittstellen **\_ IInkOverlayEvents** und **\_ IInkPictureEvents** (dispinterfaces) mit der ID DISPID \_ IOESelectionResized definiert.</span><span class="sxs-lookup"><span data-stu-id="878e5-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResized.</span></span>

## <a name="requirements"></a><span data-ttu-id="878e5-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="878e5-114">Requirements</span></span>



| <span data-ttu-id="878e5-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="878e5-115">Requirement</span></span> | <span data-ttu-id="878e5-116">Wert</span><span class="sxs-lookup"><span data-stu-id="878e5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="878e5-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="878e5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="878e5-118">Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="878e5-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="878e5-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="878e5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="878e5-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="878e5-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="878e5-121">Header</span><span class="sxs-lookup"><span data-stu-id="878e5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="878e5-122"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="878e5-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="878e5-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="878e5-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="878e5-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="878e5-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="878e5-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="878e5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="878e5-126">Inkpicture</span><span class="sxs-lookup"><span data-stu-id="878e5-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="878e5-127">[**Selection Property \[ InkPicture-Steuerelement\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="878e5-127">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="878e5-128">**InkRectangle-Klasse**</span><span class="sxs-lookup"><span data-stu-id="878e5-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

