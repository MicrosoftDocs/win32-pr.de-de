---
title: IDWriteFactory2 CreateGlyphRunAnalysis-Methode
description: Erstellt ein Glyphenlaufanalyseobjekt, das Informationen kapselt, die zum Rendern einer Glyphenlauf verwendet werden.
ms.assetid: 13cecfbf-8bb6-88a2-c8b2-3243f6cb92fd
keywords:
- CreateGlyphRunAnalysis-Methode Direct Write
- CreateGlyphRunAnalysis-Methode Direct Write , IDWriteFactory2-Schnittstelle
- IDWriteFactory2-Schnittstelle Direct Write , CreateGlyphRunAnalysis-Methode
topic_type:
- apiref
api_name:
- IDWriteFactory2.CreateGlyphRunAnalysis
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4ea5c2dc4cb97b1b9ba02e786efc20a4e2a44990b9a1d28b862aeab254079a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048830"
---
# <a name="idwritefactory2createglyphrunanalysis-method"></a>IDWriteFactory2::CreateGlyphRunAnalysis-Methode

Erstellt ein Glyphenlaufanalyseobjekt, das Informationen kapselt, die zum Rendern einer Glyphenlauf verwendet werden.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT CreateGlyphRunAnalysis(
  [in]           const DWRITE_GLYPH_RUN           *glyphRun,
  [in, optional] const DWRITE_MATRIX              *transform,
                       DWRITE_RENDERING_MODE      renderingMode,
                       DWRITE_MEASURING_MODE      measuringMode,
                       DWRITE_GRID_FIT_MODE       gridFitMode,
                       DWRITE_TEXT_ANTIALIAS_MODE antialiasMode,
                       FLOAT                      baselineOriginX,
                       FLOAT                      baselineOriginY,
  [out]                IDWriteGlyphRunAnalysis    **glyphRunAnalysis
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*glyphRun* \[ In\]
</dt> <dd>

Typ: **const [**DWRITE \_ GLYPH \_ RUN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) \***

Struktur, die die Eigenschaften der Glyphen-Ausführung angibt.

</dd> <dt>

*transformieren* \[ in, optional\]
</dt> <dd>

Typ: **const [**DWRITE \_ MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***

Optionale Transformation, die auf die Glyphen und ihre Positionen angewendet wird. Diese Transformation wird nach der durch emSize und pixelsPerDip angegebenen Skalierung angewendet.

</dd> <dt>

*renderingMode* 
</dt> <dd>

Typ: **\_ DWRITE-RENDERINGMODUS \_**

Gibt den Renderingmodus an, bei dem es sich um einen der Rasterrenderingmodi (d. h. nicht standard und not outline) sein muss.

</dd> <dt>

*measuringMode* 
</dt> <dd>

Typ: **[ **DWRITE-MESSMODUS \_ \_**](/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode)**

Gibt die Methode zum Messen von Glyphen an.

</dd> <dt>

*gridFitMode* 
</dt> <dd>

Typ: **[ **DWRITE \_ GRID \_ FIT \_ MODE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**

Vorgehensweise zum Anpassen von Glyphengliederungen mit Rastern. Dies muss nicht standardmäßig sein.

</dd> <dt>

*antialiasMode* 
</dt> <dd>

Typ: **[ **DWRITE \_ TEXT \_ ANTIALIAS \_ MODE**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode)**

Gibt den Antialiasmodus an.

</dd> <dt>

*baselineOriginX* 
</dt> <dd>

Typ: **FLOAT**

Horizontale Position des Baselineursprungs in DIPs.

</dd> <dt>

*baselineOriginY* 
</dt> <dd>

Typ: **FLOAT**

Vertikale Position des Baselineursprungs in DIPs.

</dd> <dt>

*glyphRunAnalysis* \[ out\]
</dt> <dd>

Typ: **[ **IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis)\*\***

Empfängt einen Zeiger auf das neu erstellte Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 \|Desktop-Apps UWP-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[R2-Desktop-Apps \| UWP-Apps\]<br/>                          |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1- und Windows Runtime-Apps\]<br/> |
| Bibliothek<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDWriteFactory2**](idwritefactory2.md)
</dt> </dl>

 

