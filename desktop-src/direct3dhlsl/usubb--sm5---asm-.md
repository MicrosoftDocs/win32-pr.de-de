---
title: usubb (SM5-ASM)
description: Ganzzahl ohne Vorzeichen subtrahieren mit Auswahl.
ms.assetid: 6D42E3CA-5A37-4194-AB42-7A2337C5AB9D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111ffd134a75b8cfe19f63597cd80655201359c4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389498"
---
# <a name="usubb-sm5---asm"></a>usubb (SM5-ASM)

Ganzzahl ohne Vorzeichen subtrahieren mit Auswahl.



| usubb dest0 \[ . mask \] , dest1 \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle\] |
|--------------------------------------------------------------------------|



 



| Element                                                               | BESCHREIBUNG                                                                                       |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="dest0"></span><span id="DEST0"></span>*dest0*<br/> | \[in \] enthält die lsab-Ergebnisse der-Anweisung.<br/>                                   |
| <span id="dest1"></span><span id="DEST1"></span>*dest1*<br/> | \[in \] der entsprechenden Komponente von *dest0* , die angibt, ob eine einleihe erstellt wurde.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>    | \[in \] dem Wert, von dem subtrahiert werden soll.<br/>                                               |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/>    | \[in \] der Menge, die von *src0* subtrahiert werden soll.<br/>                                             |



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung führt eine Komponenten Weise nicht signierte Subtraktion von 32-Bit-Operanden aus *Quelle1* von *src0*, wobei der LSB-Teil des 32-Bit-Ergebnisses in *dest0* platziert wird.

Die entsprechende Komponente in *dest1* wird mit 1 geschrieben, wenn eine Kredit Erstellung erstellt wird, andernfalls 0.

*dest1* kann NULL sein, wenn die unter Leihe nicht benötigt wird.

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

 

 





