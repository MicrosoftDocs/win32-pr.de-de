---
description: Tritt auf, wenn sich die Auswahl von frei Hand Eingaben innerhalb des-Steuer Elements geändert hat, z. b. durch Änderungen an der Benutzeroberfläche, Ausschneide-und Einfüge Prozeduren oder die Selection-Eigenschaft
ms.assetid: 6b4cd9fe-b09f-4a70-9aa5-92ef9409ff1b
title: InkOverlay. SelectionChanged-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997e0c8e9620b0a269ff8cd97ff04aa3abfb1df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366173"
---
# <a name="inkoverlayselectionchanged-event"></a><span data-ttu-id="15e86-103">InkOverlay. SelectionChanged-Ereignis</span><span class="sxs-lookup"><span data-stu-id="15e86-103">InkOverlay.SelectionChanged event</span></span>

<span data-ttu-id="15e86-104">Tritt auf, wenn sich die Auswahl von frei Hand Eingaben innerhalb des-Steuer Elements geändert hat, z. b. durch Änderungen an der Benutzeroberfläche, Ausschneide-und Einfüge Prozeduren oder die [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="15e86-104">Occurs when the selection of ink within the control has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="15e86-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="15e86-105">Syntax</span></span>


```C++
void SelectionChanged();
```



## <a name="parameters"></a><span data-ttu-id="15e86-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="15e86-106">Parameters</span></span>

<span data-ttu-id="15e86-107">Dieses Ereignis weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="15e86-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="15e86-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="15e86-108">Return value</span></span>

<span data-ttu-id="15e86-109">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="15e86-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="15e86-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15e86-110">Remarks</span></span>

<span data-ttu-id="15e86-111">Es sind keine Ereignisdaten vorhanden.</span><span class="sxs-lookup"><span data-stu-id="15e86-111">There are no event data.</span></span>

<span data-ttu-id="15e86-112">Diese Ereignismethode wird in den \_ Dispatch-only-Schnittstellen iinkoverlayevents und \_ iinkpictureevents (Dispinterfaces) mit der ID DISPID \_ ioeselectionchanged definiert.</span><span class="sxs-lookup"><span data-stu-id="15e86-112">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionChanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="15e86-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15e86-113">Requirements</span></span>



| <span data-ttu-id="15e86-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15e86-114">Requirement</span></span> | <span data-ttu-id="15e86-115">Wert</span><span class="sxs-lookup"><span data-stu-id="15e86-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15e86-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="15e86-116">Minimum supported client</span></span><br/> | <span data-ttu-id="15e86-117">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15e86-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="15e86-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="15e86-118">Minimum supported server</span></span><br/> | <span data-ttu-id="15e86-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="15e86-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="15e86-120">Header</span><span class="sxs-lookup"><span data-stu-id="15e86-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="15e86-121"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="15e86-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="15e86-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="15e86-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="15e86-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15e86-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="15e86-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15e86-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15e86-125">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="15e86-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="15e86-126">**Auswahl Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="15e86-126">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> </dl>

 

 




