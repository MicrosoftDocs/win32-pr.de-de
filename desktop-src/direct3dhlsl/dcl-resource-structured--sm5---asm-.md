---
title: dcl_resource strukturiert (sm5 - asm)
description: Deklarieren Sie eine Shaderressourceneingabe, und weisen Sie sie einem t\-Platzhalterregister für die Ressource zu. | dcl_resource strukturiert (sm5 - asm)
ms.assetid: 87FC8A56-9DB2-424B-889C-2AB59885DA13
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79ec0bc0b818b345c62bb48ae6f5db68671127110ed06a85c988f8a0449fd490
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118285893"
---
# <a name="dcl_resource-structured-sm5---asm"></a>dcl \_ resource structured (sm5 - asm)

Deklarieren Sie eine Shaderressourceneingabe, und weisen Sie sie einem t \# -Platzhalterregister für die Ressource zu.



| dcl \_ resource \_ structured dstSRV, structByteStride |
|----------------------------------------------------|



 



| Element                                                                                                                                   | Beschreibung                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*<br/>                                         | \[in \] A t register declared as a reference to a ShaderResourceView of a structured buffer with the specified stride that must be bound \# to SRV slot at the \# API. <br/> |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*<br/> | \[in \] Ein uint, der die Größe der Struktur in Bytes im deklarierten Puffer angibt. Dieser Wert muss größer als 0 sein.<br/>                                   |



 

## <a name="remarks"></a>Hinweise

Der Inhalt der -Struktur hat keinen Typ. Vorgänge, die für den Arbeitsspeicher ausgeführt werden, interpretieren die Daten möglicherweise implizit so, als ob sie einen Typ haben.

Anweisungen, die auf ein strukturiertes t verweisen, nehmen eine 2D-Adresse an, wobei die erste Komponente die Struktur auswählt, und die zweite Komponente den Offset innerhalb der Struktur, das Vielfache von \# \[ \] \[ 32 \] Bits.

cs \_ 4 \_ 0 und cs \_ 4 \_ 1 unterstützen diese Anweisung.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Anweisung wird in den folgenden Shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | nein        |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





