---
title: CB_GETDROPPEDCONTROLRECT Meldung (Winuser. h)
description: Eine Anwendung sendet eine CB \_ getdroppedcontrolrect-Nachricht, um die Bildschirm Koordinaten eines Kombinations Felds im Dropdown Zustand abzurufen.
ms.assetid: fd8d78c0-e1a8-49c8-9e35-a105d00b863c
keywords:
- Windows-Steuerelemente für CB_GETDROPPEDCONTROLRECT Meldung
topic_type:
- apiref
api_name:
- CB_GETDROPPEDCONTROLRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adff5ad10ff91557b2579006dae6e1258650d74e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477334"
---
# <a name="cb_getdroppedcontrolrect-message"></a><span data-ttu-id="35a5d-104">CB \_ getdroppedcontrolrect-Meldung</span><span class="sxs-lookup"><span data-stu-id="35a5d-104">CB\_GETDROPPEDCONTROLRECT message</span></span>

<span data-ttu-id="35a5d-105">Eine Anwendung sendet eine **CB \_ getdroppedcontrolrect** -Nachricht, um die Bildschirm Koordinaten eines Kombinations Felds im Dropdown Zustand abzurufen.</span><span class="sxs-lookup"><span data-stu-id="35a5d-105">An application sends a **CB\_GETDROPPEDCONTROLRECT** message to retrieve the screen coordinates of a combo box in its dropped-down state.</span></span>

## <a name="parameters"></a><span data-ttu-id="35a5d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="35a5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35a5d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="35a5d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35a5d-108">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="35a5d-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="35a5d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="35a5d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35a5d-110">Ein Zeiger auf die [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Koordinaten des Kombinations Felds im abgehaltenten Zustand empfängt.</span><span class="sxs-lookup"><span data-stu-id="35a5d-110">A pointer to the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the coordinates of the combo box in its dropped-down state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35a5d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35a5d-111">Return value</span></span>

<span data-ttu-id="35a5d-112">Wenn die Nachricht erfolgreich ist, ist der Rückgabewert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="35a5d-112">If the message succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="35a5d-113">Wenn die Meldung fehlschlägt, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="35a5d-113">If the message fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="35a5d-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35a5d-114">Requirements</span></span>



| <span data-ttu-id="35a5d-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35a5d-115">Requirement</span></span> | <span data-ttu-id="35a5d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="35a5d-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35a5d-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="35a5d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="35a5d-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35a5d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="35a5d-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="35a5d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="35a5d-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35a5d-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="35a5d-121">Header</span><span class="sxs-lookup"><span data-stu-id="35a5d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="35a5d-122"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="35a5d-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35a5d-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35a5d-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="35a5d-124">[**Rect**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="35a5d-124">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

