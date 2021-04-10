---
title: EM_GETSEL Meldung (Winuser. h)
description: Ruft die Position des Anfangs-und des Endzeichens (in tchars) der aktuellen Auswahl in einem Bearbeitungs Steuerelement ab. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: cf12aaea-cfa7-4804-ae34-fd0992332288
keywords:
- Windows-Steuerelemente für EM_GETSEL Meldung
topic_type:
- apiref
api_name:
- EM_GETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28ba97c9043866c3e97c1c51389447498562455
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040548"
---
# <a name="em_getsel-message"></a><span data-ttu-id="1d857-105">EM \_ GetSEL-Nachricht</span><span class="sxs-lookup"><span data-stu-id="1d857-105">EM\_GETSEL message</span></span>

<span data-ttu-id="1d857-106">Ruft die Position des Anfangs-und des Endzeichens (in **TCHAR** s) der aktuellen Auswahl in einem Bearbeitungs Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="1d857-106">Gets the starting and ending character positions (in **TCHAR** s) of the current selection in an edit control.</span></span> <span data-ttu-id="1d857-107">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="1d857-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1d857-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d857-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d857-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1d857-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d857-110">Ein Zeiger auf einen **DWORD** -Wert, der die Anfangsposition der Auswahl empfängt.</span><span class="sxs-lookup"><span data-stu-id="1d857-110">A pointer to a **DWORD** value that receives the starting position of the selection.</span></span> <span data-ttu-id="1d857-111">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="1d857-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1d857-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1d857-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d857-113">Ein Zeiger auf einen **DWORD** -Wert, der die Position des ersten nicht ausgewählten Zeichens nach dem Ende der Auswahl empfängt.</span><span class="sxs-lookup"><span data-stu-id="1d857-113">A pointer to a **DWORD** value that receives the position of the first unselected character after the end of the selection.</span></span> <span data-ttu-id="1d857-114">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="1d857-114">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d857-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d857-115">Return value</span></span>

<span data-ttu-id="1d857-116">Der Rückgabewert ist ein NULL basierter Wert, der die Anfangsposition der Auswahl im [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) und die Position des ersten **tchars** nach dem letzten ausgewählten **TCHAR** im [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))-Ausdruck aufweist.</span><span class="sxs-lookup"><span data-stu-id="1d857-116">The return value is a zero-based value with the starting position of the selection in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the position of the first **TCHAR** after the last selected **TCHAR** in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span> <span data-ttu-id="1d857-117">Wenn einer dieser Werte 65.535 überschreitet, ist der Rückgabewert-1.</span><span class="sxs-lookup"><span data-stu-id="1d857-117">If either of these values exceeds 65,535, the return value is -1.</span></span>

<span data-ttu-id="1d857-118">Es ist besser, die in *wParam* und *LPARAM* zurückgegebenen Werte zu verwenden, da es sich um vollständige 32-Bit-Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="1d857-118">It is better to use the values returned in *wParam* and *lParam* because they are full 32-bit values.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d857-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d857-119">Remarks</span></span>

<span data-ttu-id="1d857-120">Wenn keine Auswahl vorhanden ist, sind die Anfangs-und Endwerte die Position der Einfügemarke.</span><span class="sxs-lookup"><span data-stu-id="1d857-120">If there is no selection, the starting and ending values are both the position of the caret.</span></span>

<span data-ttu-id="1d857-121">**Rich Edit-Steuerelemente:** Sie können auch die [**EM \_ exgetsel**](em-exgetsel.md) -Nachricht verwenden, um die gleichen Informationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1d857-121">**Rich edit controls:** You can also use the [**EM\_EXGETSEL**](em-exgetsel.md) message to retrieve the same information.</span></span> <span data-ttu-id="1d857-122">**EM \_ Exgetsel** gibt auch Start-und Endzeichen Positionen als 32-Bit-Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="1d857-122">**EM\_EXGETSEL** also returns starting and ending character positions as 32-bit values.</span></span>

<span data-ttu-id="1d857-123">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1d857-123">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="1d857-124">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="1d857-124">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d857-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d857-125">Requirements</span></span>



| <span data-ttu-id="1d857-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d857-126">Requirement</span></span> | <span data-ttu-id="1d857-127">Wert</span><span class="sxs-lookup"><span data-stu-id="1d857-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d857-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d857-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1d857-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d857-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1d857-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d857-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1d857-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d857-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1d857-132">Header</span><span class="sxs-lookup"><span data-stu-id="1d857-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d857-133"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="1d857-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d857-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d857-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="1d857-135">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="1d857-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1d857-136">**EM \_ exgetsel**</span><span class="sxs-lookup"><span data-stu-id="1d857-136">**EM\_EXGETSEL**</span></span>](em-exgetsel.md)
</dt> <dt>

[<span data-ttu-id="1d857-137">**EM- \_ tsel**</span><span class="sxs-lookup"><span data-stu-id="1d857-137">**EM\_SETSEL**</span></span>](em-setsel.md)
</dt> </dl>

 

