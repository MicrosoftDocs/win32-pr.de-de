---
title: MCM_GETSELRANGE Meldung (kommstrg. h)
description: Ruft Datumsinformationen ab, die die obere und untere Grenze des Datums Bereichs darstellen, der derzeit vom Benutzer ausgewählt wird. Sie können diese Nachricht explizit oder mit dem monthcal \_ getselrange-Makro senden.
ms.assetid: a0d0a0d5-a519-4495-a87a-2438c4590e4c
keywords:
- Windows-Steuerelemente für MCM_GETSELRANGE Meldung
topic_type:
- apiref
api_name:
- MCM_GETSELRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0d2f922b013a3eab525228bda4f5b99f33e70d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949701"
---
# <a name="mcm_getselrange-message"></a><span data-ttu-id="60828-105">MCM \_ getselrange-Nachricht</span><span class="sxs-lookup"><span data-stu-id="60828-105">MCM\_GETSELRANGE message</span></span>

<span data-ttu-id="60828-106">Ruft Datumsinformationen ab, die die obere und untere Grenze des Datums Bereichs darstellen, der derzeit vom Benutzer ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="60828-106">Retrieves date information that represents the upper and lower limits of the date range currently selected by the user.</span></span> <span data-ttu-id="60828-107">Sie können diese Nachricht explizit oder mit dem [**monthcal \_ getselrange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getselrange) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="60828-107">You can send this message explicitly or by using the [**MonthCal\_GetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getselrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="60828-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="60828-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60828-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="60828-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="60828-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="60828-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="60828-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="60828-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="60828-112">Zeiger auf ein zwei-Element-Array von [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Strukturen, das die unteren und oberen Grenzen der Auswahl des Benutzers empfängt.</span><span class="sxs-lookup"><span data-stu-id="60828-112">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that will receive the lower and upper limits of the user's selection.</span></span> <span data-ttu-id="60828-113">Die unteren und oberen Grenzwerte werden in *lprgsystimearray* \[ 0 \] bzw. *lprgsystimearray* \[ 1 platziert \] .</span><span class="sxs-lookup"><span data-stu-id="60828-113">The lower and upper limits are placed in *lprgSysTimeArray*\[0\] and *lprgSysTimeArray*\[1\], respectively.</span></span> <span data-ttu-id="60828-114">Dieser Parameter muss eine gültige Adresse sein und darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="60828-114">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60828-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="60828-115">Return value</span></span>

<span data-ttu-id="60828-116">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="60828-116">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="60828-117">**MCM \_ Getselrange** schlägt fehl, wenn es auf ein Monatskalender-Steuerelement angewendet wird, das den [**MCS- \_ MultiSelect**](month-calendar-control-styles.md) -Stil nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="60828-117">**MCM\_GETSELRANGE** will fail if applied to a month calendar control that does not use the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="60828-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60828-118">Requirements</span></span>



| <span data-ttu-id="60828-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60828-119">Requirement</span></span> | <span data-ttu-id="60828-120">Wert</span><span class="sxs-lookup"><span data-stu-id="60828-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="60828-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60828-121">Minimum supported client</span></span><br/> | <span data-ttu-id="60828-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60828-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="60828-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="60828-123">Minimum supported server</span></span><br/> | <span data-ttu-id="60828-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60828-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="60828-125">Header</span><span class="sxs-lookup"><span data-stu-id="60828-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="60828-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="60828-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60828-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60828-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60828-128">Uhrzeiten im Monatskalender-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="60828-128">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

