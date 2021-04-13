---
title: IDWriteFactory2-Methode für die Methode "samatecustomrenderingpara"
description: Erstellt ein Renderparameter-Objekt mit den angegebenen Eigenschaften.
ms.assetid: 947d50fd-888c-2f0b-25c2-b19b0e6fad58
keywords:
- Methode der Methode "kreatecustomrenderingparser" direkt schreiben
- Methode "samatecustomrenderingparser" Direct Write, IDWriteFactory2 Interface
- IDWriteFactory2 Interface Direct Write, Methode "kreatecustomrenderingparameams"
topic_type:
- apiref
api_name:
- IDWriteFactory2.CreateCustomRenderingParams
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bd69cde6858061b69b8143dcdd0560342e65f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392047"
---
# <a name="idwritefactory2createcustomrenderingparams-method"></a>IDWriteFactory2:: kreatecustomrenderingparameams-Methode

Erstellt ein Renderparameter-Objekt mit den angegebenen Eigenschaften.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT CreateCustomRenderingParams(
        FLOAT                   gamma,
        FLOAT                   enhancedContrast,
        FLOAT                   grayscaleEnhancedContrast,
        FLOAT                   clearTypeLevel,
        DWRITE_PIXEL_GEOMETRY   pixelGeometry,
        DWRITE_RENDERING_MODE   renderingMode,
        DWRITE_GRID_FIT_MODE    gridFitMode,
  [out] IDWriteRenderingParams2 **renderingParams
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*GAM* 
</dt> <dd>

Typ: **float**

Der für die Gammakorrektur verwendete Gamma Wert, der größer als 0 (null) sein muss und 256 nicht überschreiten darf.

</dd> <dt>

*enhancedcontrast* 
</dt> <dd>

Typ: **float**

Die Menge der Kontrastverbesserung, 0 (null) oder größer.

</dd> <dt>

*grayscaleenhancedcontrast* 
</dt> <dd>

Typ: **float**

Die Menge der Kontrastverbesserung, 0 (null) oder größer.

</dd> <dt>

*ClearTypeLevel* 
</dt> <dd>

Typ: **float**

Der Grad der ClearType-Ebene von 0,0 f (kein ClearType) bis 1.0 f (Full ClearType).

</dd> <dt>

*Pixel Geometry* 
</dt> <dd>

Type: **[ **dwrite \_ Pixel \_ Geometry**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry)**

Die Geometrie eines Geräte Pixels.

</dd> <dt>

*renderingmode* 
</dt> <dd>

Typ: **[ **dwrite \_ - \_ Renderingmodus**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)**

Methode zum Rendern von Symbolen. In den meisten Fällen sollte dies der dwrite- \_ Renderingmodus sein, damit \_ \_ automatisch ein entsprechender Modus verwendet wird.

</dd> <dt>

*gridfitmode* 
</dt> <dd>

Type: **[ **dwrite \_ Grid \_ fit \_ Mode**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**

Gewusst wie: Raster an Symbole anpassen. In den meisten Fällen sollte dies der Standardwert \_ für die Einstellung "dwrite Grid" lauten \_ \_ , um automatisch einen geeigneten Modus auszuwählen.

</dd> <dt>

*renderingparametriams* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2)\*\***

Enthält das neu erstellte Renderparameter-Objekt oder NULL bei einem Fehler.

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

 

