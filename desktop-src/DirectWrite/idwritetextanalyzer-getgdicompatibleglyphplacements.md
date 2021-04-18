---
title: Idwrite Test Textanalyzer getgdicompatibleglyphplacement-Methode
description: Platzieren Sie die Glyphen-Ausgabe der getglyphs-Methode gemäß der Schriftart und den Renderingregeln des Schreibsystems.
ms.assetid: 49312b03-9ee9-44ef-b3eb-a35631a6e693
keywords:
- Getgdicompatibleglyphplacement-Methode direkt Schreibvorgang
- Getgdicompatibleglyphplacement-Methode Direct Write, idwrite tetextanalyzer-Schnittstelle
- Idwrite tetextanalyzer-Schnittstelle Direct Write, getgdicompatibleglyphplacement-Methode
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
ms.openlocfilehash: f548e5fd20ce8814dc59657ff7bb422387c959fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364594"
---
# <a name="idwritetextanalyzergetgdicompatibleglyphplacements-method"></a>Idwrite Test Textanalyzer:: getgdicompatibleglyphplacement-Methode

Platzieren Sie die Glyphen-Ausgabe der [**getglyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs) -Methode gemäß der Schriftart und den Renderingregeln des Schreibsystems.

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

*Textstring* \[ in\]
</dt> <dd>

Typ: Konstante **WCHAR \***

Ein Array von Zeichen, das die Original Zeichenfolge enthält, aus der die Symbole stammen.

</dd> <dt>

*ClusterMap* \[ in\]
</dt> <dd>

Typ: **Konstanten UInt16 \***

Ein Zeiger auf die Zuordnung von Zeichen Bereichen zu Symbol Bereichen. Dies wird von " [**getglyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)" zurückgegeben.

</dd> <dt>

*Texteigenschaften* \[ in\]
</dt> <dd>

Type: **[ **dwrite-Strukturierungs \_ Text- \_ \_ Eigenschaften**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties)\***

Ein Zeiger auf ein Array von-Strukturen, das Strukturierungs Eigenschaften für jedes Zeichen enthält. Diese Struktur wird von " [**getglyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)" zurückgegeben.

</dd> <dt>

*TextLength* 
</dt> <dd>

Typ: **UInt32**

Die Textlänge von *Textstring*.

</dd> <dt>

*GlyphIndices* \[ in\]
</dt> <dd>

Typ: **Konstanten UInt16 \***

Ein Array von Glyphe-Indizes, die von [**getglyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)zurückgegeben werden.

</dd> <dt>

*Glyph-* \[ Eigenschaften in\]
</dt> <dd>

Typ: Konstante **[**dwrite- \_ Formen \_ Glyphe- \_ Eigenschaften**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties) \***

Ein Zeiger auf ein Array von-Strukturen, die für jedes Symbol, das von [**getglyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)zurückgegeben wird, Strukturierungs Eigenschaften enthalten.

</dd> <dt>

*GlyphCount* 
</dt> <dd>

Typ: **UInt32**

Die Anzahl von Symbolen, die von [**getglyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)zurückgegeben werden.

</dd> <dt>

*fontface* \[ in\]
</dt> <dd>

Typ: **[ **idschreitefontface**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)\***

Ein Zeiger auf die Schriftart, bei der es sich um die Quelle für die Ausgabe Symbole handelt.

</dd> <dt>

*fontemsize* 
</dt> <dd>

Typ: **float**

Die logische Schriftgröße in Dips.

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

 *issientways* 
</dt> <dd>

Typ: **bool**

Ein boolesches Flag, das auf **true** festgelegt ist, wenn der Text vertikal gezeichnet werden soll.

</dd> <dt>

 *IsRightToLeft* 
</dt> <dd>

Typ: **bool**

Ein boolesches Flag, das für Text von rechts nach links auf **true** festgelegt ist.

</dd> <dt>

 *scriptanalysis* \[ in\]
</dt> <dd>

Typ: Konstante **[**dwrite- \_ Skript \_ Analyse**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) \***

Ein Zeiger auf ein Skript Analyseergebnis eines [**AnalyzeScript**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript) -Aufrufes.

</dd> <dt>

 *localename* \[ in, optional\]
</dt> <dd>

Typ: Konstante **WCHAR \***

Ein Array von Zeichen, das das zu verwendende Gebiets Schema enthält, wenn Symbole ausgewählt werden. Beispielsweise kann das gleiche Zeichen anderen Symbolen für ja-JP und zh-CHS zugeordnet werden. Wenn dieser Wert **null** ist, wird die auf dem Skript basierende Standard Zuordnung verwendet.

</dd> <dt>

 *Features* \[ in, optional\]
</dt> <dd>

Typ: Konstante **[**dwrite- \_ Typografiefunktionen \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features) \* \***

Ein Array von Zeigern auf die Sätze von typografischen Features, die in jedem Featurebereich verwendet werden sollen.

</dd> <dt>

 *featurerangelengths* \[ in, optional\]
</dt> <dd>

Typ: **Konstanten UInt32 \***

Die Länge der einzelnen Funktionsbereiche in Zeichen. Die Summe aller Längen muss gleich " *TextLength*" sein.

</dd> <dt>

 *featureranges* 
</dt> <dd>

Typ: **UInt32**

Die Anzahl von Funktionsbereichen.

</dd> <dt>

 *glyphadvanzen* \[ vorgenommen\]
</dt> <dd>

Typ: **float \***

Wenn diese Methode zurückgegeben wird, enthält Sie die voraus Breite jedes Symbols.

</dd> <dt>

 *Glyphosat-ffsets* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **dwrite- \_ Glyphe \_ Offset**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset)\***

Wenn diese Methode zurückgegeben wird, enthält Sie den Offset des Ursprungs der einzelnen Glyphe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>Dwrite. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Idschreitetextanalyzer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer)
</dt> </dl>

 

