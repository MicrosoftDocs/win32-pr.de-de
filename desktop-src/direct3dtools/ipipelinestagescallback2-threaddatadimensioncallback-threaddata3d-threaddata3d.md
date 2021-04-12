---
description: Ein Rückruf, der den Host über die Anzahl der Threads und Gruppen des Compute-Shaders in der zugeordneten Anforderung benachrichtigt.
MS-HAID: vspixengine.IPipeLineStagesCallback2\_ThreadDataDimensionCallback\_ThreadData3D\_ThreadData3D
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesCallback2:: threaddatadimensioncallback-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E8765C14-0A55-468D-BCA8-3E28E5476DFB
api_name:
- IPipeLineStagesCallback2.ThreadDataDimensionCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 93a8ee64c863128513563f3ce50dd2bfcdd77714
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392821"
---
# <a name="span-idvspixengineipipelinestagescallback2_threaddatadimensioncallback_threaddata3d_threaddata3dspanipipelinestagescallback2threaddatadimensioncallback-method"></a><span data-ttu-id="b6bb3-103"><span id="vspixengine.ipipelinestagescallback2_threaddatadimensioncallback_threaddata3d_threaddata3d"></span>IPipeLineStagesCallback2:: threaddatadimensioncallback-Methode</span><span class="sxs-lookup"><span data-stu-id="b6bb3-103"><span id="vspixengine.ipipelinestagescallback2_threaddatadimensioncallback_threaddata3d_threaddata3d"></span>IPipeLineStagesCallback2::ThreadDataDimensionCallback method</span></span>

<span data-ttu-id="b6bb3-104">Ein Rückruf, der den Host über die Anzahl der Threads und Gruppen des Compute-Shaders in der zugeordneten Anforderung benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="b6bb3-104">A callback that notifies the host of the number of threads and groups of the compute shader in the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6bb3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6bb3-105">Syntax</span></span>


```C++
HRESULT ThreadDataDimensionCallback(
   ThreadData3D threadGroupCount,
   ThreadData3D threadGroupSize
);
```

## <a name="parameters"></a><span data-ttu-id="b6bb3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6bb3-106">Parameters</span></span>

<span data-ttu-id="b6bb3-107">*threadgroupcount* </span><span class="sxs-lookup"><span data-stu-id="b6bb3-107">*threadGroupCount* </span></span>  
<span data-ttu-id="b6bb3-108">Die mehrdimensionale Anzahl von Thread Gruppen.</span><span class="sxs-lookup"><span data-stu-id="b6bb3-108">The multi-dimensional count of thread groups.</span></span>

<span data-ttu-id="b6bb3-109">*threadgroupsize* </span><span class="sxs-lookup"><span data-stu-id="b6bb3-109">*threadGroupSize* </span></span>  
<span data-ttu-id="b6bb3-110">Die mehrdimensionale Größe der einzelnen Thread Gruppen.</span><span class="sxs-lookup"><span data-stu-id="b6bb3-110">The multi-dimensional size of each thread group.</span></span>

## <a name="return-value"></a><span data-ttu-id="b6bb3-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b6bb3-111">Return value</span></span>

<span data-ttu-id="b6bb3-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="b6bb3-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b6bb3-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b6bb3-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6bb3-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6bb3-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b6bb3-115">Header</span><span class="sxs-lookup"><span data-stu-id="b6bb3-115">Header</span></span></p></td><td><span data-ttu-id="b6bb3-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b6bb3-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b6bb3-117"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6bb3-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b6bb3-118">**IPipeLineStagesCallback2**</span><span class="sxs-lookup"><span data-stu-id="b6bb3-118">**IPipeLineStagesCallback2**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback2)

 

 
