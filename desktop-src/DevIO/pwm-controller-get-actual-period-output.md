---
description: Enthält den effektiven Ausgabesignal Zeitraum für einen Pulse Width Modulation (PWM)-Controller.
ms.assetid: 280F564F-FF7F-4121-B726-9F9AF9E98EB7
title: PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT Struktur (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: f63057299a8ef37ed1b38151958d2e0061ad2727
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748344"
---
# <a name="pwm_controller_get_actual_period_output-structure"></a><span data-ttu-id="ce6fb-103">PWM- \_ Controller \_ get \_ Actual \_ Period \_ Output Structure</span><span class="sxs-lookup"><span data-stu-id="ce6fb-103">PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD\_OUTPUT structure</span></span>

<span data-ttu-id="ce6fb-104">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="ce6fb-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ce6fb-105">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="ce6fb-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ce6fb-106">Enthält den effektiven Ausgabesignal Zeitraum für einen Pulse Width Modulation (PWM)-Controller.</span><span class="sxs-lookup"><span data-stu-id="ce6fb-106">Contains the effective output signal period for a Pulse Width Modulation (PWM) controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce6fb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce6fb-107">Syntax</span></span>


```C++
typedef struct _PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT {
  PWM_PERIOD ActualPeriod;
} PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="ce6fb-108">Member</span><span class="sxs-lookup"><span data-stu-id="ce6fb-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ce6fb-109">**Actualperiod**</span><span class="sxs-lookup"><span data-stu-id="ce6fb-109">**ActualPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="ce6fb-110">Der effektive Ausgabesignal Zeitraum, wie er in den Ausgabekanälen des Controllers gemessen wird.</span><span class="sxs-lookup"><span data-stu-id="ce6fb-110">The effective output signal period as it would be measured on the output channels of the controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce6fb-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce6fb-111">Requirements</span></span>



| <span data-ttu-id="ce6fb-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce6fb-112">Requirement</span></span> | <span data-ttu-id="ce6fb-113">Wert</span><span class="sxs-lookup"><span data-stu-id="ce6fb-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce6fb-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce6fb-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ce6fb-115">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce6fb-115">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ce6fb-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce6fb-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ce6fb-117">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce6fb-117">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ce6fb-118">KMDF-Mindestversion</span><span class="sxs-lookup"><span data-stu-id="ce6fb-118">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="ce6fb-119">1.19</span><span class="sxs-lookup"><span data-stu-id="ce6fb-119">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="ce6fb-120">UMDF-Mindestversion</span><span class="sxs-lookup"><span data-stu-id="ce6fb-120">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="ce6fb-121">2.19</span><span class="sxs-lookup"><span data-stu-id="ce6fb-121">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="ce6fb-122">Header</span><span class="sxs-lookup"><span data-stu-id="ce6fb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce6fb-123"><dt>PWM. h (Include PWM. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce6fb-123"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce6fb-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce6fb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce6fb-125">**IOCTL \_ PWM- \_ Controller \_ get \_ tatsächlicher \_ Zeitraum**</span><span class="sxs-lookup"><span data-stu-id="ce6fb-125">**IOCTL\_PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD**)
</dt> </dl>

 

 




