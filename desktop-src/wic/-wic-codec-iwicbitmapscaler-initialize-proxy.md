---
description: Proxy Funktion für die Initialize-Methode.
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
ms.openlocfilehash: cc317adc831b0cf0759580d5c6924fb3f0997524
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369102"
---
# <a name="iwicbitmapscaler_initialize_proxy-function"></a>IWICBitmapScaler \_ Initialize \_ Proxy-Funktion

Proxy Funktion für die [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapscaler-initialize) -Methode.

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

*Dies \_ PTR* \[ in\]
</dt> <dd>

Typ: **[**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) \** _

Zeiger auf dieses [_ *IWICBitmapScaler* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) -Objekt.

</dd> <dt>

*pisource* \[ in\]
</dt> <dd>

Typ: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _

Die Eingabe Bitmap-Quelle.

</dd> <dt>

_uiWidth * \[ in\]
</dt> <dd>

Typ: **uint**

Die Ziel Breite.

</dd> <dt>

*uiheight* \[ in\]
</dt> <dd>

Typ: **uint**

Die Höhe der Größe.

</dd> <dt>

*Modus* \[ in\]
</dt> <dd>

Typ: **[ **wicbitmapinterpolationmode**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)**

Der Interpolations Modus, der bei der Skalierung verwendet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




