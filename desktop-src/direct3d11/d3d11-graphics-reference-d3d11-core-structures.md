---
title: Direct3D 11 Core-Strukturen
description: Dieser Abschnitt enthält Informationen zu den Kern Strukturen.
ms.assetid: 2a45182a-7114-4075-b8b8-147f52fe7aa9
keywords:
- Strukturen, Direct3D 11 Kerne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7025de822265d86e5da9f1da3855d2542c76abf5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390653"
---
# <a name="direct3d-11-core-structures"></a><span data-ttu-id="179f7-104">Direct3D 11 Core-Strukturen</span><span class="sxs-lookup"><span data-stu-id="179f7-104">Direct3D 11 core structures</span></span>

<span data-ttu-id="179f7-105">Dieser Abschnitt enthält Informationen zu den Kern Strukturen.</span><span class="sxs-lookup"><span data-stu-id="179f7-105">This section contains information about the core structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="179f7-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="179f7-106">In this section</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="179f7-107">Thema</span><span class="sxs-lookup"><span data-stu-id="179f7-107">Topic</span></span></th>
<th><span data-ttu-id="179f7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="179f7-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="179f7-109"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_blend_desc"><strong>D3D11_BLEND_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-109"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_blend_desc"><strong>D3D11_BLEND_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-110">Beschreibt den Blend-Status, den Sie in einem Aufrufen von <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-createblendstate"><strong>ID3D11Device:: kreateblendstate</strong></a> zum Erstellen eines Blend-State-Objekts verwenden.</span><span class="sxs-lookup"><span data-stu-id="179f7-110">Describes the blend state that you use in a call to <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-createblendstate"><strong>ID3D11Device::CreateBlendState</strong></a> to create a blend-state object.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-111"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1"><strong>D3D11_BLEND_DESC1</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-111"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1"><strong>D3D11_BLEND_DESC1</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="179f7-112">Diese Struktur wird von der Direct3D 11,1-Laufzeit unterstützt, die unter Windows 8 und höheren Betriebssystemen verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="179f7-112">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="179f7-113">Beschreibt den Blend-Status, den Sie in einem <a href="/windows/win32/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1"><strong>ID3D11Device1:: CreateBlendState1</strong></a> -Befehl verwenden, um ein Blend-State-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="179f7-113">Describes the blend state that you use in a call to <a href="/windows/win32/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1"><strong>ID3D11Device1::CreateBlendState1</strong></a> to create a blend-state object.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-114"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_box"><strong>D3D11_BOX</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-114"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_box"><strong>D3D11_BOX</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-115">Definiert ein 3D-Feld.</span><span class="sxs-lookup"><span data-stu-id="179f7-115">Defines a 3D box.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-116"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_desc"><strong>D3D11_COUNTER_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-116"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_desc"><strong>D3D11_COUNTER_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-117">Beschreibt einen-Counter.</span><span class="sxs-lookup"><span data-stu-id="179f7-117">Describes a counter.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-118"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_info"><strong>D3D11_COUNTER_INFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-118"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_info"><strong>D3D11_COUNTER_INFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-119">Informationen zu den Leistungs Leistungsdaten der Grafikkarte.</span><span class="sxs-lookup"><span data-stu-id="179f7-119">Information about the video card's performance counter capabilities.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-120"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc"><strong>D3D11_DEPTH_STENCIL_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-120"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc"><strong>D3D11_DEPTH_STENCIL_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-121">Beschreibt den Status der tiefen Schablone.</span><span class="sxs-lookup"><span data-stu-id="179f7-121">Describes depth-stencil state.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-122"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc"><strong>D3D11_DEPTH_STENCILOP_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-122"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc"><strong>D3D11_DEPTH_STENCILOP_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-123">Schablonen Vorgänge, die auf der Grundlage der Ergebnisse des Schablonen Tests ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="179f7-123">Stencil operations that can be performed based on the results of stencil test.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-124"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_indexed_instanced_indirect_args"><strong>D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-124"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_indexed_instanced_indirect_args"><strong>D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-125">Argumente zum Zeichnen indizierter instanziierten, indirekt.</span><span class="sxs-lookup"><span data-stu-id="179f7-125">Arguments for draw indexed instanced indirect.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-126"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_instanced_indirect_args"><strong>D3D11_DRAW_INSTANCED_INDIRECT_ARGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-126"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_instanced_indirect_args"><strong>D3D11_DRAW_INSTANCED_INDIRECT_ARGS</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-127">Argumente für eine indirekte zeichnen-Instanz.</span><span class="sxs-lookup"><span data-stu-id="179f7-127">Arguments for draw instanced indirect.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-128"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info"><strong>D3D11_FEATURE_DATA_ARCHITECTURE_INFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-128"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info"><strong>D3D11_FEATURE_DATA_ARCHITECTURE_INFO</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="179f7-129">Diese Struktur wird von der Direct3D 11,1-Laufzeit unterstützt, die unter Windows 8 und höheren Betriebssystemen verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="179f7-129">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="179f7-130">Beschreibt Informationen zur Direct3D 11,1-Adapter Architektur.</span><span class="sxs-lookup"><span data-stu-id="179f7-130">Describes information about Direct3D 11.1 adapter architecture.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-131"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-131"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="179f7-132">Diese Struktur wird von der Direct3D 11,1-Laufzeit unterstützt, die unter Windows 8 und höheren Betriebssystemen verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="179f7-132">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="179f7-133">Beschreibt Direct3D 9-Funktions Optionen im aktuellen Grafiktreiber.</span><span class="sxs-lookup"><span data-stu-id="179f7-133">Describes Direct3D 9 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-134"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options1"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS1</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-134"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options1"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS1</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-135">Beschreibt Direct3D 9-Funktions Optionen im aktuellen Grafiktreiber.</span><span class="sxs-lookup"><span data-stu-id="179f7-135">Describes Direct3D 9 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-136"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support"><strong>D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-136"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support"><strong>D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="179f7-137">Diese Struktur wird von der Direct3D 11,1-Laufzeit unterstützt, die unter Windows 8 und höheren Betriebssystemen verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="179f7-137">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="179f7-138">Beschreibt die Direct3D 9-Schatten Unterstützung im aktuellen Grafiktreiber.</span><span class="sxs-lookup"><span data-stu-id="179f7-138">Describes Direct3D 9 shadow support in the current graphics driver.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-139"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_simple_instancing_support"><strong>D3D11_FEATURE_DATA_D3D9_SIMPLE_INSTANCING_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-139"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_simple_instancing_support"><strong>D3D11_FEATURE_DATA_D3D9_SIMPLE_INSTANCING_SUPPORT</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-140">Beschreibt, ob einfache Instanziierung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="179f7-140">Describes whether simple instancing is supported.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-141"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options"><strong>D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-141"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options"><strong>D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-142">Beschreibt die Unterstützung von Compute-Shader und der Rohund strukturierten Puffer im aktuellen Grafiktreiber.</span><span class="sxs-lookup"><span data-stu-id="179f7-142">Describes compute shader and raw and structured buffer support in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-143"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-143"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="179f7-144">Diese Struktur wird von der Direct3D 11,1-Laufzeit unterstützt, die unter Windows 8 und höheren Betriebssystemen verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="179f7-144">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="179f7-145">Beschreibt Direct3D 11,1-Funktions Optionen im aktuellen Grafiktreiber.</span><span class="sxs-lookup"><span data-stu-id="179f7-145">Describes Direct3D 11.1 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-146"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS1</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-146"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS1</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-147">Beschreibt Direct3D 11,2-Funktions Optionen im aktuellen Grafiktreiber.</span><span class="sxs-lookup"><span data-stu-id="179f7-147">Describes Direct3D 11.2 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-148"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS2</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-148"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS2</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-149">Beschreibt Direct3D 11,3-Funktions Optionen im aktuellen Grafiktreiber.</span><span class="sxs-lookup"><span data-stu-id="179f7-149">Describes Direct3D 11.3 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-150"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS3</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-150"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS3</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-151">Beschreibt Direct3D 11,3-Funktions Optionen im aktuellen Grafiktreiber.</span><span class="sxs-lookup"><span data-stu-id="179f7-151">Describes Direct3D 11.3 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-152"><a href="/windows/win32/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS4</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-152"><a href="/windows/win32/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS4</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-153">Beschreibt Direct3D 11,4-Funktions Optionen im aktuellen Grafiktreiber.</span><span class="sxs-lookup"><span data-stu-id="179f7-153">Describes Direct3D 11.4 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-154"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options5"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS5</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-154"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options5"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS5</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-155">Beschreibt die Ebene der Unterstützung für freigegebene Ressourcen im aktuellen Grafiktreiber.</span><span class="sxs-lookup"><span data-stu-id="179f7-155">Describes the level of support for shared resources in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-156"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_doubles"><strong>D3D11_FEATURE_DATA_DOUBLES</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-156"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_doubles"><strong>D3D11_FEATURE_DATA_DOUBLES</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-157">Beschreibt die Unterstützung doppelter Datentypen im aktuellen Grafiktreiber.</span><span class="sxs-lookup"><span data-stu-id="179f7-157">Describes double data type support in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-158"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-158"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-159">Beschreibt, welche Ressourcen vom aktuellen Grafiktreiber für ein bestimmtes Format unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="179f7-159">Describes which resources are supported by the current graphics driver for a given format.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-160"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-160"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-161">Beschreibt, welche Optionen für ungeordnete Ressourcen vom aktuellen Grafiktreiber für ein bestimmtes Format unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="179f7-161">Describes which unordered resource options are supported by the current graphics driver for a given format.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-162"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_gpu_virtual_address_support"><strong>D3D11_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-162"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_gpu_virtual_address_support"><strong>D3D11_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-163">Beschreibt die Unterstützung der Unterstützung virtueller GPU-Adressen, einschließlich der maximalen Adress Bits pro Ressource und pro Prozess.</span><span class="sxs-lookup"><span data-stu-id="179f7-163">Describes feature data GPU virtual address support, including maximum address bits per resource and per process.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-164"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_marker_support"><strong>D3D11_FEATURE_DATA_MARKER_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-164"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_marker_support"><strong>D3D11_FEATURE_DATA_MARKER_SUPPORT</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-165">Beschreibt, ob eine GPU-Profil Erstellungs Methode unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="179f7-165">Describes whether a GPU profiling technique is supported.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-166"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_shader_cache"><strong>D3D11_FEATURE_DATA_SHADER_CACHE</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-166"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_shader_cache"><strong>D3D11_FEATURE_DATA_SHADER_CACHE</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-167">Beschreibt die Ebene der Shader-Zwischenspeicherung, die im aktuellen Grafiktreiber unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="179f7-167">Describes the level of shader caching supported in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-168"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support"><strong>D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-168"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support"><strong>D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="179f7-169">Diese Struktur wird von der Direct3D 11,1-Laufzeit unterstützt, die unter Windows 8 und höheren Betriebssystemen verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="179f7-169">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="179f7-170">Beschreibt die Optionen für die Genauigkeits Unterstützung für Shader im aktuellen Grafiktreiber.</span><span class="sxs-lookup"><span data-stu-id="179f7-170">Describes precision support options for shaders in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-171"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_threading"><strong>D3D11_FEATURE_DATA_THREADING</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-171"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_threading"><strong>D3D11_FEATURE_DATA_THREADING</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-172">Beschreibt die Multithreading-Funktionen, die vom aktuellen Grafiktreiber unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="179f7-172">Describes the multi-threading features that are supported by the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-173"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_input_element_desc"><strong>D3D11_INPUT_ELEMENT_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-173"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_input_element_desc"><strong>D3D11_INPUT_ELEMENT_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-174">Eine Beschreibung eines einzelnen Elements für die Eingabe-Assembler-Stufe.</span><span class="sxs-lookup"><span data-stu-id="179f7-174">A description of a single element for the input-assembler stage.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-175"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_pipeline_statistics"><strong>D3D11_QUERY_DATA_PIPELINE_STATISTICS</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-175"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_pipeline_statistics"><strong>D3D11_QUERY_DATA_PIPELINE_STATISTICS</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-176">Abfrage Informationen zur Grafik Pipeline Aktivität zwischen Aufrufen von <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>Verknüpfung id3d11devicecontext aus:: begin</strong></a> und <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>Verknüpfung id3d11devicecontext aus:: End</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="179f7-176">Query information about graphics-pipeline activity in between calls to <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>ID3D11DeviceContext::Begin</strong></a> and <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>ID3D11DeviceContext::End</strong></a>.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-177"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_so_statistics"><strong>D3D11_QUERY_DATA_SO_STATISTICS</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-177"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_so_statistics"><strong>D3D11_QUERY_DATA_SO_STATISTICS</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-178">Abfrage Informationen über die Menge der Daten, die an die Stream-Ausgabepuffer zwischen <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>Verknüpfung id3d11devicecontext aus:: begin</strong></a> und <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>Verknüpfung id3d11devicecontext aus:: End</strong></a>gestreamt werden.</span><span class="sxs-lookup"><span data-stu-id="179f7-178">Query information about the amount of data streamed out to the stream-output buffers in between <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>ID3D11DeviceContext::Begin</strong></a> and <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>ID3D11DeviceContext::End</strong></a>.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-179"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_timestamp_disjoint"><strong>D3D11_QUERY_DATA_TIMESTAMP_DISJOINT</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-179"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_timestamp_disjoint"><strong>D3D11_QUERY_DATA_TIMESTAMP_DISJOINT</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-180">Abfrage Informationen über die Zuverlässigkeit einer Zeitstempel-Abfrage.</span><span class="sxs-lookup"><span data-stu-id="179f7-180">Query information about the reliability of a timestamp query.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-181"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_desc"><strong>D3D11_QUERY_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-181"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_desc"><strong>D3D11_QUERY_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-182">Beschreibt eine Abfrage.</span><span class="sxs-lookup"><span data-stu-id="179f7-182">Describes a query.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-183"><a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_query_desc1"><strong>D3D11_QUERY_DESC1</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-183"><a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_query_desc1"><strong>D3D11_QUERY_DESC1</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-184">Beschreibt eine Abfrage.</span><span class="sxs-lookup"><span data-stu-id="179f7-184">Describes a query.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-185"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_rasterizer_desc"><strong>D3D11_RASTERIZER_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-185"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_rasterizer_desc"><strong>D3D11_RASTERIZER_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-186">Beschreibt den Status des Rasterizers.</span><span class="sxs-lookup"><span data-stu-id="179f7-186">Describes rasterizer state.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-187"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1"><strong>D3D11_RASTERIZER_DESC1</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-187"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1"><strong>D3D11_RASTERIZER_DESC1</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="179f7-188">Diese Struktur wird von der Direct3D 11,1-Laufzeit unterstützt, die unter Windows 8 und höheren Betriebssystemen verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="179f7-188">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="179f7-189">Beschreibt den Status des Rasterizers.</span><span class="sxs-lookup"><span data-stu-id="179f7-189">Describes rasterizer state.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-190"><a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2"><strong>D3D11_RASTERIZER_DESC2</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-190"><a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2"><strong>D3D11_RASTERIZER_DESC2</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-191">Beschreibt den Status des Rasterizers.</span><span class="sxs-lookup"><span data-stu-id="179f7-191">Describes rasterizer state.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-192"><a href="d3d11-rect.md"><strong>D3D11_RECT</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-192"><a href="d3d11-rect.md"><strong>D3D11_RECT</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-193">D3D11_RECT wird wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="179f7-193">D3D11_RECT is declared as follows:</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-194"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_render_target_blend_desc"><strong>D3D11_RENDER_TARGET_BLEND_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-194"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_render_target_blend_desc"><strong>D3D11_RENDER_TARGET_BLEND_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-195">Beschreibt den Blend-Zustand für ein Renderziel.</span><span class="sxs-lookup"><span data-stu-id="179f7-195">Describes the blend state for a render target.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-196"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1"><strong>D3D11_RENDER_TARGET_BLEND_DESC1</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-196"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1"><strong>D3D11_RENDER_TARGET_BLEND_DESC1</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="179f7-197">Diese Struktur wird von der Direct3D 11,1-Laufzeit unterstützt, die unter Windows 8 und höheren Betriebssystemen verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="179f7-197">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="179f7-198">Beschreibt den Blend-Zustand für ein Renderziel.</span><span class="sxs-lookup"><span data-stu-id="179f7-198">Describes the blend state for a render target.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-199"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_sampler_desc"><strong>D3D11_SAMPLER_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-199"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_sampler_desc"><strong>D3D11_SAMPLER_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-200">Beschreibt einen samplerzustand.</span><span class="sxs-lookup"><span data-stu-id="179f7-200">Describes a sampler state.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-201"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_so_declaration_entry"><strong>D3D11_SO_DECLARATION_ENTRY</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-201"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_so_declaration_entry"><strong>D3D11_SO_DECLARATION_ENTRY</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-202">Beschreibung eines Vertex-Elements in einem Vertex-Puffer in einem Ausgabe Slot.</span><span class="sxs-lookup"><span data-stu-id="179f7-202">Description of a vertex element in a vertex buffer in an output slot.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="179f7-203"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_viewport"><strong>D3D11_VIEWPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="179f7-203"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_viewport"><strong>D3D11_VIEWPORT</strong></a></span></span><br/></td>
<td><span data-ttu-id="179f7-204">Definiert die Abmessungen eines Viewports.</span><span class="sxs-lookup"><span data-stu-id="179f7-204">Defines the dimensions of a viewport.</span></span><br/></td>
</tr>
</tbody>
</table>

<span data-ttu-id="179f7-205">Außerdem gibt es eine 2D-Rechteck Struktur, die in D3D11. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="179f7-205">In addition, there's a 2D rectangle structure defined in D3D11.h.</span></span>

```cpp
typedef RECT D3D11_RECT;
```

<span data-ttu-id="179f7-206">Dokumentation finden Sie unter [Rect](/previous-versions/dd162897%28v%3dvs.85%29) in [Windows GDI](../gdi/windows-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="179f7-206">For documentation, see [RECT](/previous-versions/dd162897%28v%3dvs.85%29) in [Windows GDI](../gdi/windows-gdi.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="179f7-207">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="179f7-207">Related topics</span></span>

[<span data-ttu-id="179f7-208">Kern Referenz</span><span class="sxs-lookup"><span data-stu-id="179f7-208">Core Reference</span></span>](d3d11-graphics-reference-d3d11-core.md)