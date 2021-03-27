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
# <a name="hlsl-shader-model-5"></a>HLSL-Shader-Modell 5

Dieser Abschnitt enthält ein Übersichts Material für die High-Level Shader-Sprache, insbesondere die neuen Features in Shader Model 5, die in Microsoft Direct3D 11 eingeführt wurden.

## <a name="in-this-section"></a>In diesem Abschnitt



| Element                                                                                                                                                                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Dynamic_Linking"></span><span id="dynamic_linking"></span><span id="DYNAMIC_LINKING"></span>[Dynamisches Verknüpfen](overviews-direct3d-11-hlsl-dynamic-linking.md)<br/>                                 | Durch dynamisches Verknüpfen kann die Laufzeit eine Entscheidung zur zeichnungszeit (anstatt zur Kompilierzeit) treffen, welche Codepfad ausgeführt werden soll. Dadurch wird das Probleme mit der Shader-Verbreitung reduziert, das durch Shader mit nahezu identischen Eingabe Signaturen verursacht wird.<br/>                                                                                                                         |
| <span id="Geometry_Shader_Features"></span><span id="geometry_shader_features"></span><span id="GEOMETRY_SHADER_FEATURES"></span>[Geometry-Shaderfunktionen](overviews-direct3d-11-hlsl-gs-features.md)<br/> | Neue Geometry-shaderfeatures, einschließlich der Instanziierung, die eine Leistungssteigerung bietet, wenn die Reihenfolge der primitiven im Stream keine Rolle spielt, und mehrerer Punkt-Ausgabestreams, sodass ein Shader Vertices in mehr als einem Stream ausgeben kann.<br/>                                                                                                                |
| <span id="Tessellation"></span><span id="tessellation"></span><span id="TESSELLATION"></span>[Mosaik](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)<br/>                                        | Die Direct3D 11-Laufzeit unterstützt drei neue Phasen, die das Mosaik implementieren, das untergeordnete Oberflächen auf niedriger Detailebene in die GPU konvertiert. Mosaik Kacheln (oder unterbrechen) hoch geordnete Oberflächen in geeignete Strukturen zum Rendern. Die drei Mosaik Phasen sind Hull-Shader-, Mosaik-und Domänen-Shader-Phasen.<br/> |



 

Außerdem deckt der Referenz Abschnitt viele neue API-Elemente für Shader Model 5 ab, darunter [Attribute](d3d11-graphics-reference-sm5-attributes.md), [intrinsische Funktionen](d3d11-graphics-reference-sm5-intrinsics.md), [Shader-Modell 5-Objekte und-Methoden](d3d11-graphics-reference-sm5-objects.md)und [System Werte](d3d11-graphics-reference-sm5-system-values.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieranleitung für HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

