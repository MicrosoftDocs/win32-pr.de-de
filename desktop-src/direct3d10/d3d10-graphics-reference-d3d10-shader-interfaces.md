---
description: 'Dieser Abschnitt enthält Informationen zu den folgenden Shaderschnittstellen:'
ms.assetid: d8770b45-a05c-4dd8-9fa7-08fb4330d734
title: Shaderschnittstellen (Direct3D 10-Grafiken)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96962407492f5fc6b6f7bbacd155c265ffd03e11eff31f2b012a2d1c644d3f9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409150"
---
# <a name="shader-interfaces-direct3d-10-graphics"></a>Shaderschnittstellen (Direct3D 10-Grafiken)

Dieser Abschnitt enthält Informationen zu den folgenden Shaderschnittstellen:

Jede dieser Shaderschnittstellen verwaltet einen kompilierten Shader. Die -Schnittstelle wird erstellt, wenn ein Shader kompiliert wird, und dann an verschiedene APIs übergeben, die Zugriff auf einen kompilierten Shader benötigen. z. B. beim Binden eines Shaders an eine Pipelinephase oder beim Abrufen einer Shadersignatur.



| Pipeline-Stage Schnittstellen                                      | BESCHREIBUNG                                                                                                                                 |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3D10GeometryShader-Schnittstelle**](/windows/win32/api/d3d10/nn-d3d10-id3d10geometryshader) | Ein geometry-shader implementiert eine primitive Verarbeitung in der [Geometry-Shader-Stufe.](d3d10-graphics-programming-guide-pipeline-stages.md) |
| [**ID3D10PixelShader-Schnittstelle**](/windows/win32/api/d3d10/nn-d3d10-id3d10pixelshader)       | Ein Pixel-Shader implementiert die Verarbeitung pro Pixel in der [Pixel-Shader-Stufe.](d3d10-graphics-programming-guide-pipeline-stages.md)           |
| [**ID3D10VertexShader-Schnittstelle**](/windows/win32/api/d3d10/nn-d3d10-id3d10vertexshader)     | Ein Vertex-Shader implementiert die Verarbeitung pro Scheitelpunkt in der [Vertex-Shader-Stufe.](d3d10-graphics-programming-guide-pipeline-stages.md)        |



 

Shader-Reflektionsschnittstellen ermöglichen es einer Anwendung, den Inhalt eines Shaders zur Entwurfszeit bzw. zur Erstellungszeit zu überprüfen. Shader-Reflektion ist zum Festlegen von Variablen zur Laufzeit nicht nützlich, da es sich um eine Spiegelung der Shaderdaten handelt, und unterstützt daher keine Methoden zum Festlegen von Daten.



| Shader-Reflection Schnittstellen                                                                   | BESCHREIBUNG                                                                        |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**ID3D10ShaderReflection-Schnittstelle**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)                             | Eine COM-Schnittstelle zum Lesen von Informationen aus einem kompilierten Shader zur Erstellungszeit.     |
| [**ID3D10ShaderReflectionConstantBuffer-Schnittstelle**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionconstantbuffer) | Eine Hilfsschnittstelle zum Abrufen einer Shader-Reflektions-Konstantenpufferschnittstelle.      |
| [**ID3D10ShaderReflectionType-Schnittstelle**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectiontype)                     | Eine Hilfsschnittstelle zum Abrufen einer Shader-Reflektionstyp-Schnittstelle.                 |
| [**ID3D10ShaderReflectionVariable-Schnittstelle**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionvariable)             | Eine Hilfsschnittstelle zum Abrufen einer Shader-Reflektionsvariablen-Schnittstelle.             |
| [**ID3D10ShaderResourceView-Schnittstelle**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)                         | Eine Shader-Reflektionsschnittstelle zum Lesen von Informationen aus einer Shaderressourcenansicht. |



 

Shaderreflektions-APIs implementieren eine COM-Shaderreflektionsschnittstelle ([**ID3D10ShaderReflection Interface**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)) und mehrere Nicht-COM-Hilfsschnittstellen (die restlichen Schnittstellen). **Die ID3D10ShaderReflection-Schnittstelle** wird erstellt, wenn ein Shaderreflektionsobjekt erstellt wird. Es folgt den COM-Standardregeln. Durch das Erstellen der Schnittstelle wird die Verweisanzahl erhöht, und die Schnittstelle muss freigegeben werden, wenn sie nicht mehr benötigt wird. Die verbleibenden Shader-Reflektionsschnittstellen sind Hilfsschnittstellen, die nicht von IUnknown erben. Dies bedeutet, dass sie keine Verweisanzahl ändern, wenn sie erstellt werden, und sie müssen nicht zerstört werden, wenn Sie mit ihnen fertig sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader-Referenz](d3d10-graphics-reference-d3d10-shader.md)
</dt> </dl>

 

 
