---
description: Tritt ein, wenn die Position der aktuellen Auswahl geändert wird, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und-Einfügen-Prozeduren oder von der Selection-Eigenschaft.
ms.assetid: 7cd7a5b1-4ae6-4038-afd0-6ef9d0700938
title: InkOverlay. SelectionMoving-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9afc77198a6a7228e44b3f2bad8015c25a939812
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355340"
---
# <a name="inkoverlayselectionmoving-event"></a><span data-ttu-id="d67a7-103">InkOverlay. SelectionMoving-Ereignis</span><span class="sxs-lookup"><span data-stu-id="d67a7-103">InkOverlay.SelectionMoving event</span></span>

<span data-ttu-id="d67a7-104">Tritt ein, wenn die Position der aktuellen Auswahl geändert wird, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und-Einfügen-Prozeduren oder von der [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d67a7-104">Occurs when the position of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="d67a7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d67a7-105">Syntax</span></span>


```C++
void SelectionMoving(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="d67a7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d67a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d67a7-107">*Cursor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d67a7-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d67a7-108">Das Rechteck, in das die Auswahl nach dem **SelectionMoving** -Ereignis verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="d67a7-108">The rectangle to which the selection is moved after the **SelectionMoving** event.</span></span>

> [!Note]  
> <span data-ttu-id="d67a7-109">Dieses Rechteck wird in Client Fenster Koordinaten angegeben, das Szenarien wie das Beibehalten des Seitenverhältnisses bei der Größenänderung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="d67a7-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d67a7-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d67a7-110">Return value</span></span>

<span data-ttu-id="d67a7-111">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d67a7-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d67a7-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d67a7-112">Remarks</span></span>

<span data-ttu-id="d67a7-113">Diese Ereignismethode wird in den \_ Dispatch-only-Schnittstellen iinkoverlayevents und \_ iinkpictureevents (Dispinterfaces) mit einer ID aus DISPID \_ ioeselectionmoving definiert.</span><span class="sxs-lookup"><span data-stu-id="d67a7-113">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID off DISPID\_IOESelectionMoving.</span></span>

## <a name="requirements"></a><span data-ttu-id="d67a7-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d67a7-114">Requirements</span></span>



| <span data-ttu-id="d67a7-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d67a7-115">Requirement</span></span> | <span data-ttu-id="d67a7-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d67a7-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d67a7-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d67a7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d67a7-118">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d67a7-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d67a7-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d67a7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d67a7-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d67a7-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d67a7-121">Header</span><span class="sxs-lookup"><span data-stu-id="d67a7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d67a7-122"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d67a7-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d67a7-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d67a7-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="d67a7-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d67a7-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d67a7-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d67a7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d67a7-126">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d67a7-126">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="d67a7-127">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d67a7-127">**InkOverlay Class**</span></span>
</dt> <dt>

[<span data-ttu-id="d67a7-128">**Auswahl Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="d67a7-128">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="d67a7-129">**Inkrechteck-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d67a7-129">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 




