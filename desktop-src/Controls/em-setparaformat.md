---
title: EM_SETPARAFORMAT Meldung (RichEdit. h)
description: Legt die Absatz Formatierung für die aktuelle Auswahl in einem Rich-Edit-Steuerelement fest.
ms.assetid: 2d612e1b-1489-4055-929b-e0b2719f6ec2
keywords:
- Windows-Steuerelemente für EM_SETPARAFORMAT Meldung
topic_type:
- apiref
api_name:
- EM_SETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8780ed79650a90a8d85ee8025dbe97e9af36aa1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476338"
---
# <a name="em_setparaformat-message"></a><span data-ttu-id="f6922-104">EM \_ SetParaFormat-Meldung</span><span class="sxs-lookup"><span data-stu-id="f6922-104">EM\_SETPARAFORMAT message</span></span>

<span data-ttu-id="f6922-105">Legt die Absatz Formatierung für die aktuelle Auswahl in einem Rich-Edit-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="f6922-105">Sets the paragraph formatting for the current selection in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f6922-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6922-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6922-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f6922-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6922-108">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="f6922-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f6922-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f6922-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6922-110">Ein Zeiger auf eine [**paraformat**](/windows/desktop/api/Richedit/ns-richedit-paraformat) -Struktur, die die neuen Absatz Formatierungs Attribute angibt.</span><span class="sxs-lookup"><span data-stu-id="f6922-110">Pointer to a [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure specifying the new paragraph formatting attributes.</span></span> <span data-ttu-id="f6922-111">Nur die Attribute, die vom **dwMask** -Member angegeben werden, werden geändert.</span><span class="sxs-lookup"><span data-stu-id="f6922-111">Only the attributes specified by the **dwMask** member are changed.</span></span>

<span data-ttu-id="f6922-112">Microsoft Rich Edit 2,0 und höher: dieser Parameter kann ein Zeiger auf eine [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) -Struktur sein, die eine Erweiterung der [**paraformat**](/windows/desktop/api/Richedit/ns-richedit-paraformat) -Struktur ist.</span><span class="sxs-lookup"><span data-stu-id="f6922-112">Microsoft Rich Edit 2.0 and later: This parameter can be a pointer to a [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) structure, which is an extension of the [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure.</span></span> <span data-ttu-id="f6922-113">Vor dem Senden der **EM- \_ SetParaFormat** -Meldung legen Sie den **CBSIZE** -Member der Struktur fest, um die Version der Struktur anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f6922-113">Before sending the **EM\_SETPARAFORMAT** message, set the structure's **cbSize** member to indicate the version of the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6922-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f6922-114">Return value</span></span>

<span data-ttu-id="f6922-115">Wenn der Vorgang erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f6922-115">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="f6922-116">Wenn der Vorgang fehlschlägt, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f6922-116">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6922-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6922-117">Requirements</span></span>



| <span data-ttu-id="f6922-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f6922-118">Requirement</span></span> | <span data-ttu-id="f6922-119">Wert</span><span class="sxs-lookup"><span data-stu-id="f6922-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f6922-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f6922-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f6922-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f6922-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f6922-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f6922-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f6922-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f6922-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f6922-124">Header</span><span class="sxs-lookup"><span data-stu-id="f6922-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6922-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6922-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6922-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6922-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="f6922-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="f6922-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f6922-128">**Paraformat**</span><span class="sxs-lookup"><span data-stu-id="f6922-128">**PARAFORMAT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[<span data-ttu-id="f6922-129">**PARAFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="f6922-129">**PARAFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 





