---
title: EM_SETHYPHENATEINFO Meldung (RichEdit. h)
description: Legt die Methode fest, mit der ein Rich-Edit-Steuerelement eine Bindestriche hat
ms.assetid: 67126cb8-ab50-49a9-b32f-2245debf2fe3
keywords:
- Windows-Steuerelemente für EM_SETHYPHENATEINFO Meldung
topic_type:
- apiref
api_name:
- EM_SETHYPHENATEINFO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8369d463ae03e9410347ab58a50346625e3de47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859172"
---
# <a name="em_sethyphenateinfo-message"></a><span data-ttu-id="6db90-104">EM- \_ logphenateinfo-Nachricht</span><span class="sxs-lookup"><span data-stu-id="6db90-104">EM\_SETHYPHENATEINFO message</span></span>

<span data-ttu-id="6db90-105">Legt die Methode fest, mit der ein Rich-Edit-Steuerelement eine Bindestriche hat</span><span class="sxs-lookup"><span data-stu-id="6db90-105">Sets the way a rich edit control does hyphenation.</span></span>

## <a name="parameters"></a><span data-ttu-id="6db90-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6db90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6db90-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6db90-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6db90-108">Zeiger auf eine [**hyphenateingefo**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="6db90-108">Pointer to a [**HYPHENATEINFO**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6db90-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6db90-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6db90-110">Nicht verwendet, muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="6db90-110">Not used, must be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6db90-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6db90-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6db90-112">Um die Bindestriche zu aktivieren, muss der Client " [**EM \_ settypographyoptions**](em-settypographyoptions.md)" aufzurufen, wobei " \_ advancedtypografie" angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6db90-112">To enable hyphenation, the client must call [**EM\_SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md), specifying TO\_ADVANCEDTYPOGRAPHY.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6db90-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6db90-113">Requirements</span></span>



| <span data-ttu-id="6db90-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6db90-114">Requirement</span></span> | <span data-ttu-id="6db90-115">Wert</span><span class="sxs-lookup"><span data-stu-id="6db90-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6db90-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6db90-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6db90-117">Nur Windows XP mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6db90-117">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6db90-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6db90-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6db90-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6db90-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6db90-120">Header</span><span class="sxs-lookup"><span data-stu-id="6db90-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6db90-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6db90-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6db90-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6db90-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6db90-123">**EM \_ gethyphenateingefo**</span><span class="sxs-lookup"><span data-stu-id="6db90-123">**EM\_GETHYPHENATEINFO**</span></span>](em-gethyphenateinfo.md)
</dt> </dl>

 

 





