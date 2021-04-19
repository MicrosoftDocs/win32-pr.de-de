---
description: Tritt auf, wenn sich die Größe der aktuellen Auswahl geändert hat, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und einfügeprozeduren oder von der Selection-Eigenschaft.
ms.assetid: 4e7f461f-2909-40ab-98d8-b763d489eb62
title: InkPicture. SelectionResized-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b90e04533e3551fd4e1ba4ac661d8060377e6d06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360818"
---
# <a name="inkpictureselectionresized-event"></a><span data-ttu-id="0bb4e-103">InkPicture. SelectionResized-Ereignis</span><span class="sxs-lookup"><span data-stu-id="0bb4e-103">InkPicture.SelectionResized event</span></span>

<span data-ttu-id="0bb4e-104">Tritt auf, wenn sich die Größe der aktuellen Auswahl geändert hat, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und einfügeprozeduren oder von der [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0bb4e-104">Occurs when the size of the current selection has changed, for example through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bb4e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0bb4e-105">Syntax</span></span>


```C++
void SelectionResized(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="0bb4e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0bb4e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bb4e-107">*Oldselectionrect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0bb4e-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bb4e-108">Das umgebende Rechteck der ausgewählten [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung, wie es vorhanden war, bevor das **SelectionResized** -Ereignis ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="0bb4e-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionResized** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="0bb4e-109">Dieses Rechteck wird in Freihand Raumkoordinaten angegeben, die rückgängig-Szenarien ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="0bb4e-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bb4e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0bb4e-110">Return value</span></span>

<span data-ttu-id="0bb4e-111">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0bb4e-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bb4e-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0bb4e-112">Remarks</span></span>

<span data-ttu-id="0bb4e-113">Diese Ereignismethode wird in den Dispatch-only-Schnittstellen **\_ iinkoverlayevents** und **\_ iinkpictureevents** (Dispinterfaces) mit der ID DISPID \_ ioeselectionresized definiert.</span><span class="sxs-lookup"><span data-stu-id="0bb4e-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResized.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bb4e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0bb4e-114">Requirements</span></span>



| <span data-ttu-id="0bb4e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0bb4e-115">Requirement</span></span> | <span data-ttu-id="0bb4e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0bb4e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bb4e-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0bb4e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0bb4e-118">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0bb4e-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="0bb4e-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0bb4e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0bb4e-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0bb4e-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="0bb4e-121">Header</span><span class="sxs-lookup"><span data-stu-id="0bb4e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bb4e-122"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0bb4e-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0bb4e-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0bb4e-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="0bb4e-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bb4e-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="0bb4e-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0bb4e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bb4e-126">InkPicture</span><span class="sxs-lookup"><span data-stu-id="0bb4e-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="0bb4e-127">[**Bild-Steuerelement für Auswahl Eigenschaften \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="0bb4e-127">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="0bb4e-128">**Inkrechteck-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0bb4e-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

