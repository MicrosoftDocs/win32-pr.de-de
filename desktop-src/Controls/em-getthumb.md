---
title: EM_GETTHUMB Meldung (Winuser. h)
description: Ruft die Position des Bild Lauf Felds (Ziehpunkt) in der vertikalen Schiebe Leiste eines mehrzeiligen Bearbeitungs Steuer Elements ab. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 04bd0102-1652-405b-8c42-50e138abaf75
keywords:
- Windows-Steuerelemente für EM_GETTHUMB Meldung
topic_type:
- apiref
api_name:
- EM_GETTHUMB
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e6689c530794e11897f1f88a7d5864058d53aa8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105111"
---
# <a name="em_getthumb-message"></a><span data-ttu-id="2c0fd-105">EM \_ getthumb-Nachricht</span><span class="sxs-lookup"><span data-stu-id="2c0fd-105">EM\_GETTHUMB message</span></span>

<span data-ttu-id="2c0fd-106">Ruft die Position des Bild Lauf Felds (Ziehpunkt) in der vertikalen Schiebe Leiste eines mehrzeiligen Bearbeitungs Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="2c0fd-106">Gets the position of the scroll box (thumb) in the vertical scroll bar of a multiline edit control.</span></span> <span data-ttu-id="2c0fd-107">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="2c0fd-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2c0fd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c0fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c0fd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c0fd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c0fd-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="2c0fd-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2c0fd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c0fd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c0fd-112">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="2c0fd-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c0fd-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2c0fd-113">Return value</span></span>

<span data-ttu-id="2c0fd-114">Der Rückgabewert ist die Position des Bild Lauf Felds.</span><span class="sxs-lookup"><span data-stu-id="2c0fd-114">The return value is the position of the scroll box.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c0fd-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c0fd-115">Remarks</span></span>

<span data-ttu-id="2c0fd-116">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 2,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2c0fd-116">**Rich Edit:** Supported in Microsoft Rich Edit 2.0 and later.</span></span> <span data-ttu-id="2c0fd-117">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="2c0fd-117">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c0fd-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c0fd-118">Requirements</span></span>



| <span data-ttu-id="2c0fd-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c0fd-119">Requirement</span></span> | <span data-ttu-id="2c0fd-120">Wert</span><span class="sxs-lookup"><span data-stu-id="2c0fd-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c0fd-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c0fd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2c0fd-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c0fd-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2c0fd-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c0fd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2c0fd-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c0fd-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2c0fd-125">Header</span><span class="sxs-lookup"><span data-stu-id="2c0fd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c0fd-126"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="2c0fd-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





