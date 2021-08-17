---
title: Vergleich von Shadermodellen und Shaderprofilen
description: Vergleich von Shadermodellen und Shaderprofilen
ms.assetid: 6224f05e-20b1-42ea-96fb-63dd0edb720e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d7f6a37b1d37225425a60cc42887d5e587d9522929bc78a28dbb5bf5854493f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726150"
---
# <a name="shader-models-vs-shader-profiles"></a>Vergleich von Shadermodellen und Shaderprofilen

Die Schattierungssprache auf hoher Ebene für DirectX implementiert eine Reihe von Shadermodellen. Mit HLSL können Sie C-ähnliche programmierbare Shader für die Direct3D-Pipeline erstellen. Jedes Shadermodell baut auf den Funktionen des Modells auf, bevor es verfügbar ist, und implementiert mehr Funktionalität mit weniger Einschränkungen.

Shadermodell 1 wurde mit DirectX 8 gestartet und enthielt Assemblyebene und C-ähnliche Anweisungen. Dieses Modell weist viele Einschränkungen auf, die durch frühe programmierbare Shaderhardware verursacht werden. Shadermodell 2 und 3 wurden aufgrund der Anzahl von Anweisungen erheblich erweitert, und Konstanten-Shader könnten verwenden. Sie sind viel leistungsstärker als Shadermodell 1, haben aber dennoch einige der bestehenden Einschränkungen des ersten Shadermodells.

Ab Windows Vista ist das Shadermodell 4 ein vollständiges Design. Sie ermöglicht unbegrenzte Anweisungen und Konstanten (innerhalb der Hardwareeinschränkungen Ihres Computers), verfügt über Vorlagenobjekte, um die Textursampling übersichtlicher und effizienter zu gestalten, und weist die geringsten Einschränkungen jedes Shadermodells auf. Es ist jedoch das Windows Driver Model erforderlich, das nur unter dem Betriebssystem Windows Vista (oder höher) verfügbar ist.

## <a name="shader-profiles"></a>Shaderprofile

Ein Shaderprofil ist das Ziel zum Kompilieren eines Shaders. In dieser Tabelle sind die Shaderprofile aufgeführt, die von den einzelnen Shadermodellen unterstützt werden.



| Shadermodell                                                   | Shaderprofile                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Shadermodell 1](dx-graphics-hlsl-sm1.md)         | Vs \_ 1 \_ 1                                                                                                                                                                                                                                                                                              |
| [Shadermodell 2](dx-graphics-hlsl-sm2.md)         | ps \_ 2 \_ 0, ps \_ 2 \_ x, vs \_ 2 \_ 0, vs \_ 2 \_ x, ps \_ 4 \_ 0 \_ level \_ 9 \_ 0, ps \_ 4 \_ 0 level \_ \_ 9 \_ 1, ps \_ 4 \_ 0 level \_ \_ 9 \_ 3, vs \_ 4 \_ 0 level \_ \_ 9 \_ 0, vs \_ 4 \_ 0 level \_ \_ 9 \_ 1, vs \_ 4 \_ 0 level \_ \_ 9 \_ 3, lib \_ 4 \_ 0 level \_ \_ 9 \_ 1, lib \_ 4 \_ 0 level \_ \_ 9 \_ 3                                                                      |
| [Shadermodell 3](dx-graphics-hlsl-sm3.md)         | ps \_ 3 \_ 0, vs \_ 3 \_ 0                                                                                                                                                                                                                                                                                    |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)         | cs \_ 4 \_ 0, gs \_ 4 \_ 0, ps \_ 4 \_ 0, vs \_ 4 \_ 0, cs \_ 4 \_ 1, gs \_ 4 \_ 1, ps \_ 4 \_ 1, vs \_ 4 \_ 1, lib \_ 4 \_ 0, lib \_ 4 \_ 1                                                                                                                                                                                                  |
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) | cs \_ 5 \_ 0, ds \_ 5 \_ 0, gs \_ 5 \_ 0, hs \_ 5 \_ 0, ps \_ 5 \_ 0, vs \_ 5 \_ 0, lib \_ 5 \_ 0 (obwohl gs \_ 4 \_ 0, gs \_ 4 \_ 1, ps \_ 4 \_ 0, ps \_ 4 \_ 1, vs \_ 4 \_ 0 und vs \_ 4 \_ 1 im Shadermodell 4.0 eingeführt wurden, fügt Shadermodell 5 diesen Shaderprofilen Unterstützung für strukturierte Puffer und Byteadresspuffer hinzu.)<br/> |
| [Shadermodell 6](shader-model-6-0.md)             | cs \_ 6 \_ 0, ds \_ 6 \_ 0, gs \_ 6 \_ 0, hs \_ 6 \_ 0, ps \_ 6 \_ 0, vs \_ 6 \_ 0, lib \_ 6 \_ 0                                                                                                                                                                                                                                 |

Unterschiede zwischen Direct3D 9 und Direct3D 10:

- Mit Direct3D 9 wurden die Shadermodelle 1, 2 und 3 eingeführt.
- Direct3D 10 hat Shadermodell 4 eingeführt.
- Mit Direct3D 10.1 wurde das Shadermodell 4.1 eingeführt.



 

## <a name="effect-profiles"></a>Effektprofile

Ein Effektprofil ist das Ziel zum Kompilieren eines Effekts/Shaders. In dieser Tabelle sind die Effektprofile aufgeführt, die von jeder Version von Direct3D unterstützt werden.

Unterschiede zwischen Direct3D 9 und Direct3D 10:

- Direct3D 9 hat effect-framework profiles fx \_ 1 \_ 0 und fx \_ 2 \_ 0 eingeführt.
- Direct3D 10 hat effect-framework profile fx \_ 4 \_ 0 eingeführt.
- Direct3D 10.1 hat effect-framework profile fx \_ 4 \_ 1 eingeführt.
- Direct3D 11 hat effect-framework profile fx \_ 5 \_ 0 eingeführt.

> [!Note]  
> Diese Legacyeffektprofile sind veraltet.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz für HLSL](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 





