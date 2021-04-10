---
description: Tritt ein, wenn die Position der aktuellen Auswahl geändert wird, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und-Einfügen-Prozeduren oder von der Selection-Eigenschaft.
ms.assetid: 310003a1-f282-4efa-9a75-c575a9193a77
title: InkPicture. SelectionMoving-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2dbc0064e22f21faf80d67f51ca1eeb58b6433
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050445"
---
# <a name="inkpictureselectionmoving-event"></a><span data-ttu-id="b2c74-103">InkPicture. SelectionMoving-Ereignis</span><span class="sxs-lookup"><span data-stu-id="b2c74-103">InkPicture.SelectionMoving event</span></span>

<span data-ttu-id="b2c74-104">Tritt ein, wenn die Position der aktuellen Auswahl geändert wird, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und-Einfügen-Prozeduren oder von der [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b2c74-104">Occurs when the position of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2c74-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2c74-105">Syntax</span></span>


```C++
void SelectionMoving(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="b2c74-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2c74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2c74-107">*Cursor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2c74-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2c74-108">Das Rechteck, in das die Auswahl nach dem **SelectionMoving** -Ereignis verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="b2c74-108">The rectangle to which the selection is moved after the **SelectionMoving** event.</span></span>

> [!Note]  
> <span data-ttu-id="b2c74-109">Dieses Rechteck wird in Client Fenster Koordinaten angegeben, das Szenarien wie das Beibehalten des Seitenverhältnisses bei der Größenänderung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="b2c74-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2c74-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b2c74-110">Return value</span></span>

<span data-ttu-id="b2c74-111">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b2c74-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2c74-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2c74-112">Remarks</span></span>

<span data-ttu-id="b2c74-113">Diese Ereignismethode wird in den Dispatch-only-Schnittstellen **\_ iinkoverlayevents** und **\_ iinkpictureevents** (Dispinterfaces) mit der ID DISPID \_ ioeselectionmoving definiert.</span><span class="sxs-lookup"><span data-stu-id="b2c74-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionMoving.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2c74-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2c74-114">Requirements</span></span>



| <span data-ttu-id="b2c74-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2c74-115">Requirement</span></span> | <span data-ttu-id="b2c74-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b2c74-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2c74-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b2c74-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b2c74-118">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b2c74-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b2c74-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b2c74-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b2c74-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b2c74-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="b2c74-121">Header</span><span class="sxs-lookup"><span data-stu-id="b2c74-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2c74-122"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b2c74-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b2c74-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b2c74-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="b2c74-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2c74-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="b2c74-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2c74-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2c74-126">InkPicture</span><span class="sxs-lookup"><span data-stu-id="b2c74-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="b2c74-127">[**Bild-Steuerelement für Auswahl Eigenschaften \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="b2c74-127">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="b2c74-128">**Inkrechteck-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b2c74-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 




