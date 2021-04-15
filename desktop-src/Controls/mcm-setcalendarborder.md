---
title: MCM_SETCALENDARBORDER Meldung (kommstrg. h)
description: Legt die Größe des Rahmens in Pixel fest. Sie können diese Nachricht explizit oder mit dem monthcal- \_ setcalendarborder-Makro senden.
ms.assetid: 2a64a08f-a1fb-47a8-8f09-725807e87a03
keywords:
- Windows-Steuerelemente für MCM_SETCALENDARBORDER Meldung
topic_type:
- apiref
api_name:
- MCM_SETCALENDARBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09b870346e8d8b475833657dd83141ba1fe11715
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476626"
---
# <a name="mcm_setcalendarborder-message"></a><span data-ttu-id="35edd-105">MCM \_ setcalendarborder-Meldung</span><span class="sxs-lookup"><span data-stu-id="35edd-105">MCM\_SETCALENDARBORDER message</span></span>

<span data-ttu-id="35edd-106">Legt die Größe des Rahmens in Pixel fest.</span><span class="sxs-lookup"><span data-stu-id="35edd-106">Sets the size of the border, in pixels.</span></span> <span data-ttu-id="35edd-107">Sie können diese Nachricht explizit oder mit dem [**monthcal- \_ setcalendarborder**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalendarborder) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="35edd-107">You can send this message explicitly or by using the [**MonthCal\_SetCalendarBorder**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalendarborder) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="35edd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="35edd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35edd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="35edd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35edd-110">**True** gibt an, dass die Rahmengröße auf die Anzahl der Pixel festgelegt wird, die *LPARAM* angibt.</span><span class="sxs-lookup"><span data-stu-id="35edd-110">If **TRUE**, then the border size is set to the number of pixels that *lParam* specifies.</span></span> <span data-ttu-id="35edd-111">Wenn der Wert **false** ist, wird die Rahmengröße auf den Standardwert zurückgesetzt, der durch das Design angegeben wird, oder 0 (null), wenn keine Designs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="35edd-111">If **FALSE**, then the border size is reset to the default value specified by the theme, or zero if themes are not being used.</span></span>

</dd> <dt>

<span data-ttu-id="35edd-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="35edd-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35edd-113">Anzahl der Pixel der Rahmengröße.</span><span class="sxs-lookup"><span data-stu-id="35edd-113">Number of pixels of the border size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35edd-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35edd-114">Return value</span></span>

<span data-ttu-id="35edd-115">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="35edd-115">Not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="35edd-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35edd-116">Requirements</span></span>



| <span data-ttu-id="35edd-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35edd-117">Requirement</span></span> | <span data-ttu-id="35edd-118">Wert</span><span class="sxs-lookup"><span data-stu-id="35edd-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="35edd-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="35edd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="35edd-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35edd-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="35edd-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="35edd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="35edd-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35edd-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="35edd-123">Header</span><span class="sxs-lookup"><span data-stu-id="35edd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="35edd-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="35edd-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





