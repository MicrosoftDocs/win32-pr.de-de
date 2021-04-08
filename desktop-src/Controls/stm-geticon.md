---
title: STM_GETICON Meldung (Winuser. h)
description: Eine Anwendung sendet die STM \_ GetIcon-Nachricht, um ein Handle für das Symbol abzurufen, das einem statischen Steuerelement mit dem SS-Symbolstil zugeordnet ist \_ .
ms.assetid: e6b0a006-696b-401d-b894-b1db697c8939
keywords:
- Windows-Steuerelemente für STM_GETICON Meldung
topic_type:
- apiref
api_name:
- STM_GETICON
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64f55d2a2f8315b99526e51a69891f6f0056e8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103126"
---
# <a name="stm_geticon-message"></a><span data-ttu-id="9ed56-104">STM- \_ GetIcon-Nachricht</span><span class="sxs-lookup"><span data-stu-id="9ed56-104">STM\_GETICON message</span></span>

<span data-ttu-id="9ed56-105">Eine Anwendung sendet die **STM \_ GetIcon** -Nachricht, um ein Handle für das Symbol abzurufen, das einem statischen Steuerelement mit dem SS-Symbolstil zugeordnet ist \_ .</span><span class="sxs-lookup"><span data-stu-id="9ed56-105">An application sends the **STM\_GETICON** message to retrieve a handle to the icon associated with a static control that has the SS\_ICON style.</span></span>

## <a name="parameters"></a><span data-ttu-id="9ed56-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ed56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ed56-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9ed56-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ed56-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="9ed56-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9ed56-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ed56-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ed56-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="9ed56-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ed56-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ed56-111">Return value</span></span>

<span data-ttu-id="9ed56-112">Der Rückgabewert ist ein Handle für das Symbol, oder **null** , wenn entweder das statische Steuerelement kein zugeordnetes Symbol aufweist oder wenn ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="9ed56-112">The return value is a handle to the icon, or **NULL** if either the static control has no associated icon or if an error occurred.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ed56-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ed56-113">Requirements</span></span>



| <span data-ttu-id="9ed56-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ed56-114">Requirement</span></span> | <span data-ttu-id="9ed56-115">Wert</span><span class="sxs-lookup"><span data-stu-id="9ed56-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ed56-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ed56-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9ed56-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ed56-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9ed56-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ed56-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9ed56-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ed56-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9ed56-120">Header</span><span class="sxs-lookup"><span data-stu-id="9ed56-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ed56-121"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="9ed56-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ed56-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ed56-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ed56-123">**STM \_ -Ziel**</span><span class="sxs-lookup"><span data-stu-id="9ed56-123">**STM\_SETICON**</span></span>](stm-seticon.md)
</dt> </dl>

 

 





