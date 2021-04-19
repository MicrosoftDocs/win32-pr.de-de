---
description: Identifiziert den Abfragetyp.
ms.assetid: 575c4e71-3cab-4123-a2a5-d23b53e87111
title: D3DQUERYTYPE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DQUERYTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 21cb3e2f2254d54caacd4217d3e0023446a0c6f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355021"
---
# <a name="d3dquerytype-enumeration"></a><span data-ttu-id="56389-103">D3DQUERYTYPE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="56389-103">D3DQUERYTYPE enumeration</span></span>

<span data-ttu-id="56389-104">Identifiziert den Abfragetyp.</span><span class="sxs-lookup"><span data-stu-id="56389-104">Identifies the query type.</span></span> <span data-ttu-id="56389-105">Weitere Informationen zu Abfragen finden Sie unter [Abfragen (Direct3D 9)](queries.md) .</span><span class="sxs-lookup"><span data-stu-id="56389-105">For information about queries, see [Queries (Direct3D 9)](queries.md)</span></span>

## <a name="syntax"></a><span data-ttu-id="56389-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="56389-106">Syntax</span></span>


```C++
typedef enum D3DQUERYTYPE { 
  D3DQUERYTYPE_VCACHE             = 4,
  D3DQUERYTYPE_ResourceManager    = 5,
  D3DQUERYTYPE_VERTEXSTATS        = 6,
  D3DQUERYTYPE_EVENT              = 8,
  D3DQUERYTYPE_OCCLUSION          = 9,
  D3DQUERYTYPE_TIMESTAMP          = 10,
  D3DQUERYTYPE_TIMESTAMPDISJOINT  = 11,
  D3DQUERYTYPE_TIMESTAMPFREQ      = 12,
  D3DQUERYTYPE_PIPELINETIMINGS    = 13,
  D3DQUERYTYPE_INTERFACETIMINGS   = 14,
  D3DQUERYTYPE_VERTEXTIMINGS      = 15,
  D3DQUERYTYPE_PIXELTIMINGS       = 16,
  D3DQUERYTYPE_BANDWIDTHTIMINGS   = 17,
  D3DQUERYTYPE_CACHEUTILIZATION   = 18,
  D3DQUERYTYPE_MEMORYPRESSURE     = 19
} D3DQUERYTYPE, *LPD3DQUERYTYPE;
```



## <a name="constants"></a><span data-ttu-id="56389-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="56389-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="56389-108"><span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**D3DQUERYTYPE \_ VCACHE**</span><span class="sxs-lookup"><span data-stu-id="56389-108"><span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**D3DQUERYTYPE\_VCACHE**</span></span>
</dt> <dd>

<span data-ttu-id="56389-109">Fragen Sie Treiber Hinweise zum Datenlayout für Scheitelpunkt Caching ab.</span><span class="sxs-lookup"><span data-stu-id="56389-109">Query for driver hints about data layout for vertex caching.</span></span>

</dd> <dt>

<span data-ttu-id="56389-110"><span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**D3DQUERYTYPE \_ ResourceManager**</span><span class="sxs-lookup"><span data-stu-id="56389-110"><span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**D3DQUERYTYPE\_ResourceManager**</span></span>
</dt> <dd>

<span data-ttu-id="56389-111">Fragen Sie den Ressourcen-Manager ab.</span><span class="sxs-lookup"><span data-stu-id="56389-111">Query the resource manager.</span></span> <span data-ttu-id="56389-112">Für diese Abfrage müssen die geräteverhaltenflags [D3DCREATE \_ deaktivierte \_ Treiber \_ Verwaltung](d3dcreate.md)einschließen.</span><span class="sxs-lookup"><span data-stu-id="56389-112">For this query, the device behavior flags must include [D3DCREATE\_DISABLE\_DRIVER\_MANAGEMENT](d3dcreate.md).</span></span>

</dd> <dt>

<span data-ttu-id="56389-113"><span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**D3DQUERYTYPE \_ vertexstats**</span><span class="sxs-lookup"><span data-stu-id="56389-113"><span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**D3DQUERYTYPE\_VERTEXSTATS**</span></span>
</dt> <dd>

<span data-ttu-id="56389-114">Abfragen von Vertex-Statistiken.</span><span class="sxs-lookup"><span data-stu-id="56389-114">Query vertex statistics.</span></span>

</dd> <dt>

<span data-ttu-id="56389-115"><span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**D3DQUERYTYPE- \_ Ereignis**</span><span class="sxs-lookup"><span data-stu-id="56389-115"><span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**D3DQUERYTYPE\_EVENT**</span></span>
</dt> <dd>

<span data-ttu-id="56389-116">Fragen Sie alle asynchronen Ereignisse ab, die von API-aufrufen ausgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="56389-116">Query for any and all asynchronous events that have been issued from API calls.</span></span>

</dd> <dt>

<span data-ttu-id="56389-117"><span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**D3DQUERYTYPE- \_ oksion**</span><span class="sxs-lookup"><span data-stu-id="56389-117"><span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**D3DQUERYTYPE\_OCCLUSION**</span></span>
</dt> <dd>

<span data-ttu-id="56389-118">Eine oksions Abfrage gibt die Anzahl der Pixel zurück, die z-Tests bestehen.</span><span class="sxs-lookup"><span data-stu-id="56389-118">An occlusion query returns the number of pixels that pass z-testing.</span></span> <span data-ttu-id="56389-119">Diese Pixel sind für primitive, die zwischen dem Problem [**D3DISSUE \_ Begin**](d3dissue-begin.md) und [**D3DISSUE \_ End**](d3dissue-end.md)gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="56389-119">These pixels are for primitives drawn between the issue of [**D3DISSUE\_BEGIN**](d3dissue-begin.md) and [**D3DISSUE\_END**](d3dissue-end.md).</span></span> <span data-ttu-id="56389-120">Dadurch kann eine Anwendung das Okklusions Ergebnis auf 0 überprüfen.</span><span class="sxs-lookup"><span data-stu-id="56389-120">This enables an application to check the occlusion result against 0.</span></span> <span data-ttu-id="56389-121">NULL ist vollständig verdeckt, d. h., die Pixel sind von der aktuellen Kameraposition aus nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="56389-121">Zero is fully occluded, which means the pixels are not visible from the current camera position.</span></span>

</dd> <dt>

<span data-ttu-id="56389-122"><span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**D3DQUERYTYPE- \_ Zeitstempel**</span><span class="sxs-lookup"><span data-stu-id="56389-122"><span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**D3DQUERYTYPE\_TIMESTAMP**</span></span>
</dt> <dd>

<span data-ttu-id="56389-123">Gibt einen 64-Bit-Zeitstempel zurück.</span><span class="sxs-lookup"><span data-stu-id="56389-123">Returns a 64-bit timestamp.</span></span>

</dd> <dt>

<span data-ttu-id="56389-124"><span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**D3DQUERYTYPE \_ timestampdisjoint**</span><span class="sxs-lookup"><span data-stu-id="56389-124"><span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**D3DQUERYTYPE\_TIMESTAMPDISJOINT**</span></span>
</dt> <dd>

<span data-ttu-id="56389-125">Verwenden Sie diese Abfrage, um eine Anwendung zu benachrichtigen, wenn sich die Häufigkeit des Zählers für den D3DQUERYTYPE- \_ Zeitstempel geändert hat.</span><span class="sxs-lookup"><span data-stu-id="56389-125">Use this query to notify an application if the counter frequency has changed from the D3DQUERYTYPE\_TIMESTAMP.</span></span>

</dd> <dt>

<span data-ttu-id="56389-126"><span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**D3DQUERYTYPE \_ timestampfreq**</span><span class="sxs-lookup"><span data-stu-id="56389-126"><span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**D3DQUERYTYPE\_TIMESTAMPFREQ**</span></span>
</dt> <dd>

<span data-ttu-id="56389-127">Dieses Abfrageergebnis ist **true** , wenn die Werte von D3DQUERYTYPE \_ timestamp-Abfragen während der gesamten Dauer der D3DQUERYTYPE \_ timestampdisjoint-Abfrage nicht garantiert werden können.</span><span class="sxs-lookup"><span data-stu-id="56389-127">This query result is **TRUE** if the values from D3DQUERYTYPE\_TIMESTAMP queries cannot be guaranteed to be continuous throughout the duration of the D3DQUERYTYPE\_TIMESTAMPDISJOINT query.</span></span> <span data-ttu-id="56389-128">Andernfalls ist das Abfrageergebnis **false**.</span><span class="sxs-lookup"><span data-stu-id="56389-128">Otherwise, the query result is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="56389-129"><span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**D3DQUERYTYPE \_ pipelinetimings**</span><span class="sxs-lookup"><span data-stu-id="56389-129"><span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**D3DQUERYTYPE\_PIPELINETIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="56389-130">Prozentsatz der Zeit für die Verarbeitung von Pipeline Daten.</span><span class="sxs-lookup"><span data-stu-id="56389-130">Percent of time processing pipeline data.</span></span>

</dd> <dt>

<span data-ttu-id="56389-131"><span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**D3DQUERYTYPE \_ interfacetimings**</span><span class="sxs-lookup"><span data-stu-id="56389-131"><span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**D3DQUERYTYPE\_INTERFACETIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="56389-132">Der Prozentsatz der Zeit, die Daten im Treiber verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="56389-132">Percent of time processing data in the driver.</span></span>

</dd> <dt>

<span data-ttu-id="56389-133"><span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**D3DQUERYTYPE \_ vertextimings**</span><span class="sxs-lookup"><span data-stu-id="56389-133"><span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**D3DQUERYTYPE\_VERTEXTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="56389-134">Der Prozentsatz der Zeit, die Vertex-shaderdaten verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="56389-134">Percent of time processing vertex shader data.</span></span>

</dd> <dt>

<span data-ttu-id="56389-135"><span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**D3DQUERYTYPE \_ pixeltimings**</span><span class="sxs-lookup"><span data-stu-id="56389-135"><span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**D3DQUERYTYPE\_PIXELTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="56389-136">Der Prozentsatz der Zeit, die Pixel-shaderdaten verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="56389-136">Percent of time processing pixel shader data.</span></span>

</dd> <dt>

<span data-ttu-id="56389-137"><span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**D3DQUERYTYPE \_ bandwidthtimings**</span><span class="sxs-lookup"><span data-stu-id="56389-137"><span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**D3DQUERYTYPE\_BANDWIDTHTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="56389-138">Vergleichsmessungen für den Durchsatz, um die Leistung einer Anwendung besser zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="56389-138">Throughput measurement comparisons for help in understanding the performance of an application.</span></span>

</dd> <dt>

<span data-ttu-id="56389-139"><span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**D3DQUERYTYPE \_ cacheutilization**</span><span class="sxs-lookup"><span data-stu-id="56389-139"><span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**D3DQUERYTYPE\_CACHEUTILIZATION**</span></span>
</dt> <dd>

<span data-ttu-id="56389-140">Messen Sie die Leistung der Cache-Treffer Rate für Texturen und indizierte Vertices.</span><span class="sxs-lookup"><span data-stu-id="56389-140">Measure the cache hit-rate performance for textures and indexed vertices.</span></span>

</dd> <dt>

<span data-ttu-id="56389-141"><span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**D3DQUERYTYPE \_ memorypressure**</span><span class="sxs-lookup"><span data-stu-id="56389-141"><span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**D3DQUERYTYPE\_MEMORYPRESSURE**</span></span>
</dt> <dd>

<span data-ttu-id="56389-142">Effizienz der Arbeitsspeicher Belegung, die in einer [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) -Struktur enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="56389-142">Efficiency of memory allocation contained in a [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) structure.</span></span>



|                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56389-143">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="56389-143">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="56389-144">D3DQUERYTYPE \_ memorypressure ist nur in Direct3D9Ex verfügbar, die unter Windows 7 (oder einem höheren aktuellen Betriebssystem) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="56389-144">D3DQUERYTYPE\_MEMORYPRESSURE is only available in Direct3D9Ex running on Windows 7 (or more current operating system).</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="56389-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56389-145">Requirements</span></span>



| <span data-ttu-id="56389-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56389-146">Requirement</span></span> | <span data-ttu-id="56389-147">Wert</span><span class="sxs-lookup"><span data-stu-id="56389-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56389-148">Header</span><span class="sxs-lookup"><span data-stu-id="56389-148">Header</span></span><br/> | <dl> <span data-ttu-id="56389-149"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="56389-149"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56389-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56389-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56389-151">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="56389-151">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="56389-152">**IDirect3DDevice9:: kreatequery**</span><span class="sxs-lookup"><span data-stu-id="56389-152">**IDirect3DDevice9::CreateQuery**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery)
</dt> </dl>

 

 
