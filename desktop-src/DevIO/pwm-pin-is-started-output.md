---
description: Enthält den aktuellen Signal Generierungs Status einer PIN.
ms.assetid: 07D76F8D-C5B5-4500-BFA2-452989868027
title: PWM_PIN_IS_STARTED_OUTPUT Struktur (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_IS_STARTED_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 11350c3bb0fbec0f05ab3153c339f8fa30baeed5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339678"
---
# <a name="pwm_pin_is_started_output-structure"></a><span data-ttu-id="72067-103">PWM- \_ Pin \_ wird gestartet- \_ \_ Ausgabestruktur</span><span class="sxs-lookup"><span data-stu-id="72067-103">PWM\_PIN\_IS\_STARTED\_OUTPUT structure</span></span>

<span data-ttu-id="72067-104">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="72067-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="72067-105">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="72067-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="72067-106">Enthält den aktuellen Signal Generierungs Status einer PIN.</span><span class="sxs-lookup"><span data-stu-id="72067-106">Contains the current signal generation state of a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="72067-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="72067-107">Syntax</span></span>


```C++
typedef struct _PWM_PIN_IS_STARTED_OUTPUT {
  BOOLEAN IsStarted;
} PWM_PIN_IS_STARTED_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="72067-108">Member</span><span class="sxs-lookup"><span data-stu-id="72067-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="72067-109">**IsStarted**</span><span class="sxs-lookup"><span data-stu-id="72067-109">**IsStarted**</span></span>
</dt> <dd>

<span data-ttu-id="72067-110">Der Status der aktuellen Signalgenerierung der PIN.</span><span class="sxs-lookup"><span data-stu-id="72067-110">The pin current signal generation state.</span></span> <span data-ttu-id="72067-111">Der Wert true bedeutet, dass die PIN gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="72067-111">A value of true means that the pin is started.</span></span> <span data-ttu-id="72067-112">Der Wert false bedeutet, dass die PIN angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="72067-112">A value of false means that the pin is stopped.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="72067-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72067-113">Requirements</span></span>



| <span data-ttu-id="72067-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72067-114">Requirement</span></span> | <span data-ttu-id="72067-115">Wert</span><span class="sxs-lookup"><span data-stu-id="72067-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72067-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="72067-116">Minimum supported client</span></span><br/> | <span data-ttu-id="72067-117">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72067-117">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="72067-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="72067-118">Minimum supported server</span></span><br/> | <span data-ttu-id="72067-119">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72067-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="72067-120">KMDF-Mindestversion</span><span class="sxs-lookup"><span data-stu-id="72067-120">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="72067-121">1.19</span><span class="sxs-lookup"><span data-stu-id="72067-121">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="72067-122">UMDF-Mindestversion</span><span class="sxs-lookup"><span data-stu-id="72067-122">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="72067-123">2.19</span><span class="sxs-lookup"><span data-stu-id="72067-123">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="72067-124">Header</span><span class="sxs-lookup"><span data-stu-id="72067-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="72067-125"><dt>PWM. h (Include PWM. h)</dt></span><span class="sxs-lookup"><span data-stu-id="72067-125"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72067-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72067-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72067-127">**IOCTL \_ PWM- \_ PIN wurde \_ \_ gestartet.**</span><span class="sxs-lookup"><span data-stu-id="72067-127">**IOCTL\_PWM\_PIN\_IS\_STARTED**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**)
</dt> </dl>

 

 




