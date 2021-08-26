---
title: HLSL-Shadermodell 5
description: HLSL-Shadermodell 5
ms.assetid: 072c1ff2-ca1b-427c-9969-aa24ebb4ee38
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 537b2460b73f30397561dea37bcb3711b64a935c43d45662428585a47d6f6574
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095350"
---
# <a name="hlsl-shader-model-5"></a>HLSL-Shadermodell 5

Dieser Abschnitt enthält Übersichtsmaterial für die High-Level Shader-Sprache, insbesondere die neuen Features im Shadermodell 5, die in Microsoft Direct3D 11 eingeführt wurden.

## <a name="in-this-section"></a>In diesem Abschnitt



| Element                                                                                                                                                                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Dynamic_Linking"></span><span id="dynamic_linking"></span><span id="DYNAMIC_LINKING"></span>[Dynamische Verknüpfung](overviews-direct3d-11-hlsl-dynamic-linking.md)<br/>                                 | Die dynamische Verknüpfung ermöglicht der Laufzeit, zur Zeichnenzeit (anstatt zur Kompilierzeit) eine Entscheidung darüber zu treffen, welcher Codepfad ausgeführt werden soll. Dadurch wird das Durchdringungsproblem des Shaders reduziert, das durch Shader mit nahezu identischen Eingabesignaturen verursacht wird.<br/>                                                                                                                         |
| <span id="Geometry_Shader_Features"></span><span id="geometry_shader_features"></span><span id="GEOMETRY_SHADER_FEATURES"></span>[Geometry Shader-Features](overviews-direct3d-11-hlsl-gs-features.md)<br/> | Neue Geometrie-Shaderfeatures, z. B.: Instanziierung, die eine Leistungssteigerung ermöglicht, wenn die Reihenfolge von Primitiven im Stream keine Rolle spielt, und mehrere Punktausgabestreams, sodass ein Shader Scheitelpunkte in mehr als einem Stream ausgeben kann.<br/>                                                                                                                |
| <span id="Tessellation"></span><span id="tessellation"></span><span id="TESSELLATION"></span>[Tessellation](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)<br/>                                        | Die Direct3D 11-Runtime unterstützt drei neue Phasen, die Mosaik implementieren, wodurch Unterteilungsoberflächen mit geringen Details in Primitive mit höheren Details auf der GPU konvertiert werden. Mosaikkacheln (oder unterteilt) oberflächen hoher Ordnung in geeignete Strukturen für das Rendering. Die drei Mosaikstufen sind die Stufen "hull-shader", "tessellator" und "domain-shader".<br/> |



 

Darüber hinaus werden im Referenzabschnitt viele neue API-Elemente für Shadermodell 5 behandelt, darunter [Attribute,](d3d11-graphics-reference-sm5-attributes.md) [systeminterne Funktionen,](d3d11-graphics-reference-sm5-intrinsics.md) [Shadermodell 5-Objekte und -Methoden](d3d11-graphics-reference-sm5-objects.md)sowie [Systemwerte.](d3d11-graphics-reference-sm5-system-values.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieranleitung für HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

