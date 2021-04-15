---
title: EM_SETIMEMODEBIAS Meldung (RichEdit. h)
description: Legen Sie den Modus für den Eingabemethoden-Editor (IME) für ein Rich-Edit-Steuerelement fest.
ms.assetid: 4a3f97eb-fe80-4e84-a73e-3ed6d73644de
keywords:
- Windows-Steuerelemente für EM_SETIMEMODEBIAS Meldung
topic_type:
- apiref
api_name:
- EM_SETIMEMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48fbd93971a57cffa3441c2a3db0816572f761d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477319"
---
# <a name="em_setimemodebias-message"></a><span data-ttu-id="95c4a-104">EM- \_ /timemodebias-Nachricht</span><span class="sxs-lookup"><span data-stu-id="95c4a-104">EM\_SETIMEMODEBIAS message</span></span>

<span data-ttu-id="95c4a-105">Legen Sie den Modus für den Eingabemethoden-Editor (IME) für ein Rich-Edit-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="95c4a-105">Set the Input Method Editor (IME) mode bias for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="95c4a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="95c4a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95c4a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="95c4a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95c4a-108">Wert des IME-Modus-Bias.</span><span class="sxs-lookup"><span data-stu-id="95c4a-108">IME mode bias value.</span></span> <span data-ttu-id="95c4a-109">Dies kann einer der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="95c4a-109">It can be one of the following.</span></span>



| <span data-ttu-id="95c4a-110">Wert</span><span class="sxs-lookup"><span data-stu-id="95c4a-110">Value</span></span>                                                                                                                                                                                        | <span data-ttu-id="95c4a-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="95c4a-111">Meaning</span></span>                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="IMF_SMODE_PLAURALCLAUSE"></span><span id="imf_smode_plauralclause"></span><dl> <span data-ttu-id="95c4a-112"><dt>**IMF- \_ smode- \_ plauralklausel**</dt></span><span class="sxs-lookup"><span data-stu-id="95c4a-112"><dt>**IMF\_SMODE\_PLAURALCLAUSE**</dt></span></span> </dl> | <span data-ttu-id="95c4a-113">Legt die Verschiebung des IME-Modus auf Name fest.</span><span class="sxs-lookup"><span data-stu-id="95c4a-113">Sets the IME mode bias to Name.</span></span><br/> |
| <span id="IMF_SMODE_NONE"></span><span id="imf_smode_none"></span><dl> <span data-ttu-id="95c4a-114"><dt>**IMF- \_ smode- \_ keine**</dt></span><span class="sxs-lookup"><span data-stu-id="95c4a-114"><dt>**IMF\_SMODE\_NONE**</dt></span></span> </dl>                            | <span data-ttu-id="95c4a-115">Keine Neigung.</span><span class="sxs-lookup"><span data-stu-id="95c4a-115">No bias.</span></span><br/>                        |



 

</dd> <dt>

<span data-ttu-id="95c4a-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95c4a-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95c4a-117">Dieser Wert muss mit dem Wert von *wParam* identisch sein.</span><span class="sxs-lookup"><span data-stu-id="95c4a-117">This must be the same value as *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95c4a-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95c4a-118">Return value</span></span>

<span data-ttu-id="95c4a-119">Diese Meldung gibt die neue Einstellung für den IME-Modus zurück.</span><span class="sxs-lookup"><span data-stu-id="95c4a-119">This message returns the new IME mode bias setting.</span></span>

## <a name="remarks"></a><span data-ttu-id="95c4a-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95c4a-120">Remarks</span></span>

<span data-ttu-id="95c4a-121">Wenn der IME eine Liste alternativer Optionen für einen Satz von Zeichen generiert, legt diese Meldung die Kriterien fest, mit denen einige der Optionen oben in der Liste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="95c4a-121">When the IME generates a list of alternative choices for a set of characters, this message sets the criteria by which some of the choices will appear at the top of the list.</span></span>

<span data-ttu-id="95c4a-122">Um den TSF-Modus (Text Services Framework) festzulegen, verwenden Sie [**EM \_ setctfmodebias**](em-setctfmodebias.md).</span><span class="sxs-lookup"><span data-stu-id="95c4a-122">To set the Text Services Framework (TSF) mode bias, use [**EM\_SETCTFMODEBIAS**](em-setctfmodebias.md).</span></span>

<span data-ttu-id="95c4a-123">Die Anwendung sollte [**EM- \_ isime**](em-isime.md) aufrufen, bevor diese Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="95c4a-123">The application should call [**EM\_ISIME**](em-isime.md) before calling this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="95c4a-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95c4a-124">Requirements</span></span>



| <span data-ttu-id="95c4a-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95c4a-125">Requirement</span></span> | <span data-ttu-id="95c4a-126">Wert</span><span class="sxs-lookup"><span data-stu-id="95c4a-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95c4a-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95c4a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="95c4a-128">Nur Windows XP mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95c4a-128">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95c4a-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95c4a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="95c4a-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95c4a-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95c4a-131">Header</span><span class="sxs-lookup"><span data-stu-id="95c4a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="95c4a-132"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="95c4a-132"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95c4a-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95c4a-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="95c4a-134">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="95c4a-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="95c4a-135">**EM- \_ isime**</span><span class="sxs-lookup"><span data-stu-id="95c4a-135">**EM\_ISIME**</span></span>](em-isime.md)
</dt> <dt>

[<span data-ttu-id="95c4a-136">**EM \_ setctf modebias**</span><span class="sxs-lookup"><span data-stu-id="95c4a-136">**EM\_SETCTFMODEBIAS**</span></span>](em-setctfmodebias.md)
</dt> </dl>

 

 





