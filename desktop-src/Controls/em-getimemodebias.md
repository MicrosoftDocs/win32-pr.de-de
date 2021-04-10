---
title: EM_GETIMEMODEBIAS Meldung (RichEdit. h)
description: Ruft den IME-Modus (Eingabemethoden-Editor) für ein Microsoft Rich Edit-Steuerelement ab.
ms.assetid: e8ca899f-3423-4814-86e9-133dfd11f9a6
keywords:
- Windows-Steuerelemente für EM_GETIMEMODEBIAS Meldung
topic_type:
- apiref
api_name:
- EM_GETIMEMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea13e151ae9d487340ee440e3b123ae70b437a02
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040804"
---
# <a name="em_getimemodebias-message"></a><span data-ttu-id="a7efd-104">EM \_ getimemodebias-Nachricht</span><span class="sxs-lookup"><span data-stu-id="a7efd-104">EM\_GETIMEMODEBIAS message</span></span>

<span data-ttu-id="a7efd-105">Ruft den IME-Modus (Eingabemethoden-Editor) für ein Microsoft Rich Edit-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="a7efd-105">Retrieves the Input Method Editor (IME) mode bias for a Microsoft Rich Edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a7efd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7efd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7efd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a7efd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a7efd-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="a7efd-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a7efd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a7efd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a7efd-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="a7efd-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7efd-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a7efd-111">Return value</span></span>

<span data-ttu-id="a7efd-112">Diese Meldung gibt die aktuelle Einstellung für den IME-Modus zurück.</span><span class="sxs-lookup"><span data-stu-id="a7efd-112">This message returns the current IME mode bias setting.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7efd-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7efd-113">Remarks</span></span>

<span data-ttu-id="a7efd-114">Verwenden Sie [**EM \_ getctfmodebias**](em-getctfmodebias.md), um den Text Dienst-Framework-Modus zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a7efd-114">To get the Text Services Framework mode bias, use [**EM\_GETCTFMODEBIAS**](em-getctfmodebias.md).</span></span>

<span data-ttu-id="a7efd-115">Die Anwendung sollte [**EM- \_ isime**](em-isime.md) aufrufen, bevor diese Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a7efd-115">The application should call [**EM\_ISIME**](em-isime.md) before calling this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7efd-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7efd-116">Requirements</span></span>



| <span data-ttu-id="a7efd-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7efd-117">Requirement</span></span> | <span data-ttu-id="a7efd-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a7efd-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a7efd-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a7efd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a7efd-120">Nur Windows XP mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7efd-120">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a7efd-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a7efd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a7efd-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7efd-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a7efd-123">Header</span><span class="sxs-lookup"><span data-stu-id="a7efd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7efd-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7efd-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7efd-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7efd-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="a7efd-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="a7efd-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a7efd-127">**EM- \_ isime**</span><span class="sxs-lookup"><span data-stu-id="a7efd-127">**EM\_ISIME**</span></span>](em-isime.md)
</dt> <dt>

[<span data-ttu-id="a7efd-128">**EM \_ getctf modebias**</span><span class="sxs-lookup"><span data-stu-id="a7efd-128">**EM\_GETCTFMODEBIAS**</span></span>](em-getctfmodebias.md)
</dt> </dl>

 

 





