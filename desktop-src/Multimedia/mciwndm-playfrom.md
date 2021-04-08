---
title: MCIWNDM_PLAYFROM Meldung (VFW. h)
description: Die mciwndm \_ playfrom-Meldung gibt den Inhalt eines MCI-Geräts vom angegebenen Speicherort bis zum Ende des Inhalts oder bis zur Beendigung der Wiedergabe durch einen anderen Befehl wieder. Sie können diese Nachricht explizit oder mithilfe des Makros mciwndplayfrom senden.
ms.assetid: 1c47f8eb-2a1b-4671-a9f8-fd6d59a5c7c6
keywords:
- MCIWNDM_PLAYFROM-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYFROM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0fa1b3f4b3359e1609b3ba12009fe5879c304a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949530"
---
# <a name="mciwndm_playfrom-message"></a><span data-ttu-id="9aa4d-105">Mciwndm \_ playfrom-Meldung</span><span class="sxs-lookup"><span data-stu-id="9aa4d-105">MCIWNDM\_PLAYFROM message</span></span>

<span data-ttu-id="9aa4d-106">Die **mciwndm \_ playfrom** -Meldung gibt den Inhalt eines MCI-Geräts vom angegebenen Speicherort bis zum Ende des Inhalts oder bis zur Beendigung der Wiedergabe durch einen anderen Befehl wieder.</span><span class="sxs-lookup"><span data-stu-id="9aa4d-106">The **MCIWNDM\_PLAYFROM** message plays the content of an MCI device from the specified location to the end of the content or until another command stops playback.</span></span> <span data-ttu-id="9aa4d-107">Sie können diese Nachricht explizit oder mithilfe des Makros [**mciwndplayfrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) senden.</span><span class="sxs-lookup"><span data-stu-id="9aa4d-107">You can send this message explicitly or by using the [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) macro.</span></span>


```C++
MCIWNDM_PLAYFROM 
wParam = 0; 
lParam = (LPARAM) (LONG) lPos; 
```



## <a name="parameters"></a><span data-ttu-id="9aa4d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9aa4d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aa4d-109"><span id="lPos"></span><span id="lpos"></span><span id="LPOS"></span>*lPos*</span><span class="sxs-lookup"><span data-stu-id="9aa4d-109"><span id="lPos"></span><span id="lpos"></span><span id="LPOS"></span>*lPos*</span></span>
</dt> <dd>

<span data-ttu-id="9aa4d-110">Start Speicherort.</span><span class="sxs-lookup"><span data-stu-id="9aa4d-110">Starting location.</span></span> <span data-ttu-id="9aa4d-111">Die Einheiten für den Start Speicherort hängen vom aktuellen Zeitformat ab.</span><span class="sxs-lookup"><span data-stu-id="9aa4d-111">The units for the starting location depend on the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aa4d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9aa4d-112">Return Value</span></span>

<span data-ttu-id="9aa4d-113">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="9aa4d-113">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9aa4d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9aa4d-114">Remarks</span></span>

<span data-ttu-id="9aa4d-115">Sie können auch einen Start-und einen endspeicherort für die Wiedergabe angeben, indem Sie das [**mciwndplayfromto**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="9aa4d-115">You can also specify both a starting and ending location for playback by using the [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aa4d-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9aa4d-116">Requirements</span></span>



| <span data-ttu-id="9aa4d-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9aa4d-117">Requirement</span></span> | <span data-ttu-id="9aa4d-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9aa4d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9aa4d-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9aa4d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9aa4d-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9aa4d-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9aa4d-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9aa4d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9aa4d-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9aa4d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9aa4d-123">Header</span><span class="sxs-lookup"><span data-stu-id="9aa4d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9aa4d-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="9aa4d-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9aa4d-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9aa4d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aa4d-126">**Mciwndplayfrom**</span><span class="sxs-lookup"><span data-stu-id="9aa4d-126">**MCIWndPlayFrom**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom)
</dt> <dt>

[<span data-ttu-id="9aa4d-127">**Mciwndplayfromto**</span><span class="sxs-lookup"><span data-stu-id="9aa4d-127">**MCIWndPlayFromTo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> </dl>

 

 





