---
title: HDM_SETFILTERCHANGETIMEOUT Meldung (kommstrg. h)
description: Legt das Timeout Intervall zwischen dem Zeitpunkt fest, an dem eine Änderung in den Filter Attributen stattfindet, und dem Veröffentlichen einer Hdn \_ FilterChange-Benachrichtigung. Sie können diese Nachricht explizit senden oder das-Header \_ setfilterchangetimeout-Makro verwenden.
ms.assetid: 9bc8e0e7-d7c1-4dd6-9d39-6ae937f19d60
keywords:
- Windows-Steuerelemente für HDM_SETFILTERCHANGETIMEOUT Meldung
topic_type:
- apiref
api_name:
- HDM_SETFILTERCHANGETIMEOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9876634d12cd15001c296151694cb755ed1b34e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040857"
---
# <a name="hdm_setfilterchangetimeout-message"></a><span data-ttu-id="e5af3-105">HDM- \_ setfilterchangetimeout-Meldung</span><span class="sxs-lookup"><span data-stu-id="e5af3-105">HDM\_SETFILTERCHANGETIMEOUT message</span></span>

<span data-ttu-id="e5af3-106">Legt das Timeout Intervall zwischen dem Zeitpunkt fest, an dem eine Änderung in den Filter Attributen stattfindet, und dem Veröffentlichen einer [Hdn \_ FilterChange](hdn-filterchange.md) -Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="e5af3-106">Sets the timeout interval between the time a change takes place in the filter attributes and the posting of an [HDN\_FILTERCHANGE](hdn-filterchange.md) notification.</span></span> <span data-ttu-id="e5af3-107">Sie können diese Nachricht explizit senden oder das- [**Header \_ setfilterchangetimeout**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfilterchangetimeout) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="e5af3-107">You can send this message explicitly or use the [**Header\_SetFilterChangeTimeout**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfilterchangetimeout) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e5af3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5af3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5af3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e5af3-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e5af3-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="e5af3-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e5af3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e5af3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5af3-112">Der Timeoutwert in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="e5af3-112">The timeout value, in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5af3-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e5af3-113">Return value</span></span>

<span data-ttu-id="e5af3-114">Gibt den Index des geänderten Filter Steuer Elements zurück.</span><span class="sxs-lookup"><span data-stu-id="e5af3-114">Returns the index of the filter control being modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5af3-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5af3-115">Requirements</span></span>



| <span data-ttu-id="e5af3-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e5af3-116">Requirement</span></span> | <span data-ttu-id="e5af3-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e5af3-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e5af3-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e5af3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e5af3-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e5af3-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e5af3-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e5af3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e5af3-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e5af3-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e5af3-122">Header</span><span class="sxs-lookup"><span data-stu-id="e5af3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5af3-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5af3-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5af3-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5af3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5af3-125">Hdn- \_ Filter Änderung</span><span class="sxs-lookup"><span data-stu-id="e5af3-125">HDN\_FILTERCHANGE</span></span>](hdn-filterchange.md)
</dt> </dl>

 

 





