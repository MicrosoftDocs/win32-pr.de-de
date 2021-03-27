---
description: Gibt an, wie die Pipeline Vertex-Daten interpretiert, die an die Eingabe-Assembler-Phase gebunden sind. Diese primitiven topologiewerte bestimmen, wie die Scheitelpunkt Daten auf dem Bildschirm gerendert werden.
ms.assetid: ca0547b2-d0f8-4edc-a62c-3c903e1b33ea
title: D3D11 \_ primitive \_ topologieenumeration
ms.date: 06/26/2019
ms.topic: reference
ms.openlocfilehash: 1d2beab107a3f3abe03e5a17f068e1b508422241
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104995270"
---
# <a name="d3d11_primitive_topology-enumeration"></a><span data-ttu-id="09a14-104">D3D11 \_ primitive \_ topologieenumeration</span><span class="sxs-lookup"><span data-stu-id="09a14-104">D3D11\_PRIMITIVE\_TOPOLOGY enumeration</span></span>

<span data-ttu-id="09a14-105">Gibt an, wie die Pipeline Vertex-Daten interpretiert, die an die Eingabe-Assembler-Phase gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="09a14-105">How the pipeline interprets vertex data that is bound to the input-assembler stage.</span></span> <span data-ttu-id="09a14-106">Diese primitiven topologiewerte bestimmen, wie die Scheitelpunkt Daten auf dem Bildschirm gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="09a14-106">These primitive topology values determine how the vertex data is rendered on screen.</span></span>

## <a name="syntax"></a><span data-ttu-id="09a14-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="09a14-107">Syntax</span></span>


```C++
} D3D11_PRIMITIVE_TOPOLOGY;
```



## <a name="constants"></a><span data-ttu-id="09a14-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="09a14-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="09a14-109"><span id="D3D11_PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="d3d11_primitive_topology_undefined"></span>**D3D11 \_ primitive \_ Topologie nicht \_ definiert**</span><span class="sxs-lookup"><span data-stu-id="09a14-109"><span id="D3D11_PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="d3d11_primitive_topology_undefined"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-110">Die IA-Phase wurde nicht mit einer primitiven Topologie initialisiert.</span><span class="sxs-lookup"><span data-stu-id="09a14-110">The IA stage has not been initialized with a primitive topology.</span></span> <span data-ttu-id="09a14-111">Die IA-Phase funktioniert nur dann ordnungsgemäß, wenn eine primitive Topologie definiert ist.</span><span class="sxs-lookup"><span data-stu-id="09a14-111">The IA stage will not function properly unless a primitive topology is defined.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-112"><span id="D3D11_PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="d3d11_primitive_topology_pointlist"></span>**D3D11 \_ primitive \_ Topologie- \_ PointList**</span><span class="sxs-lookup"><span data-stu-id="09a14-112"><span id="D3D11_PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="d3d11_primitive_topology_pointlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_POINTLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-113">Interpretiert die Scheitelpunkt Daten als eine Liste von Punkten.</span><span class="sxs-lookup"><span data-stu-id="09a14-113">Interpret the vertex data as a list of points.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-114"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="d3d11_primitive_topology_linelist"></span>**D3D11 \_ primitive \_ Topologie- \_ LineList**</span><span class="sxs-lookup"><span data-stu-id="09a14-114"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="d3d11_primitive_topology_linelist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_LINELIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-115">Interpretiert die Scheitelpunkt Daten als eine Liste von Zeilen.</span><span class="sxs-lookup"><span data-stu-id="09a14-115">Interpret the vertex data as a list of lines.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-116"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="d3d11_primitive_topology_linestrip"></span>**D3D11 \_ primitive \_ Topologie ( \_ linestrip)**</span><span class="sxs-lookup"><span data-stu-id="09a14-116"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="d3d11_primitive_topology_linestrip"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_LINESTRIP**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-117">Interpretiert die Scheitelpunkt Daten als Zeilen Streifen.</span><span class="sxs-lookup"><span data-stu-id="09a14-117">Interpret the vertex data as a line strip.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-118"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="d3d11_primitive_topology_trianglelist"></span>**D3D11 \_ primitive \_ Topologie ( \_ drei)**</span><span class="sxs-lookup"><span data-stu-id="09a14-118"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="d3d11_primitive_topology_trianglelist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_TRIANGLELIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-119">Interpretiert die Scheitelpunkt Daten als eine Liste von Dreiecken.</span><span class="sxs-lookup"><span data-stu-id="09a14-119">Interpret the vertex data as a list of triangles.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-120"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="d3d11_primitive_topology_trianglestrip"></span>**D3D11 \_ primitive \_ Topologie ( \_ drei)**</span><span class="sxs-lookup"><span data-stu-id="09a14-120"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="d3d11_primitive_topology_trianglestrip"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_TRIANGLESTRIP**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-121">Interpretieren Sie die Scheitelpunkt Daten als Dreiecks Streifen.</span><span class="sxs-lookup"><span data-stu-id="09a14-121">Interpret the vertex data as a triangle strip.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-122"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="d3d11_primitive_topology_linelist_adj"></span>**D3D11 \_ primitive \_ Topologie \_ LineList \_ ADJ**</span><span class="sxs-lookup"><span data-stu-id="09a14-122"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="d3d11_primitive_topology_linelist_adj"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_LINELIST\_ADJ**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-123">Interpretieren Sie die Scheitelpunkt Daten als Liste von Zeilen mit Daten.</span><span class="sxs-lookup"><span data-stu-id="09a14-123">Interpret the vertex data as list of lines with adjacency data.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-124"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="d3d11_primitive_topology_linestrip_adj"></span>**D3D11 \_ primitive \_ Topologie ( \_ linestrip) \_**</span><span class="sxs-lookup"><span data-stu-id="09a14-124"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="d3d11_primitive_topology_linestrip_adj"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_LINESTRIP\_ADJ**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-125">Interpretieren Sie die Scheitelpunkt Daten als Zeilen Streifen mit Daten der Daten.</span><span class="sxs-lookup"><span data-stu-id="09a14-125">Interpret the vertex data as line strip with adjacency data.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-126"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="d3d11_primitive_topology_trianglelist_adj"></span>**D3D11 \_ primitive \_ Topologie \_ (in \_ TL)**</span><span class="sxs-lookup"><span data-stu-id="09a14-126"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="d3d11_primitive_topology_trianglelist_adj"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_TRIANGLELIST\_ADJ**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-127">Interpretieren Sie die Scheitelpunkt Daten als Liste von Dreiecken mit Daten.</span><span class="sxs-lookup"><span data-stu-id="09a14-127">Interpret the vertex data as list of triangles with adjacency data.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-128"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="d3d11_primitive_topology_trianglestrip_adj"></span>**D3D11 \_ primitive \_ Topologie, \_ \_ ADJ**</span><span class="sxs-lookup"><span data-stu-id="09a14-128"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="d3d11_primitive_topology_trianglestrip_adj"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_TRIANGLESTRIP\_ADJ**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-129">Interpretieren Sie die Scheitelpunkt Daten als Dreiecks Streifen mit Daten der Daten.</span><span class="sxs-lookup"><span data-stu-id="09a14-129">Interpret the vertex data as triangle strip with adjacency data.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-130"><span id="D3D11_PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_1_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 1 \_ - \_ Patchliste für Kontrollpunkt \_**</span><span class="sxs-lookup"><span data-stu-id="09a14-130"><span id="D3D11_PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_1_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_1\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-131">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-131">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-132"><span id="D3D11_PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_2_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 2 \_ - \_ Patchliste für Kontrollpunkte \_**</span><span class="sxs-lookup"><span data-stu-id="09a14-132"><span id="D3D11_PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_2_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_2\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-133">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-133">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-134"><span id="D3D11_PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_3_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 3 \_ - \_ Patchliste für Steuerungspunkt \_**</span><span class="sxs-lookup"><span data-stu-id="09a14-134"><span id="D3D11_PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_3_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_3\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-135">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-135">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-136"><span id="D3D11_PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_4_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 4 \_ - \_ Patchliste für Steuerungspunkt \_**</span><span class="sxs-lookup"><span data-stu-id="09a14-136"><span id="D3D11_PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_4_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_4\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-137">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-137">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-138"><span id="D3D11_PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_5_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 5- \_ Steuerungs \_ Punkt- \_ Patchliste**</span><span class="sxs-lookup"><span data-stu-id="09a14-138"><span id="D3D11_PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_5_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_5\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-139">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-139">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-140"><span id="D3D11_PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_6_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 6 \_ , \_ Patchliste für Steuerungspunkt \_**</span><span class="sxs-lookup"><span data-stu-id="09a14-140"><span id="D3D11_PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_6_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_6\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-141">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-141">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-142"><span id="D3D11_PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_7_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 7 \_ - \_ Patchliste für Steuerungspunkt \_**</span><span class="sxs-lookup"><span data-stu-id="09a14-142"><span id="D3D11_PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_7_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_7\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-143">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-143">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-144"><span id="D3D11_PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_8_control_point_patchlist"></span>**D3D11 \_ - \_ \_ \_ Kontroll \_ Punkt- \_ Patchliste für primitive Topologie 8**</span><span class="sxs-lookup"><span data-stu-id="09a14-144"><span id="D3D11_PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_8_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_8\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-145">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-145">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-146"><span id="D3D11_PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_9_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 9 \_ - \_ Patchliste für Steuerungspunkt \_**</span><span class="sxs-lookup"><span data-stu-id="09a14-146"><span id="D3D11_PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_9_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_9\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-147">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-147">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-148"><span id="D3D11_PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_10_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 10 \_ - \_ Patchliste für Steuerungspunkt \_**</span><span class="sxs-lookup"><span data-stu-id="09a14-148"><span id="D3D11_PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_10_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_10\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-149">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-149">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-150"><span id="D3D11_PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_11_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 11 \_ - \_ Patchliste für Steuerungspunkt \_**</span><span class="sxs-lookup"><span data-stu-id="09a14-150"><span id="D3D11_PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_11_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_11\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-151">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-151">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-152"><span id="D3D11_PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_12_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 12- \_ Kontroll \_ Punkt- \_ Patchliste**</span><span class="sxs-lookup"><span data-stu-id="09a14-152"><span id="D3D11_PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_12_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_12\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-153">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-153">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-154"><span id="D3D11_PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_13_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 13 \_ , \_ Patchliste für Steuerungspunkt \_**</span><span class="sxs-lookup"><span data-stu-id="09a14-154"><span id="D3D11_PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_13_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_13\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-155">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-155">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-156"><span id="D3D11_PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_14_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 14 \_ - \_ Patchliste für Steuerungspunkt \_**</span><span class="sxs-lookup"><span data-stu-id="09a14-156"><span id="D3D11_PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_14_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_14\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-157">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-157">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-158"><span id="D3D11_PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_15_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 15- \_ Steuerungs \_ Punkt- \_ Patchliste**</span><span class="sxs-lookup"><span data-stu-id="09a14-158"><span id="D3D11_PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_15_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_15\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-159">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-159">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-160"><span id="D3D11_PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_16_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 16- \_ Kontroll \_ Punkt- \_ Patchliste**</span><span class="sxs-lookup"><span data-stu-id="09a14-160"><span id="D3D11_PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_16_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_16\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-161">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-161">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-162"><span id="D3D11_PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_17_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 17 \_ Kontroll \_ Punkt- \_ Patchliste**</span><span class="sxs-lookup"><span data-stu-id="09a14-162"><span id="D3D11_PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_17_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_17\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-163">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-163">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-164"><span id="D3D11_PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_18_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 18- \_ Steuerungs \_ Punkt- \_ Patchliste**</span><span class="sxs-lookup"><span data-stu-id="09a14-164"><span id="D3D11_PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_18_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_18\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-165">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-165">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-166"><span id="D3D11_PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_19_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 19- \_ Kontroll \_ Punkt- \_ Patchliste**</span><span class="sxs-lookup"><span data-stu-id="09a14-166"><span id="D3D11_PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_19_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_19\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-167">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-167">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-168"><span id="D3D11_PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_20_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 20 \_ - \_ Patchliste für Kontrollpunkte \_**</span><span class="sxs-lookup"><span data-stu-id="09a14-168"><span id="D3D11_PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_20_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_20\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-169">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-169">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-170"><span id="D3D11_PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_21_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 21 \_ - \_ Patchliste für Steuerungspunkt \_**</span><span class="sxs-lookup"><span data-stu-id="09a14-170"><span id="D3D11_PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_21_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_21\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-171">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-171">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-172"><span id="D3D11_PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_22_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 22 \_ - \_ Patchliste für Steuerungspunkt \_**</span><span class="sxs-lookup"><span data-stu-id="09a14-172"><span id="D3D11_PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_22_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_22\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-173">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-173">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-174"><span id="D3D11_PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_23_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 23- \_ Steuerungs \_ Punkt- \_ Patchliste**</span><span class="sxs-lookup"><span data-stu-id="09a14-174"><span id="D3D11_PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_23_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_23\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-175">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-175">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-176"><span id="D3D11_PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_24_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 24- \_ Kontroll \_ Punkt- \_ Patchliste**</span><span class="sxs-lookup"><span data-stu-id="09a14-176"><span id="D3D11_PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_24_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_24\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-177">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-177">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-178"><span id="D3D11_PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_25_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 25 \_ Steuerungs \_ Punkt- \_ Patchliste**</span><span class="sxs-lookup"><span data-stu-id="09a14-178"><span id="D3D11_PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_25_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_25\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-179">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-179">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-180"><span id="D3D11_PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_26_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 26- \_ Steuerungs \_ Punkt- \_ Patchliste**</span><span class="sxs-lookup"><span data-stu-id="09a14-180"><span id="D3D11_PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_26_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_26\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-181">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-181">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-182"><span id="D3D11_PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_27_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 27 \_ Kontroll \_ Punkt- \_ Patchliste**</span><span class="sxs-lookup"><span data-stu-id="09a14-182"><span id="D3D11_PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_27_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_27\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-183">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-183">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-184"><span id="D3D11_PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_28_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 28- \_ Steuerungs \_ Punkt- \_ Patchliste**</span><span class="sxs-lookup"><span data-stu-id="09a14-184"><span id="D3D11_PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_28_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_28\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-185">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-185">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-186"><span id="D3D11_PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_29_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 29- \_ Steuerungs \_ Punkt- \_ Patchliste**</span><span class="sxs-lookup"><span data-stu-id="09a14-186"><span id="D3D11_PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_29_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_29\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-187">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-187">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-188"><span id="D3D11_PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_30_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 30- \_ Steuerungs \_ Punkt- \_ Patchliste**</span><span class="sxs-lookup"><span data-stu-id="09a14-188"><span id="D3D11_PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_30_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_30\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-189">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-189">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-190"><span id="D3D11_PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_31_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 31- \_ Steuerungs \_ Punkt- \_ Patchliste**</span><span class="sxs-lookup"><span data-stu-id="09a14-190"><span id="D3D11_PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_31_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_31\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-191">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-191">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="09a14-192"><span id="D3D11_PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_32_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 32 \_ - \_ Patchliste der Steuerungs Punkte \_**</span><span class="sxs-lookup"><span data-stu-id="09a14-192"><span id="D3D11_PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_32_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_32\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="09a14-193">Interpretieren Sie die Scheitelpunkt Daten als Patchliste.</span><span class="sxs-lookup"><span data-stu-id="09a14-193">Interpret the vertex data as a patch list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="09a14-194">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09a14-194">Remarks</span></span>

<span data-ttu-id="09a14-195">Bei der D3D11-Enumeration der **\_ primitiven \_ Topologie** handelt es sich um einen Typ, der in der D3D11. h-Header Datei als [**D3D \_ primitive \_ topologieenumeration**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology) definiert ist, die vollständig in der Header Datei D3DCommon. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="09a14-195">The **D3D11\_PRIMITIVE\_TOPOLOGY** enumeration is type defined in the D3D11.h header file as a [**D3D\_PRIMITIVE\_TOPOLOGY**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology) enumeration, which is fully defined in the D3DCommon.h header file.</span></span>
