---
title: ICM_DECOMPRESSEX_END Meldung (VFW. h)
description: Die ICM \_ decompressex- \_ Endnachricht benachrichtigt einen Video Dekomprimierung-Treiber, um die Dekomprimierung zu beenden und die für die Dekomprimierung zugewiesenen Ressourcen freizugeben. Sie können diese Nachricht explizit oder mithilfe des icdecompressexend-Makros senden.
ms.assetid: 7ed63a4e-bb17-43a3-b593-25c4a51be942
keywords:
- ICM_DECOMPRESSEX_END-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7e96f6a069e9ed2c9c52dc2f07f1ab4c5210ecd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518641"
---
# <a name="icm_decompressex_end-message"></a><span data-ttu-id="58342-105">ICM \_ decompressex- \_ Endmeldung</span><span class="sxs-lookup"><span data-stu-id="58342-105">ICM\_DECOMPRESSEX\_END message</span></span>

<span data-ttu-id="58342-106">Die **ICM \_ decompressex- \_ Endnachricht** benachrichtigt einen Video Dekomprimierung-Treiber, um die Dekomprimierung zu beenden und die für die Dekomprimierung zugewiesenen Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="58342-106">The **ICM\_DECOMPRESSEX\_END** message notifies a video decompression driver to end decompression and free resources allocated for decompression.</span></span> <span data-ttu-id="58342-107">Sie können diese Nachricht explizit oder mithilfe des [**icdecompressexend**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="58342-107">You can send this message explicitly or by using the [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) macro.</span></span>


```C++
ICM_DECOMPRESSEX_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="58342-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="58342-108">Return Value</span></span>

<span data-ttu-id="58342-109">Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="58342-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="58342-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58342-110">Remarks</span></span>

<span data-ttu-id="58342-111">Der Treiber gibt alle Ressourcen frei, die für die [**ICM- \_ decompressex- \_ Begin**](icm-decompressex-begin.md) -Nachricht zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="58342-111">The driver frees any resources allocated for the [**ICM\_DECOMPRESSEX\_BEGIN**](icm-decompressex-begin.md) message.</span></span>

<span data-ttu-id="58342-112">[**ICM \_ Das Beenden von "de CompressEx \_ Begin**](icm-decompressex-begin.md) " und " **ICM \_ \_** " wird nicht geschachtelt.</span><span class="sxs-lookup"><span data-stu-id="58342-112">[**ICM\_DECOMPRESSEX\_BEGIN**](icm-decompressex-begin.md) and **ICM\_DECOMPRESSEX\_END** do not nest.</span></span> <span data-ttu-id="58342-113">Wenn Ihr Treiber **ICM \_ decompressex \_ Begin** empfängt, bevor die Dekomprimierung mit **ICM \_ decompressex \_ End** beendet wird, sollte die Dekomprimierung mit neuen Parametern neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="58342-113">If your driver receives **ICM\_DECOMPRESSEX\_BEGIN** before decompression is stopped with **ICM\_DECOMPRESSEX\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="58342-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58342-114">Requirements</span></span>



| <span data-ttu-id="58342-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58342-115">Requirement</span></span> | <span data-ttu-id="58342-116">Wert</span><span class="sxs-lookup"><span data-stu-id="58342-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="58342-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58342-117">Minimum supported client</span></span><br/> | <span data-ttu-id="58342-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58342-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="58342-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58342-119">Minimum supported server</span></span><br/> | <span data-ttu-id="58342-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58342-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="58342-121">Header</span><span class="sxs-lookup"><span data-stu-id="58342-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="58342-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="58342-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58342-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58342-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58342-124">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="58342-124">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="58342-125">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="58342-125">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





