---
description: Identifiziert den Abfragetyp.
ms.assetid: 575c4e71-3cab-4123-a2a5-d23b53e87111
title: D3DQUERYTYPE-Enumeration (D3D9Types.h)
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
ms.openlocfilehash: 0778e879a6147c185964808ee4b4c302bd211ef3
ms.sourcegitcommit: bfab92e16614d4fa54b044917358261232bda81a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/08/2021
ms.locfileid: "113489694"
---
# <a name="d3dquerytype-enumeration"></a><span data-ttu-id="13d27-103">D3DQUERYTYPE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="13d27-103">D3DQUERYTYPE enumeration</span></span>

<span data-ttu-id="13d27-104">Identifiziert den Abfragetyp.</span><span class="sxs-lookup"><span data-stu-id="13d27-104">Identifies the query type.</span></span> <span data-ttu-id="13d27-105">Informationen zu Abfragen finden Sie unter [Abfragen (Direct3D 9).](queries.md)</span><span class="sxs-lookup"><span data-stu-id="13d27-105">For information about queries, see [Queries (Direct3D 9)](queries.md)</span></span>

## <a name="syntax"></a><span data-ttu-id="13d27-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="13d27-106">Syntax</span></span>


```C++
typedef enum D3DQUERYTYPE { 
  D3DQUERYTYPE_VCACHE             = 4,
  D3DQUERYTYPE_RESOURCEMANAGER    = 5,
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



## <a name="constants"></a><span data-ttu-id="13d27-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="13d27-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="13d27-108"><span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**D3DQUERYTYPE \_ VCACHE**</span><span class="sxs-lookup"><span data-stu-id="13d27-108"><span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**D3DQUERYTYPE\_VCACHE**</span></span>
</dt> <dd>

<span data-ttu-id="13d27-109">Abfragen von Treiberhinweisen zum Datenlayout für die Scheitelpunktzwischenspeicherung.</span><span class="sxs-lookup"><span data-stu-id="13d27-109">Query for driver hints about data layout for vertex caching.</span></span>

</dd> <dt>

<span data-ttu-id="13d27-110"><span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**D3DQUERYTYPE \_ ResourceManager**</span><span class="sxs-lookup"><span data-stu-id="13d27-110"><span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**D3DQUERYTYPE\_ResourceManager**</span></span>
</dt> <dd>

<span data-ttu-id="13d27-111">Fragen Sie den Ressourcen-Manager ab.</span><span class="sxs-lookup"><span data-stu-id="13d27-111">Query the resource manager.</span></span> <span data-ttu-id="13d27-112">Für diese Abfrage müssen die Geräteverhaltensflags [D3DCREATE \_ DISABLE DRIVER MANAGEMENT \_ \_ enthalten.](d3dcreate.md)</span><span class="sxs-lookup"><span data-stu-id="13d27-112">For this query, the device behavior flags must include [D3DCREATE\_DISABLE\_DRIVER\_MANAGEMENT](d3dcreate.md).</span></span>

</dd> <dt>

<span data-ttu-id="13d27-113"><span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**D3DQUERYTYPE \_ VERTEXSTATS**</span><span class="sxs-lookup"><span data-stu-id="13d27-113"><span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**D3DQUERYTYPE\_VERTEXSTATS**</span></span>
</dt> <dd>

<span data-ttu-id="13d27-114">Abfragen von Scheitelpunktstatistiken.</span><span class="sxs-lookup"><span data-stu-id="13d27-114">Query vertex statistics.</span></span>

</dd> <dt>

<span data-ttu-id="13d27-115"><span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**D3DQUERYTYPE-EREIGNIS \_**</span><span class="sxs-lookup"><span data-stu-id="13d27-115"><span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**D3DQUERYTYPE\_EVENT**</span></span>
</dt> <dd>

<span data-ttu-id="13d27-116">Fragen Sie alle asynchronen Ereignisse ab, die von API-Aufrufen ausgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="13d27-116">Query for any and all asynchronous events that have been issued from API calls.</span></span>

</dd> <dt>

<span data-ttu-id="13d27-117"><span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**D3DQUERYTYPE \_ OCCLUSION**</span><span class="sxs-lookup"><span data-stu-id="13d27-117"><span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**D3DQUERYTYPE\_OCCLUSION**</span></span>
</dt> <dd>

<span data-ttu-id="13d27-118">Eine Okklusionsabfrage gibt die Anzahl der Pixel zurück, die Z-Tests bestehen.</span><span class="sxs-lookup"><span data-stu-id="13d27-118">An occlusion query returns the number of pixels that pass z-testing.</span></span> <span data-ttu-id="13d27-119">Diese Pixel gelten für Primitive, die zwischen dem Problem [**von D3DISSUE \_ BEGIN**](d3dissue-begin.md) und [**D3DISSUE \_ END gezeichnet werden.**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="13d27-119">These pixels are for primitives drawn between the issue of [**D3DISSUE\_BEGIN**](d3dissue-begin.md) and [**D3DISSUE\_END**](d3dissue-end.md).</span></span> <span data-ttu-id="13d27-120">Dadurch kann eine Anwendung das Okklusionsergebnis mit 0 (0) überprüfen.</span><span class="sxs-lookup"><span data-stu-id="13d27-120">This enables an application to check the occlusion result against 0.</span></span> <span data-ttu-id="13d27-121">Null ist vollständig okkludent, was bedeutet, dass die Pixel von der aktuellen Kameraposition aus nicht sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="13d27-121">Zero is fully occluded, which means the pixels are not visible from the current camera position.</span></span>

</dd> <dt>

<span data-ttu-id="13d27-122"><span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**D3DQUERYTYPE \_ TIMESTAMP**</span><span class="sxs-lookup"><span data-stu-id="13d27-122"><span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**D3DQUERYTYPE\_TIMESTAMP**</span></span>
</dt> <dd>

<span data-ttu-id="13d27-123">Gibt einen 64-Bit-Zeitstempel zurück.</span><span class="sxs-lookup"><span data-stu-id="13d27-123">Returns a 64-bit timestamp.</span></span>

</dd> <dt>

<span data-ttu-id="13d27-124"><span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**D3DQUERYTYPE \_ TIMESTAMPDISJOINT**</span><span class="sxs-lookup"><span data-stu-id="13d27-124"><span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**D3DQUERYTYPE\_TIMESTAMPDISJOINT**</span></span>
</dt> <dd>

<span data-ttu-id="13d27-125">Verwenden Sie diese Abfrage, um eine Anwendung zu benachrichtigen, wenn sich die Zählerhäufigkeit von D3DQUERYTYPE \_ TIMESTAMP geändert hat.</span><span class="sxs-lookup"><span data-stu-id="13d27-125">Use this query to notify an application if the counter frequency has changed from the D3DQUERYTYPE\_TIMESTAMP.</span></span>

</dd> <dt>

<span data-ttu-id="13d27-126"><span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**D3DQUERYTYPE \_ TIMESTAMPFREQ**</span><span class="sxs-lookup"><span data-stu-id="13d27-126"><span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**D3DQUERYTYPE\_TIMESTAMPFREQ**</span></span>
</dt> <dd>

<span data-ttu-id="13d27-127">Dieses Abfrageergebnis ist **TRUE,** wenn nicht garantiert werden kann, dass die Werte aus D3DQUERYTYPE TIMESTAMP-Abfragen während der gesamten Dauer der \_ D3DQUERYTYPE \_ TIMESTAMPDISJOINT-Abfrage kontinuierlich sind.</span><span class="sxs-lookup"><span data-stu-id="13d27-127">This query result is **TRUE** if the values from D3DQUERYTYPE\_TIMESTAMP queries cannot be guaranteed to be continuous throughout the duration of the D3DQUERYTYPE\_TIMESTAMPDISJOINT query.</span></span> <span data-ttu-id="13d27-128">Andernfalls ist das Abfrageergebnis **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="13d27-128">Otherwise, the query result is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="13d27-129"><span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**D3DQUERYTYPE \_ PIPELINETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="13d27-129"><span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**D3DQUERYTYPE\_PIPELINETIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="13d27-130">Prozent der Zeit für die Verarbeitung von Pipelinedaten.</span><span class="sxs-lookup"><span data-stu-id="13d27-130">Percent of time processing pipeline data.</span></span>

</dd> <dt>

<span data-ttu-id="13d27-131"><span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**\_D3DQUERYTYPE-SCHNITTSTELLETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="13d27-131"><span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**D3DQUERYTYPE\_INTERFACETIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="13d27-132">Prozent der Zeit für die Verarbeitung von Daten im Treiber.</span><span class="sxs-lookup"><span data-stu-id="13d27-132">Percent of time processing data in the driver.</span></span>

</dd> <dt>

<span data-ttu-id="13d27-133"><span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**D3DQUERYTYPE \_ VERTEXTIMINGS**</span><span class="sxs-lookup"><span data-stu-id="13d27-133"><span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**D3DQUERYTYPE\_VERTEXTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="13d27-134">Prozent der Zeit für die Verarbeitung von Vertex-Shaderdaten.</span><span class="sxs-lookup"><span data-stu-id="13d27-134">Percent of time processing vertex shader data.</span></span>

</dd> <dt>

<span data-ttu-id="13d27-135"><span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**D3DQUERYTYPE \_ PIXELTIMINGS**</span><span class="sxs-lookup"><span data-stu-id="13d27-135"><span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**D3DQUERYTYPE\_PIXELTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="13d27-136">Prozent der Zeit für die Verarbeitung von Pixel-Shaderdaten.</span><span class="sxs-lookup"><span data-stu-id="13d27-136">Percent of time processing pixel shader data.</span></span>

</dd> <dt>

<span data-ttu-id="13d27-137"><span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**D3DQUERYTYPE \_ BANDWIDTHTIMINGS**</span><span class="sxs-lookup"><span data-stu-id="13d27-137"><span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**D3DQUERYTYPE\_BANDWIDTHTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="13d27-138">Vergleiche der Durchsatzmessung, um die Leistung einer Anwendung besser zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="13d27-138">Throughput measurement comparisons for help in understanding the performance of an application.</span></span>

</dd> <dt>

<span data-ttu-id="13d27-139"><span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**D3DQUERYTYPE \_ CACHEUTILIZATION**</span><span class="sxs-lookup"><span data-stu-id="13d27-139"><span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**D3DQUERYTYPE\_CACHEUTILIZATION**</span></span>
</dt> <dd>

<span data-ttu-id="13d27-140">Messen Sie die Leistung der Cachetrefferrate für Texturen und indizierte Scheitelungen.</span><span class="sxs-lookup"><span data-stu-id="13d27-140">Measure the cache hit-rate performance for textures and indexed vertices.</span></span>

</dd> <dt>

<span data-ttu-id="13d27-141"><span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**D3DQUERYTYPE \_ MEMORYPRESSURE**</span><span class="sxs-lookup"><span data-stu-id="13d27-141"><span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**D3DQUERYTYPE\_MEMORYPRESSURE**</span></span>
</dt> <dd>

<span data-ttu-id="13d27-142">Effizienz der Speicherzuweisung in einer [**D3DMEMORYPRESSURE-Struktur.**](d3dmemorypressure.md)</span><span class="sxs-lookup"><span data-stu-id="13d27-142">Efficiency of memory allocation contained in a [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) structure.</span></span>

<span data-ttu-id="13d27-143">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="13d27-143">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

- <span data-ttu-id="13d27-144">D3DQUERYTYPE MEMORYPRESSURE ist nur in Direct3D9Ex verfügbar, das auf \_ Windows 7 (oder mehr aktuellem Betriebssystem) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="13d27-144">D3DQUERYTYPE\_MEMORYPRESSURE is only available in Direct3D9Ex running on Windows 7 (or more current operating system).</span></span>



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="13d27-145">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="13d27-145">Requirements</span></span>



| <span data-ttu-id="13d27-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13d27-146">Requirement</span></span> | <span data-ttu-id="13d27-147">Wert</span><span class="sxs-lookup"><span data-stu-id="13d27-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13d27-148">Header</span><span class="sxs-lookup"><span data-stu-id="13d27-148">Header</span></span><br/> | <dl> <span data-ttu-id="13d27-149"><dt>D3D9Types.h</dt></span><span class="sxs-lookup"><span data-stu-id="13d27-149"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13d27-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13d27-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13d27-151">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="13d27-151">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="13d27-152">**IDirect3DDevice9::CreateQuery**</span><span class="sxs-lookup"><span data-stu-id="13d27-152">**IDirect3DDevice9::CreateQuery**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery)
</dt> </dl>

 

 
