---
title: LB_SETITEMHEIGHT Meldung (Winuser. h)
description: Legt die Höhe von Elementen in einem Listenfeld in Pixel fest. Wenn das Listenfeld den lbs-Besitzer für das- \_ Objekt aufweist, legt diese Meldung die Höhe des durch den wParam-Parameter angegebenen Elements fest. Andernfalls legt diese Meldung die Höhe aller Elemente im Listenfeld fest.
ms.assetid: 3ac8e935-6de8-465f-a525-1f493b06ee7c
keywords:
- Windows-Steuerelemente für LB_SETITEMHEIGHT Meldung
topic_type:
- apiref
api_name:
- LB_SETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9985c5131a9eb1c8f0c45b6ab399b9e270f962cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478540"
---
# <a name="lb_setitemheight-message"></a><span data-ttu-id="a8313-106">LB- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="a8313-106">LB\_SETITEMHEIGHT message</span></span>

<span data-ttu-id="a8313-107">Legt die Höhe von Elementen in einem Listenfeld in Pixel fest.</span><span class="sxs-lookup"><span data-stu-id="a8313-107">Sets the height, in pixels, of items in a list box.</span></span> <span data-ttu-id="a8313-108">Wenn das Listenfeld den [**lbs- \_**](list-box-styles.md) Besitzer für das-Objekt aufweist, legt diese Meldung die Höhe des durch den *wParam* -Parameter angegebenen Elements fest.</span><span class="sxs-lookup"><span data-stu-id="a8313-108">If the list box has the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style, this message sets the height of the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="a8313-109">Andernfalls legt diese Meldung die Höhe aller Elemente im Listenfeld fest.</span><span class="sxs-lookup"><span data-stu-id="a8313-109">Otherwise, this message sets the height of all items in the list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="a8313-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8313-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8313-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a8313-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8313-112">Gibt den NULL basierten Index des Elements im Listenfeld an.</span><span class="sxs-lookup"><span data-stu-id="a8313-112">Specifies the zero-based index of the item in the list box.</span></span> <span data-ttu-id="a8313-113">Verwenden Sie diesen Parameter nur, wenn das Listenfeld [**den \_ lbs**](list-box-styles.md) -Besitzer des "lbs"-Stils aufweist. andernfalls legen Sie es auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="a8313-113">Use this parameter only if the list box has the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style; otherwise, set it to zero.</span></span>

<span data-ttu-id="a8313-114">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt.</span><span class="sxs-lookup"><span data-stu-id="a8313-114">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="a8313-115">Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen.</span><span class="sxs-lookup"><span data-stu-id="a8313-115">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="a8313-116">Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.</span><span class="sxs-lookup"><span data-stu-id="a8313-116">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="a8313-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8313-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8313-118">Gibt die Höhe des Elements in Pixel an.</span><span class="sxs-lookup"><span data-stu-id="a8313-118">Specifies the height, in pixels, of the item.</span></span> <span data-ttu-id="a8313-119">Die maximale Höhe beträgt 255 Pixel.</span><span class="sxs-lookup"><span data-stu-id="a8313-119">The maximum height is 255 pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8313-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8313-120">Return value</span></span>

<span data-ttu-id="a8313-121">Wenn der Index oder die Höhe ungültig ist, ist der Rückgabewert lb \_ Err.</span><span class="sxs-lookup"><span data-stu-id="a8313-121">If the index or height is invalid, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8313-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8313-122">Requirements</span></span>



| <span data-ttu-id="a8313-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8313-123">Requirement</span></span> | <span data-ttu-id="a8313-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a8313-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8313-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8313-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a8313-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8313-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a8313-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8313-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a8313-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8313-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a8313-129">Header</span><span class="sxs-lookup"><span data-stu-id="a8313-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8313-130"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="a8313-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8313-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8313-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8313-132">**LB- \_ GetItemHeight**</span><span class="sxs-lookup"><span data-stu-id="a8313-132">**LB\_GETITEMHEIGHT**</span></span>](lb-getitemheight.md)
</dt> </dl>

 

 





