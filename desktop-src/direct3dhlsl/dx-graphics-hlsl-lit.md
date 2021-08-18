---
title: Beleuchtet
description: Gibt einen Beleuchtungskoeffizientenvektor zurück.
ms.assetid: 6ae116df-41b7-42f1-96cb-da480a7c1bab
keywords:
- lit HLSL
topic_type:
- apiref
api_name:
- lit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d3f941fe3aad52f352f5a36d3642141b31e08ef00c25dd8687c8fc7a8ed2de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118791625"
---
# <a name="lit"></a>Beleuchtet

Gibt einen Beleuchtungskoeffizientenvektor zurück.



| *ret* lit(*n \_ dot \_ l*, *n \_ dot \_ h*, *m*) |
|------------------------------------------|



 

Diese Funktion gibt einen Beleuchtungskoeffizientenvektor (ambient, diffuse, specular, 1) zurück, wobei:

-   ambient = 1
-   diffuse = n · l < 0 ? 0 : n · L
-   specular = n · l < 0 \| \| n · h < 0 ? 0 : (n · h) ^ m

Wobei der Vektor n der normale Vektor ist, ist l die Richtung zum Licht und h der halbe Vektor.

## <a name="parameters"></a>Parameter



| Element                                                                       | BESCHREIBUNG                                                                              |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="n_dot_l"></span><span id="N_DOT_L"></span>*n \_ Punkt \_ l*<br/> | \[in \] Das Punktprodukt der normalisierten Oberflächennorm und des Lichtvektors.<br/> |
| <span id="n_dot_h"></span><span id="N_DOT_H"></span>*n \_ punkt \_ h*<br/> | \[in \] Das Punktprodukt des Halbwinkelvektors und der Oberflächennorm normal.<br/>       |
| <span id="m"></span><span id="M"></span>*M*<br/>                     | \[in \] einem Glanzlicht exponenten.<br/>                                                   |



 

## <a name="return-value"></a>Rückgabewert

Der Beleuchtungskoeffizientenvektor.

## <a name="type-description"></a>Typbeschreibung



| Name        | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size |
|-------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *n \_ Punkt \_ l* | [**Skalare**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *n \_ punkt \_ h* | [**Skalare**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *m*         | [**Skalare**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *Ret*       | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt           |
|------------------------------------------------------------------------------------|---------------------|
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shadermodelle | Ja                 |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | ja (im Vergleich \_ \_ zu nur 1 1) |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

