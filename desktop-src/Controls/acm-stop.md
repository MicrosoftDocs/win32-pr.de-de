---
title: ACM_STOP Meldung (kommstrg. h)
description: Beendet die Wiedergabe eines AVI-Clips in einem Animations Steuerelement. Sie können diese Nachricht explizit oder mithilfe des Makros animieren- \_ Ende senden.
ms.assetid: ba39a579-665e-4d45-8f1f-f190acd76db7
keywords:
- Windows-Steuerelemente für ACM_STOP Meldung
topic_type:
- apiref
api_name:
- ACM_STOP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e81cfc92ac2778ae559fcd9fb8db2b0cd7bb866
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103138"
---
# <a name="acm_stop-message"></a><span data-ttu-id="114ec-105">ACM- \_ Stoppmeldung</span><span class="sxs-lookup"><span data-stu-id="114ec-105">ACM\_STOP message</span></span>

<span data-ttu-id="114ec-106">Beendet die Wiedergabe eines AVI-Clips in einem Animations Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="114ec-106">Stops playing an AVI clip in an animation control.</span></span> <span data-ttu-id="114ec-107">Sie können diese Nachricht explizit oder mithilfe des Makros [**animieren- \_ Ende**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop) senden.</span><span class="sxs-lookup"><span data-stu-id="114ec-107">You can send this message explicitly or by using the [**Animate\_Stop**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="114ec-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="114ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="114ec-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="114ec-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="114ec-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="114ec-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="114ec-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="114ec-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="114ec-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="114ec-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="114ec-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="114ec-113">Return value</span></span>

<span data-ttu-id="114ec-114">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="114ec-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="114ec-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="114ec-115">Requirements</span></span>



| <span data-ttu-id="114ec-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="114ec-116">Requirement</span></span> | <span data-ttu-id="114ec-117">Wert</span><span class="sxs-lookup"><span data-stu-id="114ec-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="114ec-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="114ec-118">Minimum supported client</span></span><br/> | <span data-ttu-id="114ec-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="114ec-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="114ec-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="114ec-120">Minimum supported server</span></span><br/> | <span data-ttu-id="114ec-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="114ec-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="114ec-122">Header</span><span class="sxs-lookup"><span data-stu-id="114ec-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="114ec-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="114ec-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





