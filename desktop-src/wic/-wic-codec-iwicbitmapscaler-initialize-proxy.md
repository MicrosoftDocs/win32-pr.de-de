---
description: 'IWICBitmapScaler_Initialize_Proxy-Funktion: Proxyfunktion für die Initialize-Methode.'
ms.assetid: 47a717d2-9aac-4230-bdb3-093212eb5448
title: IWICBitmapScaler_Initialize_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapScaler_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: be9fee37147ff3fcadf1ea13f566aab3d34faf00d7a3c7f126af7b401d7af538
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965319"
---
# <a name="iwicbitmapscaler_initialize_proxy-function"></a>IWICBitmapScaler Initialize \_ \_ Proxy-Funktion

Proxyfunktion für die [**Initialize-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapscaler-initialize)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICBitmapScaler_Initialize_Proxy(
  _In_ IWICBitmapScaler           *THIS_PTR,
  _In_ IWICBitmapSource           *pISource,
  _In_ UINT                       uiWidth,
  _In_ UINT                       uiHeight,
  _In_ WICBitmapInterpolationMode mode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*THIS \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\***

Zeiger auf dieses [**IWICBitmapScaler-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)

</dd> <dt>

*pISource* \[ In\]
</dt> <dd>

Typ: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

Die Eingabebitmapquelle.

</dd> <dt>

*uiWidth* \[ In\]
</dt> <dd>

Typ: **UINT**

Die Zielbreite.

</dd> <dt>

*uiHeight* \[ In\]
</dt> <dd>

Typ: **UINT**

Die Desinationshöhe.

</dd> <dt>

*-Modus* \[ In\]
</dt> <dd>

Typ: **[ **WICBitmapInterpolationMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)**

Der Interpolationsmodus, der beim Skalieren verwendet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




