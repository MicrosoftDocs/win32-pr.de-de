---
title: EM_FMTLINES Meldung (Winuser. h)
description: Legt ein Flag fest, das bestimmt, ob ein mehrzeilige Bearbeitungs Steuerelement weiche Zeilenumbruch Zeichen einschließt. Ein weicher Zeilenumbruch besteht aus zwei Wagen Rückläufen und einem Zeilenvorschub und wird am Ende einer Zeile eingefügt, die aufgrund von wordwrapping unterbrochen wird.
ms.assetid: bfc08062-b0a7-4ba7-8858-00cb20895c77
keywords:
- Windows-Steuerelemente für EM_FMTLINES Meldung
topic_type:
- apiref
api_name:
- EM_FMTLINES
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c12a22ee8c30ffa74705f670a16caa3651e9b44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477118"
---
# <a name="em_fmtlines-message"></a><span data-ttu-id="ac91e-105">EM-Fehler \_ Zeilen Meldung</span><span class="sxs-lookup"><span data-stu-id="ac91e-105">EM\_FMTLINES message</span></span>

<span data-ttu-id="ac91e-106">Legt ein Flag fest, das bestimmt, ob ein mehrzeilige Bearbeitungs Steuerelement weiche Zeilenumbruch Zeichen einschließt.</span><span class="sxs-lookup"><span data-stu-id="ac91e-106">Sets a flag that determines whether a multiline edit control includes soft line-break characters.</span></span> <span data-ttu-id="ac91e-107">Ein weicher Zeilenumbruch besteht aus zwei Wagen Rückläufen und einem Zeilenvorschub und wird am Ende einer Zeile eingefügt, die aufgrund von wordwrapping unterbrochen wird.</span><span class="sxs-lookup"><span data-stu-id="ac91e-107">A soft line break consists of two carriage returns and a line feed and is inserted at the end of a line that is broken because of wordwrapping.</span></span>

## <a name="parameters"></a><span data-ttu-id="ac91e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac91e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac91e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ac91e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ac91e-110">Gibt an, ob weiche Zeilenumbruch Zeichen eingefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ac91e-110">Specifies whether soft line-break characters are to be inserted.</span></span> <span data-ttu-id="ac91e-111">Der Wert **true** fügt die Zeichen ein. bei einem Wert von **false** werden diese entfernt.</span><span class="sxs-lookup"><span data-stu-id="ac91e-111">A value of **TRUE** inserts the characters; a value of **FALSE** removes them.</span></span>

</dd> <dt>

<span data-ttu-id="ac91e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ac91e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ac91e-113">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ac91e-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac91e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac91e-114">Return value</span></span>

<span data-ttu-id="ac91e-115">Der Rückgabewert ist identisch mit dem *wParam* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="ac91e-115">The return value is identical to the *wParam* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac91e-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac91e-116">Remarks</span></span>

<span data-ttu-id="ac91e-117">Diese Nachricht wirkt sich nur auf den Puffer aus, der von der [**EM \_ GetHandle**](em-gethandle.md) -Nachricht zurückgegeben wird, und auf den Text, der von der [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext)</span><span class="sxs-lookup"><span data-stu-id="ac91e-117">This message affects only the buffer returned by the [**EM\_GETHANDLE**](em-gethandle.md) message and the text returned by the [**WM\_GETTEXT**](/windows/desktop/winmsg/wm-gettext) message.</span></span> <span data-ttu-id="ac91e-118">Dies hat keine Auswirkung auf die Anzeige des Texts innerhalb des Bearbeitungs Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="ac91e-118">It has no effect on the display of the text within the edit control.</span></span>

<span data-ttu-id="ac91e-119">Die **EM- \_ fmtlines** -Nachricht wirkt sich nicht auf eine Zeile aus, die mit einem harten Zeilenumbruch endet.</span><span class="sxs-lookup"><span data-stu-id="ac91e-119">The **EM\_FMTLINES** message does not affect a line that ends with a hard line break.</span></span> <span data-ttu-id="ac91e-120">Ein harter Zeilenumbruch besteht aus einem Wagen Rücklauf und einem Zeilenvorschub.</span><span class="sxs-lookup"><span data-stu-id="ac91e-120">A hard line break consists of one carriage return and a line feed.</span></span>

> [!Note]  
> <span data-ttu-id="ac91e-121">Die Größe des Texts ändert sich, wenn diese Nachricht verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="ac91e-121">The size of the text changes when this message is processed.</span></span>

 

<span data-ttu-id="ac91e-122">Umfassende **Bearbeitung:** Die **EM \_** -Meldung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ac91e-122">**Rich Edit:** The **EM\_FMTLINES** message is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac91e-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac91e-123">Requirements</span></span>



| <span data-ttu-id="ac91e-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac91e-124">Requirement</span></span> | <span data-ttu-id="ac91e-125">Wert</span><span class="sxs-lookup"><span data-stu-id="ac91e-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac91e-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac91e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ac91e-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac91e-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ac91e-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac91e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ac91e-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac91e-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ac91e-130">Header</span><span class="sxs-lookup"><span data-stu-id="ac91e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac91e-131"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="ac91e-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac91e-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac91e-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="ac91e-133">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="ac91e-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ac91e-134">**EM \_ GetHandle**</span><span class="sxs-lookup"><span data-stu-id="ac91e-134">**EM\_GETHANDLE**</span></span>](em-gethandle.md)
</dt> <dt>

<span data-ttu-id="ac91e-135">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="ac91e-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="ac91e-136">**WM \_ gettext**</span><span class="sxs-lookup"><span data-stu-id="ac91e-136">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

