---
title: ICM_GETINFO Meldung (VFW. h)
description: Die ICM \_ GetInfo-Nachricht fragt einen Video Komprimierungs Treiber ab, um eine Beschreibung von sich selbst in einer icinfo-Struktur zurückzugeben.
ms.assetid: 8029f247-9777-4a34-9e84-908482094493
keywords:
- ICM_GETINFO-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_GETINFO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 634803b7dd9a3b8900c35fabedcadb99908c2b31
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337935"
---
# <a name="icm_getinfo-message"></a><span data-ttu-id="8bb44-104">ICM \_ GetInfo-Nachricht</span><span class="sxs-lookup"><span data-stu-id="8bb44-104">ICM\_GETINFO message</span></span>

<span data-ttu-id="8bb44-105">Die **ICM \_ GetInfo** -Nachricht fragt einen Video Komprimierungs Treiber ab, um eine Beschreibung von sich selbst in einer [**icinfo**](/windows/desktop/api/Vfw/ns-vfw-icinfo) -Struktur zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="8bb44-105">The **ICM\_GETINFO** message queries a video compression driver to return a description of itself in an [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) structure.</span></span>


```C++
ICM_GETINFO 
wParam = (DWORD) (LPVOID) lpicinfo; 
lParam = sizeof(ICINFO); 
```



## <a name="parameters"></a><span data-ttu-id="8bb44-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8bb44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bb44-107"><span id="lpicinfo"></span><span id="LPICINFO"></span>*lpicinfo*</span><span class="sxs-lookup"><span data-stu-id="8bb44-107"><span id="lpicinfo"></span><span id="LPICINFO"></span>*lpicinfo*</span></span>
</dt> <dd>

<span data-ttu-id="8bb44-108">Zeiger auf eine **icinfo** -Struktur, die Informationen enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="8bb44-108">Pointer to an **ICINFO** structure to contain information.</span></span>

</dd> <dt>

<span data-ttu-id="8bb44-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="8bb44-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="8bb44-110">Größe von **icinfo**(in Bytes).</span><span class="sxs-lookup"><span data-stu-id="8bb44-110">Size, in bytes, of **ICINFO**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bb44-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8bb44-111">Return Value</span></span>

<span data-ttu-id="8bb44-112">Gibt die Größe von [**icinfo**](/windows/desktop/api/Vfw/ns-vfw-icinfo) (in Bytes) oder 0 (null) zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="8bb44-112">Returns the size, in bytes, of [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) or zero if an error occurs..</span></span>

## <a name="remarks"></a><span data-ttu-id="8bb44-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8bb44-113">Remarks</span></span>

<span data-ttu-id="8bb44-114">Normalerweise senden Anwendungen diese Nachricht, um eine Liste der installierten Kompressoren anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8bb44-114">Typically, applications send this message to display a list of the installed compressors.</span></span>

<span data-ttu-id="8bb44-115">Der Treiber sollte alle Elemente der [**icinfo**](/windows/desktop/api/Vfw/ns-vfw-icinfo) -Struktur mit Ausnahme von **szdriver** ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="8bb44-115">The driver should fill all members of the [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) structure except **szDriver**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bb44-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8bb44-116">Requirements</span></span>



| <span data-ttu-id="8bb44-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8bb44-117">Requirement</span></span> | <span data-ttu-id="8bb44-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8bb44-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8bb44-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8bb44-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8bb44-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8bb44-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8bb44-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8bb44-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8bb44-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8bb44-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8bb44-123">Header</span><span class="sxs-lookup"><span data-stu-id="8bb44-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bb44-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bb44-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bb44-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8bb44-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bb44-126">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="8bb44-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="8bb44-127">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="8bb44-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





