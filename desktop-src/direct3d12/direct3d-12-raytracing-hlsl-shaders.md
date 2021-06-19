---
title: Direct3D 12-Raytracing, HLSL-Shader
description: Hier finden Sie Links zu Artikeln, die HLSL-Shader (High-Level Shader Language) beschreiben, die die Direct3D 12-Raytracingpipeline unterstützen.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca19081b1ea963851e82d18912153434c3e38d1
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394835"
---
# <a name="direct3d-12-raytracing-hlsl-shaders"></a>Direct3D 12-Raytracing, HLSL-Shader

Die folgenden HLSL-Shader unterstützen die Direct3D 12-Raytracingpipeline. Bei diesen Shadern handelt es sich um Funktionen, die in eine Bibliothek kompiliert werden, wobei das Zielmodell lib_6_3 und durch ein Attribut *[shader("shadertype")]* in der Shaderfunktion identifiziert wird. Informationen dazu, was für jeden Shadertyp zulässig ist, finden Sie unter **Systeminterne** Funktionen und **Systemwerte.**

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                       | Beschreibung                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Any Hit-Shader**](any-hit-shader.md)<br/>                              | Ein Shader, der aufgerufen wird, wenn Strahlschnittmengen nicht deckend sind.<br/>                                                                                                                                                                                                                                              |
| [**Callable-Shader**](callable-shader.md)<br/>                              | Ein Shader, der von einem anderen Shader mit der systeminternen **CallShader-Eigenschaft** aufgerufen wird.<br/>                                                                                                                                                                                                                                              |
| [**Closest Hit-Shader**](closest-hit-shader.md)<br/>                              | Ein Shader, der aufgerufen wird, wenn er aktiviert ist und der nächste Treffer bestimmt wurde oder die Suche nach Strahlschnitten beendet wurde.<br/>                                                                                                                                                                                                                                              |
| [**Intersection-Shader**](intersection-shader.md)<br/>                              | Ein Shader, der verwendet wird, um benutzerdefinierte Schnittmengenprimitive für Lichtstrahl zu implementieren, der ein zugeordnetes umgebendes Volumen (begrenzungsfeld) überschneidet.<br/>                                                                                                                                                                                                                                              |
| [**Miss-Shader**](miss-shader.md)<br/>                              | Ein Shader, der aufgerufen wird, wenn keine Strahlkreuzungen gefunden oder akzeptiert werden.<br/>                                                                                                                                                                                                                                              |
| [**Ray Generation-Shader**](ray-generation-shader.md)<br/>                              | Ein Shader, der [**TraceRay**](traceray-function.md) aufruft, um Lichtstrahl zu generieren.<br/>                                                                                                                                                                                                                                              |

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kernreferenz](direct3d-12-core-reference.md)
</dt> <dt>

[Referenz für Direct3D 12](direct3d-12-reference.md)
</dt> </dl>

 

 





