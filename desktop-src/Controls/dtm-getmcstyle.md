---
title: DTM_GETMCSTYLE Meldung (kommstrg. h)
description: Ruft den Stil eines DTP-Steuer Elements ab. Senden Sie diese Nachricht explizit oder mithilfe des DateTime- \_ getmonthcalstyle-Makros.
ms.assetid: 8983898f-e23a-4247-838c-56364f695429
keywords:
- Windows-Steuerelemente für DTM_GETMCSTYLE Meldung
topic_type:
- apiref
api_name:
- DTM_GETMCSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cae82d271d0e9aece54046527dfa3bedcef657f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956832"
---
# <a name="dtm_getmcstyle-message"></a><span data-ttu-id="2c658-105">DTM \_ getmcstyle-Nachricht</span><span class="sxs-lookup"><span data-stu-id="2c658-105">DTM\_GETMCSTYLE message</span></span>

<span data-ttu-id="2c658-106">Ruft den Stil eines DTP-Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="2c658-106">Gets the style of a date and time picker (DTP) control.</span></span> <span data-ttu-id="2c658-107">Senden Sie diese Nachricht explizit oder mithilfe des [**DateTime- \_ getmonthcalstyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle) -Makros.</span><span class="sxs-lookup"><span data-stu-id="2c658-107">Send this message explicitly or by using the [**DateTime\_GetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2c658-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c658-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c658-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c658-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c658-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="2c658-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2c658-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c658-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2c658-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="2c658-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c658-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2c658-113">Return value</span></span>

<span data-ttu-id="2c658-114">Gibt den Stil Wert des-Steuer Elements zurück.</span><span class="sxs-lookup"><span data-stu-id="2c658-114">Returns the style value of the control.</span></span> <span data-ttu-id="2c658-115">Weitere Informationen finden Sie unter [Month Calendar Control Styles](month-calendar-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="2c658-115">For more information see [Month Calendar Control Styles](month-calendar-control-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c658-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c658-116">Requirements</span></span>



| <span data-ttu-id="2c658-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c658-117">Requirement</span></span> | <span data-ttu-id="2c658-118">Wert</span><span class="sxs-lookup"><span data-stu-id="2c658-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2c658-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c658-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2c658-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c658-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2c658-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c658-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2c658-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c658-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2c658-123">Header</span><span class="sxs-lookup"><span data-stu-id="2c658-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c658-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c658-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





