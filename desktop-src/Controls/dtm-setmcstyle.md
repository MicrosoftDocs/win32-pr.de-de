---
title: DTM_SETMCSTYLE Meldung (kommstrg. h)
description: Legt den Stil eines Steuer Elements für die Datums-und Zeitauswahl fest. Senden Sie diese Nachricht explizit oder mithilfe des DateTime- \_ setmonthcalstyle-Makros.
ms.assetid: 6b480a1e-c76e-4026-ab2a-5ec53df6fa28
keywords:
- Windows-Steuerelemente für DTM_SETMCSTYLE Meldung
topic_type:
- apiref
api_name:
- DTM_SETMCSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3691dfbd62847bc490c3a45e1d640d19b09cca6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104840"
---
# <a name="dtm_setmcstyle-message"></a><span data-ttu-id="3bff1-105">DTM- \_ ltmcstyle-Nachricht</span><span class="sxs-lookup"><span data-stu-id="3bff1-105">DTM\_SETMCSTYLE message</span></span>

<span data-ttu-id="3bff1-106">Legt den Stil eines Steuer Elements für die Datums-und Zeitauswahl fest.</span><span class="sxs-lookup"><span data-stu-id="3bff1-106">Sets the style of a date and time picker (DTP) control.</span></span> <span data-ttu-id="3bff1-107">Senden Sie diese Nachricht explizit oder mithilfe des [**DateTime- \_ setmonthcalstyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle) -Makros.</span><span class="sxs-lookup"><span data-stu-id="3bff1-107">Send this message explicitly or by using the [**DateTime\_SetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3bff1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3bff1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bff1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3bff1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3bff1-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="3bff1-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3bff1-111">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3bff1-111">*lParam* \[in\]</span></span>
</dt> <dd><span data-ttu-id="3bff1-112">Ein-Stilwert.</span><span class="sxs-lookup"><span data-stu-id="3bff1-112">A style value.</span></span> <span data-ttu-id="3bff1-113">Weitere Informationen finden Sie unter <a href="month-calendar-control-styles.md">Month Calendar Control Styles</a>.</span><span class="sxs-lookup"><span data-stu-id="3bff1-113">For more information see <a href="month-calendar-control-styles.md">Month Calendar Control Styles</a>.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bff1-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3bff1-114">Return value</span></span>

<span data-ttu-id="3bff1-115">Gibt den Wert des vorherigen Stils zurück.</span><span class="sxs-lookup"><span data-stu-id="3bff1-115">Returns the value of the previous style.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bff1-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3bff1-116">Requirements</span></span>



| <span data-ttu-id="3bff1-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3bff1-117">Requirement</span></span> | <span data-ttu-id="3bff1-118">Wert</span><span class="sxs-lookup"><span data-stu-id="3bff1-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3bff1-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3bff1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3bff1-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3bff1-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3bff1-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3bff1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3bff1-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3bff1-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3bff1-123">Header</span><span class="sxs-lookup"><span data-stu-id="3bff1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bff1-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bff1-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





