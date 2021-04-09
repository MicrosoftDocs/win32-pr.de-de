---
title: EM_GETPARAFORMAT Meldung (RichEdit. h)
description: Ruft die Absatz Formatierung der aktuellen Auswahl in einem Rich-Edit-Steuerelement ab.
ms.assetid: 79a7d34f-5da1-452d-b31f-b2eec913f5cb
keywords:
- Windows-Steuerelemente für EM_GETPARAFORMAT Meldung
topic_type:
- apiref
api_name:
- EM_GETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49060861a955e85d153fc9041c9b364db109f83a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957005"
---
# <a name="em_getparaformat-message"></a><span data-ttu-id="1bcc7-104">EM \_ GetParaFormat-Meldung</span><span class="sxs-lookup"><span data-stu-id="1bcc7-104">EM\_GETPARAFORMAT message</span></span>

<span data-ttu-id="1bcc7-105">Ruft die Absatz Formatierung der aktuellen Auswahl in einem Rich-Edit-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="1bcc7-105">Retrieves the paragraph formatting of the current selection in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1bcc7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1bcc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bcc7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1bcc7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1bcc7-108">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1bcc7-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1bcc7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1bcc7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1bcc7-110">Ein Zeiger auf eine [**paraformat**](/windows/desktop/api/Richedit/ns-richedit-paraformat) -Struktur, die die Absatz Formatierungs Attribute der aktuellen Auswahl empfängt.</span><span class="sxs-lookup"><span data-stu-id="1bcc7-110">Pointer to a [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure that receives the paragraph formatting attributes of the current selection.</span></span>

<span data-ttu-id="1bcc7-111">Wenn mehr als ein Absatz ausgewählt ist, empfängt die Struktur die Attribute des ersten Absatzes, und der **dwMask** -Member gibt an, welche Attribute in der gesamten Auswahl konsistent sind.</span><span class="sxs-lookup"><span data-stu-id="1bcc7-111">If more than one paragraph is selected, the structure receives the attributes of the first paragraph, and the **dwMask** member specifies which attributes are consistent throughout the entire selection.</span></span>

<span data-ttu-id="1bcc7-112">Microsoft Rich Edit 2,0 und höher: dieser Parameter kann ein Zeiger auf eine [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) -Struktur sein, die eine Erweiterung der [**paraformat**](/windows/desktop/api/Richedit/ns-richedit-paraformat) -Struktur ist.</span><span class="sxs-lookup"><span data-stu-id="1bcc7-112">Microsoft Rich Edit 2.0 and later: This parameter can be a pointer to a [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) structure, which is an extension of the [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure.</span></span> <span data-ttu-id="1bcc7-113">Vor dem Senden der **EM \_ GetParaFormat** -Meldung legen Sie den **CBSIZE** -Member der Struktur so fest, dass die Version der Struktur angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1bcc7-113">Before sending the **EM\_GETPARAFORMAT** message, set the structure's **cbSize** member to indicate the version of the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bcc7-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1bcc7-114">Return value</span></span>

<span data-ttu-id="1bcc7-115">Diese Meldung gibt den Wert des **dwMask** -Members der [**paraformat**](/windows/desktop/api/Richedit/ns-richedit-paraformat) -Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="1bcc7-115">This message returns the value of the **dwMask** member of the [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bcc7-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1bcc7-116">Requirements</span></span>



| <span data-ttu-id="1bcc7-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1bcc7-117">Requirement</span></span> | <span data-ttu-id="1bcc7-118">Wert</span><span class="sxs-lookup"><span data-stu-id="1bcc7-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1bcc7-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1bcc7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1bcc7-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1bcc7-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1bcc7-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1bcc7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1bcc7-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1bcc7-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1bcc7-123">Header</span><span class="sxs-lookup"><span data-stu-id="1bcc7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bcc7-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bcc7-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bcc7-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1bcc7-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="1bcc7-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="1bcc7-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1bcc7-127">**Paraformat**</span><span class="sxs-lookup"><span data-stu-id="1bcc7-127">**PARAFORMAT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[<span data-ttu-id="1bcc7-128">**PARAFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="1bcc7-128">**PARAFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 





