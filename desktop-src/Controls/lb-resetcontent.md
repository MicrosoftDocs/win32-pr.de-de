---
title: LB_RESETCONTENT Meldung (Winuser. h)
description: Entfernt alle Elemente aus einem Listenfeld.
ms.assetid: 3865e45e-62da-457a-801c-2f9a61687022
keywords:
- Windows-Steuerelemente für LB_RESETCONTENT Meldung
topic_type:
- apiref
api_name:
- LB_RESETCONTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0091871df045812dcaa7a159cc456a1350d20f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859168"
---
# <a name="lb_resetcontent-message"></a><span data-ttu-id="fc7b2-104">LB- \_ resetcontent-Nachricht</span><span class="sxs-lookup"><span data-stu-id="fc7b2-104">LB\_RESETCONTENT message</span></span>

<span data-ttu-id="fc7b2-105">Entfernt alle Elemente aus einem Listenfeld.</span><span class="sxs-lookup"><span data-stu-id="fc7b2-105">Removes all items from a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="fc7b2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc7b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc7b2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fc7b2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc7b2-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="fc7b2-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fc7b2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fc7b2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc7b2-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="fc7b2-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc7b2-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fc7b2-111">Return value</span></span>

<span data-ttu-id="fc7b2-112">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fc7b2-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc7b2-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc7b2-113">Remarks</span></span>

<span data-ttu-id="fc7b2-114">Wenn im Listenfeld ein vom Besitzer gezeichneter Stil, aber nicht der [**lbs \_ hasstrings**](list-box-styles.md) -Stil enthalten ist, erhält der Besitzer des Listen Felds eine [**WM \_ DeleteItem**](wm-deleteitem.md) -Meldung für jedes Element im Listenfeld.</span><span class="sxs-lookup"><span data-stu-id="fc7b2-114">If the list box has an owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the owner of the list box receives a [**WM\_DELETEITEM**](wm-deleteitem.md) message for each item in the list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc7b2-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fc7b2-115">Requirements</span></span>



| <span data-ttu-id="fc7b2-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fc7b2-116">Requirement</span></span> | <span data-ttu-id="fc7b2-117">Wert</span><span class="sxs-lookup"><span data-stu-id="fc7b2-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc7b2-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fc7b2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fc7b2-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc7b2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fc7b2-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fc7b2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fc7b2-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc7b2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fc7b2-122">Header</span><span class="sxs-lookup"><span data-stu-id="fc7b2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc7b2-123"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="fc7b2-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc7b2-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc7b2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc7b2-125">**WM- \_ DeleteItem**</span><span class="sxs-lookup"><span data-stu-id="fc7b2-125">**WM\_DELETEITEM**</span></span>](wm-deleteitem.md)
</dt> </dl>

 

 





