---
description: Proxy Funktion für die Initialize-Methode.
ms.assetid: 60925f5c-aca4-4f49-96d2-9b58d8310e3c
title: IWICBitmapClipper_Initialize_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapClipper_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 83c41b8802546b36ad309306ecc83a34c5d3a0c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128968"
---
# <a name="iwicbitmapclipper_initialize_proxy-function"></a>Iwicbitmapclipperinitialize- \_ \_ Proxy Funktion

Proxy Funktion für die [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICBitmapClipper_Initialize_Proxy(
  _In_       IWICBitmapClipper *THIS_PTR,
  _In_       IWICBitmapSource  *pISource,
  _In_ const WICRect           *prc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dies \_ PTR* \[ in\]
</dt> <dd>

Typ: **[**iwicbitmapclipper_**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) \**

Zeiger auf dieses [_ *iwicbitmapclipperobjekt* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) .

</dd> <dt>

*pisource* \[ in\]
</dt> <dd>

Typ: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _

Die Eingabe Bitmap-Quelle.

</dd> <dt>

_prc * \[ in\]
</dt> <dd>

Typ: * Konstante *[**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _

Das Rechteck der zu Clip enden Bitmap-Quelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




