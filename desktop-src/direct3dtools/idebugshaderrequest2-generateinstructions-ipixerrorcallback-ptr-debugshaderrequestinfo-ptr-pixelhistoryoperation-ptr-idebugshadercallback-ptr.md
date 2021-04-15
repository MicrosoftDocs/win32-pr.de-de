---
description: Fordert zum Generieren von shaderablaufverfolgungs-Anweisungen in einer Debuganforderung auf. Das Ablauf Verfolgungs basierte Debuggen erfolgt auf der CPU (Warp) anstelle der GPU.
MS-HAID: vspixengine.IDebugShaderRequest2\_GenerateInstructions\_IPixErrorCallback\_ptr\_DebugShaderRequestInfo\_ptr\_PixelHistoryOperation\_ptr\_IDebugShaderCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IDebugShaderRequest2:: generateingestructions-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 50685D38-AA85-43D7-9199-12B3776708C2
api_name:
- IDebugShaderRequest2.GenerateInstructions
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e9c1bc2f6b3f885159f21cd7e644545d7639d6b3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521859"
---
# <a name="span-idvspixengineidebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptrspanidebugshaderrequest2generateinstructions-method"></a><span data-ttu-id="96af5-104"><span id="vspixengine.idebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptr"></span>IDebugShaderRequest2:: generateingestructions-Methode</span><span class="sxs-lookup"><span data-stu-id="96af5-104"><span id="vspixengine.idebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptr"></span>IDebugShaderRequest2::GenerateInstructions method</span></span>

<span data-ttu-id="96af5-105">Fordert zum Generieren von shaderablaufverfolgungs-Anweisungen in einer Debuganforderung auf.</span><span class="sxs-lookup"><span data-stu-id="96af5-105">Requests to generate shader trace instructions in a debug request.</span></span> <span data-ttu-id="96af5-106">Das Ablauf Verfolgungs basierte Debuggen erfolgt auf der CPU (Warp) anstelle der GPU.</span><span class="sxs-lookup"><span data-stu-id="96af5-106">Trace-based debugging occurs on the CPU (warp) instead of the GPU.</span></span>

## <a name="syntax"></a><span data-ttu-id="96af5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="96af5-107">Syntax</span></span>


```C++
HRESULT GenerateInstructions(
   IPixErrorCallback *      errorCallback,
   DebugShaderRequestInfo * requestInfo,
   PixelHistoryOperation *  pPixelHistory,
   IDebugShaderCallback *   pCallback
);
```

## <a name="parameters"></a><span data-ttu-id="96af5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="96af5-108">Parameters</span></span>

<span data-ttu-id="96af5-109">*errorcallback* </span><span class="sxs-lookup"><span data-stu-id="96af5-109">*errorCallback* </span></span>  
<span data-ttu-id="96af5-110">Die Adresse eines Rückrufs für Fehler, die beim Erstellen von shaderablaufverfolgungs-Anweisungen auftreten können.</span><span class="sxs-lookup"><span data-stu-id="96af5-110">The address of a callback for errors that might occur while generating shader trace instructions.</span></span>

<span data-ttu-id="96af5-111">*RequestInfo* </span><span class="sxs-lookup"><span data-stu-id="96af5-111">*requestInfo* </span></span>  
<span data-ttu-id="96af5-112">Die Adresse einer debugshaderrequestinfo-Struktur, die das angeforderte Ereignis/Scheitelpunkt/Pixel beschreibt.</span><span class="sxs-lookup"><span data-stu-id="96af5-112">The address of a DebugShaderRequestInfo structure that describes the requested event/vertex/pixel.</span></span>

<span data-ttu-id="96af5-113">*ppixelhistory* </span><span class="sxs-lookup"><span data-stu-id="96af5-113">*pPixelHistory* </span></span>  
<span data-ttu-id="96af5-114">Die Adresse der Pixel Verlaufs Ergebnisse, die zum Suchen des zugeordneten Pixels zum Debuggen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="96af5-114">The address of pixel history results used for finding the associated pixel to debug.</span></span> <span data-ttu-id="96af5-115">Gilt nur beim Debuggen eines Pixelshaders.</span><span class="sxs-lookup"><span data-stu-id="96af5-115">Only applies when debugging a pixel shader.</span></span>

<span data-ttu-id="96af5-116">*pCallback* </span><span class="sxs-lookup"><span data-stu-id="96af5-116">*pCallback* </span></span>  
<span data-ttu-id="96af5-117">Die Adresse eines Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="96af5-117">The address of a callback used to notify the host of results.</span></span>

## <a name="return-value"></a><span data-ttu-id="96af5-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="96af5-118">Return value</span></span>

<span data-ttu-id="96af5-119">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="96af5-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="96af5-120">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="96af5-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="96af5-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96af5-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="96af5-122">Header</span><span class="sxs-lookup"><span data-stu-id="96af5-122">Header</span></span></p></td><td><span data-ttu-id="96af5-123">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="96af5-123">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="96af5-124"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96af5-124"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="96af5-125">**IDebugShaderRequest2**</span><span class="sxs-lookup"><span data-stu-id="96af5-125">**IDebugShaderRequest2**</span></span>](/windows/desktop/direct3dtools/idebugshaderrequest2)

 

 
