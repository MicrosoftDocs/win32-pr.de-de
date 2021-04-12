---
description: Enthält einen gewünschten Duty-Cycle-Prozentsatz für eine PIN oder einen Kanal in einem PWM-Controller (Pulse Width Modulation).
ms.assetid: CA699703-2D9B-4841-99AD-9C27FF428394
title: PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT Struktur (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 98811ace7ce8fce760e10757b8bf012cc2b9b27d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392934"
---
# <a name="pwm_pin_set_active_duty_cycle_percentage_input-structure"></a><span data-ttu-id="a0813-103">PWM- \_ Pin \_ Set \_ Active \_ Duty \_ Cycle \_ Prozentsatz der \_ Eingabe Struktur</span><span class="sxs-lookup"><span data-stu-id="a0813-103">PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE\_INPUT structure</span></span>

<span data-ttu-id="a0813-104">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="a0813-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a0813-105">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="a0813-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a0813-106">Enthält einen gewünschten Duty-Cycle-Prozentsatz für eine PIN oder einen Kanal in einem PWM-Controller (Pulse Width Modulation).</span><span class="sxs-lookup"><span data-stu-id="a0813-106">Contains a desired duty cycle percentage for a pin or channel in a Pulse Width Modulation (PWM) controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0813-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0813-107">Syntax</span></span>


```C++
typedef struct _PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT {
  PWM_PERCENTAGE Percentage;
} PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT;
```



## <a name="members"></a><span data-ttu-id="a0813-108">Member</span><span class="sxs-lookup"><span data-stu-id="a0813-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a0813-109">**Percentage**</span><span class="sxs-lookup"><span data-stu-id="a0813-109">**Percentage**</span></span>
</dt> <dd>

<span data-ttu-id="a0813-110">Der gewünschte PWM-Signal-Duty-Cycle als PWM- \_ Prozentsatz, bei dem es sich um einen ULONGLONG-Wert handelt.</span><span class="sxs-lookup"><span data-stu-id="a0813-110">The desired PWM signal duty cycle, as a PWM\_PERCENTAGE, which is a ULONGLONG value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0813-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0813-111">Requirements</span></span>



| <span data-ttu-id="a0813-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0813-112">Requirement</span></span> | <span data-ttu-id="a0813-113">Wert</span><span class="sxs-lookup"><span data-stu-id="a0813-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0813-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a0813-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a0813-115">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a0813-115">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a0813-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a0813-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a0813-117">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a0813-117">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a0813-118">KMDF-Mindestversion</span><span class="sxs-lookup"><span data-stu-id="a0813-118">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="a0813-119">1.19</span><span class="sxs-lookup"><span data-stu-id="a0813-119">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="a0813-120">UMDF-Mindestversion</span><span class="sxs-lookup"><span data-stu-id="a0813-120">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="a0813-121">2.19</span><span class="sxs-lookup"><span data-stu-id="a0813-121">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="a0813-122">Header</span><span class="sxs-lookup"><span data-stu-id="a0813-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0813-123"><dt>PWM. h (Include PWM. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0813-123"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0813-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0813-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0813-125">**IOCTL \_ PWM \_ Pin \_ Set \_ Active \_ Duty \_ Cycle \_ Prozentsatz**</span><span class="sxs-lookup"><span data-stu-id="a0813-125">**IOCTL\_PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




