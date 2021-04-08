---
title: MCIWNDM_GETMODE Meldung (VFW. h)
description: Die mciwndm \_ getMode-Nachricht Ruft den aktuellen Betriebsmodus eines MCI-Geräts ab. MCI-Geräte verfügen über mehrere Betriebsmodi, die durch Konstanten festgelegt werden. Sie können diese Nachricht explizit oder mithilfe des mciwndgetmode-Makros senden.
ms.assetid: cc327281-434e-4047-9e15-c04a10953f47
keywords:
- MCIWNDM_GETMODE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETMODE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5daefea2c550a1d0cf807ae03840c38ae8b2567c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102842"
---
# <a name="mciwndm_getmode-message"></a><span data-ttu-id="7b87b-106">Mciwndm \_ getMode-Meldung</span><span class="sxs-lookup"><span data-stu-id="7b87b-106">MCIWNDM\_GETMODE message</span></span>

<span data-ttu-id="7b87b-107">Die **mciwndm \_ getMode** -Nachricht Ruft den aktuellen Betriebsmodus eines MCI-Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="7b87b-107">The **MCIWNDM\_GETMODE** message retrieves the current operating mode of an MCI device.</span></span> <span data-ttu-id="7b87b-108">MCI-Geräte verfügen über mehrere Betriebsmodi, die durch Konstanten festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7b87b-108">MCI devices have several operating modes, which are designated by constants.</span></span> <span data-ttu-id="7b87b-109">Sie können diese Nachricht explizit oder mithilfe des [**mciwndgetmode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="7b87b-109">You can send this message explicitly or by using the [**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode) macro.</span></span>


```C++
MCIWNDM_GETMODE 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="7b87b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b87b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b87b-111"><span id="len"></span><span id="LEN"></span>*Nest*</span><span class="sxs-lookup"><span data-stu-id="7b87b-111"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="7b87b-112">Größe (in Bytes) des Puffers.</span><span class="sxs-lookup"><span data-stu-id="7b87b-112">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="7b87b-113"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="7b87b-113"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="7b87b-114">Ein Zeiger auf den Anwendungs definierten Puffer, der verwendet wird, um den Modus zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="7b87b-114">Pointer to the application-defined buffer used to return the mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b87b-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7b87b-115">Return Value</span></span>

<span data-ttu-id="7b87b-116">Gibt eine ganze Zahl zurück, die der MCI-Konstante entspricht, die den Modus definiert.</span><span class="sxs-lookup"><span data-stu-id="7b87b-116">Returns an integer corresponding to the MCI constant defining the mode.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b87b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b87b-117">Remarks</span></span>

<span data-ttu-id="7b87b-118">Wenn die auf NULL endenden Zeichenfolge, die den Modus beschreibt, länger als der Puffer ist, wird Sie abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="7b87b-118">If the null-terminated string describing the mode is longer than the buffer, it is truncated.</span></span>

<span data-ttu-id="7b87b-119">Nicht alle Geräte können in jedem Modus betrieben werden.</span><span class="sxs-lookup"><span data-stu-id="7b87b-119">Not all devices can operate in every mode.</span></span> <span data-ttu-id="7b87b-120">Beispielsweise ist das MCIAVI-Gerät ein Wiedergabe Gerät. der Aufzeichnungsmodus wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7b87b-120">For example, the MCIAVI device is a playback device; it doesn't support the recording mode.</span></span> <span data-ttu-id="7b87b-121">Die folgenden Modi können mithilfe von **mciwndm \_ getMode** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7b87b-121">The following modes can be retrieved by using **MCIWNDM\_GETMODE**.</span></span>



| <span data-ttu-id="7b87b-122">Betriebsmodus</span><span class="sxs-lookup"><span data-stu-id="7b87b-122">Operating mode</span></span> | <span data-ttu-id="7b87b-123">MCI-Konstante</span><span class="sxs-lookup"><span data-stu-id="7b87b-123">MCI constant</span></span>          |
|----------------|-----------------------|
| <span data-ttu-id="7b87b-124">nicht bereit</span><span class="sxs-lookup"><span data-stu-id="7b87b-124">not ready</span></span>      | <span data-ttu-id="7b87b-125">MCI- \_ Modus \_ nicht \_ bereit</span><span class="sxs-lookup"><span data-stu-id="7b87b-125">MCI\_MODE\_NOT\_READY</span></span> |
| <span data-ttu-id="7b87b-126">open</span><span class="sxs-lookup"><span data-stu-id="7b87b-126">open</span></span>           | <span data-ttu-id="7b87b-127">MCI- \_ Modus \_ geöffnet</span><span class="sxs-lookup"><span data-stu-id="7b87b-127">MCI\_MODE\_OPEN</span></span>       |
| <span data-ttu-id="7b87b-128">angehalten</span><span class="sxs-lookup"><span data-stu-id="7b87b-128">paused</span></span>         | <span data-ttu-id="7b87b-129">MCI- \_ Modus anhalten \_</span><span class="sxs-lookup"><span data-stu-id="7b87b-129">MCI\_MODE\_PAUSE</span></span>      |
| <span data-ttu-id="7b87b-130">Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="7b87b-130">playing</span></span>        | <span data-ttu-id="7b87b-131">MCI- \_ Modus \_ abspielen</span><span class="sxs-lookup"><span data-stu-id="7b87b-131">MCI\_MODE\_PLAY</span></span>       |
| <span data-ttu-id="7b87b-132">Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="7b87b-132">recording</span></span>      | <span data-ttu-id="7b87b-133">MCI- \_ Modus- \_ Datensatz</span><span class="sxs-lookup"><span data-stu-id="7b87b-133">MCI\_MODE\_RECORD</span></span>     |
| <span data-ttu-id="7b87b-134">Suchen</span><span class="sxs-lookup"><span data-stu-id="7b87b-134">seeking</span></span>        | <span data-ttu-id="7b87b-135">MCI- \_ Modus- \_ Suche</span><span class="sxs-lookup"><span data-stu-id="7b87b-135">MCI\_MODE\_SEEK</span></span>       |
| <span data-ttu-id="7b87b-136">stopped</span><span class="sxs-lookup"><span data-stu-id="7b87b-136">stopped</span></span>        | <span data-ttu-id="7b87b-137">MCI- \_ Modus wird \_ beendet</span><span class="sxs-lookup"><span data-stu-id="7b87b-137">MCI\_MODE\_STOP</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="7b87b-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b87b-138">Requirements</span></span>



| <span data-ttu-id="7b87b-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b87b-139">Requirement</span></span> | <span data-ttu-id="7b87b-140">Wert</span><span class="sxs-lookup"><span data-stu-id="7b87b-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7b87b-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7b87b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="7b87b-142">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b87b-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7b87b-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7b87b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="7b87b-144">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b87b-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7b87b-145">Header</span><span class="sxs-lookup"><span data-stu-id="7b87b-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b87b-146"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b87b-146"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b87b-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b87b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b87b-148">**Mciwndgetmode**</span><span class="sxs-lookup"><span data-stu-id="7b87b-148">**MCIWndGetMode**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode)
</dt> </dl>

 

 





