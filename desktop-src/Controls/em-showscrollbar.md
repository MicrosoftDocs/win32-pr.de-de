---
title: EM_SHOWSCROLLBAR Meldung (RichEdit. h)
description: Blendet eine der Bild Lauf leisten im Host Fenster eines Rich-Edit-Steuer Elements ein oder aus.
ms.assetid: 0a6ec010-4870-4faf-9dc2-1da961dc8194
keywords:
- Windows-Steuerelemente für EM_SHOWSCROLLBAR Meldung
topic_type:
- apiref
api_name:
- EM_SHOWSCROLLBAR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb569b194be3d744db67f98b71a595ba18a2d3a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949775"
---
# <a name="em_showscrollbar-message"></a><span data-ttu-id="a5ed1-104">EM- \_ ShowScrollbar-Meldung</span><span class="sxs-lookup"><span data-stu-id="a5ed1-104">EM\_SHOWSCROLLBAR message</span></span>

<span data-ttu-id="a5ed1-105">Blendet eine der Bild Lauf leisten im Host Fenster eines Rich-Edit-Steuer Elements ein oder aus.</span><span class="sxs-lookup"><span data-stu-id="a5ed1-105">Shows or hides one of the scroll bars in the host window of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a5ed1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5ed1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5ed1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a5ed1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a5ed1-108">Gibt an, welche Bild Lauf Leiste angezeigt werden soll: horizontal oder vertikal.</span><span class="sxs-lookup"><span data-stu-id="a5ed1-108">Identifies which scroll bar to display: horizontal or vertical.</span></span> <span data-ttu-id="a5ed1-109">Dieser Parameter muss **SB \_ Vert** oder **SB \_ Horz** sein.</span><span class="sxs-lookup"><span data-stu-id="a5ed1-109">This parameter must be **SB\_VERT** or **SB\_HORZ**.</span></span>

</dd> <dt>

<span data-ttu-id="a5ed1-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a5ed1-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a5ed1-111">Gibt an, ob die Bild Lauf Leiste angezeigt oder ausgeblendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a5ed1-111">Specifies whether to show the scroll bar or hide it.</span></span> <span data-ttu-id="a5ed1-112">Geben Sie **true** an, um die Scrollleiste anzuzeigen, und **false** , um sie auszublenden.</span><span class="sxs-lookup"><span data-stu-id="a5ed1-112">Specify **TRUE** to show the scroll bar and **FALSE** to hide it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5ed1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a5ed1-113">Return value</span></span>

<span data-ttu-id="a5ed1-114">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a5ed1-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5ed1-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5ed1-115">Remarks</span></span>

<span data-ttu-id="a5ed1-116">Diese Methode ist nur gültig, wenn das Steuerelement direkt aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="a5ed1-116">This method is only valid when the control is in-place active.</span></span> <span data-ttu-id="a5ed1-117">Aufrufe, die während des inaktiven Steuer Elements ausgeführt werden, können fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="a5ed1-117">Calls made while the control is inactive may fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5ed1-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5ed1-118">Requirements</span></span>



| <span data-ttu-id="a5ed1-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5ed1-119">Requirement</span></span> | <span data-ttu-id="a5ed1-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a5ed1-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5ed1-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a5ed1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a5ed1-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5ed1-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a5ed1-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a5ed1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a5ed1-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5ed1-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a5ed1-125">Header</span><span class="sxs-lookup"><span data-stu-id="a5ed1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5ed1-126"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5ed1-126"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5ed1-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5ed1-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="a5ed1-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="a5ed1-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a5ed1-129">**EM \_ getscrollpos**</span><span class="sxs-lookup"><span data-stu-id="a5ed1-129">**EM\_GETSCROLLPOS**</span></span>](em-getscrollpos.md)
</dt> <dt>

[<span data-ttu-id="a5ed1-130">**EM- \_ setscrollpos**</span><span class="sxs-lookup"><span data-stu-id="a5ed1-130">**EM\_SETSCROLLPOS**</span></span>](em-setscrollpos.md)
</dt> </dl>

 

 





