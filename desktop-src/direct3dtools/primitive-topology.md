---
description: Eine-Aufzählung, die zur Angabe der Topologie eines Netzes verwendet wird. Weitere Informationen finden Sie unter meshdatavertcallback.
MS-HAID: vspixengine.PRIMITIVE\_TOPOLOGY
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PRIMITIVE_TOPOLOGY-Enumeration
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A845DD10-C735-4EA1-82D3-07F3B26508E7
api_name:
- PRIMITIVE_TOPOLOGY
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7e448fcaaeaa2b1b50bd77b18ac4b3ac3f5e122a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041296"
---
# <a name="span-idvspixengineprimitive_topologyspanprimitive_topology-enumeration"></a><span data-ttu-id="f2874-104"><span id="vspixengine.primitive_topology"></span>PRIMITIVE \_ topologieenumeration</span><span class="sxs-lookup"><span data-stu-id="f2874-104"><span id="vspixengine.primitive_topology"></span>PRIMITIVE\_TOPOLOGY enumeration</span></span>

<span data-ttu-id="f2874-105">Eine-Aufzählung, die zur Angabe der Topologie eines Netzes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f2874-105">An enum used to indicate the topology of a mesh.</span></span> <span data-ttu-id="f2874-106">Weitere Informationen finden Sie unter meshdatavertcallback.</span><span class="sxs-lookup"><span data-stu-id="f2874-106">See MeshDataVertCallback.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2874-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2874-107">Syntax</span></span>


```C++
} PRIMITIVE_TOPOLOGY;
```

## <a name="constants"></a><span data-ttu-id="f2874-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="f2874-108">Constants</span></span>

<span data-ttu-id="f2874-109"><span id="PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="primitive_topology_undefined"></span>**PRIMITIVE \_ Topologie nicht \_ definiert**</span><span class="sxs-lookup"><span data-stu-id="f2874-109"><span id="PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="primitive_topology_undefined"></span>**PRIMITIVE\_TOPOLOGY\_UNDEFINED**</span></span>  
<span data-ttu-id="f2874-110">Die Topologie des Netzes ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="f2874-110">The topology of the mesh is undefined.</span></span>

<span data-ttu-id="f2874-111"><span id="PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="primitive_topology_pointlist"></span>**PRIMITIVE \_ \_ topologiepointlist**</span><span class="sxs-lookup"><span data-stu-id="f2874-111"><span id="PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="primitive_topology_pointlist"></span>**PRIMITIVE\_TOPOLOGY\_POINTLIST**</span></span>  
<span data-ttu-id="f2874-112">Die Topologie des Netzes ist eine Punkt Liste.</span><span class="sxs-lookup"><span data-stu-id="f2874-112">The topology of the mesh is a point list.</span></span>

<span data-ttu-id="f2874-113"><span id="PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="primitive_topology_linelist"></span>**PRIMITIVE \_ Topologie- \_ LineList**</span><span class="sxs-lookup"><span data-stu-id="f2874-113"><span id="PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="primitive_topology_linelist"></span>**PRIMITIVE\_TOPOLOGY\_LINELIST**</span></span>  
<span data-ttu-id="f2874-114">Die Topologie des Netzes ist eine Linien Liste.</span><span class="sxs-lookup"><span data-stu-id="f2874-114">The topology of the mesh is a line list.</span></span>

<span data-ttu-id="f2874-115"><span id="PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="primitive_topology_linestrip"></span>**PRIMITIVE \_ Topologie ( \_ linestrip)**</span><span class="sxs-lookup"><span data-stu-id="f2874-115"><span id="PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="primitive_topology_linestrip"></span>**PRIMITIVE\_TOPOLOGY\_LINESTRIP**</span></span>  
<span data-ttu-id="f2874-116">Die Topologie des Netzes ist ein Linien Streifen.</span><span class="sxs-lookup"><span data-stu-id="f2874-116">The topology of the mesh is a line strip.</span></span>

<span data-ttu-id="f2874-117"><span id="PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="primitive_topology_trianglelist"></span>**PRIMITIVE \_ Topologie ( \_ drei)**</span><span class="sxs-lookup"><span data-stu-id="f2874-117"><span id="PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="primitive_topology_trianglelist"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLELIST**</span></span>  
<span data-ttu-id="f2874-118">Die Topologie des Netzes ist eine Dreiecks Liste.</span><span class="sxs-lookup"><span data-stu-id="f2874-118">The topology of the mesh is a triangle list.</span></span>

<span data-ttu-id="f2874-119"><span id="PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="primitive_topology_trianglestrip"></span>**primitiver \_ \_ topologiestrip**</span><span class="sxs-lookup"><span data-stu-id="f2874-119"><span id="PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="primitive_topology_trianglestrip"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLESTRIP**</span></span>  
<span data-ttu-id="f2874-120">Die Topologie des Netzes ist ein Dreiecks Streifen.</span><span class="sxs-lookup"><span data-stu-id="f2874-120">The topology of the mesh is a triangle strip.</span></span>

<span data-ttu-id="f2874-121"><span id="PRIMITIVE_TOPOLOGY_TRIANGLEFAN"></span><span id="primitive_topology_trianglefan"></span>**primitiver \_ \_ topologielüfter**</span><span class="sxs-lookup"><span data-stu-id="f2874-121"><span id="PRIMITIVE_TOPOLOGY_TRIANGLEFAN"></span><span id="primitive_topology_trianglefan"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLEFAN**</span></span>  
<span data-ttu-id="f2874-122">Die Topologie des Netzes ist ein Dreiecks Lüfter.</span><span class="sxs-lookup"><span data-stu-id="f2874-122">The topology of the mesh is a triangle fan.</span></span>

<span data-ttu-id="f2874-123"><span id="PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="primitive_topology_linelist_adj"></span>**PRIMITIVE \_ Topologie- \_ LineList \_ ADJ**</span><span class="sxs-lookup"><span data-stu-id="f2874-123"><span id="PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="primitive_topology_linelist_adj"></span>**PRIMITIVE\_TOPOLOGY\_LINELIST\_ADJ**</span></span>  
<span data-ttu-id="f2874-124">Die Topologie des Netzes ist eine Zeilen Liste mit der Nähe.</span><span class="sxs-lookup"><span data-stu-id="f2874-124">The topology of the mesh is a line list with adjacency.</span></span>

<span data-ttu-id="f2874-125"><span id="PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="primitive_topology_linestrip_adj"></span>**PRIMITIVE \_ Topologie, \_ linestrip, \_ ADJ**</span><span class="sxs-lookup"><span data-stu-id="f2874-125"><span id="PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="primitive_topology_linestrip_adj"></span>**PRIMITIVE\_TOPOLOGY\_LINESTRIP\_ADJ**</span></span>  
<span data-ttu-id="f2874-126">Die Topologie des Netzes ist ein Zeilen Streifen mit der Nähe.</span><span class="sxs-lookup"><span data-stu-id="f2874-126">The topology of the mesh is a line strip with adjacency.</span></span>

<span data-ttu-id="f2874-127"><span id="PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="primitive_topology_trianglelist_adj"></span>**PRIMITIVE \_ Topologie, " \_ tanglelist", \_ ADJ**</span><span class="sxs-lookup"><span data-stu-id="f2874-127"><span id="PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="primitive_topology_trianglelist_adj"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLELIST\_ADJ**</span></span>  
<span data-ttu-id="f2874-128">Die Topologie des Netzes ist eine Dreiecks Liste mit der Nähe.</span><span class="sxs-lookup"><span data-stu-id="f2874-128">The topology of the mesh is a triangle list with adjacency.</span></span>

<span data-ttu-id="f2874-129"><span id="PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="primitive_topology_trianglestrip_adj"></span>**PRIMITIVE \_ Topologie, \_ \_ ADJ**</span><span class="sxs-lookup"><span data-stu-id="f2874-129"><span id="PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="primitive_topology_trianglestrip_adj"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLESTRIP\_ADJ**</span></span>  
<span data-ttu-id="f2874-130">Die Topologie des Netzes ist ein Dreiecks Streifen mit der Nähe.</span><span class="sxs-lookup"><span data-stu-id="f2874-130">The topology of the mesh is a triangle strip with adjacency.</span></span>

<span data-ttu-id="f2874-131"><span id="PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_1_control_point_patchlist"></span>**PRIMITIVE \_ Topologie \_ 1 \_ , \_ Patchliste für Kontrollpunkt \_**</span><span class="sxs-lookup"><span data-stu-id="f2874-131"><span id="PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_1_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_1\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-132">Die Topologie des Netzes ist eine Patchliste mit einem Steuerungspunkt.</span><span class="sxs-lookup"><span data-stu-id="f2874-132">The topology of the mesh is a patch list with 1 control point.</span></span>

<span data-ttu-id="f2874-133"><span id="PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_2_control_point_patchlist"></span>**PRIMITIVE \_ Topologie \_ 2 \_ - \_ Patchliste für Kontrollpunkte \_**</span><span class="sxs-lookup"><span data-stu-id="f2874-133"><span id="PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_2_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_2\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-134">Die Topologie des Netzes ist eine Patchliste mit 2 Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-134">The topology of the mesh is a patch list with 2 control points.</span></span>

<span data-ttu-id="f2874-135"><span id="PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_3_control_point_patchlist"></span>**PRIMITIVE \_ Topologie \_ 3 \_ - \_ Patchliste für Steuerungspunkt \_**</span><span class="sxs-lookup"><span data-stu-id="f2874-135"><span id="PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_3_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_3\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-136">Die Topologie des Netzes ist eine Patchliste mit drei Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-136">The topology of the mesh is a patch list with 3 control points.</span></span>

<span data-ttu-id="f2874-137"><span id="PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_4_control_point_patchlist"></span>**\_ \_ \_ Kontroll \_ Punkt- \_ Patchliste für primitive Topologie 4**</span><span class="sxs-lookup"><span data-stu-id="f2874-137"><span id="PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_4_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_4\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-138">Die Topologie des Netzes ist eine Patchliste mit vier Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-138">The topology of the mesh is a patch list with 4 control points.</span></span>

<span data-ttu-id="f2874-139"><span id="PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_5_control_point_patchlist"></span>**PRIMITIVE \_ Topologie \_ 5 \_ , \_ Patchliste für Steuerungspunkt \_**</span><span class="sxs-lookup"><span data-stu-id="f2874-139"><span id="PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_5_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_5\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-140">Die Topologie des Netzes ist eine Patchliste mit fünf Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-140">The topology of the mesh is a patch list with 5 control points.</span></span>

<span data-ttu-id="f2874-141"><span id="PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_6_control_point_patchlist"></span>**Liste der primitiven \_ Topologie \_ 6- \_ Steuerungs \_ Punkte \_**</span><span class="sxs-lookup"><span data-stu-id="f2874-141"><span id="PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_6_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_6\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-142">Die Topologie des Netzes ist eine Patchliste mit 6 Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-142">The topology of the mesh is a patch list with 6 control points.</span></span>

<span data-ttu-id="f2874-143"><span id="PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_7_control_point_patchlist"></span>**Verwaltungs \_ Punkt- \_ \_ \_ \_ Patchliste für primitive Topologie 7**</span><span class="sxs-lookup"><span data-stu-id="f2874-143"><span id="PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_7_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_7\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-144">Die Topologie des Netzes ist eine Patchliste mit 7 Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-144">The topology of the mesh is a patch list with 7 control points.</span></span>

<span data-ttu-id="f2874-145"><span id="PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_8_control_point_patchlist"></span>**Grund \_ Wert- \_ \_ \_ \_ Patchliste für die primitive Topologie 8**</span><span class="sxs-lookup"><span data-stu-id="f2874-145"><span id="PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_8_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_8\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-146">Die Topologie des Netzes ist eine Patchliste mit acht Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-146">The topology of the mesh is a patch list with 8 control points.</span></span>

<span data-ttu-id="f2874-147"><span id="PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_9_control_point_patchlist"></span>**\_ \_ \_ Kontroll \_ Punkt- \_ Patchliste für primitive Topologie 9**</span><span class="sxs-lookup"><span data-stu-id="f2874-147"><span id="PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_9_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_9\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-148">Die Topologie des Netzes ist eine Patchliste mit 9 Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-148">The topology of the mesh is a patch list with 9 control points.</span></span>

<span data-ttu-id="f2874-149"><span id="PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_10_control_point_patchlist"></span>**\_ \_ \_ Kontroll \_ Punkt- \_ Patchliste für primitive Topologie 10**</span><span class="sxs-lookup"><span data-stu-id="f2874-149"><span id="PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_10_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_10\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-150">Die Topologie des Netzes ist eine Patchliste mit 10 Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-150">The topology of the mesh is a patch list with 10 control points.</span></span>

<span data-ttu-id="f2874-151"><span id="PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_11_control_point_patchlist"></span>**\_ \_ \_ Kontroll \_ Punkt- \_ Patchliste für primitive Topologie 11**</span><span class="sxs-lookup"><span data-stu-id="f2874-151"><span id="PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_11_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_11\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-152">Die Topologie des Netzes ist eine Patchliste mit 11 Kontrollpunkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-152">The topology of the mesh is a patch list with 11 control points.</span></span>

<span data-ttu-id="f2874-153"><span id="PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_12_control_point_patchlist"></span>**\_ \_ \_ Kontroll \_ Punkt- \_ Patchliste für primitive Topologie 12**</span><span class="sxs-lookup"><span data-stu-id="f2874-153"><span id="PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_12_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_12\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-154">Die Topologie des Netzes ist eine Patchliste mit 12 Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-154">The topology of the mesh is a patch list with 12 control points.</span></span>

<span data-ttu-id="f2874-155"><span id="PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_13_control_point_patchlist"></span>**PRIMITIVE \_ Topologie \_ 13 \_ , \_ Patchliste für Steuerungspunkt \_**</span><span class="sxs-lookup"><span data-stu-id="f2874-155"><span id="PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_13_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_13\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-156">Die Topologie des Netzes ist eine Patchliste mit 13 Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-156">The topology of the mesh is a patch list with 13 control points.</span></span>

<span data-ttu-id="f2874-157"><span id="PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_14_control_point_patchlist"></span>**PRIMITIVE \_ Topologie \_ 14- \_ Steuerungs \_ Punkt- \_ Patchliste**</span><span class="sxs-lookup"><span data-stu-id="f2874-157"><span id="PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_14_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_14\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-158">Die Topologie des Netzes ist eine Patchliste mit 14 Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-158">The topology of the mesh is a patch list with 14 control points.</span></span>

<span data-ttu-id="f2874-159"><span id="PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_15_control_point_patchlist"></span>**PRIMITIVE \_ Topologie \_ 15- \_ Steuerungs \_ Punkt- \_ Patchliste**</span><span class="sxs-lookup"><span data-stu-id="f2874-159"><span id="PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_15_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_15\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-160">Die Topologie des Netzes ist eine Patchliste mit 15 Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-160">The topology of the mesh is a patch list with 15 control points.</span></span>

<span data-ttu-id="f2874-161"><span id="PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_16_control_point_patchlist"></span>**PRIMITIVE \_ Topologie \_ 16 \_ , \_ Patchliste für Kontrollpunkte \_**</span><span class="sxs-lookup"><span data-stu-id="f2874-161"><span id="PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_16_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_16\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-162">Die Topologie des Netzes ist eine Patchliste mit 16 Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-162">The topology of the mesh is a patch list with 16 control points.</span></span>

<span data-ttu-id="f2874-163"><span id="PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_17_control_point_patchlist"></span>**PRIMITIVE \_ Topologie \_ 17 \_ - \_ Patchliste für Steuerungspunkt \_**</span><span class="sxs-lookup"><span data-stu-id="f2874-163"><span id="PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_17_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_17\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-164">Die Topologie des Netzes ist eine Patchliste mit 17 Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-164">The topology of the mesh is a patch list with 17 control points.</span></span>

<span data-ttu-id="f2874-165"><span id="PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_18_control_point_patchlist"></span>**PRIMITIVE \_ Topologie \_ 18 ( \_ Steuerungs \_ Punkt- \_ Patchliste)**</span><span class="sxs-lookup"><span data-stu-id="f2874-165"><span id="PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_18_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_18\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-166">Die Topologie des Netzes ist eine Patchliste mit 18 Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-166">The topology of the mesh is a patch list with 18 control points.</span></span>

<span data-ttu-id="f2874-167"><span id="PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_19_control_point_patchlist"></span>**PRIMITIVE \_ Topologie \_ 19- \_ Steuerungs \_ Punkt- \_ Patchliste**</span><span class="sxs-lookup"><span data-stu-id="f2874-167"><span id="PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_19_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_19\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-168">Die Topologie des Netzes ist eine Patchliste mit 19 Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-168">The topology of the mesh is a patch list with 19 control points.</span></span>

<span data-ttu-id="f2874-169"><span id="PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_20_control_point_patchlist"></span>**PRIMITIVE \_ Topologie \_ 20 \_ Patchliste für Kontroll \_ Punkte \_**</span><span class="sxs-lookup"><span data-stu-id="f2874-169"><span id="PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_20_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_20\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-170">Die Topologie des Netzes ist eine Patchliste mit 20 Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-170">The topology of the mesh is a patch list with 20 control points.</span></span>

<span data-ttu-id="f2874-171"><span id="PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_21_control_point_patchlist"></span>**\_ \_ \_ Kontroll \_ Punkt- \_ Patchliste für primitive Topologie 21**</span><span class="sxs-lookup"><span data-stu-id="f2874-171"><span id="PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_21_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_21\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-172">Die Topologie des Netzes ist eine Patchliste mit 21 Kontrollpunkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-172">The topology of the mesh is a patch list with 21 control points.</span></span>

<span data-ttu-id="f2874-173"><span id="PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_22_control_point_patchlist"></span>**PRIMITIVE \_ Topologie \_ 22 \_ - \_ Patchliste für Kontrollpunkte \_**</span><span class="sxs-lookup"><span data-stu-id="f2874-173"><span id="PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_22_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_22\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-174">Die Topologie des Netzes ist eine Patchliste mit 22 Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-174">The topology of the mesh is a patch list with 22 control points.</span></span>

<span data-ttu-id="f2874-175"><span id="PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_23_control_point_patchlist"></span>**PRIMITIVE \_ Topologie \_ 23 \_ , \_ Patchliste für Steuerungspunkt \_**</span><span class="sxs-lookup"><span data-stu-id="f2874-175"><span id="PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_23_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_23\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-176">Die Topologie des Netzes ist eine Patchliste mit 23 Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-176">The topology of the mesh is a patch list with 23 control points.</span></span>

<span data-ttu-id="f2874-177"><span id="PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_24_control_point_patchlist"></span>**PRIMITIVE \_ Topologie \_ 24- \_ Steuerungs \_ Punkt- \_ Patchliste**</span><span class="sxs-lookup"><span data-stu-id="f2874-177"><span id="PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_24_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_24\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-178">Die Topologie des Netzes ist eine Patchliste mit 24 Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-178">The topology of the mesh is a patch list with 24 control points.</span></span>

<span data-ttu-id="f2874-179"><span id="PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_25_control_point_patchlist"></span>**PRIMITIVE \_ Topologie \_ 25 \_ Steuerungs \_ Punkt- \_ Patchliste**</span><span class="sxs-lookup"><span data-stu-id="f2874-179"><span id="PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_25_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_25\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-180">Die Topologie des Netzes ist eine Patchliste mit 25 Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-180">The topology of the mesh is a patch list with 25 control points.</span></span>

<span data-ttu-id="f2874-181"><span id="PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_26_control_point_patchlist"></span>**PRIMITIVE \_ Topologie \_ 26- \_ Steuerungs \_ Punkt- \_ Patchliste**</span><span class="sxs-lookup"><span data-stu-id="f2874-181"><span id="PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_26_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_26\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-182">Die Topologie des Netzes ist eine Patchliste mit 26 Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-182">The topology of the mesh is a patch list with 26 control points.</span></span>

<span data-ttu-id="f2874-183"><span id="PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_27_control_point_patchlist"></span>**PRIMITIVE \_ Topologie \_ 27- \_ Steuerungs \_ Punkt- \_ Patchliste**</span><span class="sxs-lookup"><span data-stu-id="f2874-183"><span id="PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_27_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_27\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-184">Die Topologie des Netzes ist eine Patchliste mit 27 Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-184">The topology of the mesh is a patch list with 27 control points.</span></span>

<span data-ttu-id="f2874-185"><span id="PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_28_control_point_patchlist"></span>**PRIMITIVE \_ Topologie \_ 28 \_ , \_ Patchliste für Steuerungspunkt \_**</span><span class="sxs-lookup"><span data-stu-id="f2874-185"><span id="PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_28_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_28\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-186">Die Topologie des Netzes ist eine Patchliste mit 28 Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-186">The topology of the mesh is a patch list with 28 control points.</span></span>

<span data-ttu-id="f2874-187"><span id="PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_29_control_point_patchlist"></span>**PRIMITIVE \_ Topologie \_ 29- \_ Steuerungs \_ Punkt- \_ Patchliste**</span><span class="sxs-lookup"><span data-stu-id="f2874-187"><span id="PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_29_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_29\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-188">Die Topologie des Netzes ist eine Patchliste mit 29 Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-188">The topology of the mesh is a patch list with 29 control points.</span></span>

<span data-ttu-id="f2874-189"><span id="PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_30_control_point_patchlist"></span>**PRIMITIVE \_ Topologie \_ 30- \_ Steuerungs \_ Punkt- \_ Patchliste**</span><span class="sxs-lookup"><span data-stu-id="f2874-189"><span id="PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_30_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_30\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-190">Die Topologie des Netzes ist eine Patchliste mit 30 Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-190">The topology of the mesh is a patch list with 30 control points.</span></span>

<span data-ttu-id="f2874-191"><span id="PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_31_control_point_patchlist"></span>**\_ \_ \_ Kontroll \_ Punkt- \_ Patchliste der primitiven Topologie 31**</span><span class="sxs-lookup"><span data-stu-id="f2874-191"><span id="PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_31_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_31\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-192">Die Topologie des Netzes ist eine Patchliste mit 31 Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-192">The topology of the mesh is a patch list with 31 control points.</span></span>

<span data-ttu-id="f2874-193"><span id="PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_32_control_point_patchlist"></span>**PRIMITIVE \_ Topologie \_ 32 \_ - \_ Patchliste für Steuerungspunkt \_**</span><span class="sxs-lookup"><span data-stu-id="f2874-193"><span id="PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_32_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_32\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="f2874-194">Die Topologie des Netzes ist eine Patchliste mit 32-Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="f2874-194">The topology of the mesh is a patch list with 32 control points.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2874-195">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2874-195">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f2874-196">Header</span><span class="sxs-lookup"><span data-stu-id="f2874-196">Header</span></span></p></td><td><span data-ttu-id="f2874-197">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f2874-197">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



