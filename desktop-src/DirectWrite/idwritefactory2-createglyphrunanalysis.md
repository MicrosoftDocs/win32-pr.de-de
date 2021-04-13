---
title: IDWriteFactory2-Methode "comateglyphrunanalysis"
description: Erstellt ein Symbol zum Ausführen von Symbolen, das Informationen kapselt, die zum renderischen Ausführen von Symbolen verwendet werden.
ms.assetid: 13cecfbf-8bb6-88a2-c8b2-3243f6cb92fd
keywords:
- Methode "comateglyphrunanalysis" direkt schreiben
- Methode "IDWriteFactory2" der Methode "" der Methode ""
- IDWriteFactory2 Interface Direct Write, Methode "kreateglyphrunanalysis"
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
ms.openlocfilehash: abd944c45fc271a22a0942556038073ebcc591cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392046"
---
# <a name="idwritefactory2createglyphrunanalysis-method"></a>IDWriteFactory2:: kreateglyphrunanalysis-Methode

Erstellt ein Symbol zum Ausführen von Symbolen, das Informationen kapselt, die zum renderischen Ausführen von Symbolen verwendet werden.

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

*GlyphRun* \[ in\]
</dt> <dd>

Typ: * Konstante *[**dwrite- \_ Glyphe \_ Ausführen**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) \** _

-Struktur, die die Eigenschaften der Symbol Führung angibt.

</dd> <dt>

_transform * \[ in, optional\]
</dt> <dd>

Typ: * Konstante *[**dwrite- \_ Matrix**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \** _

Optionale Transformation, die auf die Symbole und deren Positionen angewendet wird. Diese Transformation wird nach der durch "emSize" und "pixelsperdip" angegebenen Skalierung angewendet.

</dd> <dt>

_renderingMode * 
</dt> <dd>

Typ: **dwrite- \_ Renderingmodus \_**

Gibt den Renderingmodus an, bei dem es sich um einen der Raster Renderingmodi handeln muss (d. h. nicht default und Not Umriss).

</dd> <dt>

*measuringmode* 
</dt> <dd>

Typ: **[ **dwrite \_ - \_ Messmodus**](/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode)**

Gibt die Methode an, mit der Symbole gemessen werden.

</dd> <dt>

*gridfitmode* 
</dt> <dd>

Type: **[ **dwrite \_ Grid \_ fit \_ Mode**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**

Gewusst wie: Symbole mit Rasteranpassung. Dies darf nicht der Standardwert sein.

</dd> <dt>

*antialiasmode* 
</dt> <dd>

Type: **[ **dwrite \_ Text \_ Antialias \_ Mode**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode)**

Gibt den AntiAlias Modus an.

</dd> <dt>

*baselineoriginx* 
</dt> <dd>

Typ: **float**

Die horizontale Position des Basis Linien Ursprungs in Dips.

</dd> <dt>

*baselineoriginy* 
</dt> <dd>

Typ: **float**

Vertikale Position des Basis Linien Ursprungs in Dips.

</dd> <dt>

*glyphrunanalysis* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **idschreiteglyphrunanalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis)\*\***

Empfängt einen Zeiger auf das neu erstellte-Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps \| UWP-apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                          |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]<br/> |
| Bibliothek<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDWriteFactory2**](idwritefactory2.md)
</dt> </dl>

 

