---
description: Proxy Funktion für die getcolorkontexte-Methode.
ms.assetid: 1925a64e-558d-4931-a3c3-b35d2b92a292
title: IWICBitmapFrameDecode_GetColorContexts_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameDecode_GetColorContexts_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8e22166e98e4ef276a6bf1d72dfc860cf8fb511e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214546"
---
# <a name="iwicbitmapframedecode_getcolorcontexts_proxy-function"></a>IWICBitmapFrameDecode \_ getcolorkontexte- \_ Proxy Funktion

Proxy Funktion für die [**getcolorkontexte**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICBitmapFrameDecode_GetColorContexts_Proxy(
  _In_    IWICBitmapFrameDecode *THIS_PTR,
  _In_    UINT                  cCount,
  _Inout_ IWICColorContext      **ppIColorContexts,
  _Out_   UINT                  *pcActualCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dies \_ PTR* \[ in\]
</dt> <dd>

Typ: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _

Zeiger auf dieses [_ *IWICBitmapFrameDecode* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) -Objekt.

</dd> <dt>

*ccount* \[ in\]
</dt> <dd>

Typ: **uint**

Die Anzahl der abzurufenden Farb Kontexte.

Dieser Wert muss die Größe von (oder kleiner als) sein, die für *ppicolorkontexte* verfügbar ist.

</dd> <dt>

*ppicolorkontexte* \[ in, out\]
</dt> <dd>

Typ: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***

Ein Zeiger, der einen Zeiger auf die [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) -Objekte empfängt.

</dd> <dt>

*pcActualCount* \[ vorgenommen\]
</dt> <dd>

Typ: **uint \** _

Ein Zeiger, der die Anzahl der Farb Kontexte im Bild Rahmen empfängt.

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



 

 




