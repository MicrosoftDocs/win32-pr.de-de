---
title: MCM_SETSELRANGE Meldung (kommstrg. h)
description: Legt die Auswahl für ein Monatskalender-Steuerelement auf einen bestimmten Datumsbereich fest. Sie können diese Nachricht explizit oder mit dem monthcal- \_ setselrange-Makro senden.
ms.assetid: 750b0c83-6baa-4caa-a738-feae8751a70e
keywords:
- Windows-Steuerelemente für MCM_SETSELRANGE Meldung
topic_type:
- apiref
api_name:
- MCM_SETSELRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad28966ab67a5e7c0d27dd8fc9c367ec30e4cd7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040169"
---
# <a name="mcm_setselrange-message"></a><span data-ttu-id="1ce04-105">MCM \_ setselrange-Nachricht</span><span class="sxs-lookup"><span data-stu-id="1ce04-105">MCM\_SETSELRANGE message</span></span>

<span data-ttu-id="1ce04-106">Legt die Auswahl für ein Monatskalender-Steuerelement auf einen bestimmten Datumsbereich fest.</span><span class="sxs-lookup"><span data-stu-id="1ce04-106">Sets the selection for a month calendar control to a given date range.</span></span> <span data-ttu-id="1ce04-107">Sie können diese Nachricht explizit oder mit dem [**monthcal- \_ setselrange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setselrange) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="1ce04-107">You can send this message explicitly or by using the [**MonthCal\_SetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setselrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1ce04-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ce04-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ce04-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1ce04-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1ce04-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="1ce04-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1ce04-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ce04-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ce04-112">Ein Zeiger auf ein Array aus zwei Elementen von [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Strukturen, die Datumsinformationen enthalten, die die Auswahl Limits darstellen.</span><span class="sxs-lookup"><span data-stu-id="1ce04-112">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that contain date information representing the selection limits.</span></span> <span data-ttu-id="1ce04-113">Das erste ausgewählte Datum muss in *lpsystimearray* \[ 0 angegeben werden \] , und das Datum der letzten Auswahl muss in *lpsystimearray* \[ 1 angegeben werden \] .</span><span class="sxs-lookup"><span data-stu-id="1ce04-113">The first selected date must be specified in *lpSysTimeArray*\[0\], and the last selected date must be specified in *lpSysTimeArray*\[1\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ce04-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1ce04-114">Return value</span></span>

<span data-ttu-id="1ce04-115">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="1ce04-115">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="1ce04-116">Diese Nachricht schlägt fehl, wenn Sie auf ein Monatskalender-Steuerelement angewendet wird, das den [**MCS- \_ MultiSelect**](month-calendar-control-styles.md) -Stil nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1ce04-116">This message will fail if applied to a month calendar control that does not use the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ce04-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ce04-117">Requirements</span></span>



| <span data-ttu-id="1ce04-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ce04-118">Requirement</span></span> | <span data-ttu-id="1ce04-119">Wert</span><span class="sxs-lookup"><span data-stu-id="1ce04-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ce04-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1ce04-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1ce04-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1ce04-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1ce04-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1ce04-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1ce04-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1ce04-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1ce04-124">Header</span><span class="sxs-lookup"><span data-stu-id="1ce04-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ce04-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ce04-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ce04-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ce04-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ce04-127">Uhrzeiten im Monatskalender-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="1ce04-127">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

