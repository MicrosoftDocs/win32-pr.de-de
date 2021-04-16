---
description: Ein Rückruf, der den Host der Pipeline Stufen Mesh-Informationen benachrichtigt, die von der assocaas-Anforderung zurückgegeben werden.
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataVertCallback\_UINT\_UINT\_MeshDataBufferLayoutEntry\_arr\_UINT\_UINT\_BYTE\_arr\_UINT\_BYTE\_arr\_UINT\_UINT\_UINT\_UINT\_BOOL\_UINT\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ipipelinestagescallback:: meshdatavertcallback-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E75EDE35-AC8E-4452-B79B-860C39B156F0
api_name:
- IPipeLineStagesCallback.MeshDataVertCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3c878851b0c3cfe32128d766f4dcb35a7437579d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521387"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uintspanipipelinestagescallbackmeshdatavertcallback-method"></a><span data-ttu-id="a2559-103"><span id="vspixengine.ipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uint"></span>Ipipelinestagescallback:: meshdatavertcallback-Methode</span><span class="sxs-lookup"><span data-stu-id="a2559-103"><span id="vspixengine.ipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uint"></span>IPipeLineStagesCallback::MeshDataVertCallback method</span></span>

<span data-ttu-id="a2559-104">Ein Rückruf, der den Host der Pipeline Stufen Mesh-Informationen benachrichtigt, die von der assocaas-Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a2559-104">A callback that notifies the host of pipeline stages mesh information returned by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2559-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2559-105">Syntax</span></span>


```C++
HRESULT MeshDataVertCallback(
   UINT                         numVertices,
   UINT                         numBufferLayoutEntries,
   MeshDataBufferLayoutEntry [] count1_entries,
   UINT                         stride,
   UINT                         numVBBytes,
   BYTE []                      count4_pVBData,
   UINT                         numIBBytes,
   BYTE []                      count6_pIBData,
   UINT                         indexSize,
   UINT                         IBOffset,
   UINT                         baseVertex,
   UINT                         minVertex,
   BOOL                         IBIndexesVB,
   UINT                         numIndices,
   UINT                         topology
);
```

## <a name="parameters"></a><span data-ttu-id="a2559-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2559-106">Parameters</span></span>

<span data-ttu-id="a2559-107">*numvertices* </span><span class="sxs-lookup"><span data-stu-id="a2559-107">*numVertices* </span></span>  
<span data-ttu-id="a2559-108">Die Anzahl der Vertices in den Ergebnissen.</span><span class="sxs-lookup"><span data-stu-id="a2559-108">The number of vertices in the results.</span></span>

<span data-ttu-id="a2559-109">*numbufferlayoutentries* </span><span class="sxs-lookup"><span data-stu-id="a2559-109">*numBufferLayoutEntries* </span></span>  
<span data-ttu-id="a2559-110">Die Anzahl der Puffer Layout-Einträge in den Ergebnissen.</span><span class="sxs-lookup"><span data-stu-id="a2559-110">The number of buffer layout entries in the results.</span></span>

<span data-ttu-id="a2559-111">*count1- \_ Einträge* </span><span class="sxs-lookup"><span data-stu-id="a2559-111">*count1\_entries* </span></span>  
<span data-ttu-id="a2559-112">Die Puffer Layout-entierung.</span><span class="sxs-lookup"><span data-stu-id="a2559-112">The buffer layout entires.</span></span> <span data-ttu-id="a2559-113">Diese beschreiben die Shader-Ausgabe Signatur.</span><span class="sxs-lookup"><span data-stu-id="a2559-113">These describe the shader output signature.</span></span>

<span data-ttu-id="a2559-114">*Schritt* </span><span class="sxs-lookup"><span data-stu-id="a2559-114">*stride* </span></span>  
<span data-ttu-id="a2559-115">Die Größe (stride) eines gesamten Ausgabe Segments.</span><span class="sxs-lookup"><span data-stu-id="a2559-115">The size (stride) of an entire output chunk.</span></span>

<span data-ttu-id="a2559-116">*numvbbytes* </span><span class="sxs-lookup"><span data-stu-id="a2559-116">*numVBBytes* </span></span>  
<span data-ttu-id="a2559-117">Die Größe des Scheitelpunkt Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a2559-117">The size of the vertex buffer in bytes.</span></span>

<span data-ttu-id="a2559-118">*count4 \_ pvbdata* </span><span class="sxs-lookup"><span data-stu-id="a2559-118">*count4\_pVBData* </span></span>  
<span data-ttu-id="a2559-119">Der Scheitelpunkt Puffer.</span><span class="sxs-lookup"><span data-stu-id="a2559-119">The vertex buffer.</span></span>

<span data-ttu-id="a2559-120">*numibbytes* </span><span class="sxs-lookup"><span data-stu-id="a2559-120">*numIBBytes* </span></span>  
<span data-ttu-id="a2559-121">Die Größe des Index Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a2559-121">The size of the index buffer in bytes.</span></span>

<span data-ttu-id="a2559-122">*count6 \_ pibdata* </span><span class="sxs-lookup"><span data-stu-id="a2559-122">*count6\_pIBData* </span></span>  
<span data-ttu-id="a2559-123">Der Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="a2559-123">The index buffer.</span></span>

<span data-ttu-id="a2559-124">*indexSize* </span><span class="sxs-lookup"><span data-stu-id="a2559-124">*indexSize* </span></span>  
<span data-ttu-id="a2559-125">Die Größe der einzelnen Indizes in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a2559-125">The size of each index in bytes.</span></span>

<span data-ttu-id="a2559-126">*Iboffset* </span><span class="sxs-lookup"><span data-stu-id="a2559-126">*IBOffset* </span></span>  
<span data-ttu-id="a2559-127">Ein Offset im Index Puffer, der angibt, wo Indizes verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a2559-127">An offset into the index buffer that specifies where indices should start being used.</span></span>

<span data-ttu-id="a2559-128">*basevertex* </span><span class="sxs-lookup"><span data-stu-id="a2559-128">*baseVertex* </span></span>  
<span data-ttu-id="a2559-129">Ein Offset in den Scheitelpunkt Puffer, der angibt, wo Scheitel Punkte verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a2559-129">An offset into the vertex buffer that specifies where vertices should start being used.</span></span>

<span data-ttu-id="a2559-130">*minvertex*</span><span class="sxs-lookup"><span data-stu-id="a2559-130">*minVertex*</span></span>   

<span data-ttu-id="a2559-131">*Ibindexesvb* </span><span class="sxs-lookup"><span data-stu-id="a2559-131">*IBIndexesVB* </span></span>  
<span data-ttu-id="a2559-132">true, wenn der Index Puffer verwendet wird. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="a2559-132">true when the index buffer is used; otherwise false.</span></span>

<span data-ttu-id="a2559-133">*numindizes* </span><span class="sxs-lookup"><span data-stu-id="a2559-133">*numIndices* </span></span>  
<span data-ttu-id="a2559-134">Die Anzahl der verwendeten Indizes.</span><span class="sxs-lookup"><span data-stu-id="a2559-134">The number of indices used.</span></span>

<span data-ttu-id="a2559-135">*Topologie* </span><span class="sxs-lookup"><span data-stu-id="a2559-135">*topology* </span></span>  
<span data-ttu-id="a2559-136">Die topolologie des Shaders.</span><span class="sxs-lookup"><span data-stu-id="a2559-136">The topolology of the shader.</span></span> <span data-ttu-id="a2559-137">Dies ist nicht notwendigerweise identisch mit der Topologie des zugeordneten Draw-Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="a2559-137">This is not necessarily the same as the topology of the associated draw call.</span></span>

## <a name="return-value"></a><span data-ttu-id="a2559-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a2559-138">Return value</span></span>

<span data-ttu-id="a2559-139">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a2559-139">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a2559-140">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a2559-140">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2559-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2559-141">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a2559-142">Header</span><span class="sxs-lookup"><span data-stu-id="a2559-142">Header</span></span></p></td><td><span data-ttu-id="a2559-143">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="a2559-143">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="a2559-144"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2559-144"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="a2559-145">**Ipipelinestagescallback**</span><span class="sxs-lookup"><span data-stu-id="a2559-145">**IPipeLineStagesCallback**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
