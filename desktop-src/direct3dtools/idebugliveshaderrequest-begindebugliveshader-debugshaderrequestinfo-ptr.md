---
description: Anforderungen zum Debuggen eines Shaders auf der GPU (Live Debugging) vs CPU (Ablauf Verfolgungs basiertes Debuggen).
MS-HAID: vspixengine.IDebugLiveShaderRequest\_BeginDebugLiveShader\_DebugShaderRequestInfo\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Idebugliveshaderrequest:: begindebugliveshader-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 805B2B68-C251-4192-85A3-F857B3F204C7
api_name:
- IDebugLiveShaderRequest.BeginDebugLiveShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2b09bff6a414df620e06263e13d94c2f39e36903
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746752"
---
# <a name="span-idvspixengineidebugliveshaderrequest_begindebugliveshader_debugshaderrequestinfo_ptrspanidebugliveshaderrequestbegindebugliveshader-method"></a><span data-ttu-id="b0268-103"><span id="vspixengine.idebugliveshaderrequest_begindebugliveshader_debugshaderrequestinfo_ptr"></span>Idebugliveshaderrequest:: begindebugliveshader-Methode</span><span class="sxs-lookup"><span data-stu-id="b0268-103"><span id="vspixengine.idebugliveshaderrequest_begindebugliveshader_debugshaderrequestinfo_ptr"></span>IDebugLiveShaderRequest::BeginDebugLiveShader method</span></span>

<span data-ttu-id="b0268-104">Anforderungen zum Debuggen eines Shaders auf der GPU (Live Debugging) vs CPU (Ablauf Verfolgungs basiertes Debuggen).</span><span class="sxs-lookup"><span data-stu-id="b0268-104">Requests to debug a shader on the GPU (live debugging) vs CPU (trace-based debugging).</span></span>

## <a name="syntax"></a><span data-ttu-id="b0268-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0268-105">Syntax</span></span>


```C++
HRESULT BeginDebugLiveShader(
   DebugShaderRequestInfo * requestInfo
);
```

## <a name="parameters"></a><span data-ttu-id="b0268-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0268-106">Parameters</span></span>

<span data-ttu-id="b0268-107">*RequestInfo* </span><span class="sxs-lookup"><span data-stu-id="b0268-107">*requestInfo* </span></span>  
<span data-ttu-id="b0268-108">Die Adresse einer debugshaderrequestinfo-Struktur, die das angeforderte Ereignis/Scheitelpunkt/Pixel beschreibt.</span><span class="sxs-lookup"><span data-stu-id="b0268-108">The address of a DebugShaderRequestInfo structure that describes the requested event/vertex/pixel.</span></span>

## <a name="return-value"></a><span data-ttu-id="b0268-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b0268-109">Return value</span></span>

<span data-ttu-id="b0268-110">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="b0268-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b0268-111">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b0268-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0268-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0268-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b0268-113">Header</span><span class="sxs-lookup"><span data-stu-id="b0268-113">Header</span></span></p></td><td><span data-ttu-id="b0268-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b0268-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b0268-115"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0268-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b0268-116">**Idebugliveshaderrequest**</span><span class="sxs-lookup"><span data-stu-id="b0268-116">**IDebugLiveShaderRequest**</span></span>](/windows/desktop/direct3dtools/idebugliveshaderrequest)

 

 
