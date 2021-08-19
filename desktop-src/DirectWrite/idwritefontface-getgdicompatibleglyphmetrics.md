---
title: IDWriteFontFace GetGdiCompatibleGlyphMetrics-Methode
description: Abrufen von Glyphenmetriken in Schriftentwurfseinheiten mit den Rückgabewerten, die mit dem von GDI erzeugten Wert kompatibel sind.
ms.assetid: 7bda3916-6db3-4f56-b18c-288506c0b646
keywords:
- GetGdiCompatibleGlyphMetrics-Methode – Direkter Schreibzugriff
- GetGdiCompatibleGlyphMetrics-Methode Direct Write, IDWriteFontFace-Schnittstelle
- IDWriteFontFace-Schnittstelle Direct Write , GetGdiCompatibleGlyphMetrics-Methode
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
ms.openlocfilehash: bd36fc09ff8161ba8fb72d3b55b9351b0a7d2a6bd3f3f11a71c15a8d9422f6c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816500"
---
# <a name="idwritefontfacegetgdicompatibleglyphmetrics-method"></a>IDWriteFontFace::GetGdiCompatibleGlyphMetrics-Methode

Abrufen von Glyphenmetriken in Schriftentwurfseinheiten mit den Rückgabewerten, die mit dem von GDI erzeugten Wert kompatibel sind.

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

Typ: **FLOAT**

Der ogische Schriftgrad der Schriftart in DIP-Einheiten.

</dd> <dt>

*pixelsPerDip* 
</dt> <dd>

Typ: **FLOAT**

Die Anzahl der physischen Pixel pro DIP.

</dd> <dt>

*transformieren* \[ in, optional\]
</dt> <dd>

Typ: **const [**DWRITE \_ MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***

Eine optionale Transformation, die auf die Glyphen und ihre Positionen angewendet wird. Diese Transformation wird nach der Skalierung angewendet, die durch den Schriftgrad und *pixelsPerDip angegeben wird.*

</dd> <dt>

*useGdiNatural* 
</dt> <dd>

Typ: **BOOL**

Wenn false festgelegt **ist,** sind die Metriken mit den Metriken des GDI-Aliastexts identisch. Wenn diese Eigenschaft **auf TRUE** festgelegt ist, sind die Metriken identisch mit den Metriken von Text, der von GDI mithilfe einer Schriftart gemessen wird, die mit **CLEARTYPE NATURAL QUALITY erstellt \_ \_ wurde.**

</dd> <dt>

*glyphIndices* \[ In\]
</dt> <dd>

Typ: **const UINT16 \***

Ein Array von Glyphenindizes, für die die Metriken berechnet werden.

</dd> <dt>

*glyphCount* 
</dt> <dd>

Typ: **UINT32**

Die Anzahl der Elemente im *glyphIndices-Array.*

</dd> <dt>

*glyphMetrics* \[ out\]
</dt> <dd>

Typ: **[ **METRIKEN \_ DES DWRITE-GLYPHEN \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics)\***

Ein Array von [**\_ DWRITE-GLYPH-METRIKstrukturen, \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) die von dieser Funktion gefüllt werden. Die Metriken befinden sich in Schriftentwurfseinheiten.

</dd> <dt>

*isSideways* 
</dt> <dd>

Typ: **BOOL**

Ein BOOL-Wert, der angibt, ob die Schriftart in einer seitwärts ausgeführten Ausführung verwendet wird. Dies kann sich auf die Glyphenmetriken auswirken, wenn die Schriftart über eine schräge Simulation verfügt, da sich die schräge Simulation seitwärts von der nicht seitlichen schrägen Simulation unterscheidet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

HRESULT-Standardfehlercode.  Wenn einer der Eingabe-Glyphenindizes außerhalb des gültigen Glyphenindexbereichs für das aktuelle Schriftartgesicht liegt, wird **E \_ INVALIDARG** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 

