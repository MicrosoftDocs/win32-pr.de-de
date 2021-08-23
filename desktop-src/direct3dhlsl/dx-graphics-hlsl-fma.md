---
title: fma (Corecrt \_ math.h)
description: Gibt das fused-Additionszeichen mit doppelter Genauigkeit von a \ b + c zurück.
ms.assetid: C4EF2552-7388-4CA8-B78F-6B2D4C8FC5F6
keywords:
- fma HLSL
topic_type:
- apiref
api_name:
- fma
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2b9a6932a1b0f0f8f1f7bc674920162def49e556c8d5b757547d4837caa60b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120204"
---
# <a name="fma"></a>fma

Gibt das fused-Additionszeichen b + c mit doppelter Genauigkeit \* zurück.



| *ret* fma(double *a*, *b*, *c*); |
|----------------------------------|



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="a"></span><span id="A"></span>*Eine*
</dt> <dd>

\[in \] Der erste Wert in der fused-Multiplikationshinzufügung.

</dd> <dt>

<span id="b"></span><span id="B"></span>*B*
</dt> <dd>

\[in \] Der zweite Wert in der fused-Multiplikationshinzufügung.

</dd> <dt>

<span id="c"></span><span id="C"></span>*C*
</dt> <dd>

\[in \] Der dritte Wert in der fused-Multiplikationshinzufügung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die fused-Multiplikation von Parametern *mit* doppelter Genauigkeit a \* *b*  +  *c*. Der zurückgegebene Wert muss auf 0,5 Einheiten der geringsten Genauigkeit (ULP) genau sein.

## <a name="remarks"></a>Hinweise

Die **systeminterne fma-Eigenschaft** muss NaNs, INFs und Denorms unterstützen.

Um die systeminterne **fma-Funktion** in Ihrem Shadercode zu verwenden, rufen Sie die [**ID3D11Device::CheckFeatureSupport-Methode**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) mit [**D3D11 \_ FEATURE \_ D3D11 \_ OPTIONS**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) auf, um zu überprüfen, ob das Direct3D-Gerät die Featureoption [**ExtendedDoublesShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) unterstützt. Die **systeminterne fma-Datei** erfordert einen WDDM 1.2-Anzeigetreiber, und alle WDDM 1.2-Anzeigetreiber müssen **fma** unterstützen. Wenn Ihre App ein Renderinggerät mit [der Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11.0 oder 11.1 erstellt und das Kompilierungsziel das Shadermodell 5 oder höher ist, kann der HLSL-Quellcode die systeminterne **fma-Funktion** verwenden.

### <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                         |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| *Eine*   | [**Skalar,**](dx-graphics-hlsl-intrinsic-functions.md) **Vektor** oder **Matrix** | [**Doppel**](/windows/desktop/WinProg/windows-data-types)                       | any                          |
| *b*   | entspricht der Eingabe *eines*                                                                                              | [**Doppel**](/windows/desktop/WinProg/windows-data-types)                       | die gleichen Dimensionen wie die Eingabe *eines* |
| *c*   | entspricht der Eingabe *eines*                                                                                              | [**Doppel**](/windows/desktop/WinProg/windows-data-types)                       | die gleichen Dimensionen wie die Eingabe *eines* |
| *Ret* | entspricht der Eingabe *eines*                                                                                              | [**Doppel**](/windows/desktop/WinProg/windows-data-types)                       | die gleichen Dimensionen wie die Eingabe *eines* |



 

### <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                | Unterstützt |
|-------------------------------------------------------------|-----------|
| [Shadermodell 5 oder höher](d3d11-graphics-reference-sm5.md) | Ja       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 \|Desktop-Apps UWP-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 \|Desktop-Apps UWP-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Corecrt \_ math.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Systeminterne Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

