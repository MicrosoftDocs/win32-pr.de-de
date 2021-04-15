---
title: MCM_GETCURSEL Meldung (kommstrg. h)
description: Ruft das aktuell ausgewählte Datum ab. Sie können diese Nachricht explizit oder mit dem monthcal \_ getcurrsel-Makro senden.
ms.assetid: d4edc9ed-7c92-4ec8-bfa1-8ae597826b3f
keywords:
- Windows-Steuerelemente für MCM_GETCURSEL Meldung
topic_type:
- apiref
api_name:
- MCM_GETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dece95c65e900119c7043c0d5eda22bf473e6c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477556"
---
# <a name="mcm_getcursel-message"></a><span data-ttu-id="f3646-105">MCM \_ getcurrsel-Meldung</span><span class="sxs-lookup"><span data-stu-id="f3646-105">MCM\_GETCURSEL message</span></span>

<span data-ttu-id="f3646-106">Ruft das aktuell ausgewählte Datum ab.</span><span class="sxs-lookup"><span data-stu-id="f3646-106">Retrieves the currently selected date.</span></span> <span data-ttu-id="f3646-107">Sie können diese Nachricht explizit oder mit dem [**monthcal \_ getcurrsel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcursel) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="f3646-107">You can send this message explicitly or by using the [**MonthCal\_GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f3646-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3646-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3646-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f3646-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f3646-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="f3646-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f3646-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f3646-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3646-112">Ein Zeiger auf eine [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur, die die aktuell ausgewählten Datumsinformationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="f3646-112">Pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that will receive the currently selected date information.</span></span> <span data-ttu-id="f3646-113">Dieser Parameter muss eine gültige Adresse sein und darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="f3646-113">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3646-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f3646-114">Return value</span></span>

<span data-ttu-id="f3646-115">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="f3646-115">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="f3646-116">Diese Meldung schlägt immer fehl, wenn Sie auf die Steuerelemente für Monatskalender angewendet wird, die auf den [**MCS- \_ MultiSelect**](month-calendar-control-styles.md) -Stil</span><span class="sxs-lookup"><span data-stu-id="f3646-116">This message will always fail when applied to month calendar controls set to the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3646-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3646-117">Requirements</span></span>



| <span data-ttu-id="f3646-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3646-118">Requirement</span></span> | <span data-ttu-id="f3646-119">Wert</span><span class="sxs-lookup"><span data-stu-id="f3646-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f3646-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f3646-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f3646-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3646-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f3646-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f3646-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f3646-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3646-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f3646-124">Header</span><span class="sxs-lookup"><span data-stu-id="f3646-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3646-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3646-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3646-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3646-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3646-127">Uhrzeiten im Monatskalender-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="f3646-127">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

