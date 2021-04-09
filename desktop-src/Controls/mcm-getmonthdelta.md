---
title: MCM_GETMONTHDELTA Meldung (kommstrg. h)
description: Ruft die Bild Lauf Rate für ein Monatskalender-Steuerelement ab. Die Scrollrate entspricht der Anzahl von Monaten, die das Steuerelement seine Anzeige verschiebt, wenn der Benutzer auf eine Bild Lauf Schaltfläche klickt. Sie können diese Nachricht explizit oder mit dem monthcal \_ getmonthdelta-Makro senden.
ms.assetid: 6db02993-b22c-430f-8928-8bd5768b2151
keywords:
- Windows-Steuerelemente für MCM_GETMONTHDELTA Meldung
topic_type:
- apiref
api_name:
- MCM_GETMONTHDELTA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01eaa40b930e6317cc2be6b674f0cea58115ae40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106659"
---
# <a name="mcm_getmonthdelta-message"></a><span data-ttu-id="94153-106">MCM \_ getmonthdelta-Meldung</span><span class="sxs-lookup"><span data-stu-id="94153-106">MCM\_GETMONTHDELTA message</span></span>

<span data-ttu-id="94153-107">Ruft die Bild Lauf Rate für ein Monatskalender-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="94153-107">Retrieves the scroll rate for a month calendar control.</span></span> <span data-ttu-id="94153-108">Die Scrollrate entspricht der Anzahl von Monaten, die das Steuerelement seine Anzeige verschiebt, wenn der Benutzer auf eine Bild Lauf Schaltfläche klickt.</span><span class="sxs-lookup"><span data-stu-id="94153-108">The scroll rate is the number of months that the control moves its display when the user clicks a scroll button.</span></span> <span data-ttu-id="94153-109">Sie können diese Nachricht explizit oder mit dem [**monthcal \_ getmonthdelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthdelta) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="94153-109">You can send this message explicitly or by using the [**MonthCal\_GetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthdelta) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="94153-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="94153-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94153-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="94153-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="94153-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="94153-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="94153-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="94153-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="94153-114">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="94153-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94153-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="94153-115">Return value</span></span>

<span data-ttu-id="94153-116">Wenn der Monat Delta zuvor mithilfe der [**MCM- \_ setmonthdelta**](mcm-setmonthdelta.md) -Nachricht festgelegt wurde, gibt einen int-Wert zurück, der die aktuelle Scrollrate des Monats Kalenders darstellt.</span><span class="sxs-lookup"><span data-stu-id="94153-116">If the month delta was previously set using the [**MCM\_SETMONTHDELTA**](mcm-setmonthdelta.md) message, returns an INT value that represents the month calendar's current scroll rate.</span></span> <span data-ttu-id="94153-117">Wenn das Delta für den Monat nicht zuvor mithilfe der **MCM- \_ setmonthdelta** -Nachricht festgelegt wurde, oder wenn der Monat Delta auf den Standardwert zurückgesetzt wurde, gibt einen int-Wert zurück, der die aktuelle Anzahl der sichtbaren Monate darstellt.</span><span class="sxs-lookup"><span data-stu-id="94153-117">If the month delta was not previously set using the **MCM\_SETMONTHDELTA** message, or the month delta was reset to the default, returns an INT value that represents the current number of months visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="94153-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94153-118">Requirements</span></span>



| <span data-ttu-id="94153-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94153-119">Requirement</span></span> | <span data-ttu-id="94153-120">Wert</span><span class="sxs-lookup"><span data-stu-id="94153-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="94153-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94153-121">Minimum supported client</span></span><br/> | <span data-ttu-id="94153-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94153-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="94153-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94153-123">Minimum supported server</span></span><br/> | <span data-ttu-id="94153-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94153-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="94153-125">Header</span><span class="sxs-lookup"><span data-stu-id="94153-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="94153-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="94153-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





