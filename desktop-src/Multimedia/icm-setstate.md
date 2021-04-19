---
title: ICM_SETSTATE Meldung (VFW. h)
description: In der ICM- \_ SetState-Meldung wird ein Video Komprimierungs Treiber benachrichtigt, um den Status des-Kompressors festzulegen. Sie können diese Nachricht explizit oder mithilfe des icsetstate-Makros senden.
ms.assetid: d1a91847-2893-4c8b-9ca1-02db71ec2c81
keywords:
- ICM_SETSTATE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_SETSTATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 230e0aaf3752016efd276d7d55624ee2abb4f8e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339606"
---
# <a name="icm_setstate-message"></a><span data-ttu-id="3fd15-105">ICM- \_ SetState-Meldung</span><span class="sxs-lookup"><span data-stu-id="3fd15-105">ICM\_SETSTATE message</span></span>

<span data-ttu-id="3fd15-106">In der **ICM- \_ SetState** -Meldung wird ein Video Komprimierungs Treiber benachrichtigt, um den Status des-Kompressors festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3fd15-106">The **ICM\_SETSTATE** message notifies a video compression driver to set the state of the compressor.</span></span> <span data-ttu-id="3fd15-107">Sie können diese Nachricht explizit oder mithilfe des [**icsetstate**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="3fd15-107">You can send this message explicitly or by using the [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) macro.</span></span>


```C++
ICM_SETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a><span data-ttu-id="3fd15-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3fd15-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fd15-109"><span id="pv"></span><span id="PV"></span>*teuren*</span><span class="sxs-lookup"><span data-stu-id="3fd15-109"><span id="pv"></span><span id="PV"></span>*pv*</span></span>
</dt> <dd>

<span data-ttu-id="3fd15-110">Zeiger auf einen Speicherblock, der Konfigurationsdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="3fd15-110">Pointer to a block of memory containing configuration data.</span></span> <span data-ttu-id="3fd15-111">Sie können **null** für diesen Parameter angeben, um den-Kompressor auf den Standardzustand zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="3fd15-111">You can specify **NULL** for this parameter to reset the compressor to its default state.</span></span>

</dd> <dt>

<span data-ttu-id="3fd15-112"><span id="cb"></span><span id="CB"></span>*betrieben*</span><span class="sxs-lookup"><span data-stu-id="3fd15-112"><span id="cb"></span><span id="CB"></span>*cb*</span></span>
</dt> <dd>

<span data-ttu-id="3fd15-113">Größe des Speicherblocks in Bytes.</span><span class="sxs-lookup"><span data-stu-id="3fd15-113">Size, in bytes, of the block of memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fd15-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3fd15-114">Return Value</span></span>

<span data-ttu-id="3fd15-115">Gibt die Anzahl der Bytes zurück, die vom-Kompressor bei erfolgreicher Ausführung verwendet werden, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="3fd15-115">Returns the number of bytes used by the compressor if successful or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fd15-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3fd15-116">Remarks</span></span>

<span data-ttu-id="3fd15-117">Die von dieser Nachricht verwendeten Informationen sind privat und spezifisch für einen bestimmten Kompressor.</span><span class="sxs-lookup"><span data-stu-id="3fd15-117">The information used by this message is private and specific to a given compressor.</span></span> <span data-ttu-id="3fd15-118">Client Anwendungen sollten diese Nachricht nur zum Wiederherstellen von Informationen verwenden, die zuvor mit der [**ICM \_ GetState**](icm-getstate.md) -Nachricht abgerufen wurden, und die [**ICM \_**](icm-configure.md) -Konfigurations Nachricht verwenden, um die Konfiguration eines Video Komprimierungs Treibers anzupassen.</span><span class="sxs-lookup"><span data-stu-id="3fd15-118">Client applications should use this message only to restore information previously obtained with the [**ICM\_GETSTATE**](icm-getstate.md) message and should use the [**ICM\_CONFIGURE**](icm-configure.md) message to adjust the configuration of a video compression driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fd15-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3fd15-119">Requirements</span></span>



| <span data-ttu-id="3fd15-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3fd15-120">Requirement</span></span> | <span data-ttu-id="3fd15-121">Wert</span><span class="sxs-lookup"><span data-stu-id="3fd15-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3fd15-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3fd15-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3fd15-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3fd15-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3fd15-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3fd15-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3fd15-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3fd15-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3fd15-126">Header</span><span class="sxs-lookup"><span data-stu-id="3fd15-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fd15-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fd15-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fd15-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3fd15-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fd15-129">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="3fd15-129">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="3fd15-130">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="3fd15-130">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





