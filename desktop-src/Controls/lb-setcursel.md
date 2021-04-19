---
title: LB_SETCURSEL Meldung (Winuser. h)
description: Wählt eine Zeichenfolge aus und führt ggf. einen Bildlauf in die Ansicht aus. Wenn die neue Zeichenfolge ausgewählt ist, wird die Hervorhebung im Listenfeld aus der zuvor ausgewählten Zeichenfolge entfernt.
ms.assetid: 28d81f9d-a926-400c-8803-dcdb0e8f193d
keywords:
- Windows-Steuerelemente für LB_SETCURSEL Meldung
topic_type:
- apiref
api_name:
- LB_SETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77d1305ccece9c220d6a20e72e0ee54a428f8b13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344702"
---
# <a name="lb_setcursel-message"></a><span data-ttu-id="84955-105">LB- \_ setcurrsel-Nachricht</span><span class="sxs-lookup"><span data-stu-id="84955-105">LB\_SETCURSEL message</span></span>

<span data-ttu-id="84955-106">Wählt eine Zeichenfolge aus und führt ggf. einen Bildlauf in die Ansicht aus.</span><span class="sxs-lookup"><span data-stu-id="84955-106">Selects a string and scrolls it into view, if necessary.</span></span> <span data-ttu-id="84955-107">Wenn die neue Zeichenfolge ausgewählt ist, wird die Hervorhebung im Listenfeld aus der zuvor ausgewählten Zeichenfolge entfernt.</span><span class="sxs-lookup"><span data-stu-id="84955-107">When the new string is selected, the list box removes the highlight from the previously selected string.</span></span>

## <a name="parameters"></a><span data-ttu-id="84955-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="84955-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84955-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="84955-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="84955-110">Gibt den NULL basierten Index der ausgewählten Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="84955-110">Specifies the zero-based index of the string that is selected.</span></span> <span data-ttu-id="84955-111">Wenn dieser Parameter-1 ist, wird für das Listenfeld festgelegt, dass keine Auswahl vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="84955-111">If this parameter is -1, the list box is set to have no selection.</span></span>

<span data-ttu-id="84955-112">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt.</span><span class="sxs-lookup"><span data-stu-id="84955-112">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="84955-113">Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen.</span><span class="sxs-lookup"><span data-stu-id="84955-113">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="84955-114">Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.</span><span class="sxs-lookup"><span data-stu-id="84955-114">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="84955-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="84955-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="84955-116">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="84955-116">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84955-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="84955-117">Return value</span></span>

<span data-ttu-id="84955-118">Wenn ein Fehler auftritt, ist der Rückgabewert lb \_ Err.</span><span class="sxs-lookup"><span data-stu-id="84955-118">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="84955-119">Wenn der *wParam* -Parameter-1 ist, ist der Rückgabewert "lb err", obwohl \_ kein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="84955-119">If the *wParam* parameter is -1, the return value is LB\_ERR even though no error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="84955-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84955-120">Remarks</span></span>

<span data-ttu-id="84955-121">Verwenden Sie diese Meldung nur für Listenfelder mit einfacher Auswahl.</span><span class="sxs-lookup"><span data-stu-id="84955-121">Use this message only with single-selection list boxes.</span></span> <span data-ttu-id="84955-122">Sie können Sie nicht verwenden, um eine Auswahl in einem Listenfeld mit Mehrfachauswahl festzulegen oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="84955-122">You cannot use it to set or remove a selection in a multiple-selection list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="84955-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84955-123">Requirements</span></span>



| <span data-ttu-id="84955-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84955-124">Requirement</span></span> | <span data-ttu-id="84955-125">Wert</span><span class="sxs-lookup"><span data-stu-id="84955-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84955-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="84955-126">Minimum supported client</span></span><br/> | <span data-ttu-id="84955-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84955-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="84955-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="84955-128">Minimum supported server</span></span><br/> | <span data-ttu-id="84955-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84955-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="84955-130">Header</span><span class="sxs-lookup"><span data-stu-id="84955-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="84955-131"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="84955-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84955-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84955-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84955-133">**LB- \_ getcurrsel**</span><span class="sxs-lookup"><span data-stu-id="84955-133">**LB\_GETCURSEL**</span></span>](lb-getcursel.md)
</dt> </dl>

 

 





