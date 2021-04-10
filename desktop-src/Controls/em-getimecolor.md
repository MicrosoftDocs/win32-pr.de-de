---
title: EM_GETIMECOLOR Meldung (RichEdit. h)
description: Ruft die-Kompositions Farbe des Eingabemethoden-Editors (IME) ab.
ms.assetid: 788ac56c-f2d8-4e9a-8829-b92dcd76e6de
keywords:
- Windows-Steuerelemente für EM_GETIMECOLOR Meldung
topic_type:
- apiref
api_name:
- EM_GETIMECOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8a19061651787ff94575f8bc64a69f06d445a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956826"
---
# <a name="em_getimecolor-message"></a><span data-ttu-id="3ec9c-104">EM \_ getimecolor-Meldung</span><span class="sxs-lookup"><span data-stu-id="3ec9c-104">EM\_GETIMECOLOR message</span></span>

<span data-ttu-id="3ec9c-105">Ruft die-Kompositions Farbe des Eingabemethoden-Editors (IME) ab.</span><span class="sxs-lookup"><span data-stu-id="3ec9c-105">Retrieves the Input Method Editor (IME) composition color.</span></span>

> [!Note]  
> <span data-ttu-id="3ec9c-106">Diese Meldung wird nur in asiatischen Sprachversionen von Microsoft Rich Edit 1,0 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3ec9c-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="3ec9c-107">Sie wird in höheren Versionen der Rich-Edit-Version nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3ec9c-107">It is not supported in any later versions of Rich Edit.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="3ec9c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ec9c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ec9c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3ec9c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3ec9c-110">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="3ec9c-110">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3ec9c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3ec9c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3ec9c-112">Ein Array aus vier Elementen von [**compcolor**](/windows/desktop/api/Richedit/ns-richedit-compcolor) -Strukturen, das die Kompositions Farbe empfängt.</span><span class="sxs-lookup"><span data-stu-id="3ec9c-112">A four-element array of [**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) structures that receives the composition color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ec9c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3ec9c-113">Return value</span></span>

<span data-ttu-id="3ec9c-114">Wenn der Vorgang erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="3ec9c-114">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="3ec9c-115">Wenn der Vorgang fehlschlägt, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="3ec9c-115">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ec9c-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3ec9c-116">Requirements</span></span>



| <span data-ttu-id="3ec9c-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ec9c-117">Requirement</span></span> | <span data-ttu-id="3ec9c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="3ec9c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3ec9c-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3ec9c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3ec9c-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3ec9c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3ec9c-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3ec9c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3ec9c-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3ec9c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3ec9c-123">Header</span><span class="sxs-lookup"><span data-stu-id="3ec9c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ec9c-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ec9c-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ec9c-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ec9c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ec9c-126">**Compcolor**</span><span class="sxs-lookup"><span data-stu-id="3ec9c-126">**COMPCOLOR**</span></span>](/windows/desktop/api/Richedit/ns-richedit-compcolor)
</dt> </dl>

 

 





