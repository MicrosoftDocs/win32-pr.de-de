---
title: dcl_resource strukturiert (SM5-ASM)
description: Deklarieren Sie eine shaderressourceneingabe, und weisen Sie Sie einem t \-a-Platzhalter Register für die Ressource zu. | dcl_resource strukturiert (SM5-ASM)
ms.assetid: 87FC8A56-9DB2-424B-889C-2AB59885DA13
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ab993e0cb260529c3419210c33f5d735a625bce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219181"
---
# <a name="dcl_resource-structured-sm5---asm"></a>strukturierte DCL \_ -Ressource (SM5-ASM)

Deklarieren Sie eine shaderressourceneingabe, und weisen Sie Sie einem t \# -a-Platzhalter Register für die Ressource zu.



| DCL- \_ Ressource \_ strukturiert dstsrv, structbytestride |
|----------------------------------------------------|



 



| Element                                                                                                                                   | BESCHREIBUNG                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstsrv*<br/>                                         | \[in \] einem t-Register, das \# als Verweis auf einen shaderresourceview eines strukturierten Puffers mit dem angegebenen Schritt deklariert wurde, der an den SRV-Slot \# an der API gebunden werden muss. <br/> |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structbytestride*<br/> | \[in \] einem uint, das die Größe der-Struktur in Bytes in dem deklarierten Puffer angibt. Dieser Wert muss größer als 0 sein.<br/>                                   |



 

## <a name="remarks"></a>Bemerkungen

Der Inhalt der-Struktur hat keinen Typ. für den Arbeitsspeicher ausgeführte Vorgänge können die Daten implizit als Typ interpretieren.

Anweisungen, die auf eine strukturierte t verweisen \# , benötigen eine 2D-Adresse, bei der die erste Komponente \[ struct \] auswählt und die zweite Komponente \[ Offset innerhalb von Struktur, mehrere von 32 Bits, auswählt \] .

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

 

 





