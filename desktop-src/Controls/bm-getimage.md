---
title: BM_GETIMAGE Meldung (Winuser. h)
description: Ruft ein Handle für das Bild (Symbol oder Bitmap) ab, das der Schaltfläche zugeordnet ist.
ms.assetid: 766ea1b0-418d-41b8-b31d-0fcc58e03893
keywords:
- Windows-Steuerelemente für BM_GETIMAGE Meldung
topic_type:
- apiref
api_name:
- BM_GETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9319f5310b40ff76a011e1a06b2be1d41be611f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340968"
---
# <a name="bm_getimage-message"></a><span data-ttu-id="f11f3-104">BM \_ GetImage-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f11f3-104">BM\_GETIMAGE message</span></span>

<span data-ttu-id="f11f3-105">Ruft ein Handle für das Bild (Symbol oder Bitmap) ab, das der Schaltfläche zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f11f3-105">Retrieves a handle to the image (icon or bitmap) associated with the button.</span></span>

## <a name="parameters"></a><span data-ttu-id="f11f3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f11f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f11f3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f11f3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f11f3-108">Der Typ des Bilds, das der Schaltfläche zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f11f3-108">The type of image to associate with the button.</span></span> <span data-ttu-id="f11f3-109">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="f11f3-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="f11f3-110">Wert</span><span class="sxs-lookup"><span data-stu-id="f11f3-110">Value</span></span>                                                                                                                                                      | <span data-ttu-id="f11f3-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f11f3-111">Meaning</span></span>              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <span data-ttu-id="f11f3-112"><dt>**Bild \_ Bitmap**</dt></span><span class="sxs-lookup"><span data-stu-id="f11f3-112"><dt>**IMAGE\_BITMAP**</dt></span></span> </dl> | <span data-ttu-id="f11f3-113">Eine Bitmap.</span><span class="sxs-lookup"><span data-stu-id="f11f3-113">A bitmap.</span></span><br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <span data-ttu-id="f11f3-114"><dt>**Bild \_ Symbol**</dt></span><span class="sxs-lookup"><span data-stu-id="f11f3-114"><dt>**IMAGE\_ICON**</dt></span></span> </dl>       | <span data-ttu-id="f11f3-115">Symbol</span><span class="sxs-lookup"><span data-stu-id="f11f3-115">An icon.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="f11f3-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f11f3-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f11f3-117">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f11f3-117">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f11f3-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f11f3-118">Return value</span></span>

<span data-ttu-id="f11f3-119">Der Rückgabewert ist, sofern vorhanden, ein Handle für das Bild. Andernfalls ist der Wert **null**.</span><span class="sxs-lookup"><span data-stu-id="f11f3-119">The return value is a handle to the image, if any; otherwise, it is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f11f3-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f11f3-120">Requirements</span></span>



| <span data-ttu-id="f11f3-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f11f3-121">Requirement</span></span> | <span data-ttu-id="f11f3-122">Wert</span><span class="sxs-lookup"><span data-stu-id="f11f3-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f11f3-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f11f3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f11f3-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f11f3-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f11f3-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f11f3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f11f3-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f11f3-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f11f3-127">Header</span><span class="sxs-lookup"><span data-stu-id="f11f3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f11f3-128"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="f11f3-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f11f3-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f11f3-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="f11f3-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="f11f3-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f11f3-131">**BM- \_ Zeitrahmen**</span><span class="sxs-lookup"><span data-stu-id="f11f3-131">**BM\_SETIMAGE**</span></span>](bm-setimage.md)
</dt> <dt>

<span data-ttu-id="f11f3-132">**Licher**</span><span class="sxs-lookup"><span data-stu-id="f11f3-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f11f3-133">Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="f11f3-133">Buttons</span></span>](buttons.md)
</dt> </dl>

 

 





