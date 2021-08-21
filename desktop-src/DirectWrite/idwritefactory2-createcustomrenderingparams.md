---
title: IDWriteFactory2 CreateCustomRenderingParams-Methode
description: Erstellt ein Renderingparameterobjekt mit den angegebenen Eigenschaften.
ms.assetid: 947d50fd-888c-2f0b-25c2-b19b0e6fad58
keywords:
- CreateCustomRenderingParams-Methode – Direkter Schreibzugriff
- CreateCustomRenderingParams-Methode Direct Write, IDWriteFactory2-Schnittstelle
- IDWriteFactory2-Schnittstelle Direct Write , CreateCustomRenderingParams-Methode
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
ms.openlocfilehash: 2e85057c28e1ad969fe72711c86aab9657126c760ea3041a08bc5101877686a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071691"
---
# <a name="idwritefactory2createcustomrenderingparams-method"></a>IDWriteFactory2::CreateCustomRenderingParams-Methode

Erstellt ein Renderingparameterobjekt mit den angegebenen Eigenschaften.

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

*Gamma* 
</dt> <dd>

Typ: **FLOAT**

Der für die Gammakorrektur verwendete Gammawert, der größer als 0 (null) sein muss und 256 nicht überschreiten darf.

</dd> <dt>

*enhancedContrast* 
</dt> <dd>

Typ: **FLOAT**

Die Kontrasterweiterung 0 (null) oder größer.

</dd> <dt>

*grayscaleEnhancedContrast* 
</dt> <dd>

Typ: **FLOAT**

Die Kontrasterweiterung 0 (null) oder größer.

</dd> <dt>

*clearTypeLevel* 
</dt> <dd>

Typ: **FLOAT**

Der Grad der ClearType-Ebene von 0,0f (kein ClearType) bis 1,0f (vollständiger ClearType).

</dd> <dt>

*pixelGeometry* 
</dt> <dd>

Typ: **[ **DWRITE \_ PIXEL \_ GEOMETRY**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry)**

Die Geometrie eines Gerätepixels.

</dd> <dt>

*renderingMode* 
</dt> <dd>

Typ: **[ **DWRITE-RENDERINGMODUS \_ \_**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)**

Methode zum Rendern von Glyphen. In den meisten Fällen sollte dies DWRITE \_ RENDERING \_ MODE DEFAULT \_ sein, damit automatisch ein entsprechender Modus verwendet wird.

</dd> <dt>

*gridFitMode* 
</dt> <dd>

Typ: **[ **DWRITE \_ GRID \_ FIT \_ MODE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**

Gitternetz-Anpassungs-Glyphengliederungen. In den meisten Fällen sollte dies DWRITE GRID FIT DEFAULT sein, \_ um automatisch einen geeigneten Modus zu \_ \_ wählen.

</dd> <dt>

*renderingParams* \[ out\]
</dt> <dd>

Typ: **[ **IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2)\*\***

Enthält das neu erstellte Renderingparameterobjekt oder NULL bei einem Fehler.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Desktop-Apps \| UWP-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[R2-Desktop-Apps \| UWP-Apps\]<br/>                          |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 und Windows Runtime-Apps\]<br/> |
| Bibliothek<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDWriteFactory2**](idwritefactory2.md)
</dt> </dl>

 

