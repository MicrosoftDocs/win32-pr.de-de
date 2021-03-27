---
title: HLSL-Shader-Modell 5
description: HLSL-Shader-Modell 5
ms.assetid: 072c1ff2-ca1b-427c-9969-aa24ebb4ee38
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b33b0e2f009b796eb0b8828cc195fb9543ba2b9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858322"
---
# <a name="hlsl-shader-model-5"></a><span data-ttu-id="467bd-103">HLSL-Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="467bd-103">HLSL Shader Model 5</span></span>

<span data-ttu-id="467bd-104">Dieser Abschnitt enthält ein Übersichts Material für die High-Level Shader-Sprache, insbesondere die neuen Features in Shader Model 5, die in Microsoft Direct3D 11 eingeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="467bd-104">This section contains overview material for the High-Level Shader Language, specifically the new features in shader model 5 introduced in Microsoft Direct3D 11.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="467bd-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="467bd-105">In This Section</span></span>



| <span data-ttu-id="467bd-106">Element</span><span class="sxs-lookup"><span data-stu-id="467bd-106">Item</span></span>                                                                                                                                                                                                               | <span data-ttu-id="467bd-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="467bd-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="467bd-108"><span id="Dynamic_Linking"></span><span id="dynamic_linking"></span><span id="DYNAMIC_LINKING"></span>[Dynamisches Verknüpfen](overviews-direct3d-11-hlsl-dynamic-linking.md)</span><span class="sxs-lookup"><span data-stu-id="467bd-108"><span id="Dynamic_Linking"></span><span id="dynamic_linking"></span><span id="DYNAMIC_LINKING"></span>[Dynamic Linking](overviews-direct3d-11-hlsl-dynamic-linking.md)</span></span><br/>                                 | <span data-ttu-id="467bd-109">Durch dynamisches Verknüpfen kann die Laufzeit eine Entscheidung zur zeichnungszeit (anstatt zur Kompilierzeit) treffen, welche Codepfad ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="467bd-109">Dynamic linking allows the runtime to make a decision at draw-time (rather than compile-time) about which code path to run.</span></span> <span data-ttu-id="467bd-110">Dadurch wird das Probleme mit der Shader-Verbreitung reduziert, das durch Shader mit nahezu identischen Eingabe Signaturen verursacht wird.</span><span class="sxs-lookup"><span data-stu-id="467bd-110">This reduces the shader proliferation problem caused by shaders with nearly identical input signatures.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="467bd-111"><span id="Geometry_Shader_Features"></span><span id="geometry_shader_features"></span><span id="GEOMETRY_SHADER_FEATURES"></span>[Geometry-Shaderfunktionen](overviews-direct3d-11-hlsl-gs-features.md)</span><span class="sxs-lookup"><span data-stu-id="467bd-111"><span id="Geometry_Shader_Features"></span><span id="geometry_shader_features"></span><span id="GEOMETRY_SHADER_FEATURES"></span>[Geometry Shader Features](overviews-direct3d-11-hlsl-gs-features.md)</span></span><br/> | <span data-ttu-id="467bd-112">Neue Geometry-shaderfeatures, einschließlich der Instanziierung, die eine Leistungssteigerung bietet, wenn die Reihenfolge der primitiven im Stream keine Rolle spielt, und mehrerer Punkt-Ausgabestreams, sodass ein Shader Vertices in mehr als einem Stream ausgeben kann.</span><span class="sxs-lookup"><span data-stu-id="467bd-112">New geometry shader features including: instancing, which provides a performance boost when the order of primitives in the stream doesn't matter, and multiple point output streams so a shader can output vertices on more than one stream.</span></span><br/>                                                                                                                |
| <span data-ttu-id="467bd-113"><span id="Tessellation"></span><span id="tessellation"></span><span id="TESSELLATION"></span>[Mosaik](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)</span><span class="sxs-lookup"><span data-stu-id="467bd-113"><span id="Tessellation"></span><span id="tessellation"></span><span id="TESSELLATION"></span>[Tessellation](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)</span></span><br/>                                        | <span data-ttu-id="467bd-114">Die Direct3D 11-Laufzeit unterstützt drei neue Phasen, die das Mosaik implementieren, das untergeordnete Oberflächen auf niedriger Detailebene in die GPU konvertiert.</span><span class="sxs-lookup"><span data-stu-id="467bd-114">The Direct3D 11 runtime supports three new stages that implement tessellation, which converts low-detail subdivision surfaces into higher-detail primitives on the GPU.</span></span> <span data-ttu-id="467bd-115">Mosaik Kacheln (oder unterbrechen) hoch geordnete Oberflächen in geeignete Strukturen zum Rendern.</span><span class="sxs-lookup"><span data-stu-id="467bd-115">Tessellation tiles (or breaks up) high-order surfaces into suitable structures for rendering.</span></span> <span data-ttu-id="467bd-116">Die drei Mosaik Phasen sind Hull-Shader-, Mosaik-und Domänen-Shader-Phasen.</span><span class="sxs-lookup"><span data-stu-id="467bd-116">The three tessellation stages are hull-shader, tessellator, and domain-shader stages.</span></span><br/> |



 

<span data-ttu-id="467bd-117">Außerdem deckt der Referenz Abschnitt viele neue API-Elemente für Shader Model 5 ab, darunter [Attribute](d3d11-graphics-reference-sm5-attributes.md), [intrinsische Funktionen](d3d11-graphics-reference-sm5-intrinsics.md), [Shader-Modell 5-Objekte und-Methoden](d3d11-graphics-reference-sm5-objects.md)und [System Werte](d3d11-graphics-reference-sm5-system-values.md).</span><span class="sxs-lookup"><span data-stu-id="467bd-117">In addition, the reference section covers many new API elements for shader model 5 including: [attributes](d3d11-graphics-reference-sm5-attributes.md), [intrinsic functions](d3d11-graphics-reference-sm5-intrinsics.md), [shader model 5 objects and methods](d3d11-graphics-reference-sm5-objects.md), and [system values](d3d11-graphics-reference-sm5-system-values.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="467bd-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="467bd-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="467bd-119">Programmieranleitung für HLSL</span><span class="sxs-lookup"><span data-stu-id="467bd-119">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

