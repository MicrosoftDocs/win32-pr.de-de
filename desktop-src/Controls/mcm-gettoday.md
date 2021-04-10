---
title: MCM_GETTODAY Meldung (kommstrg. h)
description: Ruft die Datumsinformationen für das Datum ab, das als \ 0034; heute \ 0034; angegeben ist. für ein Monatskalender-Steuerelement. Sie können diese Nachricht explizit oder mit dem monthcal \_ gettoday-Makro senden.
ms.assetid: a79feb57-6aa3-4c96-95f3-7018b6b8327f
keywords:
- Windows-Steuerelemente für MCM_GETTODAY Meldung
topic_type:
- apiref
api_name:
- MCM_GETTODAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21538af3c573b3d972b7f16bfe024e0d36211644
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956539"
---
# <a name="mcm_gettoday-message"></a><span data-ttu-id="bbd06-105">MCM \_ gettoday-Meldung</span><span class="sxs-lookup"><span data-stu-id="bbd06-105">MCM\_GETTODAY message</span></span>

<span data-ttu-id="bbd06-106">Ruft die Datumsinformationen für das als "heute" angegebene Datum für ein Monatskalender-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="bbd06-106">Retrieves the date information for the date specified as "today" for a month calendar control.</span></span> <span data-ttu-id="bbd06-107">Sie können diese Nachricht explizit oder mit dem [**monthcal \_ gettoday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_gettoday) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="bbd06-107">You can send this message explicitly or by using the [**MonthCal\_GetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_gettoday) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bbd06-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bbd06-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbd06-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bbd06-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bbd06-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="bbd06-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bbd06-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bbd06-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bbd06-112">Zeiger auf eine [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur, die die Datumsinformationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="bbd06-112">Pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that will receive the date information.</span></span> <span data-ttu-id="bbd06-113">Dieser Parameter muss eine gültige Adresse sein und darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="bbd06-113">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbd06-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bbd06-114">Return value</span></span>

<span data-ttu-id="bbd06-115">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="bbd06-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbd06-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bbd06-116">Requirements</span></span>



| <span data-ttu-id="bbd06-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bbd06-117">Requirement</span></span> | <span data-ttu-id="bbd06-118">Wert</span><span class="sxs-lookup"><span data-stu-id="bbd06-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bbd06-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bbd06-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bbd06-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bbd06-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bbd06-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bbd06-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bbd06-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bbd06-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bbd06-123">Header</span><span class="sxs-lookup"><span data-stu-id="bbd06-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbd06-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbd06-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbd06-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bbd06-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbd06-126">Uhrzeiten im Monatskalender-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="bbd06-126">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

