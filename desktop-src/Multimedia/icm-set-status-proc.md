---
title: ICM_SET_STATUS_PROC Meldung (VFW. h)
description: Die ICM \_ Set \_ Status \_ proc-Nachricht stellt eine Status Rückruffunktion mit dem Status eines langwierigen Vorgangs bereit.
ms.assetid: a1bcd840-b94b-487e-91d6-67411a8a3a2d
keywords:
- ICM_SET_STATUS_PROC-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_SET_STATUS_PROC
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d7ad2745ab53c2e04a1588ddbf1b1e5d755202
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479389"
---
# <a name="icm_set_status_proc-message"></a><span data-ttu-id="a794e-104">ICM \_ - \_ Status-proc- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="a794e-104">ICM\_SET\_STATUS\_PROC message</span></span>

<span data-ttu-id="a794e-105">Die **ICM \_ Set \_ Status \_ proc** -Nachricht stellt eine Status Rückruffunktion mit dem Status eines langwierigen Vorgangs bereit.</span><span class="sxs-lookup"><span data-stu-id="a794e-105">The **ICM\_SET\_STATUS\_PROC** message provides a status callback function with the status of a lengthy operation.</span></span>


```C++
ICM_SET_STATUS_PROC 
wParam = (DWORD_PTR)icsetstatusProc; 
lParam = sizeof(ICSETSTATUSPROC); 
```



## <a name="parameters"></a><span data-ttu-id="a794e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a794e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a794e-107"><span id="icsetstatusProc"></span><span id="icsetstatusproc"></span><span id="ICSETSTATUSPROC"></span>*icsetstatusproc*</span><span class="sxs-lookup"><span data-stu-id="a794e-107"><span id="icsetstatusProc"></span><span id="icsetstatusproc"></span><span id="ICSETSTATUSPROC"></span>*icsetstatusProc*</span></span>
</dt> <dd>

<span data-ttu-id="a794e-108">Zeiger auf eine [**icsetstatusproc**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="a794e-108">Pointer to an [**ICSETSTATUSPROC**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a794e-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="a794e-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="a794e-110">Größe von **icsetstatusproc** in Byte.</span><span class="sxs-lookup"><span data-stu-id="a794e-110">Size, in bytes, of **ICSETSTATUSPROC**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a794e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a794e-111">Return Value</span></span>

<span data-ttu-id="a794e-112">Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="a794e-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a794e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a794e-113">Remarks</span></span>

<span data-ttu-id="a794e-114">Die Unterstützung dieser Nachricht ist optional, wird jedoch dringend empfohlen, wenn die Komprimierung oder Dekomprimierung länger als ungefähr eine Zehntelsekunde dauert.</span><span class="sxs-lookup"><span data-stu-id="a794e-114">Support of this message is optional but strongly recommended if compression or decompression takes longer than approximately one-tenth of a second.</span></span>

<span data-ttu-id="a794e-115">Eine Anwendung kann diese Nachricht in regelmäßigen Abständen an eine Status Rückruffunktion senden.</span><span class="sxs-lookup"><span data-stu-id="a794e-115">An application can send this message periodically to a status callback function during lengthy operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="a794e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a794e-116">Requirements</span></span>



| <span data-ttu-id="a794e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a794e-117">Requirement</span></span> | <span data-ttu-id="a794e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a794e-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a794e-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a794e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a794e-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a794e-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a794e-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a794e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a794e-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a794e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a794e-123">Header</span><span class="sxs-lookup"><span data-stu-id="a794e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a794e-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="a794e-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a794e-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a794e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a794e-126">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="a794e-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="a794e-127">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="a794e-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





