---
description: Eine Rückruffunktion, die zum Benachrichtigen des Hosts über den Fortschritt des Engines verwendet wird. Dadurch kann der Host auch feststellen, dass die Engine weiterhin ausgeführt wird.
title: 'Istatuscallback:: Status-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4DC2A05F-506C-4AB4-98E1-58827056700D
api_name:
- IStatusCallback.Status
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 09fba28486bd6f1c43e4b0c4fb0dfcf495e0722b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106340094"
---
# <a name="span-idvspixengineistatuscallback_status_dword_dword_dwordspanistatuscallbackstatus-method"></a><span data-ttu-id="b01d6-104"><span id="vspixengine.istatuscallback_status_dword_dword_dword"></span>Istatuscallback:: Status-Methode</span><span class="sxs-lookup"><span data-stu-id="b01d6-104"><span id="vspixengine.istatuscallback_status_dword_dword_dword"></span>IStatusCallback::Status method</span></span>

<span data-ttu-id="b01d6-105">Eine Rückruffunktion, die verwendet wird, um den Host über den Fortschritt der Engine zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="b01d6-105">A callback function used to notify the host of the engine's progress.</span></span> <span data-ttu-id="b01d6-106">Dadurch kann der Host auch feststellen, dass die Engine weiterhin ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b01d6-106">This also serves as a way for the host to determine that the engine is still running.</span></span>

## <a name="syntax"></a><span data-ttu-id="b01d6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b01d6-107">Syntax</span></span>


```C++
HRESULT Status(
   DWORD dwMillisecondsElapsed,
   DWORD dwFramesCaptured,
   DWORD dwFramesElapsed
);
```

## <a name="parameters"></a><span data-ttu-id="b01d6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b01d6-108">Parameters</span></span>

<span data-ttu-id="b01d6-109">*dwmillisecondselapsed* </span><span class="sxs-lookup"><span data-stu-id="b01d6-109">*dwMillisecondsElapsed* </span></span>  
<span data-ttu-id="b01d6-110">Die seit dem letzten Aufruf des Status verstrichene Zeit in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="b01d6-110">The time elapsed since the last call to Status, in milliseconds.</span></span>

<span data-ttu-id="b01d6-111">*dwframesaufgezeichnet* </span><span class="sxs-lookup"><span data-stu-id="b01d6-111">*dwFramesCaptured* </span></span>  
<span data-ttu-id="b01d6-112">Die Anzahl der Frames, die seit dem letzten Status aufgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="b01d6-112">The number of frames that have been captures since the last call to Status.</span></span>

<span data-ttu-id="b01d6-113">*dwframesverstrichene* </span><span class="sxs-lookup"><span data-stu-id="b01d6-113">*dwFramesElapsed* </span></span>  
<span data-ttu-id="b01d6-114">Die Anzahl der Frames, die seit dem letzten Status aufgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="b01d6-114">The number of frames elapsed since the last call to Status.</span></span>

## <a name="return-value"></a><span data-ttu-id="b01d6-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b01d6-115">Return value</span></span>

<span data-ttu-id="b01d6-116">Wenn diese Methode erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b01d6-116">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="b01d6-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b01d6-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b01d6-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b01d6-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b01d6-119">Header</span><span class="sxs-lookup"><span data-stu-id="b01d6-119">Header</span></span></p></td><td><span data-ttu-id="b01d6-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b01d6-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b01d6-121"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b01d6-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b01d6-122">**Istatus Callback**</span><span class="sxs-lookup"><span data-stu-id="b01d6-122">**IStatusCallback**</span></span>](/windows/desktop/direct3dtools/istatuscallback)

 

 
