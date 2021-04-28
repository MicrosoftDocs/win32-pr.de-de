---
description: 'InkPicture.SelectionMoving-Ereignis: Tritt ein, wenn sich die Position der aktuellen Auswahl ändert, z. B. durch Änderungen an der Benutzeroberfläche, Ausschneide- und Einfügeprozeduren oder die Selection-Eigenschaft.'
ms.assetid: 310003a1-f282-4efa-9a75-c575a9193a77
title: InkPicture.SelectionMoving-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eee50fe1115ce72dff0674ad4e6c2457500c7de8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086458"
---
# <a name="inkpictureselectionmoving-event"></a><span data-ttu-id="81ee6-103">InkPicture.SelectionMoving-Ereignis</span><span class="sxs-lookup"><span data-stu-id="81ee6-103">InkPicture.SelectionMoving event</span></span>

<span data-ttu-id="81ee6-104">Tritt ein, wenn sich die Position der aktuellen Auswahl ändert, z. B. durch Änderungen [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) an der Benutzeroberfläche, Prozeduren zum Ausschneiden und Einfügen oder die Selection-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="81ee6-104">Occurs when the position of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="81ee6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="81ee6-105">Syntax</span></span>


```C++
void SelectionMoving(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="81ee6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="81ee6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81ee6-107">*CurSelectionRect* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="81ee6-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81ee6-108">Das Rechteck, in das die Auswahl nach dem **SelectionMoving-Ereignis** verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="81ee6-108">The rectangle to which the selection is moved after the **SelectionMoving** event.</span></span>

> [!Note]  
> <span data-ttu-id="81ee6-109">Dieses Rechteck wird in Clientfensterkoordinaten angegeben, was Szenarien wie das Beibehalten des Seitenverhältnisses bei der Größenänderung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="81ee6-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81ee6-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81ee6-110">Return value</span></span>

<span data-ttu-id="81ee6-111">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="81ee6-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="81ee6-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81ee6-112">Remarks</span></span>

<span data-ttu-id="81ee6-113">Diese Ereignismethode wird in den Dispatch-only-Schnittstellen **\_ IInkOverlayEvents** und **\_ IInkPictureEvents** (dispinterfaces) mit der ID DISPID \_ IOESelectionMoving definiert.</span><span class="sxs-lookup"><span data-stu-id="81ee6-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionMoving.</span></span>

## <a name="requirements"></a><span data-ttu-id="81ee6-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81ee6-114">Requirements</span></span>



| <span data-ttu-id="81ee6-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81ee6-115">Requirement</span></span> | <span data-ttu-id="81ee6-116">Wert</span><span class="sxs-lookup"><span data-stu-id="81ee6-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81ee6-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="81ee6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="81ee6-118">Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="81ee6-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="81ee6-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="81ee6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="81ee6-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="81ee6-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="81ee6-121">Header</span><span class="sxs-lookup"><span data-stu-id="81ee6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="81ee6-122"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="81ee6-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="81ee6-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="81ee6-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="81ee6-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81ee6-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="81ee6-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="81ee6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81ee6-126">Inkpicture</span><span class="sxs-lookup"><span data-stu-id="81ee6-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="81ee6-127">[**Selection Property \[ InkPicture-Steuerelement\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="81ee6-127">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="81ee6-128">**InkRectangle-Klasse**</span><span class="sxs-lookup"><span data-stu-id="81ee6-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 




