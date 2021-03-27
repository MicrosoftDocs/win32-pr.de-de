---
title: Shader-Modelle vs shaderprofile
description: Shader-Modelle vs shaderprofile
ms.assetid: 6224f05e-20b1-42ea-96fb-63dd0edb720e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 93a8d5c02662bff285c13461e8d716b03b8553b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856676"
---
# <a name="shader-models-vs-shader-profiles"></a>Shader-Modelle vs shaderprofile

Die allgemeine Schattierungs Sprache für DirectX implementiert eine Reihe von shadermodellen. Mit HLSL können Sie C-ähnliche programmierbare Shader für die Direct3D-Pipeline erstellen. Jedes Shader-Modell baut auf den Untertiteln des Modells vor, wobei mehr Funktionen mit weniger Einschränkungen implementiert werden.

Shadermodell 1 hat mit DirectX 8 begonnen und umfasst Assemblyebene und C-ähnliche Anweisungen. Dieses Modell weist viele Einschränkungen auf, die durch eine frühe programmierbare shaderhardware verursacht werden. Das Shadermodell 2 und 3 wurde in der Anzahl der Anweisungen stark erweitert, und Konstanten können verwenden. Sie sind viel leistungsfähiger als Shader-Modell 1, aber dennoch einige der vorhandenen Einschränkungen des ersten shadermodells.

Ab Windows Vista ist Shader Model 4 eine komplette Umgestaltung. Sie ermöglicht unbegrenzte Anweisungen und Konstanten (innerhalb von Hardware Einschränkungen Ihres Computers), verfügt über vorlagenbasierte Objekte, die die Textur Stichproben Bereinigung vereinfachen und effizienter sind und über die geringsten Einschränkungen jedes shadermodells verfügen. Dies erfordert jedoch die Windows-Treibermodell, die nur auf dem Betriebssystem Windows Vista (oder höher) verfügbar ist.

## <a name="shader-profiles"></a>Shaderprofile

Ein Shader-Profil ist das Ziel für die Kompilierung eines Shaders. in dieser Tabelle werden die shaderprofile aufgelistet, die von den einzelnen Shader-Modellen unterstützt werden.



|                                                    |                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Shadermodell                                       | Shaderprofile                                                                                                                                                                                                                                                                                       |
| [Shader-Modell 1](dx-graphics-hlsl-sm1.md)         | vs \_ 1 \_ 1                                                                                                                                                                                                                                                                                              |
| [Shadermodell 2](dx-graphics-hlsl-sm2.md)         | PS \_ 2 \_ 0, PS \_ 2 \_ x, vs \_ 2 \_ 0, vs \_ 2 \_ x, PS \_ 4 \_ 0 \_ Ebene \_ 9 \_ 0, PS \_ 4 \_ 0 \_ Ebene \_ 9 \_ 1, PS \_ 4 \_ 0 \_ Ebene \_ 9 \_ 3, vs \_ 4 \_ 0 \_ Ebene \_ 9 \_ 0, vs \_ 4 \_ 0 \_ Ebene \_ 9 \_ 1, vs \_ 4 \_ 0 \_ Ebene \_ 9 \_ 3, lib \_ 4 \_ 0 \_ Ebene \_ 9 \_ 1, lib \_ 4 \_ 0 \_ Ebene \_ 9 \_ 3                                                                      |
| [Shader-Modell 3](dx-graphics-hlsl-sm3.md)         | PS \_ 3 \_ 0, vs \_ 3 \_ 0                                                                                                                                                                                                                                                                                    |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)         | CS \_ 4 \_ 0, GS \_ 4 \_ 0, PS \_ 4 \_ 0, vs \_ 4 \_ 0, CS \_ 4 \_ 1, GS \_ 4 \_ 1, PS \_ 4 \_ 1, vs \_ 4 \_ 1, lib \_ 4 \_ 0, lib \_ 4 \_ 1                                                                                                                                                                                                  |
| [Shader-Modell 5](d3d11-graphics-reference-sm5.md) | CS \_ 5 \_ 0, DS \_ 5 \_ 0, GS \_ 5 \_ 0, HS \_ 5 \_ 0, PS \_ 5 \_ 0, vs \_ 5 \_ 0, lib \_ 5 \_ 0 (obwohl GS \_ 4 \_ 0, GS \_ 4 \_ 1, PS \_ 4 \_ 0, PS \_ 4 \_ 1, vs \_ 4 \_ 0 und vs \_ 4 \_ 1 im Shader-Modell 4,0 eingeführt wurden, fügt Shader Model 5 Unterstützung für diese shaderprofile für strukturierte Puffer und Byte Adress Puffer hinzu.)<br/> |
| [Shader-Modell 6](shader-model-6-0.md)             | CS \_ 6 0 \_ , DS \_ 6 \_ 0, GS \_ 6 \_ 0, HS \_ 6 \_ 0, PS \_ 6 \_ 0, vs \_ 6 \_ 0, lib \_ 6 \_ 0                                                                                                                                                                                                                                 |



 



|                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen Direct3D 9 und Direct3D 10:<br/> Direct3D 9 hat die Shader-Modelle 1, 2 und 3 eingeführt.<br/> Direct3D 10 hat Shader Model 4 eingeführt.<br/> Direct3D 10,1 hat das Shadermodell 4,1 eingeführt.<br/> |



 

## <a name="effect-profiles"></a>Effekt profile

Ein Effekt Profil ist das Ziel zum Kompilieren eines Effekts/Shader. in dieser Tabelle werden die Effekt Profile aufgelistet, die von den einzelnen Versionen von Direct3D unterstützt werden.



|                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen Direct3D 9 und Direct3D 10:<br/> Direct3D 9 hat die Auswirkung-Framework-profile FX \_ 1 \_ 0 und FX \_ 2 \_ 0 eingeführt.<br/> Direct3D 10 hat das Effect-Framework-Profil FX \_ 4 \_ 0 eingeführt.<br/> Direct3D 10,1 hat das Effect-Framework-Profil FX \_ 4 \_ 1 eingeführt.<br/> Direct3D 11 hat das Effect-Framework-Profil FX \_ 5 \_ 0 eingeführt.<br/> |



 

> [!Note]  
> Diese Legacy Effekt Profile sind veraltet.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verweis für HLSL](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 





