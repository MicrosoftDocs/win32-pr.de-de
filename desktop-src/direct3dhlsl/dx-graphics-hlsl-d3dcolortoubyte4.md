---
title: D3DCOLORtoUBYTE4
description: Konvertiert einen gleitkommabasierten 4D-Vektor, der von einer D3DCOLOR-Datei festgelegt wird, in ein UBYTE4-Format.
ms.assetid: 20a7be00-1e36-41c3-bc98-933b3faa8f35
keywords:
- D3DCOLORtoUBYTE4 HLSL
topic_type:
- apiref
api_name:
- D3DCOLORtoUBYTE4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cea438b8c305c7ff76b6f9795c9f2c869a0f262f70e670d2e34c5b882de7c9c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789800"
---
# <a name="d3dcolortoubyte4"></a>D3DCOLORtoUBYTE4

Konvertiert einen gleitkommabasierten 4D-Vektor, der von einer D3DCOLOR-Datei festgelegt wird, in ein UBYTE4-Format.



| *ret* D3DCOLORtoUBYTE4(*x*) |
|-----------------------------|



 

Diese Funktion wischt und skaliert Komponenten des *x-Parameters.* Verwenden Sie diese Funktion, um die fehlende UBYTE4-Unterstützung in einigen Hardwarekomponenten zu kompensieren.

## <a name="parameters"></a>Parameter



| Element                                                   | Beschreibung                                              |
|--------------------------------------------------------|----------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Der zu konvertierende Gleitkommavektor4.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Die UBYTE4-Darstellung  des x-Parameters.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *x*   | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| *Ret* | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**Ganzzahl**](/windows/desktop/WinProg/windows-data-types)                      | 4    |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt |
|------------------------------------------------------------------------------------|-----------|
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shadermodelle | Ja       |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Vs \_ 1 \_ 1  |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

