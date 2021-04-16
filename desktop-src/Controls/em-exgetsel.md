---
title: EM_EXGETSEL Meldung (RichEdit. h)
description: Ruft die Position des Anfangs-und des Endzeichens der Auswahl in einem Rich-Edit-Steuerelement ab.
ms.assetid: 60fcf13e-6c45-4f4e-9b54-70f0985122fb
keywords:
- Windows-Steuerelemente für EM_EXGETSEL Meldung
topic_type:
- apiref
api_name:
- EM_EXGETSEL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b97fb43a76f0f8ac91dd16c0cfa5700c5431eb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477595"
---
# <a name="em_exgetsel-message"></a><span data-ttu-id="ba46f-104">EM \_ exgetsel-Meldung</span><span class="sxs-lookup"><span data-stu-id="ba46f-104">EM\_EXGETSEL message</span></span>

<span data-ttu-id="ba46f-105">Ruft die Position des Anfangs-und des Endzeichens der Auswahl in einem Rich-Edit-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="ba46f-105">Retrieves the starting and ending character positions of the selection in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ba46f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba46f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba46f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ba46f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba46f-108">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="ba46f-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ba46f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ba46f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba46f-110">Eine [**charrange**](/windows/desktop/api/Richedit/ns-richedit-charrange) -Struktur, die den Auswahlbereich empfängt.</span><span class="sxs-lookup"><span data-stu-id="ba46f-110">A [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) structure that receives the selection range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba46f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ba46f-111">Return value</span></span>

<span data-ttu-id="ba46f-112">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ba46f-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba46f-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba46f-113">Requirements</span></span>



| <span data-ttu-id="ba46f-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba46f-114">Requirement</span></span> | <span data-ttu-id="ba46f-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ba46f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba46f-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ba46f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ba46f-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ba46f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ba46f-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ba46f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ba46f-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ba46f-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ba46f-120">Header</span><span class="sxs-lookup"><span data-stu-id="ba46f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba46f-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba46f-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba46f-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba46f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba46f-123">**Zeichenbereich**</span><span class="sxs-lookup"><span data-stu-id="ba46f-123">**CHARRANGE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charrange)
</dt> </dl>

 

 





