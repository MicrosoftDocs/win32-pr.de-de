---
title: STM_GETIMAGE Meldung (Winuser. h)
description: Eine Anwendung sendet eine STM \_ GetImage-Nachricht zum Abrufen eines Handles zum Bild (Symbol oder Bitmap), das einem statischen Steuerelement zugeordnet ist.
ms.assetid: eb5fe67a-09be-4c13-89c6-0e2f23e8c081
keywords:
- Windows-Steuerelemente für STM_GETIMAGE Meldung
topic_type:
- apiref
api_name:
- STM_GETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77fe0c3d00a2a957530160a5ce5a21b8a1cf84e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040161"
---
# <a name="stm_getimage-message"></a><span data-ttu-id="15a46-104">STM \_ GetImage-Nachricht</span><span class="sxs-lookup"><span data-stu-id="15a46-104">STM\_GETIMAGE message</span></span>

<span data-ttu-id="15a46-105">Eine Anwendung sendet eine **STM \_ GetImage** -Nachricht zum Abrufen eines Handles zum Bild (Symbol oder Bitmap), das einem statischen Steuerelement zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="15a46-105">An application sends an **STM\_GETIMAGE** message to retrieve a handle to the image (icon or bitmap) associated with a static control.</span></span>

## <a name="parameters"></a><span data-ttu-id="15a46-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="15a46-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15a46-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="15a46-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15a46-108">Gibt den Typ des abzurufenden Bilds an.</span><span class="sxs-lookup"><span data-stu-id="15a46-108">Specifies the type of image to retrieve.</span></span> <span data-ttu-id="15a46-109">Dieser Parameter kann einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="15a46-109">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="15a46-110">Wert</span><span class="sxs-lookup"><span data-stu-id="15a46-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="15a46-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="15a46-111">Meaning</span></span>                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <span data-ttu-id="15a46-112"><dt>**Bild \_ Bitmap**</dt></span><span class="sxs-lookup"><span data-stu-id="15a46-112"><dt>**IMAGE\_BITMAP**</dt></span></span> </dl>                | <span data-ttu-id="15a46-113">Bitmap.</span><span class="sxs-lookup"><span data-stu-id="15a46-113">Bitmap.</span></span><br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <span data-ttu-id="15a46-114"><dt>**Bild \_ Cursor**</dt></span><span class="sxs-lookup"><span data-stu-id="15a46-114"><dt>**IMAGE\_CURSOR**</dt></span></span> </dl>                | <span data-ttu-id="15a46-115">Hand.</span><span class="sxs-lookup"><span data-stu-id="15a46-115">Cursor.</span></span><br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <span data-ttu-id="15a46-116"><dt>**Image- \_ enhmetafile**</dt></span><span class="sxs-lookup"><span data-stu-id="15a46-116"><dt>**IMAGE\_ENHMETAFILE**</dt></span></span> </dl> | <span data-ttu-id="15a46-117">Erweiterte Metadatei.</span><span class="sxs-lookup"><span data-stu-id="15a46-117">Enhanced metafile.</span></span><br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <span data-ttu-id="15a46-118"><dt>**Bild \_ Symbol**</dt></span><span class="sxs-lookup"><span data-stu-id="15a46-118"><dt>**IMAGE\_ICON**</dt></span></span> </dl>                      | <span data-ttu-id="15a46-119">Angezeigt.</span><span class="sxs-lookup"><span data-stu-id="15a46-119">Icon.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="15a46-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="15a46-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15a46-121">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="15a46-121">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15a46-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="15a46-122">Return value</span></span>

<span data-ttu-id="15a46-123">Der Rückgabewert ist, sofern vorhanden, ein Handle für das Bild. Andernfalls ist der Wert **null**.</span><span class="sxs-lookup"><span data-stu-id="15a46-123">The return value is a handle to the image, if any; otherwise, it is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="15a46-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15a46-124">Requirements</span></span>



| <span data-ttu-id="15a46-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15a46-125">Requirement</span></span> | <span data-ttu-id="15a46-126">Wert</span><span class="sxs-lookup"><span data-stu-id="15a46-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15a46-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="15a46-127">Minimum supported client</span></span><br/> | <span data-ttu-id="15a46-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15a46-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="15a46-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="15a46-129">Minimum supported server</span></span><br/> | <span data-ttu-id="15a46-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15a46-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="15a46-131">Header</span><span class="sxs-lookup"><span data-stu-id="15a46-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="15a46-132"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="15a46-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15a46-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15a46-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15a46-134">**STM- \_ Zeitrahmen**</span><span class="sxs-lookup"><span data-stu-id="15a46-134">**STM\_SETIMAGE**</span></span>](stm-setimage.md)
</dt> </dl>

 

 





