---
title: EM_REDO Meldung (RichEdit. h)
description: Sendet eine EM-Wiederholungs \_ Nachricht an ein Rich Edit-Steuerelement, um die nächste Aktion in der Wiederholungs Warteschlange des Steuer Elements wiederholen.
ms.assetid: 28ec1ec2-a56d-442f-b3cb-9feeb92edaeb
keywords:
- Windows-Steuerelemente für EM_REDO Meldung
topic_type:
- apiref
api_name:
- EM_REDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bba7a684db0d40ebcfeec4a540989c4dab4c5dd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477601"
---
# <a name="em_redo-message"></a><span data-ttu-id="2ee29-104">EM-Wiederholungs \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="2ee29-104">EM\_REDO message</span></span>

<span data-ttu-id="2ee29-105">Sendet eine **EM \_** -Wiederholungs Nachricht an ein Rich Edit-Steuerelement, um die nächste Aktion in der Wiederholungs Warteschlange des Steuer Elements wiederholen.</span><span class="sxs-lookup"><span data-stu-id="2ee29-105">Sends an **EM\_REDO** message to a rich edit control to redo the next action in the control's redo queue.</span></span>

## <a name="parameters"></a><span data-ttu-id="2ee29-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ee29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ee29-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2ee29-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ee29-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="2ee29-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2ee29-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ee29-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ee29-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="2ee29-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ee29-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2ee29-111">Return value</span></span>

<span data-ttu-id="2ee29-112">Wenn der **Redo** -Vorgang erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="2ee29-112">If the **Redo** operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="2ee29-113">Wenn der **Wiederholungs Vorgang fehl** schlägt, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="2ee29-113">If the **Redo** operation fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ee29-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ee29-114">Remarks</span></span>

<span data-ttu-id="2ee29-115">Um zu ermitteln, ob in der Wiederholungs Warteschlange des Steuer Elements Aktionen vorhanden sind, senden Sie die [**EM \_ CanRedo**](em-canredo.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="2ee29-115">To determine whether there are any actions in the control's redo queue, send the [**EM\_CANREDO**](em-canredo.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ee29-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ee29-116">Requirements</span></span>



| <span data-ttu-id="2ee29-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ee29-117">Requirement</span></span> | <span data-ttu-id="2ee29-118">Wert</span><span class="sxs-lookup"><span data-stu-id="2ee29-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ee29-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2ee29-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2ee29-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2ee29-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2ee29-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2ee29-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2ee29-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2ee29-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2ee29-123">Header</span><span class="sxs-lookup"><span data-stu-id="2ee29-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ee29-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ee29-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ee29-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ee29-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="2ee29-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="2ee29-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2ee29-127">**EM \_ CanRedo**</span><span class="sxs-lookup"><span data-stu-id="2ee29-127">**EM\_CANREDO**</span></span>](em-canredo.md)
</dt> <dt>

[<span data-ttu-id="2ee29-128">**EM \_ getredoname**</span><span class="sxs-lookup"><span data-stu-id="2ee29-128">**EM\_GETREDONAME**</span></span>](em-getredoname.md)
</dt> <dt>

[<span data-ttu-id="2ee29-129">**EM \_ getundoname**</span><span class="sxs-lookup"><span data-stu-id="2ee29-129">**EM\_GETUNDONAME**</span></span>](em-getundoname.md)
</dt> <dt>

[<span data-ttu-id="2ee29-130">**EM \_ rückgängig machen**</span><span class="sxs-lookup"><span data-stu-id="2ee29-130">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





