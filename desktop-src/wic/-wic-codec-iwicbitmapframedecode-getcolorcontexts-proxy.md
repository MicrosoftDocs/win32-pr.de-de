---
description: 'IWICBitmapFrameDecode_GetColorContexts_Proxy-Funktion: Proxyfunktion für die GetColorContexts-Methode.'
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
ms.openlocfilehash: 99fb6caa9b9e654be0adc1235cad0e79a7fa1ef3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100578"
---
# <a name="iwicbitmapframedecode_getcolorcontexts_proxy-function"></a>IWICBitmapFrameDecode \_ \_ GetColorContexts-Proxyfunktion

Proxyfunktion für die [**GetColorContexts-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts)

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

*THIS \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***

Zeiger auf dieses [**IWICBitmapFrameDecode-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)

</dd> <dt>

*cCount* \[ In\]
</dt> <dd>

Typ: **UINT**

Die Anzahl der abzurufenden Farbkontexte.

Dieser Wert muss die Größe von oder kleiner als die größe sein, die *ppIColorContexts zur Verfügung steht.*

</dd> <dt>

*ppIColorContexts* \[ in, out\]
</dt> <dd>

Typ: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***

Ein Zeiger, der einen Zeiger auf die [**IWICColorContext-Objekte**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) empfängt.

</dd> <dt>

*pcActualCount* \[ out\]
</dt> <dd>

Typ: **UINT \***

Ein Zeiger, der die Anzahl von Farbkontexten empfängt, die im Bildrahmen enthalten sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




