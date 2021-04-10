---
description: Fordert zum Starten einer shaderdebugsitzung für die angegebene Pipeline Phase, Pixel/Scheitelpunkt, falls zutreffend, Ereignis und Frame.
MS-HAID: vspixengine.IDebugShaderRequest\_BeginDebugShader\_IPixErrorCallback\_ptr\_EventID\_DWORD\_DWORD\_Point2D\_PipeLineStages\_PixelHistoryOperation\_ptr\_DWORD\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Idebugshaderrequest:: begindebugshader-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC93D31C-8593-4B03-B974-87B886B9431D
api_name:
- IDebugShaderRequest.BeginDebugShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b6512dc8aa67b3f4d128be3cd2dcd2b622ba2035
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124633"
---
# <a name="span-idvspixengineidebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptrspanidebugshaderrequestbegindebugshader-method"></a><span data-ttu-id="7d2ff-103"><span id="vspixengine.idebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptr"></span>Idebugshaderrequest:: begindebugshader-Methode</span><span class="sxs-lookup"><span data-stu-id="7d2ff-103"><span id="vspixengine.idebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptr"></span>IDebugShaderRequest::BeginDebugShader method</span></span>

<span data-ttu-id="7d2ff-104">Fordert zum Starten einer shaderdebugsitzung für die angegebene Pipeline Phase, Pixel/Scheitelpunkt, falls zutreffend, Ereignis und Frame.</span><span class="sxs-lookup"><span data-stu-id="7d2ff-104">Requests to start a shader debugging session for the specified pipeline stage, pixel/vertex if applicable, event, and frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d2ff-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d2ff-105">Syntax</span></span>


```C++
HRESULT BeginDebugShader(
   IPixErrorCallback *     errorCallback,
   EventID                 eventID,
   DWORD                   frameNumber,
   DWORD                   vertex,
   Point2D                 pixel,
   PipeLineStages          stage,
   PixelHistoryOperation * pPixelHistory,
   DWORD *                 pDevice
);
```

## <a name="parameters"></a><span data-ttu-id="7d2ff-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d2ff-106">Parameters</span></span>

<span data-ttu-id="7d2ff-107">*errorcallback* </span><span class="sxs-lookup"><span data-stu-id="7d2ff-107">*errorCallback* </span></span>  
<span data-ttu-id="7d2ff-108">Die Adresse eines Rückrufs für Fehler, die während des Debuggens auftreten können.</span><span class="sxs-lookup"><span data-stu-id="7d2ff-108">The address of a callback for errors that might occur during debugging.</span></span>

<span data-ttu-id="7d2ff-109">*EventID* </span><span class="sxs-lookup"><span data-stu-id="7d2ff-109">*eventID* </span></span>  
<span data-ttu-id="7d2ff-110">Das angegebene Ereignis.</span><span class="sxs-lookup"><span data-stu-id="7d2ff-110">The specified event.</span></span>

<span data-ttu-id="7d2ff-111">*Framezahl* </span><span class="sxs-lookup"><span data-stu-id="7d2ff-111">*frameNumber* </span></span>  
<span data-ttu-id="7d2ff-112">Der angegebene Frame.</span><span class="sxs-lookup"><span data-stu-id="7d2ff-112">The specified frame.</span></span>

<span data-ttu-id="7d2ff-113">*Vertex* </span><span class="sxs-lookup"><span data-stu-id="7d2ff-113">*vertex* </span></span>  
<span data-ttu-id="7d2ff-114">Der angegebene Scheitelpunkt.</span><span class="sxs-lookup"><span data-stu-id="7d2ff-114">The specified vertex.</span></span> <span data-ttu-id="7d2ff-115">Gilt nur, wenn ein Vertexshader debuggt wird.</span><span class="sxs-lookup"><span data-stu-id="7d2ff-115">Only applies when debugging a vertex shader.</span></span>

<span data-ttu-id="7d2ff-116">*Megapixel* </span><span class="sxs-lookup"><span data-stu-id="7d2ff-116">*pixel* </span></span>  
<span data-ttu-id="7d2ff-117">Das angegebene Pixel.</span><span class="sxs-lookup"><span data-stu-id="7d2ff-117">The specified pixel.</span></span> <span data-ttu-id="7d2ff-118">Gilt nur beim Debuggen eines Pixelshaders.</span><span class="sxs-lookup"><span data-stu-id="7d2ff-118">Only applies when debugging a pixel shader.</span></span>

<span data-ttu-id="7d2ff-119">*inszeniert* </span><span class="sxs-lookup"><span data-stu-id="7d2ff-119">*stage* </span></span>  
<span data-ttu-id="7d2ff-120">Die angegebene Pipeline Phase.</span><span class="sxs-lookup"><span data-stu-id="7d2ff-120">The specified pipeline stage.</span></span>

<span data-ttu-id="7d2ff-121">*ppixelhistory* </span><span class="sxs-lookup"><span data-stu-id="7d2ff-121">*pPixelHistory* </span></span>  
<span data-ttu-id="7d2ff-122">Die Adresse der Pixel Verlaufs Ergebnisse, die zum Suchen des zugeordneten Pixels zum Debuggen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7d2ff-122">The address of pixel history results used for finding the associated pixel to debug.</span></span> <span data-ttu-id="7d2ff-123">Gilt nur beim Debuggen eines Pixelshaders.</span><span class="sxs-lookup"><span data-stu-id="7d2ff-123">Only applies when debugging a pixel shader.</span></span>

<span data-ttu-id="7d2ff-124">*pdevice* </span><span class="sxs-lookup"><span data-stu-id="7d2ff-124">*pDevice* </span></span>  
<span data-ttu-id="7d2ff-125">Die Adresse, die an die Debug-Engine für die Kommunikation mit dieser Debugsitzung übergeben werden soll (Debugmodul-lesenprozessspeicher für diese Adresse).</span><span class="sxs-lookup"><span data-stu-id="7d2ff-125">The address to pass to the debug engine for communicating with this debug session (debug engine readprocessmemory on this address).</span></span>

## <a name="return-value"></a><span data-ttu-id="7d2ff-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7d2ff-126">Return value</span></span>

<span data-ttu-id="7d2ff-127">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="7d2ff-127">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7d2ff-128">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7d2ff-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d2ff-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d2ff-129">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="7d2ff-130">Header</span><span class="sxs-lookup"><span data-stu-id="7d2ff-130">Header</span></span></p></td><td><span data-ttu-id="7d2ff-131">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="7d2ff-131">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="7d2ff-132"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d2ff-132"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="7d2ff-133">**Idebugshaderrequest**</span><span class="sxs-lookup"><span data-stu-id="7d2ff-133">**IDebugShaderRequest**</span></span>](/windows/desktop/direct3dtools/idebugshaderrequest)

 

 
