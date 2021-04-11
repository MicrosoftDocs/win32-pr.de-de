---
title: BM_SETIMAGE Meldung (Winuser. h)
description: Verknüpft ein neues Bild (Symbol oder Bitmap) mit der Schaltfläche.
ms.assetid: bf05e684-63d0-4583-960b-f329edafb151
keywords:
- Windows-Steuerelemente für BM_SETIMAGE Meldung
topic_type:
- apiref
api_name:
- BM_SETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65d083c4fb509d51eb017bb7d3d38fab07b4c006
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103134"
---
# <a name="bm_setimage-message"></a><span data-ttu-id="8fc8b-104">BM- \_ abtimage-Nachricht</span><span class="sxs-lookup"><span data-stu-id="8fc8b-104">BM\_SETIMAGE message</span></span>

<span data-ttu-id="8fc8b-105">Verknüpft ein neues Bild (Symbol oder Bitmap) mit der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="8fc8b-105">Associates a new image (icon or bitmap) with the button.</span></span>

## <a name="parameters"></a><span data-ttu-id="8fc8b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8fc8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fc8b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8fc8b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8fc8b-108">Der Typ des Bilds, das der Schaltfläche zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8fc8b-108">The type of image to associate with the button.</span></span> <span data-ttu-id="8fc8b-109">Dieser Parameter kann einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="8fc8b-109">This parameter can be one of the following values:</span></span>

-   <span data-ttu-id="8fc8b-110">Bild \_ Bitmap</span><span class="sxs-lookup"><span data-stu-id="8fc8b-110">IMAGE\_BITMAP</span></span>
-   <span data-ttu-id="8fc8b-111">Bild \_ Symbol</span><span class="sxs-lookup"><span data-stu-id="8fc8b-111">IMAGE\_ICON</span></span>

</dd> <dt>

<span data-ttu-id="8fc8b-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8fc8b-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8fc8b-113">Ein Handle (**HICON** oder **hBitmap**) für das Bild, das der Schaltfläche zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8fc8b-113">A handle (**HICON** or **HBITMAP**) to the image to associate with the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fc8b-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8fc8b-114">Return value</span></span>

<span data-ttu-id="8fc8b-115">Der Rückgabewert ist ein Handle für das Bild, das zuvor der Schaltfläche zugeordnet ist, sofern vorhanden. Andernfalls ist der Wert **null**.</span><span class="sxs-lookup"><span data-stu-id="8fc8b-115">The return value is a handle to the image previously associated with the button, if any; otherwise, it is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fc8b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8fc8b-116">Remarks</span></span>

<span data-ttu-id="8fc8b-117">Die Darstellung von Text, ein Symbol oder beides auf einem Schaltflächen-Steuerelement hängt vom Buch [**-und dem Karten- \_**](button-styles.md) [**\_ Bitmapformat**](button-styles.md) ab und gibt an, ob die BM-ablaufnachricht aufgerufen wird. **\_**</span><span class="sxs-lookup"><span data-stu-id="8fc8b-117">The appearance of text, an icon, or both on a button control depends on the [**BS\_ICON**](button-styles.md) and [**BS\_BITMAP**](button-styles.md) styles, and whether the **BM\_SETIMAGE** message is called.</span></span> <span data-ttu-id="8fc8b-118">Die folgenden Ergebnisse sind möglich:</span><span class="sxs-lookup"><span data-stu-id="8fc8b-118">The possible results are as follows:</span></span>



| <span data-ttu-id="8fc8b-119">Das SB-Symbol oder das SB- \_ \_ bitmapset?</span><span class="sxs-lookup"><span data-stu-id="8fc8b-119">BS\_ICON or BS\_BITMAP Set?</span></span> | <span data-ttu-id="8fc8b-120">BM- \_ Image aufgerufen?</span><span class="sxs-lookup"><span data-stu-id="8fc8b-120">BM\_SETIMAGE Called?</span></span> | <span data-ttu-id="8fc8b-121">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="8fc8b-121">Result</span></span>              |
|-----------------------------|----------------------|---------------------|
| <span data-ttu-id="8fc8b-122">Ja</span><span class="sxs-lookup"><span data-stu-id="8fc8b-122">Yes</span></span>                         | <span data-ttu-id="8fc8b-123">Ja</span><span class="sxs-lookup"><span data-stu-id="8fc8b-123">Yes</span></span>                  | <span data-ttu-id="8fc8b-124">Nur Symbol anzeigen.</span><span class="sxs-lookup"><span data-stu-id="8fc8b-124">Show icon only.</span></span>     |
| <span data-ttu-id="8fc8b-125">Nein</span><span class="sxs-lookup"><span data-stu-id="8fc8b-125">No</span></span>                          | <span data-ttu-id="8fc8b-126">Ja</span><span class="sxs-lookup"><span data-stu-id="8fc8b-126">Yes</span></span>                  | <span data-ttu-id="8fc8b-127">Symbol und Text anzeigen.</span><span class="sxs-lookup"><span data-stu-id="8fc8b-127">Show icon and text.</span></span> |
| <span data-ttu-id="8fc8b-128">Ja</span><span class="sxs-lookup"><span data-stu-id="8fc8b-128">Yes</span></span>                         | <span data-ttu-id="8fc8b-129">Nein</span><span class="sxs-lookup"><span data-stu-id="8fc8b-129">No</span></span>                   | <span data-ttu-id="8fc8b-130">Nur Text anzeigen.</span><span class="sxs-lookup"><span data-stu-id="8fc8b-130">Show text only.</span></span>     |
| <span data-ttu-id="8fc8b-131">Nein</span><span class="sxs-lookup"><span data-stu-id="8fc8b-131">No</span></span>                          | <span data-ttu-id="8fc8b-132">Nein</span><span class="sxs-lookup"><span data-stu-id="8fc8b-132">No</span></span>                   | <span data-ttu-id="8fc8b-133">Nur Text anzeigen</span><span class="sxs-lookup"><span data-stu-id="8fc8b-133">Show text only</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="8fc8b-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8fc8b-134">Requirements</span></span>



| <span data-ttu-id="8fc8b-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8fc8b-135">Requirement</span></span> | <span data-ttu-id="8fc8b-136">Wert</span><span class="sxs-lookup"><span data-stu-id="8fc8b-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fc8b-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8fc8b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="8fc8b-138">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8fc8b-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8fc8b-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8fc8b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="8fc8b-140">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8fc8b-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8fc8b-141">Header</span><span class="sxs-lookup"><span data-stu-id="8fc8b-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fc8b-142"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="8fc8b-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fc8b-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8fc8b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fc8b-144">**BM- \_ GetImage**</span><span class="sxs-lookup"><span data-stu-id="8fc8b-144">**BM\_GETIMAGE**</span></span>](bm-getimage.md)
</dt> </dl>

 

 





