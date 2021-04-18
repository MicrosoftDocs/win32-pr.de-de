---
title: Direct3D 12-Raytracing, HLSL-Shader
description: Die folgenden HLSL-Shader unterstützen die Direct3D 12-Raytracing-Pipeline.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1dd545532208095781f6fbca25480a6dbfd31e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106340554"
---
# <a name="direct3d-12-raytracing-hlsl-shaders"></a>Direct3D 12-Raytracing, HLSL-Shader

Die folgenden HLSL-Shader unterstützen die Direct3D 12-Raytracing-Pipeline. Diese Shader sind Funktionen, die in eine Bibliothek kompiliert werden, mit Zielmodell lib_6_3 und durch ein Attribut *[Shader ("shadertype")] in der shaderfunktion* identifiziert werden. Siehe System interne Funktionen und **System Werte** , um **zu sehen,** was für die einzelnen shadertypen zulässig ist.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Any Hit-Shader**](any-hit-shader.md)<br/>                              | Ein Shader, der aufgerufen wird, wenn Ray-Schnittmengen nicht deckend sind.<br/>                                                                                                                                                                                                                                              |
| [**Callable-Shader**](callable-shader.md)<br/>                              | Ein Shader, der von einem anderen Shader mit der systeminternen Funktion **callshader** aufgerufen wird.<br/>                                                                                                                                                                                                                                              |
| [**Closest Hit-Shader**](closest-hit-shader.md)<br/>                              | Ein Shader, der aufgerufen wird, wenn er aktiviert ist, und der nächstgelegene Treffer wurde ermittelt oder die Überprüfung der Ray-Schnittmenge wurde beendet.<br/>                                                                                                                                                                                                                                              |
| [**Intersection-Shader**](intersection-shader.md)<br/>                              | Ein Shader, der verwendet wird, um benutzerdefinierte Schnittmengen primitive für Strahlen zu implementieren, die ein zugeordnetes Begrenzungs Volume (Begrenzungsfeld) überschneiden.<br/>                                                                                                                                                                                                                                              |
| [**Miss-Shader**](miss-shader.md)<br/>                              | Ein Shader, der aufgerufen wird, wenn keine Ray-Schnittmengen gefunden oder akzeptiert werden.<br/>                                                                                                                                                                                                                                              |
| [**Ray Generation-Shader**](ray-generation-shader.md)<br/>                              | Ein Shader, der [**traceray**](traceray-function.md) aufruft, um Strahlen zu generieren.<br/>                                                                                                                                                                                                                                              |

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kern Referenz](direct3d-12-core-reference.md)
</dt> <dt>

[Referenz für Direct3D 12](direct3d-12-reference.md)
</dt> </dl>

 

 





