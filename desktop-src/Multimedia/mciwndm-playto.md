---
title: MCIWNDM_PLAYTO Meldung (VFW. h)
description: Die mciwndm \_ playto-Nachricht gibt den Inhalt eines MCI-Geräts von der aktuellen Position bis zur angegebenen Endposition oder bis zur Wiedergabe durch einen anderen Befehl wieder.
ms.assetid: ed940ee7-7b96-47da-99d3-6697f8a2e3d5
keywords:
- MCIWNDM_PLAYTO-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYTO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf0104204dc0306615ead91be036459cdf3c11d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105429"
---
# <a name="mciwndm_playto-message"></a><span data-ttu-id="84ef1-104">Mciwndm \_ playto-Meldung</span><span class="sxs-lookup"><span data-stu-id="84ef1-104">MCIWNDM\_PLAYTO message</span></span>

<span data-ttu-id="84ef1-105">Die **mciwndm \_ playto** -Nachricht gibt den Inhalt eines MCI-Geräts von der aktuellen Position bis zur angegebenen Endposition oder bis zur Wiedergabe durch einen anderen Befehl wieder.</span><span class="sxs-lookup"><span data-stu-id="84ef1-105">The **MCIWNDM\_PLAYTO** message plays the content of an MCI device from the current position to the specified ending location or until another command stops playback.</span></span> <span data-ttu-id="84ef1-106">Wenn die angegebene Endposition hinter dem Ende des Inhalts liegt, wird die Wiedergabe am Ende des Inhalts angehalten.</span><span class="sxs-lookup"><span data-stu-id="84ef1-106">If the specified ending location is beyond the end of the content, playback stops at the end of the content.</span></span> <span data-ttu-id="84ef1-107">Sie können diese Nachricht explizit oder mithilfe des Makros [**mciwndplayto**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) senden.</span><span class="sxs-lookup"><span data-stu-id="84ef1-107">You can send this message explicitly or by using the [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) macro.</span></span>


```C++
MCIWNDM_PLAYTO 
wParam = 0; 
lParam = (LPARAM) (LONG) lEnd; 
```



## <a name="parameters"></a><span data-ttu-id="84ef1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="84ef1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84ef1-109"><span id="lEnd"></span><span id="lend"></span><span id="LEND"></span>*auszu*</span><span class="sxs-lookup"><span data-stu-id="84ef1-109"><span id="lEnd"></span><span id="lend"></span><span id="LEND"></span>*lEnd*</span></span>
</dt> <dd>

<span data-ttu-id="84ef1-110">Endposition.</span><span class="sxs-lookup"><span data-stu-id="84ef1-110">Ending location.</span></span> <span data-ttu-id="84ef1-111">Die Einheiten für die Endposition hängen vom aktuellen Zeitformat ab.</span><span class="sxs-lookup"><span data-stu-id="84ef1-111">The units for the ending location depend on the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84ef1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="84ef1-112">Return Value</span></span>

<span data-ttu-id="84ef1-113">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="84ef1-113">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="84ef1-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84ef1-114">Remarks</span></span>

<span data-ttu-id="84ef1-115">Dieses Makro wird mithilfe der Makros " [**mciwndseek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) " und " [**mciwndplayto**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) " definiert, die wiederum den MCI-Befehl " [ \_ Seek](mci-seek.md) " und die **mciwndm- \_ playto** -Nachricht verwenden.</span><span class="sxs-lookup"><span data-stu-id="84ef1-115">This macro is defined using the [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) and [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) macros, which in turn use the [MCI\_SEEK](mci-seek.md) command and the **MCIWNDM\_PLAYTO** message.</span></span>

<span data-ttu-id="84ef1-116">Sie können auch einen Start-und einen endspeicherort für die Wiedergabe angeben, indem Sie das [**mciwndplayfromto**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="84ef1-116">You can also specify both a starting and ending location for playback by using the [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="84ef1-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84ef1-117">Requirements</span></span>



| <span data-ttu-id="84ef1-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84ef1-118">Requirement</span></span> | <span data-ttu-id="84ef1-119">Wert</span><span class="sxs-lookup"><span data-stu-id="84ef1-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="84ef1-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="84ef1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="84ef1-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84ef1-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="84ef1-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="84ef1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="84ef1-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84ef1-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="84ef1-124">Header</span><span class="sxs-lookup"><span data-stu-id="84ef1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="84ef1-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="84ef1-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84ef1-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84ef1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84ef1-127">MCI- \_ Suche</span><span class="sxs-lookup"><span data-stu-id="84ef1-127">MCI\_SEEK</span></span>](mci-seek.md)
</dt> <dt>

[<span data-ttu-id="84ef1-128">**Mciwndplayfromto**</span><span class="sxs-lookup"><span data-stu-id="84ef1-128">**MCIWndPlayFromTo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> <dt>

[<span data-ttu-id="84ef1-129">**Mciwndplayto**</span><span class="sxs-lookup"><span data-stu-id="84ef1-129">**MCIWndPlayTo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)
</dt> <dt>

[<span data-ttu-id="84ef1-130">**Mciwndseek**</span><span class="sxs-lookup"><span data-stu-id="84ef1-130">**MCIWndSeek**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndseek)
</dt> </dl>

 

 





