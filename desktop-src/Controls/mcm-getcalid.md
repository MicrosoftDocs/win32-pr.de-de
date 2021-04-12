---
title: MCM_GETCALID Meldung (kommstrg. h)
description: Ruft die Kalender-ID für das angegebene Kalender Steuerelement ab. Sie können diese Nachricht explizit oder mit dem monthcal \_ getcalid-Makro senden.
ms.assetid: ecfab4f3-a5af-445d-8b90-243b646524a6
keywords:
- Windows-Steuerelemente für MCM_GETCALID Meldung
topic_type:
- apiref
api_name:
- MCM_GETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb4a780d5107a7761d7dcac9b27a7cb01f3de744
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104037"
---
# <a name="mcm_getcalid-message"></a><span data-ttu-id="bc68f-105">MCM \_ getcalid-Meldung</span><span class="sxs-lookup"><span data-stu-id="bc68f-105">MCM\_GETCALID message</span></span>

<span data-ttu-id="bc68f-106">Ruft die Kalender-ID für das angegebene Kalender Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="bc68f-106">Gets the calendar ID for the given calendar control.</span></span> <span data-ttu-id="bc68f-107">Sie können diese Nachricht explizit oder mit dem [**monthcal \_ getcalid-**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalid) Makro senden.</span><span class="sxs-lookup"><span data-stu-id="bc68f-107">You can send this message explicitly or by using the [**MonthCal\_GetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalid) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bc68f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc68f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc68f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bc68f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc68f-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="bc68f-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bc68f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bc68f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc68f-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="bc68f-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc68f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc68f-113">Return value</span></span>

<span data-ttu-id="bc68f-114">ID des aktuellen Kalenders.</span><span class="sxs-lookup"><span data-stu-id="bc68f-114">ID of the current calendar.</span></span> <span data-ttu-id="bc68f-115">Eine der-Konstanten des [Kalender Bezeichner](/windows/desktop/Intl/calendar-identifiers) .</span><span class="sxs-lookup"><span data-stu-id="bc68f-115">One of the [Calendar Identifiers](/windows/desktop/Intl/calendar-identifiers) constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc68f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc68f-116">Requirements</span></span>



| <span data-ttu-id="bc68f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc68f-117">Requirement</span></span> | <span data-ttu-id="bc68f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="bc68f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc68f-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc68f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bc68f-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc68f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bc68f-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc68f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bc68f-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc68f-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bc68f-123">Header</span><span class="sxs-lookup"><span data-stu-id="bc68f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc68f-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc68f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

