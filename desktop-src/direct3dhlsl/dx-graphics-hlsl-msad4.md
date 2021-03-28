---
title: msad4
description: Vergleicht einen 4-Byte-Verweiswert und einen 8-Byte-Quellwert und sammelt einen Vektor von 4 Summen. Jede Summe entspricht der maskierten Summe absoluter Unterschiede einer anderen Byte Ausrichtung zwischen dem Verweis Wert und dem Quellwert.
ms.assetid: 6497F9AE-4524-44C2-A1C6-2A4ACB30FA9C
keywords:
- msad4 HLSL
topic_type:
- apiref
api_name:
- msad4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 552db3afd07677777b47e939d659c0f6e333e496
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104976968"
---
# <a name="msad4"></a>msad4

Vergleicht einen 4-Byte-Verweiswert und einen 8-Byte-Quellwert und sammelt einen Vektor von 4 Summen. Jede Summe entspricht der maskierten Summe absoluter Unterschiede einer anderen Byte Ausrichtung zwischen dem Verweis Wert und dem Quellwert.



| uint4 result = msad4 (uint-Referenz, uint2 Source, uint4 Accum); |
|------------------------------------------------------------------|



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="reference"></span><span id="REFERENCE"></span>*Angabe*
</dt> <dd>

\[im \] Verweis Array von 4 Bytes in einem **uint** -Wert.

</dd> <dt>

<span id="source"></span><span id="SOURCE"></span>*Ausgangs*
</dt> <dd>

\[im \] Quell Array von 8 Bytes in zwei **uint2** -Werten.

</dd> <dt>

<span id="accum"></span><span id="ACCUM"></span>*Accum*
</dt> <dd>

\[in \] einem Vektor von 4 Werten. **msad4** fügt diesen Vektor der maskierten Summe absoluter Unterschiede der verschiedenen Byte Ausrichtungen zwischen dem Verweis Wert und dem Quellwert hinzu.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein Vektor von 4 Summen. Jede Summe entspricht der maskierten Summe von absoluten Differenzen von verschiedenen Byteausrichtungen zwischen Verweiswert und Quellwert. **msad4** enthält keinen Unterschied in der Summe, wenn dieser Unterschied maskiert ist (d. h., das Verweis Byte ist 0).

## <a name="remarks"></a>Bemerkungen

Um die intrinsische **msad4** -Funktion im Shader-Code zu verwenden, müssen Sie die [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) -Methode mit [**D3D11 \_ Feature \_ D3D11- \_ Optionen**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) aufrufen, um zu überprüfen, ob das Direct3D-Gerät die Funktion [**SAD4ShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) unterstützt Die systeminterne **msad4** -Funktion erfordert einen WDDM 1,2-Anzeigetreiber, und alle WDDM 1,2-Anzeigetreiber müssen **msad4** unterstützen. Wenn Ihre APP ein renderinggerät mit [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,0 oder 11,1 erstellt und das Kompilierungs Ziel Shader-Modell 5 oder höher ist, kann der HLSL-Quellcode die systeminterne Funktion **msad4** verwenden.

Rückgabewerte sind nur bis zu 65535-Werte genau. Wenn Sie die systeminterne Funktion **msad4** mit Eingaben aufzurufen, die zu Rückgabe Werten größer als 65535 führen können, erzeugt **msad4** nicht definierte Ergebnisse.

### <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                | Unterstützt |
|-------------------------------------------------------------|-----------|
| [Shadermodell 5 oder höher](d3d11-graphics-reference-sm5.md) | ja       |



 

## <a name="examples"></a>Beispiele

Im folgenden finden Sie eine Beispiel Ergebnisberechnung für **msad4**:


```
reference = 0xA100B2C3;
source.x = 0xD7B0C372
source.y = 0x4F57C2A3
accum = {1,2,3,4}
result.x alignment source: 0xD7B0C372
result.x = accum.x + |0xD7   0xA1| + 0 (masked) + |0xC3   0xB2| + |0x72   0xC3| = 1 + 54 + 0 + 17 + 81 = 153
result.y alignment source: 0xA3D7B0C3
result.y = accum.y + |0xA3   0xA1| + 0 (masked) + |0xB0   0xB2| + |0xC3   0xC3| = 2 + 2 + 0 + 2 + 0 = 6
result.z alignment source: 0xC2A3D7B0
result.z = accum.z + |0xC2   0xA1| + 0 (masked) + |0xD7   0xB2| + |0xB0   0xC3| = 3 + 33 + 0 + 37 + 19 = 92
result.w alignment source: 0x57C2A3D7
result.w = accum.w + |0x57   0xA1| + 0 (masked) + |0xA3   0xB2| + |0xD7   0xC3| = 4 + 74 + 0 + 15 + 20 = 113
result = {153,6,92,113}
```



Im folgenden finden Sie ein Beispiel dafür, wie Sie **msad4** verwenden können, um in einem Puffer nach einem Verweis Muster zu suchen:


```
uint4 accum = {0,0,0,0};
for(uint i=0;i<REF_SIZE;i++)
    accum = msad4(
        buf_ref[i], 
        uint2(buf_src[DTid.x+i], buf_src[DTid.x+i+1]), 
        accum);
buf_accum[DTid.x] = accum;
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Intrinsische Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

