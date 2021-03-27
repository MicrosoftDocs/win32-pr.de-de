---
title: gezündet
description: Gibt einen Beleuchtungs Koeffizient-Vektor zurück.
ms.assetid: 6ae116df-41b7-42f1-96cb-da480a7c1bab
keywords:
- Lit HLSL
topic_type:
- apiref
api_name:
- lit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6dbf6f1e53218355ba1ee9ccf58dac6176007218
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858264"
---
# <a name="lit"></a>gezündet

Gibt einen Beleuchtungs Koeffizient-Vektor zurück.



| *ret* beleuchtet (*n \_ Punkt \_ l*, *n \_ Punkt \_ h*, *m*) |
|------------------------------------------|



 

Diese Funktion gibt einen Beleuchtungs Koeffizienten (Ambient, diffuse, Glanz, 1) zurück, wobei Folgendes gilt:

-   Ambient = 1
-   diffuses = n l < 0? 0: n int
-   Glanz = n l < 0 \| \| n = h < 0? 0: (n = h) ^ m

Wenn der Vektor n der normale Vektor ist, ist l die Richtung zu hell und h ist der halbvektor.

## <a name="parameters"></a>Parameter



| Element                                                                       | BESCHREIBUNG                                                                              |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="n_dot_l"></span><span id="N_DOT_L"></span>*n \_ Punkt \_ l*<br/> | \[im \] Punktprodukt der normalisierten Oberflächen normal und der Licht Vektor.<br/> |
| <span id="n_dot_h"></span><span id="N_DOT_H"></span>*n \_ Punkt \_ h*<br/> | \[im \] Punktprodukt des halb Winkel Vektors und der Oberflächen normalen.<br/>       |
| <span id="m"></span><span id="M"></span>*800*<br/>                     | \[in \] einem Glanz Exponenten.<br/>                                                   |



 

## <a name="return-value"></a>Rückgabewert

Der Beleuchtungs Koeffizient-Vektor.

## <a name="type-description"></a>Typbeschreibung



| Name        | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size |
|-------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *n \_ Punkt \_ l* | [**Skalar**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *n \_ Punkt \_ h* | [**Skalar**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *m*         | [**Skalar**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *TZI*       | [**ve**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt           |
|------------------------------------------------------------------------------------|---------------------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle | ja                 |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Ja ( \_ nur vs 1 \_ 1) |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

