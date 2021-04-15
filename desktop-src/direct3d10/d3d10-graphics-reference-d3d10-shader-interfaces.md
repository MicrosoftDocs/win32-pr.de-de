---
description: 'Dieser Abschnitt enthält Informationen zu den folgenden Shader-Schnittstellen:'
ms.assetid: d8770b45-a05c-4dd8-9fa7-08fb4330d734
title: Shader-Schnittstellen (Direct3D 10-Grafiken)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838a65d263533d0b2225515664e21c2d93114495
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483398"
---
# <a name="shader-interfaces-direct3d-10-graphics"></a>Shader-Schnittstellen (Direct3D 10-Grafiken)

Dieser Abschnitt enthält Informationen zu den folgenden Shader-Schnittstellen:

Jede dieser shaderschnittstellen verwaltet einen kompilierten Shader. Die-Schnittstelle wird erstellt, wenn ein Shader kompiliert wird, und wird dann an verschiedene APIs weitergegeben, die Zugriff auf einen kompilierten Shader benötigen. Dies ist beispielsweise der Fall, wenn ein Shader an eine Pipeline Phase gebunden oder eine shadersignatur erhalten wird.



| Pipeline-Stage Schnittstellen                                      | BESCHREIBUNG                                                                                                                                 |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3D10GeometryShader-Schnittstelle**](/windows/win32/api/d3d10/nn-d3d10-id3d10geometryshader) | Ein Geometry-Shader implementiert pro primitiver Verarbeitung in der [Geometry-Shader-Stufe](d3d10-graphics-programming-guide-pipeline-stages.md). |
| [**ID3D10PixelShader-Schnittstelle**](/windows/win32/api/d3d10/nn-d3d10-id3d10pixelshader)       | Ein Pixel-Shader implementiert die Verarbeitung pro Pixel in der [Pixel-Shader-Stufe](d3d10-graphics-programming-guide-pipeline-stages.md).           |
| [**ID3D10VertexShader-Schnittstelle**](/windows/win32/api/d3d10/nn-d3d10-id3d10vertexshader)     | Ein Vertex-Shader implementiert die Verarbeitung pro Scheitelpunkt in der [Vertex-Shader-Stufe](d3d10-graphics-programming-guide-pipeline-stages.md).        |



 

Shader-reflektionsschnittstellen ermöglichen einer Anwendung, den Inhalt eines Shaders zur Entwurfs-/Schreibzeit zu überprüfen. Die Shader-Reflektion ist für das Festlegen von Variablen zur Laufzeit nicht sinnvoll, da es sich um einen Spiegel der shaderdaten handelt, und unterstützt daher keine Methoden zum Festlegen von Daten.



| Shader-Reflection Schnittstellen                                                                   | BESCHREIBUNG                                                                        |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**ID3D10ShaderReflection-Schnittstelle**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)                             | Eine COM-Schnittstelle zum Lesen von Informationen aus einem kompilierten Shader zur Autor Zeit.     |
| [**ID3D10ShaderReflectionConstantBuffer-Schnittstelle**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionconstantbuffer) | Eine Hilfsschnittstelle zum erhalten einer Shader-Reflection-Konstante für den Puffer.      |
| [**ID3D10ShaderReflectionType-Schnittstelle**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectiontype)                     | Eine Hilfsschnittstelle zum erhalten einer Shader-Reflektionstyp-Schnittstelle.                 |
| [**ID3D10ShaderReflectionVariable-Schnittstelle**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionvariable)             | Eine Hilfsschnittstelle zum erhalten einer Shader-Reflection-Variable-Schnittstelle.             |
| [**ID3D10ShaderResourceView-Schnittstelle**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)                         | Eine Shader-reflektionssschnittstelle zum Lesen von Informationen aus einer Shader-Ressourcen Ansicht. |



 

Shader Reflection-APIs implementieren eine com-Shader-reflektionsanschnittstelle ([**ID3D10ShaderReflection Interface**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)) und mehrere nicht-com-Hilfsobjekte (die restlichen Schnittstellen). **ID3D10ShaderReflection Interface** wird erstellt, wenn ein Shader-Reflektionsobjekt erstellt wird. Es folgt den Standard-com-Regeln. das Erstellen der-Schnittstelle erhöht den Verweis Zähler, und die Schnittstelle muss freigegeben werden, wenn Sie nicht mehr benötigt wird. Die verbleibenden Shader-Reflection-Schnittstellen sind hilfsschnittstellen, die nicht von IUnknown erben. Dies bedeutet, dass Sie bei der Erstellung keinen Verweis Zähler ändern und nicht zerstört werden müssen, wenn Sie damit fertig sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader-Referenz](d3d10-graphics-reference-d3d10-shader.md)
</dt> </dl>

 

 
