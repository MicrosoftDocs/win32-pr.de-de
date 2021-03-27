---
title: FMA (corecrt \_ Math. h)
description: Gibt die multiplizierte Multiplikation mit doppelter Genauigkeit von a \ b + c zurück.
ms.assetid: C4EF2552-7388-4CA8-B78F-6B2D4C8FC5F6
keywords:
- FMA HLSL
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
ms.openlocfilehash: 287f07881a00ca53a3f1fe702cf4d95b64bf14c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391887"
---
# <a name="fma"></a>fma

Gibt die multiplizierte Multiplikation mit doppelter Genauigkeit von a \* b + c zurück.



| *ret* FMA (Double *a*, *b*, *c*); |
|----------------------------------|



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="a"></span><span id="A"></span>*ein*
</dt> <dd>

\[im \] ersten Wert in der multiplizierten Multiplikations Addition.

</dd> <dt>

<span id="b"></span><span id="B"></span>*b*
</dt> <dd>

\[im \] zweiten Wert in der Addition multiplizieren multiplizieren.

</dd> <dt>

<span id="c"></span><span id="C"></span>*scher*
</dt> <dd>

\[im \] dritten Wert in der Addition multiplizieren multiplizieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Multiplikation mit doppelter Genauigkeit multipliziert mit den Parametern *a* \* *b*  +  *c*. Der zurückgegebene Wert muss auf 0,5 Einheiten der geringsten Genauigkeit (ULP) genau sein.

## <a name="remarks"></a>Bemerkungen

Das systeminterne **FMA** -System muss Nane, INFs und denorms unterstützen.

Um die systeminterne Funktion " **FMA** " im Shader-Code zu verwenden, müssen Sie die [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) -Methode mit [**D3D11 \_ Feature \_ D3D11- \_ Optionen**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) aufrufen, um zu überprüfen, ob das Direct3D-Gerät die [**extendeddoublesshaderinstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) -Funktions Option Die systeminterne **FMA** -Funktion erfordert einen WDDM 1,2-Anzeigetreiber, und alle WDDM 1,2-Anzeigetreiber müssen **FMA** unterstützen. Wenn Ihre APP ein renderinggerät mit [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,0 oder 11,1 erstellt und das Kompilierungs Ziel Shader-Modell 5 oder höher ist, kann der HLSL-Quellcode den systeminternen **FMA** -Code verwenden.

### <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                         |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| *ein*   | [**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix** | [**Maß**](/windows/desktop/WinProg/windows-data-types)                       | any                          |
| *b*   | identisch mit Eingabe *a*                                                                                              | [**Maß**](/windows/desktop/WinProg/windows-data-types)                       | gleiche Dimensionen wie Eingabe *a* |
| *c*   | identisch mit Eingabe *a*                                                                                              | [**Maß**](/windows/desktop/WinProg/windows-data-types)                       | gleiche Dimensionen wie Eingabe *a* |
| *TZI* | identisch mit Eingabe *a*                                                                                              | [**Maß**](/windows/desktop/WinProg/windows-data-types)                       | gleiche Dimensionen wie Eingabe *a* |



 

### <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                | Unterstützt |
|-------------------------------------------------------------|-----------|
| [Shadermodell 5 oder höher](d3d11-graphics-reference-sm5.md) | ja       |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Corecrt \_ Math. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Intrinsische Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

