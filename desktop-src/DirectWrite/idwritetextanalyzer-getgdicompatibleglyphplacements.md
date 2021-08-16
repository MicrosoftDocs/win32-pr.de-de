---
title: IDWriteTextAnalyzer GetGdiCompatibleGlyphPlacements-Methode
description: Platzieren Sie die Glyphenausgabe der GetGlyphs-Methode gemäß der Schriftart und den Renderingregeln des Schreibsystems.
ms.assetid: 49312b03-9ee9-44ef-b3eb-a35631a6e693
keywords:
- GetGdiCompatibleGlyphPlacements-Methode Direct Write
- GetGdiCompatibleGlyphPlacements-Methode Direct Write , IDWriteTextAnalyzer-Schnittstelle
- IDWriteTextAnalyzer-Schnittstelle Direct Write , GetGdiCompatibleGlyphPlacements-Methode
topic_type:
- apiref
api_name:
- IDWriteTextAnalyzer.GetGdiCompatibleGlyphPlacements
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d05fcf5595500f34730a720e4a4c2e80d68922929d8055b754a26a1dc92f63c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650010"
---
# <a name="idwritetextanalyzergetgdicompatibleglyphplacements-method"></a>IDWriteTextAnalyzer::GetGdiCompatibleGlyphPlacements-Methode

Platzieren Sie die Glyphenausgabe der [**GetGlyphs-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs) gemäß der Schriftart und den Renderingregeln des Schreibsystems.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetGdiCompatibleGlyphPlacements(
  [in]           const WCHAR                           *textString,
  [in]           const UINT16                          *clusterMap,
  [in]                 DWRITE_SHAPING_TEXT_PROPERTIES  *textProps,
                       UINT32                          textLength,
  [in]           const UINT16                          *glyphIndices,
  [in]           const DWRITE_SHAPING_GLYPH_PROPERTIES *glyphProps,
                       UINT32                          glyphCount,
  [in]                 IDWriteFontFace                 *fontFace,
                       FLOAT                           fontEmSize,
                       FLOAT                           pixelsPerDip,
  [in, optional] const DWRITE_MATRIX                   *transform,
                       BOOL                            useGdiNatural,
                       BOOL                             isSideways,
                       BOOL                             isRightToLeft,
  [in]           const DWRITE_SCRIPT_ANALYSIS          * scriptAnalysis,
  [in, optional] const WCHAR                           * localeName,
  [in, optional] const DWRITE_TYPOGRAPHIC_FEATURES     ** features,
  [in, optional] const UINT32                          * featureRangeLengths,
                       UINT32                           featureRanges,
  [out]                FLOAT                           * glyphAdvances,
  [out]                DWRITE_GLYPH_OFFSET             * glyphOffsets
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*textString* \[ In\]
</dt> <dd>

Typ: **const \* WCHAR**

Ein Array von Zeichen, das die ursprüngliche Zeichenfolge enthält, aus der die Glyphen stammen.

</dd> <dt>

*clusterMap* \[ In\]
</dt> <dd>

Typ: **const UINT16 \***

Ein Zeiger auf die Zuordnung von Zeichenbereichen zu Glyphenbereichen. Dies wird von [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)zurückgegeben.

</dd> <dt>

*textProps* \[ In\]
</dt> <dd>

Typ: **[ **DWRITE-STRUKTURIERUNGSTEXTEIGENSCHAFTEN \_ \_ \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties)\***

Ein Zeiger auf ein Array von -Strukturen, das Strukturierungseigenschaften für jedes Zeichen enthält. Diese Struktur wird von [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)zurückgegeben.

</dd> <dt>

*textLength* 
</dt> <dd>

Typ: **UINT32**

Die Textlänge von *textString*.

</dd> <dt>

*glyphIndices* \[ In\]
</dt> <dd>

Typ: **const UINT16 \***

Ein Array von Glyphenindizes, die von [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)zurückgegeben werden.

</dd> <dt>

*glyphProps* \[ In\]
</dt> <dd>

Typ: **const [**DWRITE \_ SHAPING \_ GLYPH \_ PROPERTIES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties) \***

Ein Zeiger auf ein Array von -Strukturen, die Strukturierungseigenschaften für jedes von [**GetGlyphs zurückgegebene Glyphen**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)enthalten.

</dd> <dt>

*glyphCount* 
</dt> <dd>

Typ: **UINT32**

Die Anzahl von Glyphen, die von [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)zurückgegeben werden.

</dd> <dt>

*fontFace* \[ In\]
</dt> <dd>

Typ: **[ **IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)\***

Ein Zeiger auf die Schriftart, die die Quelle für die Ausgabeglyphen ist.

</dd> <dt>

*fontEmSize* 
</dt> <dd>

Typ: **FLOAT**

Der logische Schriftgrad in DIPs.

</dd> <dt>

*pixelsPerDip* 
</dt> <dd>

Typ: **FLOAT**

Die Anzahl der physischen Pixel pro DIP.

</dd> <dt>

*transformieren* \[ in, optional\]
</dt> <dd>

Typ: **const [**DWRITE \_ MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***

Eine optionale Transformation, die auf die Glyphen und ihre Positionen angewendet wird. Diese Transformation wird nach der Skalierung angewendet, die durch den Schriftgrad und *pixelsPerDip* angegeben wird.

</dd> <dt>

*useGdiNatural* 
</dt> <dd>

Typ: **BOOL**

Wenn **false** festgelegt ist, sind die Metriken mit den Metriken von GDI-Aliastext identisch. Bei Festlegung auf **TRUE** sind die Metriken mit den Metriken von Text identisch, die von GDI mithilfe einer Schriftart gemessen werden, die mit **CLEARTYPE \_ NATURAL \_ QUALITY** erstellt wurde.

</dd> <dt>

 *isSideways* 
</dt> <dd>

Typ: **BOOL**

Ein boolesches Flag, das auf **TRUE** festgelegt ist, wenn der Text vertikal gezeichnet werden soll.

</dd> <dt>

 *isRightToLeft* 
</dt> <dd>

Typ: **BOOL**

Ein boolesches Flag, das für Text von rechts nach links auf **TRUE** festgelegt ist.

</dd> <dt>

 *scriptAnalysis* \[ In\]
</dt> <dd>

Typ: **const [**DWRITE \_ SCRIPT \_ ANALYSIS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) \***

Ein Zeiger auf ein Skriptanalyseergebnis aus einem [**AnalyzeScript-Aufruf.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript)

</dd> <dt>

 *localeName* \[ in, optional\]
</dt> <dd>

Typ: **const \* WCHAR**

Ein Array von Zeichen, das das Gebietsschema enthält, das beim Auswählen von Glyphen verwendet werden soll. Beispielsweise kann das gleiche Zeichen verschiedenen Glyphen für ja-jp und zh-chs zugeordnet werden. Wenn dies **NULL** ist, wird die Standardzuordnung basierend auf dem Skript verwendet.

</dd> <dt>

 *Features* \[ in, optional\]
</dt> <dd>

Typ: **const [**DWRITE \_ TYPOGRAPHIC \_ FEATURES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features) \* \***

Ein Array von Zeigern auf die Sätze typografischer Features, die in jedem Featurebereich verwendet werden sollen.

</dd> <dt>

 *featureRangeLengths* \[ in, optional\]
</dt> <dd>

Typ: **const UINT32 \***

Die Länge jedes Featurebereichs in Zeichen. Die Summe aller Längen sollte gleich *textLength* sein.

</dd> <dt>

 *featureRanges* 
</dt> <dd>

Typ: **UINT32**

Die Anzahl der Featurebereiche.

</dd> <dt>

 *glyphAdvances* \[ out\]
</dt> <dd>

Typ: **\* FLOAT**

Enthält nach der Rückgabe dieser Methode die vorgezogene Breite jedes Glyphens.

</dd> <dt>

 *glyphOffsets* \[ out\]
</dt> <dd>

Typ: **[ **DWRITE-GLYPHENOFFSET \_ \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset)\***

Enthält nach der Rückgabe dieser Methode den Offset des Ursprungs jedes Glyphens.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IDWriteTextAnalyzer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer)
</dt> </dl>

 

