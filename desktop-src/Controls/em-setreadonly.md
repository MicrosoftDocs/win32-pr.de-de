---
title: EM_SETREADONLY Meldung (Winuser. h)
description: Legt den schreibgeschützten Stil (es ist schreibgeschützt \_ ) eines Bearbeitungs Steuer Elements fest oder entfernt diesen. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- Windows-Steuerelemente für EM_SETREADONLY Meldung
topic_type:
- apiref
api_name:
- EM_SETREADONLY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0b224e11212077703ab62ab6a180875672c879e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103554"
---
# <a name="em_setreadonly-message"></a><span data-ttu-id="497ab-105">EM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="497ab-105">EM\_SETREADONLY message</span></span>

<span data-ttu-id="497ab-106">Legt den schreibgeschützten Stil (es ist Schreib [**geschützt \_**](edit-control-styles.md)) eines Bearbeitungs Steuer Elements fest oder entfernt diesen.</span><span class="sxs-lookup"><span data-stu-id="497ab-106">Sets or removes the read-only style ([**ES\_READONLY**](edit-control-styles.md)) of an edit control.</span></span> <span data-ttu-id="497ab-107">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="497ab-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="497ab-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="497ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="497ab-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="497ab-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="497ab-110">Gibt an, ob der es- [**Schreib \_**](edit-control-styles.md) geschützte Stil festgelegt oder entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="497ab-110">Specifies whether to set or remove the [**ES\_READONLY**](edit-control-styles.md) style.</span></span> <span data-ttu-id="497ab-111">Mit dem Wert **true** wird der schreibgeschützte Stil ' es ' festgelegt; mit dem Wert ' **false** ' wird der schreibgeschützte Stil ' **es \_** ' entfernt **\_**</span><span class="sxs-lookup"><span data-stu-id="497ab-111">A value of **TRUE** sets the **ES\_READONLY** style; a value of **FALSE** removes the **ES\_READONLY** style.</span></span>

</dd> <dt>

<span data-ttu-id="497ab-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="497ab-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="497ab-113">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="497ab-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="497ab-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="497ab-114">Return value</span></span>

<span data-ttu-id="497ab-115">Wenn der Vorgang erfolgreich ist, ist der Rückgabewert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="497ab-115">If the operation succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="497ab-116">Wenn der Vorgang fehlschlägt, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="497ab-116">If the operation fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="497ab-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="497ab-117">Remarks</span></span>

<span data-ttu-id="497ab-118">Wenn ein Bearbeitungs Steuerelement den [**Stil \_ "es**](edit-control-styles.md) schreibgeschützt" aufweist, kann der Benutzer den Text im Bearbeitungs Steuerelement nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="497ab-118">When an edit control has the [**ES\_READONLY**](edit-control-styles.md) style, the user cannot change the text within the edit control.</span></span>

<span data-ttu-id="497ab-119">Verwenden Sie die [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) -Funktion mit dem GWL-Style-Flag, um zu bestimmen, ob ein Bearbeitungs Steuer [**Element den schreibgeschützten \_ Schreib**](edit-control-styles.md) Stil hat \_ .</span><span class="sxs-lookup"><span data-stu-id="497ab-119">To determine whether an edit control has the [**ES\_READONLY**](edit-control-styles.md) style, use the [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) function with the GWL\_STYLE flag.</span></span>

<span data-ttu-id="497ab-120">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="497ab-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="497ab-121">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="497ab-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="497ab-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="497ab-122">Requirements</span></span>



| <span data-ttu-id="497ab-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="497ab-123">Requirement</span></span> | <span data-ttu-id="497ab-124">Wert</span><span class="sxs-lookup"><span data-stu-id="497ab-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="497ab-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="497ab-125">Minimum supported client</span></span><br/> | <span data-ttu-id="497ab-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="497ab-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="497ab-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="497ab-127">Minimum supported server</span></span><br/> | <span data-ttu-id="497ab-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="497ab-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="497ab-129">Header</span><span class="sxs-lookup"><span data-stu-id="497ab-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="497ab-130"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="497ab-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="497ab-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="497ab-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="497ab-132">**GetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="497ab-132">**GetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)
</dt> </dl>

 

