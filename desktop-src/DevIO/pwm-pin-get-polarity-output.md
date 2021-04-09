---
description: Enthält einen Wert, der zurückgegeben werden soll.
ms.assetid: 432C10EF-AC08-4781-9BCA-A31E0DF12704
title: PWM_PIN_GET_POLARITY_OUTPUT Struktur (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_GET_POLARITY_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 81cf7b658a0024c3280db1523af34aaf2ef17262
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958333"
---
# <a name="pwm_pin_get_polarity_output-structure"></a><span data-ttu-id="db18a-103">PWM- \_ Pin \_ Get Polarität- \_ \_ Ausgabestruktur</span><span class="sxs-lookup"><span data-stu-id="db18a-103">PWM\_PIN\_GET\_POLARITY\_OUTPUT structure</span></span>

<span data-ttu-id="db18a-104">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="db18a-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="db18a-105">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="db18a-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="db18a-106">Enthält einen Wert, der zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="db18a-106">Contains a polarity value to return.</span></span>

## <a name="syntax"></a><span data-ttu-id="db18a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="db18a-107">Syntax</span></span>


```C++
typedef struct _PWM_PIN_GET_POLARITY_OUTPUT {
  PWM_POLARITY Polarity;
} PWM_PIN_GET_POLARITY_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="db18a-108">Member</span><span class="sxs-lookup"><span data-stu-id="db18a-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="db18a-109">**Gan**</span><span class="sxs-lookup"><span data-stu-id="db18a-109">**Polarity**</span></span>
</dt> <dd>

<span data-ttu-id="db18a-110">Die Polarität der PIN oder des Kanals als [**PWM- \_ polationswert**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) .</span><span class="sxs-lookup"><span data-stu-id="db18a-110">The polarity of the pin or channel as a [**PWM\_POLARITY**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) value.</span></span> <span data-ttu-id="db18a-111">Die Polarität ist entweder "hoch" oder "aktiv".</span><span class="sxs-lookup"><span data-stu-id="db18a-111">The polarity is either Active High or Active Low.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="db18a-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db18a-112">Requirements</span></span>



| <span data-ttu-id="db18a-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db18a-113">Requirement</span></span> | <span data-ttu-id="db18a-114">Wert</span><span class="sxs-lookup"><span data-stu-id="db18a-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db18a-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="db18a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="db18a-116">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db18a-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="db18a-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="db18a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="db18a-118">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db18a-118">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="db18a-119">KMDF-Mindestversion</span><span class="sxs-lookup"><span data-stu-id="db18a-119">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="db18a-120">1.19</span><span class="sxs-lookup"><span data-stu-id="db18a-120">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="db18a-121">UMDF-Mindestversion</span><span class="sxs-lookup"><span data-stu-id="db18a-121">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="db18a-122">2.19</span><span class="sxs-lookup"><span data-stu-id="db18a-122">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="db18a-123">Header</span><span class="sxs-lookup"><span data-stu-id="db18a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="db18a-124"><dt>PWM. h (Include PWM. h)</dt></span><span class="sxs-lookup"><span data-stu-id="db18a-124"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db18a-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db18a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db18a-126">**IOCTL \_ PWM- \_ Pin \_ get \_ Polarität**</span><span class="sxs-lookup"><span data-stu-id="db18a-126">**IOCTL\_PWM\_PIN\_GET\_POLARITY**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_POLARITY**)
</dt> <dt>

[<span data-ttu-id="db18a-127">**PWM- \_ Polarität**</span><span class="sxs-lookup"><span data-stu-id="db18a-127">**PWM\_POLARITY**</span></span>](/windows/win32/api/pwm/ne-pwm-pwm_polarity)
</dt> </dl>

 

