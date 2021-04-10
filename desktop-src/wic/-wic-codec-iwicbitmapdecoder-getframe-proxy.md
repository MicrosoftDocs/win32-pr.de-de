---
description: Proxy Funktion für die GetFrame-Methode.
ms.assetid: 31612afa-5017-4ddb-bdf8-25555db35da5
title: IWICBitmapDecoder_GetFrame_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetFrame_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 996c0f412aafe6063e25a346552f9c257a51eed7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343228"
---
# <a name="iwicbitmapdecoder_getframe_proxy-function"></a>IWICBitmapDecoder \_ GetFrame- \_ Proxy Funktion

Proxy Funktion für die [**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICBitmapDecoder_GetFrame_Proxy(
  _In_  IWICBitmapDecoder     *THIS_PTR,
  _In_  UINT                  index,
  _Out_ IWICBitmapFrameDecode **ppIBitmapFrame
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dies \_ PTR* \[ in\]
</dt> <dd>

Typ: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _

Zeiger auf dieses [_ *IWICBitmapDecoder* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) -Objekt.

</dd> <dt>

*Index* \[ in\]
</dt> <dd>

Typ: **uint**

Der jeweilige Frame, der abgerufen werden soll.

</dd> <dt>

*ppibitmapframe* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\*\***

Ein Zeiger, der einen Zeiger auf [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)empfängt.

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



 

 




