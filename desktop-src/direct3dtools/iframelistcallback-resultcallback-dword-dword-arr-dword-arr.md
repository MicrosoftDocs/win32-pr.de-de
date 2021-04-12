---
description: Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, welche Frames aufgezeichnet wurden.
MS-HAID: vspixengine.IFrameListCallback\_ResultCallback\_DWORD\_DWORD\_arr\_DWORD\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iframelistcallback:: resultCallback-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AEB340C6-74AA-4F8B-86D0-9C0366ECDE70
api_name:
- IFrameListCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 00a991ec2d380d9c052f02ed69bb71d233fd0d93
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482662"
---
# <a name="span-idvspixengineiframelistcallback_resultcallback_dword_dword_arr_dword_arrspaniframelistcallbackresultcallback-method"></a><span data-ttu-id="9c4f7-103"><span id="vspixengine.iframelistcallback_resultcallback_dword_dword_arr_dword_arr"></span>Iframelistcallback:: resultCallback-Methode</span><span class="sxs-lookup"><span data-stu-id="9c4f7-103"><span id="vspixengine.iframelistcallback_resultcallback_dword_dword_arr_dword_arr"></span>IFrameListCallback::ResultCallback method</span></span>

<span data-ttu-id="9c4f7-104">Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, welche Frames aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="9c4f7-104">A callback function used to notify the host of which frames were captured.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c4f7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c4f7-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD    numFrames,
   DWORD [] count0_frameNumbers,
   DWORD [] count0_frameEventIDs
);
```

## <a name="parameters"></a><span data-ttu-id="9c4f7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c4f7-106">Parameters</span></span>

<span data-ttu-id="9c4f7-107">*numFrames* </span><span class="sxs-lookup"><span data-stu-id="9c4f7-107">*numFrames* </span></span>  
<span data-ttu-id="9c4f7-108">Die Anzahl der aufgezeichneten Frames.</span><span class="sxs-lookup"><span data-stu-id="9c4f7-108">The number of frames captured.</span></span>

<span data-ttu-id="9c4f7-109">*count0 \_ frameNum* </span><span class="sxs-lookup"><span data-stu-id="9c4f7-109">*count0\_frameNumbers* </span></span>  
<span data-ttu-id="9c4f7-110">Die Frame Nummern der aufgezeichneten Frames.</span><span class="sxs-lookup"><span data-stu-id="9c4f7-110">The frame numbers of the captured frames.</span></span>

<span data-ttu-id="9c4f7-111">*count0 \_ frameeventids* </span><span class="sxs-lookup"><span data-stu-id="9c4f7-111">*count0\_frameEventIDs* </span></span>  
<span data-ttu-id="9c4f7-112">Das abschließende Ereignis, das jedem Frame zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9c4f7-112">The final event associated with each frame.</span></span>

## <a name="return-value"></a><span data-ttu-id="9c4f7-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9c4f7-113">Return value</span></span>

<span data-ttu-id="9c4f7-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="9c4f7-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9c4f7-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9c4f7-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c4f7-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c4f7-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9c4f7-117">Header</span><span class="sxs-lookup"><span data-stu-id="9c4f7-117">Header</span></span></p></td><td><span data-ttu-id="9c4f7-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="9c4f7-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="9c4f7-119"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c4f7-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="9c4f7-120">**Iframelistcallback**</span><span class="sxs-lookup"><span data-stu-id="9c4f7-120">**IFrameListCallback**</span></span>](/windows/desktop/direct3dtools/iframelistcallback)

 

 
