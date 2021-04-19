---
description: Tritt auf, wenn die Auswahl von frei Hand Eingaben innerhalb des-Steuer Elements geändert wird, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und Einfüge Prozeduren oder von der Selection-Eigenschaft.
ms.assetid: dffdb183-d363-40d3-81a2-d496433f7075
title: InkOverlay. SelectionChanging-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e830a9ea97f6722dd8ab9bdb782e4ae4ac5f44fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364173"
---
# <a name="inkoverlayselectionchanging-event"></a><span data-ttu-id="95b1a-103">InkOverlay. SelectionChanging-Ereignis</span><span class="sxs-lookup"><span data-stu-id="95b1a-103">InkOverlay.SelectionChanging event</span></span>

<span data-ttu-id="95b1a-104">Tritt auf, wenn die Auswahl von frei Hand Eingaben innerhalb des-Steuer Elements geändert wird, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und Einfüge Prozeduren oder von der [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="95b1a-104">Occurs when the selection of ink within the control is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="95b1a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="95b1a-105">Syntax</span></span>


```C++
void SelectionChanging(
  [in] IInkStrokes *NewSelection
);
```



## <a name="parameters"></a><span data-ttu-id="95b1a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="95b1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95b1a-107">*Neuauswahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95b1a-107">*NewSelection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95b1a-108">Die neue Sammlung von [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , die ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="95b1a-108">The new collection of [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) that is being selected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95b1a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95b1a-109">Return value</span></span>

<span data-ttu-id="95b1a-110">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="95b1a-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="95b1a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95b1a-111">Remarks</span></span>

<span data-ttu-id="95b1a-112">Diese Ereignismethode wird in den \_ Dispatch-only-Schnittstellen iinkoverlayevents und \_ iinkpictureevents (Dispinterfaces) mit der ID "DISPID \_ ioeselectionchanging" definiert.</span><span class="sxs-lookup"><span data-stu-id="95b1a-112">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionChanging.</span></span>

## <a name="requirements"></a><span data-ttu-id="95b1a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95b1a-113">Requirements</span></span>



| <span data-ttu-id="95b1a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95b1a-114">Requirement</span></span> | <span data-ttu-id="95b1a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="95b1a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95b1a-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95b1a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="95b1a-117">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95b1a-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="95b1a-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95b1a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="95b1a-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="95b1a-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="95b1a-120">Header</span><span class="sxs-lookup"><span data-stu-id="95b1a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="95b1a-121"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="95b1a-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="95b1a-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="95b1a-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="95b1a-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95b1a-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="95b1a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95b1a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95b1a-125">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="95b1a-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="95b1a-126">**Auswahl Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="95b1a-126">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> </dl>

 

