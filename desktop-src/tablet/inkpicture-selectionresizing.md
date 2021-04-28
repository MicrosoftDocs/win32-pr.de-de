---
description: 'InkPicture.SelectionResizing-Ereignis: Tritt ein, wenn sich die Größe der aktuellen Auswahl ändert, z. B. durch Änderungen an der Benutzeroberfläche, Ausschneide- und Einfügeprozeduren oder die Selection-Eigenschaft.'
ms.assetid: da708712-2773-45f5-9d9b-49fabe7fdb5a
title: InkPicture.SelectionResizing-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8f70b0b502fe426cfd94ce9002e8bbfc5260a88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086418"
---
# <a name="inkpictureselectionresizing-event"></a><span data-ttu-id="90872-103">InkPicture.SelectionResizing-Ereignis</span><span class="sxs-lookup"><span data-stu-id="90872-103">InkPicture.SelectionResizing event</span></span>

<span data-ttu-id="90872-104">Tritt ein, wenn sich die Größe der aktuellen Auswahl ändert, z. B. durch Änderungen [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) an der Benutzeroberfläche, Prozeduren zum Ausschneiden und Einfügen oder die Selection-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="90872-104">Occurs when the size of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="90872-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="90872-105">Syntax</span></span>


```C++
void SelectionResizing(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="90872-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="90872-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90872-107">*CurSelectionRect* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="90872-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90872-108">Das umgrenzende Rechteck der Auswahl nach dem **SelectionResizing-Ereignis.**</span><span class="sxs-lookup"><span data-stu-id="90872-108">The bounding rectangle of the selection after the **SelectionResizing** event.</span></span>

> [!Note]  
> <span data-ttu-id="90872-109">Dieses Rechteck wird in Clientfensterkoordinaten angegeben, was Szenarien wie die Beibehaltung des Seitenverhältnisses bei der Größenänderung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="90872-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90872-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="90872-110">Return value</span></span>

<span data-ttu-id="90872-111">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="90872-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="90872-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90872-112">Remarks</span></span>

<span data-ttu-id="90872-113">Diese Ereignismethode wird in den Dispatch-only-Schnittstellen **\_ IInkOverlayEvents** und **\_ IInkPictureEvents** (dispinterfaces) mit der ID DISPID \_ IOESelectionResizing definiert.</span><span class="sxs-lookup"><span data-stu-id="90872-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResizing.</span></span>

## <a name="requirements"></a><span data-ttu-id="90872-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90872-114">Requirements</span></span>



| <span data-ttu-id="90872-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90872-115">Requirement</span></span> | <span data-ttu-id="90872-116">Wert</span><span class="sxs-lookup"><span data-stu-id="90872-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90872-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="90872-117">Minimum supported client</span></span><br/> | <span data-ttu-id="90872-118">Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="90872-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="90872-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="90872-119">Minimum supported server</span></span><br/> | <span data-ttu-id="90872-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="90872-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="90872-121">Header</span><span class="sxs-lookup"><span data-stu-id="90872-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="90872-122"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="90872-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="90872-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="90872-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="90872-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90872-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="90872-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="90872-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90872-126">Inkpicture</span><span class="sxs-lookup"><span data-stu-id="90872-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="90872-127">[**Selection Property \[ InkPicture-Steuerelement\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="90872-127">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="90872-128">**InkRectangle-Klasse**</span><span class="sxs-lookup"><span data-stu-id="90872-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 




