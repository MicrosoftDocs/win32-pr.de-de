---
title: EM_CANREDO Meldung (RichEdit. h)
description: Bestimmt, ob in der Wiederholungs Warteschlange für das Steuerelement Aktionen vorhanden sind.
ms.assetid: 4a76adc8-f815-4cf7-8742-b7695e5a0f64
keywords:
- Windows-Steuerelemente für EM_CANREDO Meldung
topic_type:
- apiref
api_name:
- EM_CANREDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccfb12f8e72bdf5321151cd3a70b74f322a46591
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859056"
---
# <a name="em_canredo-message"></a><span data-ttu-id="40d0c-104">EM \_ CanRedo-Nachricht</span><span class="sxs-lookup"><span data-stu-id="40d0c-104">EM\_CANREDO message</span></span>

<span data-ttu-id="40d0c-105">Bestimmt, ob in der Wiederholungs Warteschlange für das Steuerelement Aktionen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="40d0c-105">Determines whether there are any actions in the control redo queue.</span></span>

## <a name="parameters"></a><span data-ttu-id="40d0c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="40d0c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40d0c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="40d0c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="40d0c-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="40d0c-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="40d0c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="40d0c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="40d0c-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="40d0c-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40d0c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40d0c-111">Return value</span></span>

<span data-ttu-id="40d0c-112">Wenn in der Wiederholungs Warteschlange für das Steuerelement Aktionen vorhanden sind, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="40d0c-112">If there are actions in the control redo queue, the return value is a nonzero value.</span></span>

<span data-ttu-id="40d0c-113">Wenn die Wiederholungs Warteschlange leer ist, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="40d0c-113">If the redo queue is empty, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="40d0c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40d0c-114">Remarks</span></span>

<span data-ttu-id="40d0c-115">Um den letzten Rückgängig-Vorgang zu wiederholen, senden Sie die EM-Wiederholungs Nachricht. [**\_**](em-redo.md)</span><span class="sxs-lookup"><span data-stu-id="40d0c-115">To redo the most recent undo operation, send the [**EM\_REDO**](em-redo.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="40d0c-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40d0c-116">Requirements</span></span>



| <span data-ttu-id="40d0c-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40d0c-117">Requirement</span></span> | <span data-ttu-id="40d0c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="40d0c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="40d0c-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="40d0c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="40d0c-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="40d0c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="40d0c-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="40d0c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="40d0c-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="40d0c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="40d0c-123">Header</span><span class="sxs-lookup"><span data-stu-id="40d0c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="40d0c-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="40d0c-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40d0c-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40d0c-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="40d0c-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="40d0c-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="40d0c-127">**EM \_ getredoname**</span><span class="sxs-lookup"><span data-stu-id="40d0c-127">**EM\_GETREDONAME**</span></span>](em-getredoname.md)
</dt> <dt>

[<span data-ttu-id="40d0c-128">**EM \_ getundoname**</span><span class="sxs-lookup"><span data-stu-id="40d0c-128">**EM\_GETUNDONAME**</span></span>](em-getundoname.md)
</dt> <dt>

[<span data-ttu-id="40d0c-129">**EM- \_ Wiederholung**</span><span class="sxs-lookup"><span data-stu-id="40d0c-129">**EM\_REDO**</span></span>](em-redo.md)
</dt> <dt>

[<span data-ttu-id="40d0c-130">**EM \_ rückgängig machen**</span><span class="sxs-lookup"><span data-stu-id="40d0c-130">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





