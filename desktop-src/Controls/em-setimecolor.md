---
title: EM_SETIMECOLOR Meldung (RichEdit. h)
description: Legt die Zusammensetzung der Eingabemethoden-Editor (IME) für ein Rich-Edit-Steuerelement fest.
ms.assetid: ea5449c9-7d0f-4340-8e3e-1e0b77d443f6
keywords:
- Windows-Steuerelemente für EM_SETIMECOLOR Meldung
topic_type:
- apiref
api_name:
- EM_SETIMECOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c020bb3af2b1197afc005bd0b6efec82b609b88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477322"
---
# <a name="em_setimecolor-message"></a><span data-ttu-id="10b98-104">EM- \_ Zeit Farb Meldung</span><span class="sxs-lookup"><span data-stu-id="10b98-104">EM\_SETIMECOLOR message</span></span>

<span data-ttu-id="10b98-105">Legt die Zusammensetzung der Eingabemethoden-Editor (IME) für ein Rich-Edit-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="10b98-105">Sets the Input Method Editor (IME) composition color for a rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="10b98-106">Diese Meldung wird nur in asiatischen Sprachversionen von Microsoft Rich Edit 1,0 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="10b98-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="10b98-107">Sie wird in späteren Versionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="10b98-107">It is not supported in any later versions.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="10b98-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="10b98-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10b98-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="10b98-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10b98-110">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="10b98-110">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="10b98-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="10b98-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10b98-112">Ein Zeiger auf eine [**compcolor**](/windows/desktop/api/Richedit/ns-richedit-compcolor) -Struktur, die die festzulegende Kompositions Farbe enthält.</span><span class="sxs-lookup"><span data-stu-id="10b98-112">Pointer to a [**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) structure that contains the composition color to be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10b98-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="10b98-113">Return value</span></span>

<span data-ttu-id="10b98-114">Wenn der Vorgang erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="10b98-114">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="10b98-115">Wenn der Vorgang fehlschlägt, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="10b98-115">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="10b98-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10b98-116">Requirements</span></span>



| <span data-ttu-id="10b98-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10b98-117">Requirement</span></span> | <span data-ttu-id="10b98-118">Wert</span><span class="sxs-lookup"><span data-stu-id="10b98-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10b98-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="10b98-119">Minimum supported client</span></span><br/> | <span data-ttu-id="10b98-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10b98-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="10b98-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="10b98-121">Minimum supported server</span></span><br/> | <span data-ttu-id="10b98-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10b98-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="10b98-123">Header</span><span class="sxs-lookup"><span data-stu-id="10b98-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="10b98-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="10b98-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10b98-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10b98-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="10b98-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="10b98-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="10b98-127">**EM \_ getimecolor**</span><span class="sxs-lookup"><span data-stu-id="10b98-127">**EM\_GETIMECOLOR**</span></span>](em-getimecolor.md)
</dt> <dt>

[<span data-ttu-id="10b98-128">**Compcolor**</span><span class="sxs-lookup"><span data-stu-id="10b98-128">**COMPCOLOR**</span></span>](/windows/desktop/api/Richedit/ns-richedit-compcolor)
</dt> </dl>

 

 





