---
description: Tritt ein, wenn die Größe der aktuellen Auswahl geändert wird, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und-Einfügen-Prozeduren oder von der Selection-Eigenschaft.
ms.assetid: 7fe0249c-c43d-498b-9029-cf5969201d96
title: InkOverlay. selectionresisierungsereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7debb9461aae39c0549bce863a0513b86c53ffa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217675"
---
# <a name="inkoverlayselectionresizing-event"></a><span data-ttu-id="b8c9e-103">InkOverlay. selectionresiup-Ereignis</span><span class="sxs-lookup"><span data-stu-id="b8c9e-103">InkOverlay.SelectionResizing event</span></span>

<span data-ttu-id="b8c9e-104">Tritt ein, wenn die Größe der aktuellen Auswahl geändert wird, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und-Einfügen-Prozeduren oder von der [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b8c9e-104">Occurs when the size of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8c9e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8c9e-105">Syntax</span></span>


```C++
void SelectionResizing(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="b8c9e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8c9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8c9e-107">*Cursor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8c9e-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8c9e-108">Das umgebende Rechteck der Auswahl nach dem **selectionresiup** -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="b8c9e-108">The bounding rectangle of the selection after the **SelectionResizing** event.</span></span>

> [!Note]  
> <span data-ttu-id="b8c9e-109">Dieses Rechteck wird in Client Fenster Koordinaten angegeben, das Szenarien wie das Beibehalten des Seitenverhältnisses bei der Größenänderung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="b8c9e-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8c9e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8c9e-110">Return value</span></span>

<span data-ttu-id="b8c9e-111">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b8c9e-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8c9e-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8c9e-112">Remarks</span></span>

<span data-ttu-id="b8c9e-113">Diese Ereignismethode wird in den \_ Dispatch-only-Schnittstellen iinkoverlayevents und \_ iinkpictureevents (Dispinterfaces) mit der ID DISPID \_ ioeselectionresiup definiert.</span><span class="sxs-lookup"><span data-stu-id="b8c9e-113">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResizing.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8c9e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8c9e-114">Requirements</span></span>



| <span data-ttu-id="b8c9e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8c9e-115">Requirement</span></span> | <span data-ttu-id="b8c9e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b8c9e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8c9e-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b8c9e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b8c9e-118">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8c9e-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b8c9e-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b8c9e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b8c9e-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b8c9e-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="b8c9e-121">Header</span><span class="sxs-lookup"><span data-stu-id="b8c9e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8c9e-122"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b8c9e-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b8c9e-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b8c9e-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="b8c9e-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8c9e-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="b8c9e-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8c9e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8c9e-126">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b8c9e-126">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="b8c9e-127">**Auswahl Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="b8c9e-127">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="b8c9e-128">**Inkrechteck-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b8c9e-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 




