---
title: MCIWNDM_SETREPEAT Meldung (VFW. h)
description: Die mciwndm \_ SetRepeat-Nachricht legt das wiederholungsflag fest, das der kontinuierlichen Wiedergabe zugeordnet ist.
ms.assetid: 9a8da201-9ce8-4b6c-8b76-cd9e1356c75d
keywords:
- MCIWNDM_SETREPEAT-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_SETREPEAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeae2ac3cb57f8ddbb2343ee3f42d30fa8def370
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859064"
---
# <a name="mciwndm_setrepeat-message"></a><span data-ttu-id="795a7-104">Mciwndm- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="795a7-104">MCIWNDM\_SETREPEAT message</span></span>

<span data-ttu-id="795a7-105">Die **mciwndm \_ SetRepeat** -Nachricht legt das wiederholungsflag fest, das der kontinuierlichen Wiedergabe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="795a7-105">The **MCIWNDM\_SETREPEAT** message sets the repeat flag associated with continuous playback.</span></span> <span data-ttu-id="795a7-106">Die **mciwndm \_** -Nachricht "" wird zusammen mit dem Befehl " [MCI \_ Play](mci-play.md) " verwendet, um eine fortlaufende Wiedergabe Schleife bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="795a7-106">The **MCIWNDM\_SETREPEAT** message works in conjunction with the [MCI\_PLAY](mci-play.md) command to provide a continuous playback loop.</span></span> <span data-ttu-id="795a7-107">Sie können diese Nachricht explizit oder mit dem [**mciwndltrepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="795a7-107">You can send this message explicitly or by using the [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) macro.</span></span>


```C++
MCIWNDM_SETREPEAT 
wParam = 0; 
lParam = (LPARAM) (BOOL) f; 
```



## <a name="parameters"></a><span data-ttu-id="795a7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="795a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="795a7-109"><span id="f"></span><span id="F"></span>*c*</span><span class="sxs-lookup"><span data-stu-id="795a7-109"><span id="f"></span><span id="F"></span>*f*</span></span>
</dt> <dd>

<span data-ttu-id="795a7-110">Neuer Zustand des Wiederholungs Flags.</span><span class="sxs-lookup"><span data-stu-id="795a7-110">New state of the repeat flag.</span></span> <span data-ttu-id="795a7-111">Geben Sie **true** an, um die kontinuierliche Wiedergabe zu aktivieren</span><span class="sxs-lookup"><span data-stu-id="795a7-111">Specify **TRUE** to turn on continuous playback.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="795a7-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="795a7-112">Return Value</span></span>

<span data-ttu-id="795a7-113">Gibt 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="795a7-113">Returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="795a7-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="795a7-114">Remarks</span></span>

<span data-ttu-id="795a7-115">Derzeit ist MCIAVI das einzige Gerät, das die fortlaufende Wiedergabe unterstützt.</span><span class="sxs-lookup"><span data-stu-id="795a7-115">Currently, MCIAVI is the only device that supports continuous playback.</span></span>

## <a name="requirements"></a><span data-ttu-id="795a7-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="795a7-116">Requirements</span></span>



| <span data-ttu-id="795a7-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="795a7-117">Requirement</span></span> | <span data-ttu-id="795a7-118">Wert</span><span class="sxs-lookup"><span data-stu-id="795a7-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="795a7-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="795a7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="795a7-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="795a7-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="795a7-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="795a7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="795a7-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="795a7-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="795a7-123">Header</span><span class="sxs-lookup"><span data-stu-id="795a7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="795a7-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="795a7-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="795a7-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="795a7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="795a7-126">MCI- \_ Play</span><span class="sxs-lookup"><span data-stu-id="795a7-126">MCI\_PLAY</span></span>](mci-play.md)
</dt> <dt>

[<span data-ttu-id="795a7-127">**Mciwndgtrepeat**</span><span class="sxs-lookup"><span data-stu-id="795a7-127">**MCIWndSetRepeat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)
</dt> </dl>

 

 





