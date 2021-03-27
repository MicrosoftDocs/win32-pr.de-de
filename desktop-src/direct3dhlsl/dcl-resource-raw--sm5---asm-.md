---
title: dcl_resource RAW (SM5-ASM)
description: Deklarieren Sie eine shaderressourceneingabe, und weisen Sie Sie einem t \-a-Platzhalter Register für die Ressource zu. | dcl_resource RAW (SM5-ASM)
ms.assetid: ECBA9DAB-F217-47FB-9588-F35866004E72
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd6ccc5990e34990772a072086d9e080cde67b4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219244"
---
# <a name="dcl_resource-raw-sm5---asm"></a>DCL \_ -Ressource RAW (SM5-ASM)

Deklarieren Sie eine shaderressourceneingabe, und weisen Sie Sie einem t \# -a-Platzhalter Register für die Ressource zu.



| DCL- \_ Ressource \_ RAW dstsrv |
|---------------------------|



 



| Element                                                                                           | BESCHREIBUNG                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstsrv*<br/> | \[in \] einem t- \# Register, das als Verweis auf einen shaderresourceview eines RAW-Puffers deklariert ist.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der Inhalt der-Struktur hat keinen Typ. für den Arbeitsspeicher ausgeführte Vorgänge können die Daten implizit als Typ interpretieren.

Anweisungen, die \# auf ein unformatiertes t verweisen, benötigen eine 1D-Adresse, einen 32-Bit-Wert ohne Vorzeichen, der den Byte Offset an eine 32-Bit-ausgerichtete Position im Puffer angibt. Die Adresse muss ein Vielfaches von 4 (Bytes) sein.

Für Sichten, die \# als RAW deklariert sind, muss RAW bei der Erstellung angegeben werden. andernfalls ist das Verhalten beim Zugriff über einen Shader nicht definiert.

CS \_ 4 \_ 0 und CS \_ 4 \_ 1 unterstützen diese Anweisung.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Anweisung wird in den folgenden shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shader-Modell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4,1](dx-graphics-hlsl-sm4.md)              | nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | nein        |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





