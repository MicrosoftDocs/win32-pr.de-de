---
title: MCIWNDM_SETTIMEFORMAT Meldung (VFW. h)
description: Die mciwndm- \_ settimeformat-Meldung legt das Zeitformat eines MCI-Geräts fest. Sie können diese Nachricht explizit oder mit dem mciwndsettimeformat-Makro senden.
ms.assetid: 7de82094-6d35-44fd-88e7-ebd18a558cfd
keywords:
- MCIWNDM_SETTIMEFORMAT-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMEFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcec1f0db5accad93211bf1eb6f1c9297e2b9f33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517414"
---
# <a name="mciwndm_settimeformat-message"></a><span data-ttu-id="e6601-105">Mciwndm- \_ settimeformat-Meldung</span><span class="sxs-lookup"><span data-stu-id="e6601-105">MCIWNDM\_SETTIMEFORMAT message</span></span>

<span data-ttu-id="e6601-106">Die **mciwndm- \_ settimeformat** -Meldung legt das Zeitformat eines MCI-Geräts fest.</span><span class="sxs-lookup"><span data-stu-id="e6601-106">The **MCIWNDM\_SETTIMEFORMAT** message sets the time format of an MCI device.</span></span> <span data-ttu-id="e6601-107">Sie können diese Nachricht explizit oder mit dem [**mciwndsettimeformat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="e6601-107">You can send this message explicitly or by using the [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) macro.</span></span>


```C++
MCIWNDM_SETTIMEFORMAT 
wParam = 0; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="e6601-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6601-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6601-109"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="e6601-109"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="e6601-110">Zeiger auf einen Puffer, der die NULL-terminierte Zeichenfolge enthält, die das Zeitformat angibt.</span><span class="sxs-lookup"><span data-stu-id="e6601-110">Pointer to a buffer containing the null-terminated string indicating the time format.</span></span> <span data-ttu-id="e6601-111">Geben Sie "Frames" an, um das Zeitformat auf Frames festzulegen, oder "MS", um das Zeitformat auf Millisekunden festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e6601-111">Specify "frames" to set the time format to frames, or "ms" to set the time format to milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6601-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6601-112">Return Value</span></span>

<span data-ttu-id="e6601-113">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="e6601-113">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6601-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6601-114">Remarks</span></span>

<span data-ttu-id="e6601-115">In einer Anwendung können andere Zeitformate als Frames oder Millisekunden angegeben werden, solange die Formate vom MCI-Gerät unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e6601-115">An application can specify time formats other than frames or milliseconds as long as the formats are supported by the MCI device.</span></span> <span data-ttu-id="e6601-116">Nicht kontinuierliche Formate, wie z. b. "Tracks" und "SMPTE", können dazu führen, dass sich die TrackBar in der Status-</span><span class="sxs-lookup"><span data-stu-id="e6601-116">Noncontinuous formats, such as tracks and SMPTE, can cause the trackbar to behave erratically.</span></span> <span data-ttu-id="e6601-117">Für diese Zeitformate empfiehlt es sich, die Symbolleiste zu deaktivieren, indem Sie das [**mciwndchangestyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) -Makro verwenden und den Fenster Stil mciwndf \_ noplaybar angeben.</span><span class="sxs-lookup"><span data-stu-id="e6601-117">For these time formats, you might want to turn off the toolbar by using the [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) macro and specifying the MCIWNDF\_NOPLAYBAR window style.</span></span>

<span data-ttu-id="e6601-118">Wenn Sie das Zeitformat auf Frames oder Millisekunden festlegen möchten, können Sie auch das Makro [**mciwnduseframes**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) oder [**mciwndusetime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) verwenden.</span><span class="sxs-lookup"><span data-stu-id="e6601-118">If you want to set the time format to frames or milliseconds, you can also use the [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) or [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) macro.</span></span> <span data-ttu-id="e6601-119">Eine Liste der Zeitformate finden Sie unter dem [**mciwndgettimeformat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) -Makro.</span><span class="sxs-lookup"><span data-stu-id="e6601-119">For a list of time formats, see the [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6601-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6601-120">Requirements</span></span>



| <span data-ttu-id="e6601-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6601-121">Requirement</span></span> | <span data-ttu-id="e6601-122">Wert</span><span class="sxs-lookup"><span data-stu-id="e6601-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e6601-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6601-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e6601-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6601-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e6601-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6601-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e6601-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6601-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e6601-127">Header</span><span class="sxs-lookup"><span data-stu-id="e6601-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6601-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6601-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6601-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6601-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6601-130">**Mciwndchangestyles**</span><span class="sxs-lookup"><span data-stu-id="e6601-130">**MCIWndChangeStyles**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> <dt>

[<span data-ttu-id="e6601-131">**Mciwndgettimeformat**</span><span class="sxs-lookup"><span data-stu-id="e6601-131">**MCIWndGetTimeFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> <dt>

[<span data-ttu-id="e6601-132">**Mciwndsettimeformat**</span><span class="sxs-lookup"><span data-stu-id="e6601-132">**MCIWndSetTimeFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat)
</dt> <dt>

[<span data-ttu-id="e6601-133">**Mciwnduabframes**</span><span class="sxs-lookup"><span data-stu-id="e6601-133">**MCIWndUseFrames**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes)
</dt> <dt>

[<span data-ttu-id="e6601-134">**Mciwndul-Zeit**</span><span class="sxs-lookup"><span data-stu-id="e6601-134">**MCIWndUseTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime)
</dt> </dl>

 

 





