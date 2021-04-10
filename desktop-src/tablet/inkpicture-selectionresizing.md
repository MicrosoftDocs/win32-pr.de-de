---
description: Tritt ein, wenn die Größe der aktuellen Auswahl geändert wird, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und-Einfügen-Prozeduren oder von der Selection-Eigenschaft.
ms.assetid: da708712-2773-45f5-9d9b-49fabe7fdb5a
title: InkPicture. selectionresisierungsereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa1b7923810777c6ebe0af3364121cbcee67b18d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960669"
---
# <a name="inkpictureselectionresizing-event"></a><span data-ttu-id="191bf-103">InkPicture. selectionresierend-Ereignis</span><span class="sxs-lookup"><span data-stu-id="191bf-103">InkPicture.SelectionResizing event</span></span>

<span data-ttu-id="191bf-104">Tritt ein, wenn die Größe der aktuellen Auswahl geändert wird, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und-Einfügen-Prozeduren oder von der [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="191bf-104">Occurs when the size of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="191bf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="191bf-105">Syntax</span></span>


```C++
void SelectionResizing(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="191bf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="191bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="191bf-107">*Cursor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="191bf-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="191bf-108">Das umgebende Rechteck der Auswahl nach dem **selectionresiup** -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="191bf-108">The bounding rectangle of the selection after the **SelectionResizing** event.</span></span>

> [!Note]  
> <span data-ttu-id="191bf-109">Dieses Rechteck wird in Client Fenster Koordinaten angegeben, das Szenarien wie das Beibehalten des Seitenverhältnisses bei der Größenänderung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="191bf-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="191bf-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="191bf-110">Return value</span></span>

<span data-ttu-id="191bf-111">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="191bf-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="191bf-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="191bf-112">Remarks</span></span>

<span data-ttu-id="191bf-113">Diese Ereignismethode wird in den Dispatch-only-Schnittstellen **\_ iinkoverlayevents** und **\_ iinkpictureevents** (Dispinterfaces) mit der ID DISPID \_ ioeselectionresiup definiert.</span><span class="sxs-lookup"><span data-stu-id="191bf-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResizing.</span></span>

## <a name="requirements"></a><span data-ttu-id="191bf-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="191bf-114">Requirements</span></span>



| <span data-ttu-id="191bf-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="191bf-115">Requirement</span></span> | <span data-ttu-id="191bf-116">Wert</span><span class="sxs-lookup"><span data-stu-id="191bf-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="191bf-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="191bf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="191bf-118">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="191bf-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="191bf-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="191bf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="191bf-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="191bf-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="191bf-121">Header</span><span class="sxs-lookup"><span data-stu-id="191bf-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="191bf-122"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="191bf-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="191bf-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="191bf-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="191bf-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="191bf-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="191bf-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="191bf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="191bf-126">InkPicture</span><span class="sxs-lookup"><span data-stu-id="191bf-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="191bf-127">[**Bild-Steuerelement für Auswahl Eigenschaften \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="191bf-127">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="191bf-128">**Inkrechteck-Klasse**</span><span class="sxs-lookup"><span data-stu-id="191bf-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 




