---
description: Initialisiert eine IWICColorTransform mit einer IWICBitmapSource und transformiert sie von einem IWICColorContext in einen anderen.
ms.assetid: 68C8EF36-DFFF-4FF3-BD9A-583508F9C2B1
title: IWICColorTransform_Initialize_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICColorTransform_Initialize_Proxy
api_type:
- DllExport
api_location:
- WindowsCodecsExt.dll
ms.openlocfilehash: fcfe124d03e9ad41edb49554613bc18b2cd15818b3f52db7ca368e27f5c4fcc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119841370"
---
# <a name="iwiccolortransform_initialize_proxy-function"></a>IWICColorTransform Initialize \_ \_ Proxy-Funktion

Initialisiert eine [**IWICColorTransform mit**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) [**einer IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) und transformiert sie [**von einem IWICColorContext in**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) einen anderen.

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICColorTransform_Initialize_Proxy(
  _In_ IWICColorTransform    *pIColorTransform,
  _In_ IWICBitmapSource      *pIBitmapSource,
  _In_ IWICColorContext      *pIContextSource,
  _In_ IWICColorContext      *pIContextDest,
  _In_ REFWICPixelFormatGUID pixelFmtDest
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pIColorTransform* \[ In\]
</dt> <dd>

Typ: **[ **IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)\***

Die zu initialisierende Farbtransformation.

</dd> <dt>

*pIBitmapSource* \[ In\]
</dt> <dd>

Typ: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

Die Bitmapquelle, die zum Initialisieren der Farbtransformation verwendet wird.

</dd> <dt>

*pIContextSource* \[ In\]
</dt> <dd>

Typ: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***

Die Farbkontextquelle.

</dd> <dt>

*pIContextDest* \[ In\]
</dt> <dd>

Typ: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***

Das Farbkontextziel.

</dd> <dt>

*pixelFmtDest* \[ In\]
</dt> <dd>

Typ: **REFWICPixelFormatGUID**

Die GUID des gewünschten Pixelformats.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>WindowsCodecsExt.dll</dt> </dl> |



 

 




