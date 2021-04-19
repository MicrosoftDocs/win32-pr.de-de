---
description: Tritt auf, wenn sich die Auswahl von frei Hand Eingaben innerhalb des InkPicture-Steuer Elements geändert hat, z. b. durch Änderungen an der Benutzeroberfläche, Ausschneide-und Einfüge Prozeduren oder die Auswahl Eigenschaft.
ms.assetid: e300ec91-e8f3-473f-b526-efeafafaa32a
title: InkPicture. SelectionChanged-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14594efe4e5ecda64167ec9a0e075fc60d8e9a19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369827"
---
# <a name="inkpictureselectionchanged-event"></a><span data-ttu-id="1d730-103">InkPicture. SelectionChanged-Ereignis</span><span class="sxs-lookup"><span data-stu-id="1d730-103">InkPicture.SelectionChanged event</span></span>

<span data-ttu-id="1d730-104">Tritt auf, wenn sich die Auswahl von frei Hand Eingaben innerhalb des [InkPicture](inkpicture-control-reference.md) -Steuer Elements geändert hat, z. b. durch Änderungen an der Benutzeroberfläche, Ausschneide-und Einfüge Prozeduren oder die [**Auswahl**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1d730-104">Occurs when the selection of ink within the [InkPicture](inkpicture-control-reference.md) control has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d730-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d730-105">Syntax</span></span>


```C++
void SelectionChanged();
```



## <a name="parameters"></a><span data-ttu-id="1d730-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d730-106">Parameters</span></span>

<span data-ttu-id="1d730-107">Dieses Ereignis weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="1d730-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1d730-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d730-108">Return value</span></span>

<span data-ttu-id="1d730-109">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1d730-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d730-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d730-110">Remarks</span></span>

<span data-ttu-id="1d730-111">Weitere Informationen zu diesem Ereignis finden Sie unter dem [**SelectionChanged**](inkoverlay-selectionchanged.md) -Ereignis des [**InkOverlay**](inkoverlay-class.md) -Objekts, das über die gleiche Funktionalität verfügt.</span><span class="sxs-lookup"><span data-stu-id="1d730-111">For further details about this event, refer to the [**InkOverlay**](inkoverlay-class.md) object's [**SelectionChanged**](inkoverlay-selectionchanged.md) event, which has the same functionality.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d730-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d730-112">Requirements</span></span>



| <span data-ttu-id="1d730-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d730-113">Requirement</span></span> | <span data-ttu-id="1d730-114">Wert</span><span class="sxs-lookup"><span data-stu-id="1d730-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d730-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d730-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1d730-116">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d730-116">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1d730-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d730-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1d730-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1d730-118">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="1d730-119">Header</span><span class="sxs-lookup"><span data-stu-id="1d730-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d730-120"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1d730-120"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1d730-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1d730-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="1d730-122"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d730-122"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="1d730-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d730-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d730-124">InkPicture</span><span class="sxs-lookup"><span data-stu-id="1d730-124">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="1d730-125">[**Bild-Steuerelement für Auswahl Eigenschaften \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="1d730-125">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> </dl>

 

 




