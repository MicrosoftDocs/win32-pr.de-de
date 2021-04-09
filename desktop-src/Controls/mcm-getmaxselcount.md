---
title: MCM_GETMAXSELCOUNT Meldung (kommstrg. h)
description: Ruft den maximalen Datumsbereich ab, der in einem Monatskalender-Steuerelement ausgewählt werden kann. Sie können diese Nachricht explizit oder mit dem monthcal \_ getmaxselcount-Makro senden.
ms.assetid: 34204231-3a3c-4eba-913d-b0c27769c338
keywords:
- Windows-Steuerelemente für MCM_GETMAXSELCOUNT Meldung
topic_type:
- apiref
api_name:
- MCM_GETMAXSELCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5bddfdad17cc4a0fd6499514023cb499f55f40d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040762"
---
# <a name="mcm_getmaxselcount-message"></a><span data-ttu-id="7d63a-105">MCM \_ getmaxselcount-Nachricht</span><span class="sxs-lookup"><span data-stu-id="7d63a-105">MCM\_GETMAXSELCOUNT message</span></span>

<span data-ttu-id="7d63a-106">Ruft den maximalen Datumsbereich ab, der in einem Monatskalender-Steuerelement ausgewählt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7d63a-106">Retrieves the maximum date range that can be selected in a month calendar control.</span></span> <span data-ttu-id="7d63a-107">Sie können diese Nachricht explizit oder mit dem [**monthcal \_ getmaxselcount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxselcount) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="7d63a-107">You can send this message explicitly or by using the [**MonthCal\_GetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxselcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7d63a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d63a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d63a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7d63a-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7d63a-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="7d63a-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7d63a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7d63a-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7d63a-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="7d63a-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d63a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7d63a-113">Return value</span></span>

<span data-ttu-id="7d63a-114">Gibt einen int-Wert zurück, der die Gesamtzahl der Tage darstellt, die für das-Steuerelement ausgewählt werden können.</span><span class="sxs-lookup"><span data-stu-id="7d63a-114">Returns an INT value that represents the total number of days that can be selected for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d63a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d63a-115">Remarks</span></span>

<span data-ttu-id="7d63a-116">Sie können den maximalen Datumsbereich ändern, der ausgewählt werden kann, indem Sie die [**MCM \_ setmaxselcount**](mcm-setmaxselcount.md) -Nachricht verwenden.</span><span class="sxs-lookup"><span data-stu-id="7d63a-116">You can change the maximum date range that can be selected by using the [**MCM\_SETMAXSELCOUNT**](mcm-setmaxselcount.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d63a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d63a-117">Requirements</span></span>



| <span data-ttu-id="7d63a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d63a-118">Requirement</span></span> | <span data-ttu-id="7d63a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="7d63a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d63a-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7d63a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7d63a-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d63a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7d63a-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7d63a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7d63a-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d63a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7d63a-124">Header</span><span class="sxs-lookup"><span data-stu-id="7d63a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d63a-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d63a-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





