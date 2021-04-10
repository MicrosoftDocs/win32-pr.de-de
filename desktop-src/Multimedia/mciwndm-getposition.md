---
title: MCIWNDM_GETPOSITION Meldung (VFW. h)
description: Die mciwndm \_ GetPosition-Nachricht Ruft den numerischen Wert der aktuellen Position im Inhalt des MCI-Geräts ab.
ms.assetid: 6dc5d3bd-8515-4514-a2a5-c1bee07f7acf
keywords:
- MCIWNDM_GETPOSITION-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETPOSITION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e7468b0e3698a72d3dce82bbd1591d59940d9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858704"
---
# <a name="mciwndm_getposition-message"></a><span data-ttu-id="35a25-104">Mciwndm \_ GetPosition-Nachricht</span><span class="sxs-lookup"><span data-stu-id="35a25-104">MCIWNDM\_GETPOSITION message</span></span>

<span data-ttu-id="35a25-105">Die **mciwndm \_ GetPosition** -Nachricht Ruft den numerischen Wert der aktuellen Position im Inhalt des MCI-Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="35a25-105">The **MCIWNDM\_GETPOSITION** message retrieves the numerical value of the current position within the content of the MCI device.</span></span> <span data-ttu-id="35a25-106">Dieses Makro stellt außerdem die aktuelle Position in der Zeichenfolge in einem von der Anwendung definierten Puffer bereit.</span><span class="sxs-lookup"><span data-stu-id="35a25-106">This macro also provides the current position in string form in an application-defined buffer.</span></span> <span data-ttu-id="35a25-107">Sie können diese Nachricht explizit oder mithilfe des Makros [**mciwndgetposition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) oder [**mciwndgetpositionstring**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) senden.</span><span class="sxs-lookup"><span data-stu-id="35a25-107">You can send this message explicitly or by using the [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) or [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) macro.</span></span>


```C++
MCIWNDM_GETPOSITION 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPTSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="35a25-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="35a25-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35a25-109"><span id="len"></span><span id="LEN"></span>*Nest*</span><span class="sxs-lookup"><span data-stu-id="35a25-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="35a25-110">Größe (in Bytes) des Puffers.</span><span class="sxs-lookup"><span data-stu-id="35a25-110">Size, in bytes, of the buffer.</span></span> <span data-ttu-id="35a25-111">Wenn die auf NULL endenden Zeichenfolge länger als der Puffer ist, wird Sie abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="35a25-111">If the null-terminated string is longer than the buffer, it is truncated.</span></span> <span data-ttu-id="35a25-112">Verwenden Sie 0 (null), um das Abrufen der Position als Zeichenfolge zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="35a25-112">Use zero to inhibit retrieval of the position as a string.</span></span>

</dd> <dt>

<span data-ttu-id="35a25-113"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="35a25-113"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="35a25-114">Zeiger auf einen Anwendungs definierten Puffer, der zum Zurückgeben der Position verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="35a25-114">Pointer to an application-defined buffer used to return the position.</span></span> <span data-ttu-id="35a25-115">Verwenden Sie 0 (null), um das Abrufen der Position als Zeichenfolge zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="35a25-115">Use zero to inhibit retrieval of the position as a string.</span></span> <span data-ttu-id="35a25-116">Wenn das Gerät Spuren unterstützt, werden die Zeichen folgen Positionsinformationen im Format TT: mm: SS: FF zurückgegeben, wobei TT den Titeln entspricht, mm und SS den Minuten und Sekunden entsprechen und FF den Frames entspricht.</span><span class="sxs-lookup"><span data-stu-id="35a25-116">If the device supports tracks, the string position information is returned in the form TT:MM:SS:FF where TT corresponds to tracks, MM and SS correspond to minutes and seconds, and FF corresponds to frames.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35a25-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35a25-117">Return Value</span></span>

<span data-ttu-id="35a25-118">Gibt eine ganze Zahl zurück, die der aktuellen Position entspricht.</span><span class="sxs-lookup"><span data-stu-id="35a25-118">Returns an integer corresponding to the current position.</span></span> <span data-ttu-id="35a25-119">Die Einheiten für den Positionswert hängen vom aktuellen Zeitformat ab.</span><span class="sxs-lookup"><span data-stu-id="35a25-119">The units for the position value depend on the current time format.</span></span>

## <a name="requirements"></a><span data-ttu-id="35a25-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35a25-120">Requirements</span></span>



| <span data-ttu-id="35a25-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35a25-121">Requirement</span></span> | <span data-ttu-id="35a25-122">Wert</span><span class="sxs-lookup"><span data-stu-id="35a25-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="35a25-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="35a25-123">Minimum supported client</span></span><br/> | <span data-ttu-id="35a25-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35a25-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="35a25-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="35a25-125">Minimum supported server</span></span><br/> | <span data-ttu-id="35a25-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35a25-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="35a25-127">Header</span><span class="sxs-lookup"><span data-stu-id="35a25-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="35a25-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="35a25-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35a25-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35a25-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35a25-130">**Mciwndgetposition**</span><span class="sxs-lookup"><span data-stu-id="35a25-130">**MCIWndGetPosition**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition)
</dt> <dt>

[<span data-ttu-id="35a25-131">**Mciwndgetpositionstring**</span><span class="sxs-lookup"><span data-stu-id="35a25-131">**MCIWndGetPositionString**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring)
</dt> </dl>

 

 





