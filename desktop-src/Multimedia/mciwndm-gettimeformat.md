---
title: MCIWNDM_GETTIMEFORMAT Meldung (VFW. h)
description: Die mciwndm \_ getTimeFormat-Nachricht Ruft das aktuelle Zeitformat eines MCI-Geräts in zwei Formularen als numerischen Wert und als Zeichenfolge ab. Sie können diese Nachricht explizit oder mit dem mciwndgettimeformat-Makro senden.
ms.assetid: 01844872-5444-4f3b-92a3-64f80b94d3a0
keywords:
- MCIWNDM_GETTIMEFORMAT-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETTIMEFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a09f969c009ff23bc0951ed2efbc0dbf7aa95dda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740240"
---
# <a name="mciwndm_gettimeformat-message"></a><span data-ttu-id="29778-105">Mciwndm \_ getTimeFormat-Meldung</span><span class="sxs-lookup"><span data-stu-id="29778-105">MCIWNDM\_GETTIMEFORMAT message</span></span>

<span data-ttu-id="29778-106">Die **mciwndm \_ getTimeFormat** -Meldung Ruft das aktuelle Zeitformat eines MCI-Geräts in zwei Formen ab: als numerischer Wert und als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="29778-106">The **MCIWNDM\_GETTIMEFORMAT** message retrieves the current time format of an MCI device in two forms: as a numerical value and as a string.</span></span> <span data-ttu-id="29778-107">Sie können diese Nachricht explizit oder mit dem [**mciwndgettimeformat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="29778-107">You can send this message explicitly or by using the [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) macro.</span></span>


```C++
MCIWNDM_GETTIMEFORMAT 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="29778-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="29778-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29778-109"><span id="len"></span><span id="LEN"></span>*Nest*</span><span class="sxs-lookup"><span data-stu-id="29778-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="29778-110">Größe (in Bytes) des Puffers.</span><span class="sxs-lookup"><span data-stu-id="29778-110">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="29778-111"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="29778-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="29778-112">Zeiger auf einen Puffer, der die NULL-terminierte Zeichen folgen Form des Zeit Formats enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="29778-112">Pointer to a buffer to contain the null-terminated string form of the time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29778-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="29778-113">Return Value</span></span>

<span data-ttu-id="29778-114">Gibt eine ganze Zahl zurück, die der MCI-Konstante entspricht, die das Zeitformat definiert.</span><span class="sxs-lookup"><span data-stu-id="29778-114">Returns an integer corresponding to the MCI constant defining the time format.</span></span>

## <a name="remarks"></a><span data-ttu-id="29778-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29778-115">Remarks</span></span>

<span data-ttu-id="29778-116">Wenn die Zeitformat Zeichenfolge länger als der Rückgabe Puffer ist, wird die Zeichenfolge von mciwnd abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="29778-116">If the time format string is longer than the return buffer, MCIWnd truncates the string.</span></span>

<span data-ttu-id="29778-117">Ein MCI-Gerät kann eines oder mehrere der folgenden Zeitformate unterstützen.</span><span class="sxs-lookup"><span data-stu-id="29778-117">An MCI device can support one or more of the following time formats.</span></span>



| <span data-ttu-id="29778-118">Zeitformat</span><span class="sxs-lookup"><span data-stu-id="29778-118">Time format</span></span>                      | <span data-ttu-id="29778-119">MCI-Konstante</span><span class="sxs-lookup"><span data-stu-id="29778-119">MCI constant</span></span>               |
|----------------------------------|----------------------------|
| <span data-ttu-id="29778-120">Byte</span><span class="sxs-lookup"><span data-stu-id="29778-120">Bytes</span></span>                            | <span data-ttu-id="29778-121">MCI- \_ Format ( \_ Bytes)</span><span class="sxs-lookup"><span data-stu-id="29778-121">MCI\_FORMAT\_BYTES</span></span>         |
| <span data-ttu-id="29778-122">Frames</span><span class="sxs-lookup"><span data-stu-id="29778-122">Frames</span></span>                           | <span data-ttu-id="29778-123">MCI- \_ Formatierungs \_ Frames</span><span class="sxs-lookup"><span data-stu-id="29778-123">MCI\_FORMAT\_FRAMES</span></span>        |
| <span data-ttu-id="29778-124">Stunden, Minuten, Sekunden</span><span class="sxs-lookup"><span data-stu-id="29778-124">Hours, minutes, seconds</span></span>          | <span data-ttu-id="29778-125">MCI- \_ Format \_ HMS</span><span class="sxs-lookup"><span data-stu-id="29778-125">MCI\_FORMAT\_HMS</span></span>           |
| <span data-ttu-id="29778-126">Millisekunden</span><span class="sxs-lookup"><span data-stu-id="29778-126">Milliseconds</span></span>                     | <span data-ttu-id="29778-127">MCI- \_ Format ( \_ Millisekunden)</span><span class="sxs-lookup"><span data-stu-id="29778-127">MCI\_FORMAT\_MILLISECONDS</span></span>  |
| <span data-ttu-id="29778-128">Minuten, Sekunden, Frames</span><span class="sxs-lookup"><span data-stu-id="29778-128">Minutes, seconds, frames</span></span>         | <span data-ttu-id="29778-129">MCI- \_ Format \_ MSF</span><span class="sxs-lookup"><span data-stu-id="29778-129">MCI\_FORMAT\_MSF</span></span>           |
| <span data-ttu-id="29778-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29778-130">Samples</span></span>                          | <span data-ttu-id="29778-131">MCI- \_ Format \_ Beispiele</span><span class="sxs-lookup"><span data-stu-id="29778-131">MCI\_FORMAT\_SAMPLES</span></span>       |
| <span data-ttu-id="29778-132">SMPTE 24</span><span class="sxs-lookup"><span data-stu-id="29778-132">SMPTE 24</span></span>                         | <span data-ttu-id="29778-133">MCI- \_ Format, \_ SMPTE \_ 24</span><span class="sxs-lookup"><span data-stu-id="29778-133">MCI\_FORMAT\_SMPTE\_24</span></span>     |
| <span data-ttu-id="29778-134">SMPTE 25</span><span class="sxs-lookup"><span data-stu-id="29778-134">SMPTE 25</span></span>                         | <span data-ttu-id="29778-135">MCI- \_ Format, \_ SMPTE \_ 25</span><span class="sxs-lookup"><span data-stu-id="29778-135">MCI\_FORMAT\_SMPTE\_25</span></span>     |
| <span data-ttu-id="29778-136">SMPTE 30-Drop</span><span class="sxs-lookup"><span data-stu-id="29778-136">SMPTE 30 drop</span></span>                    | <span data-ttu-id="29778-137">MCI- \_ Format \_ SMPTE \_ 30drop</span><span class="sxs-lookup"><span data-stu-id="29778-137">MCI\_FORMAT\_SMPTE\_30DROP</span></span> |
| <span data-ttu-id="29778-138">SMPTE 30 (Non-Drop)</span><span class="sxs-lookup"><span data-stu-id="29778-138">SMPTE 30 (non-drop)</span></span>              | <span data-ttu-id="29778-139">MCI- \_ Format \_ SMPTE \_ 30</span><span class="sxs-lookup"><span data-stu-id="29778-139">MCI\_FORMAT\_SMPTE\_30</span></span>     |
| <span data-ttu-id="29778-140">Spuren, Minuten, Sekunden, Frames</span><span class="sxs-lookup"><span data-stu-id="29778-140">Tracks, minutes, seconds, frames</span></span> | <span data-ttu-id="29778-141">MCI- \_ Format- \_ TMSF</span><span class="sxs-lookup"><span data-stu-id="29778-141">MCI\_FORMAT\_TMSF</span></span>          |



 

## <a name="requirements"></a><span data-ttu-id="29778-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29778-142">Requirements</span></span>



| <span data-ttu-id="29778-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29778-143">Requirement</span></span> | <span data-ttu-id="29778-144">Wert</span><span class="sxs-lookup"><span data-stu-id="29778-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="29778-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="29778-145">Minimum supported client</span></span><br/> | <span data-ttu-id="29778-146">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29778-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="29778-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="29778-147">Minimum supported server</span></span><br/> | <span data-ttu-id="29778-148">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29778-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="29778-149">Header</span><span class="sxs-lookup"><span data-stu-id="29778-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="29778-150"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="29778-150"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29778-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29778-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29778-152">**Mciwndgettimeformat**</span><span class="sxs-lookup"><span data-stu-id="29778-152">**MCIWndGetTimeFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> </dl>

 

 





