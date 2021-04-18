---
description: Initialisiert eine iwiccolortransform mit einer IWICBitmapSource und wandelt sie von einem IWICColorContext in einen anderen um.
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
ms.openlocfilehash: 29d29bfd925d979897b22711c748083b94673142
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364673"
---
# <a name="iwiccolortransform_initialize_proxy-function"></a>Iwiccolortransform- \_ \_ Proxy Funktion initialisieren

Initialisiert eine [**iwiccolortransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) mit einer [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) und wandelt sie von einem [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) in einen anderen um.

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

*picolortransform* \[ in\]
</dt> <dd>

Typ: **[ **iwiccolortransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)\***

Die Farb Transformation, die initialisiert werden soll.

</dd> <dt>

*pibitmapsource* \[ in\]
</dt> <dd>

Typ: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

Die Bitmapquelle, die zum Initialisieren der Farb Transformation verwendet wird.

</dd> <dt>

*picontextsource* \[ in\]
</dt> <dd>

Typ: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***

Die Farb Kontext Quelle.

</dd> <dt>

*picontextdest* \[ in\]
</dt> <dd>

Typ: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***

Das Farb Kontext Ziel.

</dd> <dt>

*pixelfmtdest* \[ in\]
</dt> <dd>

Typ: **reberwicpixelformatguid**

Die GUID des gewünschten Pixel Formats.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>WindowsCodecsExt.dll</dt> </dl> |



 

 




