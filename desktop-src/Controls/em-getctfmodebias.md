---
title: EM_GETCTFMODEBIAS Meldung (RichEdit. h)
description: Ruft die biaswerte des Text Dienste-frameworkmodus für ein Microsoft Rich Edit-Steuerelement ab.
ms.assetid: 2421d37d-169d-480f-a5f7-4c6033ca6c1a
keywords:
- Windows-Steuerelemente für EM_GETCTFMODEBIAS Meldung
topic_type:
- apiref
api_name:
- EM_GETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109d5eabbddca1c13fefae99c29d8c550fbd274e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104042"
---
# <a name="em_getctfmodebias-message"></a><span data-ttu-id="d6db1-104">EM \_ getctf modebias-Nachricht</span><span class="sxs-lookup"><span data-stu-id="d6db1-104">EM\_GETCTFMODEBIAS message</span></span>

<span data-ttu-id="d6db1-105">Ruft die biaswerte des Text Dienste-frameworkmodus für ein Microsoft Rich Edit-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="d6db1-105">Gets the Text Services Framework mode bias values for a Microsoft Rich Edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d6db1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6db1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6db1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d6db1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d6db1-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="d6db1-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d6db1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d6db1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d6db1-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="d6db1-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6db1-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6db1-111">Return value</span></span>

<span data-ttu-id="d6db1-112">Der aktuelle Wert des Text Services-frameworkmodus.</span><span class="sxs-lookup"><span data-stu-id="d6db1-112">The current Text Services Framework mode bias value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6db1-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6db1-113">Remarks</span></span>

<span data-ttu-id="d6db1-114">Um die Verschiebung des IME-Modus abzurufen, aufrufen Sie [**EM \_ getimemodebias**](em-getimemodebias.md).</span><span class="sxs-lookup"><span data-stu-id="d6db1-114">To get the IME mode bias, call [**EM\_GETIMEMODEBIAS**](em-getimemodebias.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6db1-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6db1-115">Requirements</span></span>



| <span data-ttu-id="d6db1-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6db1-116">Requirement</span></span> | <span data-ttu-id="d6db1-117">Wert</span><span class="sxs-lookup"><span data-stu-id="d6db1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d6db1-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d6db1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d6db1-119">Nur Windows XP mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6db1-119">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d6db1-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d6db1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d6db1-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6db1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d6db1-122">Header</span><span class="sxs-lookup"><span data-stu-id="d6db1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6db1-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6db1-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6db1-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6db1-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="d6db1-125">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="d6db1-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d6db1-126">**EM \_ setctf modebias**</span><span class="sxs-lookup"><span data-stu-id="d6db1-126">**EM\_SETCTFMODEBIAS**</span></span>](em-setctfmodebias.md)
</dt> <dt>

[<span data-ttu-id="d6db1-127">**EM \_ getimemodebias**</span><span class="sxs-lookup"><span data-stu-id="d6db1-127">**EM\_GETIMEMODEBIAS**</span></span>](em-getimemodebias.md)
</dt> </dl>

 

 





