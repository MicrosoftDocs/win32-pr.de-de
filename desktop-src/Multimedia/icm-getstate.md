---
title: ICM_GETSTATE Meldung (VFW. h)
description: Die ICM \_ GetState-Nachricht fragt einen Video Komprimierungs Treiber ab, um die aktuelle Konfiguration in einem Speicherblock zurückzugeben, oder um die Menge an Arbeitsspeicher zu ermitteln, die zum Abrufen der Konfigurationsinformationen erforderlich ist.
ms.assetid: 4b77e294-f3aa-45f9-a4f4-f103b83eae8d
keywords:
- ICM_GETSTATE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_GETSTATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b6a45dcde627a02c1a4a402ea9a2a725f0429a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106550"
---
# <a name="icm_getstate-message"></a><span data-ttu-id="381aa-104">ICM \_ GetState-Nachricht</span><span class="sxs-lookup"><span data-stu-id="381aa-104">ICM\_GETSTATE message</span></span>

<span data-ttu-id="381aa-105">Die **ICM \_ GetState** -Nachricht fragt einen Video Komprimierungs Treiber ab, um die aktuelle Konfiguration in einem Speicherblock zurückzugeben, oder um die Menge an Arbeitsspeicher zu ermitteln, die zum Abrufen der Konfigurationsinformationen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="381aa-105">The **ICM\_GETSTATE** message queries a video compression driver to return its current configuration in a block of memory or to determine the amount of memory required to retrieve the configuration information.</span></span> <span data-ttu-id="381aa-106">Sie können diese Nachricht explizit oder mithilfe des [**icgetstate**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="381aa-106">You can send this message explicitly or by using the [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) macro.</span></span>


```C++
ICM_GETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a><span data-ttu-id="381aa-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="381aa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="381aa-108"><span id="pv"></span><span id="PV"></span>*teuren*</span><span class="sxs-lookup"><span data-stu-id="381aa-108"><span id="pv"></span><span id="PV"></span>*pv*</span></span>
</dt> <dd>

<span data-ttu-id="381aa-109">Ein Zeiger auf einen Speicherblock, der die aktuellen Konfigurationsinformationen enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="381aa-109">Pointer to a block of memory to contain the current configuration information.</span></span> <span data-ttu-id="381aa-110">Sie können **null** für diesen Parameter angeben, um den für die Konfigurationsinformationen erforderlichen Arbeitsspeicher zu bestimmen, wie in [**icgetstatus esize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize).</span><span class="sxs-lookup"><span data-stu-id="381aa-110">You can specify **NULL** for this parameter to determine the amount of memory required for the configuration information, as in [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize).</span></span>

</dd> <dt>

<span data-ttu-id="381aa-111"><span id="cb"></span><span id="CB"></span>*betrieben*</span><span class="sxs-lookup"><span data-stu-id="381aa-111"><span id="cb"></span><span id="CB"></span>*cb*</span></span>
</dt> <dd>

<span data-ttu-id="381aa-112">Größe des Speicherblocks in Bytes.</span><span class="sxs-lookup"><span data-stu-id="381aa-112">Size, in bytes, of the block of memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="381aa-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="381aa-113">Return Value</span></span>

<span data-ttu-id="381aa-114">Wenn *PV* den Wert **null** hat, wird die Menge an Arbeitsspeicher in Bytes zurückgegeben, die für Konfigurationsinformationen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="381aa-114">If *pv* is **NULL**, returns the amount of memory, in bytes, required for configuration information.</span></span>

<span data-ttu-id="381aa-115">Wenn *PV* nicht **null** ist, wird bei erfolgreicher Ausführung von ICERR OK zurückgegeben, \_ andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="381aa-115">If *pv* is not **NULL**, returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="381aa-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="381aa-116">Remarks</span></span>

<span data-ttu-id="381aa-117">Die Struktur, die zum Darstellen von Konfigurationsinformationen verwendet wird, ist Treiber spezifisch und wird vom Treiber definiert.</span><span class="sxs-lookup"><span data-stu-id="381aa-117">The structure used to represent configuration information is driver specific and is defined by the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="381aa-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="381aa-118">Requirements</span></span>



| <span data-ttu-id="381aa-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="381aa-119">Requirement</span></span> | <span data-ttu-id="381aa-120">Wert</span><span class="sxs-lookup"><span data-stu-id="381aa-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="381aa-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="381aa-121">Minimum supported client</span></span><br/> | <span data-ttu-id="381aa-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="381aa-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="381aa-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="381aa-123">Minimum supported server</span></span><br/> | <span data-ttu-id="381aa-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="381aa-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="381aa-125">Header</span><span class="sxs-lookup"><span data-stu-id="381aa-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="381aa-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="381aa-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="381aa-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="381aa-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="381aa-128">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="381aa-128">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="381aa-129">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="381aa-129">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





