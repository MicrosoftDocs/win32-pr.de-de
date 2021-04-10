---
title: EM_GETIMECOMPTEXT Meldung (RichEdit. h)
description: Ruft den Eingabemethoden-Editor (IME)-Kompositions Text ab.
ms.assetid: 1516305c-5f87-4ae0-97db-8709c71abacc
keywords:
- Windows-Steuerelemente für EM_GETIMECOMPTEXT Meldung
topic_type:
- apiref
api_name:
- EM_GETIMECOMPTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 834c55d6b5e40de7dcacfeb3e2d0c2e0878a0f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956825"
---
# <a name="em_getimecomptext-message"></a><span data-ttu-id="95044-104">EM \_ getimecomptext-Nachricht</span><span class="sxs-lookup"><span data-stu-id="95044-104">EM\_GETIMECOMPTEXT message</span></span>

<span data-ttu-id="95044-105">Ruft den Eingabemethoden-Editor (IME)-Kompositions Text ab.</span><span class="sxs-lookup"><span data-stu-id="95044-105">Retrieves the Input Method Editor (IME) composition text.</span></span>

## <a name="parameters"></a><span data-ttu-id="95044-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="95044-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95044-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="95044-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95044-108">Die [**imecomptext**](/windows/desktop/api/Richedit/ns-richedit-imecomptext) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="95044-108">The [**IMECOMPTEXT**](/windows/desktop/api/Richedit/ns-richedit-imecomptext) structure.</span></span>

</dd> <dt>

<span data-ttu-id="95044-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95044-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95044-110">Der Puffer, der den Kompositions Text empfängt.</span><span class="sxs-lookup"><span data-stu-id="95044-110">The buffer that receives the composition text.</span></span> <span data-ttu-id="95044-111">Die Größe dieses Puffers ist im **CB** -Member der *wParam* -Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="95044-111">The size of this buffer is contained in the **cb** member of the *wParam* structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95044-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95044-112">Return value</span></span>

<span data-ttu-id="95044-113">Bei erfolgreicher Ausführung ist der Rückgabewert die Anzahl von Unicode-Zeichen, die in den Puffer kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="95044-113">If successful, the return value is the number of Unicode characters copied to the buffer.</span></span> <span data-ttu-id="95044-114">Andernfalls ist der Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="95044-114">Otherwise, it is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="95044-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95044-115">Remarks</span></span>

<span data-ttu-id="95044-116">Diese Meldung nimmt nur Unicode-Zeichen folgen an.</span><span class="sxs-lookup"><span data-stu-id="95044-116">This message only takes Unicode strings.</span></span>

<span data-ttu-id="95044-117">**Sicherheitswarnung:** Stellen Sie sicher, dass ein Puffer für die Größe der Eingabe ausreichend ist.</span><span class="sxs-lookup"><span data-stu-id="95044-117">**Security Warning:** Be sure to have a buffer sufficient for the size of the input.</span></span> <span data-ttu-id="95044-118">Wenn dies nicht der Fall ist, kann dies zu Problemen mit Ihrer Anwendung führen.</span><span class="sxs-lookup"><span data-stu-id="95044-118">Failure to do so could cause problems for your application.</span></span>

## <a name="requirements"></a><span data-ttu-id="95044-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95044-119">Requirements</span></span>



| <span data-ttu-id="95044-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95044-120">Requirement</span></span> | <span data-ttu-id="95044-121">Wert</span><span class="sxs-lookup"><span data-stu-id="95044-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95044-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95044-122">Minimum supported client</span></span><br/> | <span data-ttu-id="95044-123">Nur Windows XP mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95044-123">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95044-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95044-124">Minimum supported server</span></span><br/> | <span data-ttu-id="95044-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95044-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95044-126">Header</span><span class="sxs-lookup"><span data-stu-id="95044-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="95044-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="95044-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95044-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95044-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95044-129">**Imecomptext**</span><span class="sxs-lookup"><span data-stu-id="95044-129">**IMECOMPTEXT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-imecomptext)
</dt> </dl>

 

 





