---
title: ACM_ISPLAYING Meldung (kommstrg. h)
description: Überprüft, ob ein Audio-Video Interleaved-Clip (AVI) wiedergegeben wird. Sie können diese Nachricht explizit senden oder das Animieren von \_ isplay-Makro verwenden.
ms.assetid: ebb0c92a-99d2-49c1-9de1-8bdbd032be3a
keywords:
- Windows-Steuerelemente für ACM_ISPLAYING Meldung
topic_type:
- apiref
api_name:
- ACM_ISPLAYING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f663872ce02b9520e3e033cb5bc5a3da12bb3c3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040317"
---
# <a name="acm_isplaying-message"></a><span data-ttu-id="c8b71-105">ACM- \_ isplay-Nachricht</span><span class="sxs-lookup"><span data-stu-id="c8b71-105">ACM\_ISPLAYING message</span></span>

<span data-ttu-id="c8b71-106">Überprüft, ob ein Audio-Video Interleaved-Clip (AVI) wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c8b71-106">Checks whether an Audio-Video Interleaved (AVI) clip is playing.</span></span> <span data-ttu-id="c8b71-107">Sie können diese Nachricht explizit senden oder das [**Animieren von \_ isplay**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="c8b71-107">You can send this message explicitly or use the [**Animate\_IsPlaying**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c8b71-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b71-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8b71-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c8b71-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8b71-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="c8b71-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c8b71-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8b71-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8b71-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="c8b71-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8b71-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c8b71-113">Return value</span></span>

<span data-ttu-id="c8b71-114">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="c8b71-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8b71-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8b71-115">Requirements</span></span>



| <span data-ttu-id="c8b71-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8b71-116">Requirement</span></span> | <span data-ttu-id="c8b71-117">Wert</span><span class="sxs-lookup"><span data-stu-id="c8b71-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c8b71-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c8b71-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c8b71-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8b71-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c8b71-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c8b71-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c8b71-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8b71-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c8b71-122">Header</span><span class="sxs-lookup"><span data-stu-id="c8b71-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8b71-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8b71-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





