---
description: Tritt auf, wenn sich die Position der aktuellen Auswahl geändert hat, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und einfügeprozeduren oder von der Selection-Eigenschaft.
ms.assetid: 669dc6c2-1620-40f3-b4b5-7ab8967e739a
title: InkPicture. selectionverschogereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25810b87d5a0a3554c46b1a3869bb9b6c88d2fb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346878"
---
# <a name="inkpictureselectionmoved-event"></a><span data-ttu-id="fb3ab-103">InkPicture. selectionverschogereignis</span><span class="sxs-lookup"><span data-stu-id="fb3ab-103">InkPicture.SelectionMoved event</span></span>

<span data-ttu-id="fb3ab-104">Tritt auf, wenn sich die Position der aktuellen Auswahl geändert hat, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und einfügeprozeduren oder von der [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="fb3ab-104">Occurs when the position of the current selection has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb3ab-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb3ab-105">Syntax</span></span>


```C++
void SelectionMoved(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="fb3ab-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb3ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb3ab-107">*Oldselectionrect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb3ab-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb3ab-108">Das umschließende Rechteck der ausgewählten [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung, wie es vor dem Auslösen des **selectionverschochereignisses** vorhanden war.</span><span class="sxs-lookup"><span data-stu-id="fb3ab-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionMoved** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="fb3ab-109">Dieses Rechteck wird in Freihand Raumkoordinaten angegeben, die rückgängig-Szenarien ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="fb3ab-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb3ab-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb3ab-110">Return value</span></span>

<span data-ttu-id="fb3ab-111">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fb3ab-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb3ab-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb3ab-112">Remarks</span></span>

<span data-ttu-id="fb3ab-113">Diese Ereignismethode wird in den Dispatch-only-Schnittstellen **\_ iinkoverlayevents** und **\_ iinkpictureevents** (Dispinterfaces) mit der ID DISPID \_ ioeselectionverschot definiert.</span><span class="sxs-lookup"><span data-stu-id="fb3ab-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionMoved.</span></span>

<span data-ttu-id="fb3ab-114">Zum Abrufen des neuen umgebenden Rechtecks der Auflistung von Strichen, die verschoben wurden, müssen Sie die [**Selection. GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fb3ab-114">To get the new bounding rectangle of the collection of strokes that have been moved, call the [**Selection.GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb3ab-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb3ab-115">Requirements</span></span>



| <span data-ttu-id="fb3ab-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb3ab-116">Requirement</span></span> | <span data-ttu-id="fb3ab-117">Wert</span><span class="sxs-lookup"><span data-stu-id="fb3ab-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb3ab-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fb3ab-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fb3ab-119">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb3ab-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="fb3ab-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fb3ab-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fb3ab-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fb3ab-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="fb3ab-122">Header</span><span class="sxs-lookup"><span data-stu-id="fb3ab-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb3ab-123"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fb3ab-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fb3ab-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fb3ab-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="fb3ab-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb3ab-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="fb3ab-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb3ab-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb3ab-127">InkPicture</span><span class="sxs-lookup"><span data-stu-id="fb3ab-127">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="fb3ab-128">[**Bild-Steuerelement für Auswahl Eigenschaften \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="fb3ab-128">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="fb3ab-129">**Inkrechteck-Klasse**</span><span class="sxs-lookup"><span data-stu-id="fb3ab-129">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

