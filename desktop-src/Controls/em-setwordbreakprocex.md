---
title: EM_SETWORDBREAKPROCEX Meldung (RichEdit. h)
description: Legt die erweiterte Wort Umbruch Prozedur für ein Rich-Edit-Steuerelement fest.
ms.assetid: 2b45f747-ae15-470b-a786-98d8135289da
keywords:
- Windows-Steuerelemente für EM_SETWORDBREAKPROCEX Meldung
topic_type:
- apiref
api_name:
- EM_SETWORDBREAKPROCEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5973836ae173c1a61537b7d3b085fe29c168971f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949708"
---
# <a name="em_setwordbreakprocex-message"></a><span data-ttu-id="abc28-104">EM \_ setwordbreakprocex-Meldung</span><span class="sxs-lookup"><span data-stu-id="abc28-104">EM\_SETWORDBREAKPROCEX message</span></span>

<span data-ttu-id="abc28-105">Legt die erweiterte Wort Umbruch Prozedur für ein Rich-Edit-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="abc28-105">Sets the extended word-break procedure for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="abc28-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="abc28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abc28-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="abc28-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="abc28-108">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="abc28-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="abc28-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="abc28-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="abc28-110">Zeiger auf eine [*editwordbreakprocex*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) -Funktion oder **null** , um die Standardprozedur zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="abc28-110">Pointer to an [*EditWordBreakProcEx*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) function, or **NULL** to use the default procedure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abc28-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="abc28-111">Return value</span></span>

<span data-ttu-id="abc28-112">Diese Meldung gibt die Adresse der vorherigen erweiterten Wort Umbruch Prozedur zurück.</span><span class="sxs-lookup"><span data-stu-id="abc28-112">This message returns the address of the previous extended word-break procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="abc28-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abc28-113">Requirements</span></span>



| <span data-ttu-id="abc28-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="abc28-114">Requirement</span></span> | <span data-ttu-id="abc28-115">Wert</span><span class="sxs-lookup"><span data-stu-id="abc28-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="abc28-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="abc28-116">Minimum supported client</span></span><br/> | <span data-ttu-id="abc28-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abc28-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="abc28-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="abc28-118">Minimum supported server</span></span><br/> | <span data-ttu-id="abc28-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abc28-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="abc28-120">Header</span><span class="sxs-lookup"><span data-stu-id="abc28-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="abc28-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="abc28-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abc28-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abc28-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="abc28-123">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="abc28-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="abc28-124">**Editwordbreakprocex**</span><span class="sxs-lookup"><span data-stu-id="abc28-124">**EditWordBreakProcEx**</span></span>](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex)
</dt> <dt>

[<span data-ttu-id="abc28-125">**EM \_ getwordbreakprocex**</span><span class="sxs-lookup"><span data-stu-id="abc28-125">**EM\_GETWORDBREAKPROCEX**</span></span>](em-getwordbreakprocex.md)
</dt> </dl>

 

 





