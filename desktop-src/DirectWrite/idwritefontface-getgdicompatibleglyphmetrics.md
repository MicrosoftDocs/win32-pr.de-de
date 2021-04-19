---
title: Idwrite-fontface getgdicompatibleglyphmetrics-Methode
description: Ruft Symbol Metriken in Schriftart Entwurfs Einheiten mit den Rückgabe Werten ab, die mit den GDI-Werten kompatibel sind.
ms.assetid: 7bda3916-6db3-4f56-b18c-288506c0b646
keywords:
- Getgdicompatibleglyphmetrics-Methode direkt Schreibvorgang
- Getgdicompatibleglyphmetrics-Methode direkt schreiben, idschreitefontface-Schnittstelle
- Idwrite-fontface Interface Direct Write, getgdicompatibleglyphmetrics-Methode
topic_type:
- apiref
api_name:
- IDWriteFontFace.GetGdiCompatibleGlyphMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a949edbdad2f25d748e5af64ebe408c79c7372b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371636"
---
# <a name="idwritefontfacegetgdicompatibleglyphmetrics-method"></a>Idschreitefontface:: getgdicompatibleglyphmetrics-Methode

Ruft Symbol Metriken in Schriftart Entwurfs Einheiten mit den Rückgabe Werten ab, die mit den GDI-Werten kompatibel sind.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetGdiCompatibleGlyphMetrics(
                       FLOAT                emSize,
                       FLOAT                pixelsPerDip,
  [in, optional] const DWRITE_MATRIX        *transform,
                       BOOL                 useGdiNatural,
  [in]           const UINT16               *glyphIndices,
                       UINT32               glyphCount,
  [out]                DWRITE_GLYPH_METRICS *glyphMetrics,
                       BOOL                 isSideways = FALSE
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*emSize* 
</dt> <dd>

Typ: **float**

Die ogische Größe der Schriftart in DIP-Einheiten.

</dd> <dt>

*Pixel sperdip* 
</dt> <dd>

Typ: **float**

Die Anzahl der physischen Pixel pro DIP.

</dd> <dt>

*Transformation* \[ in, optional\]
</dt> <dd>

Typ: Konstante **[**dwrite- \_ Matrix**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***

Eine optionale Transformation, die auf die Symbole und deren Positionen angewendet wird. Diese Transformation wird nach der durch Schriftart Größe und *pixelsperdip* angegebenen Skalierung angewendet.

</dd> <dt>

*usegdinatural* 
</dt> <dd>

Typ: **bool**

Wenn diese Einstellung auf " **false**" festgelegt ist, sind die Metriken mit den Metriken des GDI-Alias Texts identisch. Wenn diese Eigenschaft auf " **true**" festgelegt ist, sind die Metriken identisch mit den Metriken von Text, der von GDI mithilfe einer mit **ClearType \_ Natural \_ Quality** erstellten Schriftart gemessen wird.

</dd> <dt>

*GlyphIndices* \[ in\]
</dt> <dd>

Typ: **Konstanten UInt16 \***

Ein Array von Symbol Indizes, für das die Metriken berechnet werden sollen.

</dd> <dt>

*GlyphCount* 
</dt> <dd>

Typ: **UInt32**

Die Anzahl der Elemente im *GlyphIndices* -Array.

</dd> <dt>

*GlyphMetrics* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **dwrite- \_ Glyphe- \_ Metriken**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics)\***

Ein Array von [**dwrite- \_ Glyphe- \_ Metriken**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) , die von dieser Funktion ausgefüllt werden. Die Metriken sind in Schriftart Entwurfs Einheiten.

</dd> <dt>

*issientways* 
</dt> <dd>

Typ: **bool**

Ein boolescher Wert, der angibt, ob die Schriftart in einer seitwärts lauflauf verwendet wird. Dies kann sich auf die Glyphe-Metriken auswirken, wenn die Schriftart über eine schräge Simulation verfügt, da sich die seitwärts schräge Simulation von der nicht-seitwärts schrägen

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Standard- **HRESULT** -Fehlercode. Wenn eine der Eingabe Symbol Indizes außerhalb des gültigen Symbol Index Bereichs für die aktuelle Schriftart liegt, wird **E \_ invalidArg** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>Dwrite. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Idschreitefontface**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[**Idschreitefontface**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 

