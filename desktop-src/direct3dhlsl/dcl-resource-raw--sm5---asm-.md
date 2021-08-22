---
title: dcl_resource raw (sm5 – asm)
description: Deklarieren Sie eine Shaderressourceneingabe, und weisen Sie sie einem t\-Platzhalterregister für die Ressource zu. | dcl_resource raw (sm5 – asm)
ms.assetid: ECBA9DAB-F217-47FB-9588-F35866004E72
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b228ccc8bba795e700135bfe9ba54ea311536745b7e12eea03a8963d16e73285
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793085"
---
# <a name="dcl_resource-raw-sm5---asm"></a>dcl \_ resource raw (sm5 – asm)

Deklarieren Sie eine Shaderressourceneingabe, und weisen Sie sie einem t zu– \# einem Platzhalterregister für die Ressource.



| dcl \_ resource \_ raw dstSRV |
|---------------------------|



 



| Element                                                                                           | Beschreibung                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*<br/> | \[in \] A t register declared as a reference to a \# ShaderResourceView of a raw buffer.<br/> |



 

## <a name="remarks"></a>Hinweise

Der Inhalt der Struktur hat keinen Typ. -Vorgänge, die für den Arbeitsspeicher ausgeführt werden, interpretieren die Daten möglicherweise implizit als einen -Typ.

Anweisungen, die auf ein unformatiertes t \# verweisen, nehmen eine 1D-Adresse und einen 32-Bit-Wert ohne Vorzeichen an, der den Byteoffset an eine 32-Bit-ausgerichtete Position im Puffer angibt. Die Adresse muss ein Vielfaches von 4 (Bytes) sein.

An t gebundene Sichten, die als roh deklariert sind, \# müssen bei ihrer Erstellung RAW angegeben haben. Andernfalls ist das Verhalten beim Zugriff über einen Shader nicht definiert.

cs \_ 4 \_ 0 und cs \_ 4 \_ 1 unterstützen diese Anweisung.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Anweisung wird in den folgenden Shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | Ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | Nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Nein        |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





