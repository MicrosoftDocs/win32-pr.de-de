---
description: Proxyfunktion für die GetMimeTypes-Methode.
ms.assetid: 9d05624f-da08-4475-933b-faa12bec9012
title: IWICBitmapCodecInfo_GetMimeTypes_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetMimeTypes_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fc579283b35ed7d112f17aa639be592d70f304cb83930d1219e976655f0b13c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772440"
---
# <a name="iwicbitmapcodecinfo_getmimetypes_proxy-function"></a>IWICBitmapCodecInfo \_ GetMimeTypes-Proxyfunktion \_

Proxyfunktion für die [**GetMimeTypes-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getmimetypes)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICBitmapCodecInfo_GetMimeTypes_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _In_  UINT                cchMimeTypes,
  _Out_ WCHAR               *wzMimeTypes,
  _Out_ UINT                *pcchActual
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*THIS \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\***

Zeiger auf dieses [**IWICBitmapCodecInfo-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)

</dd> <dt>

*cchMimeTypes* \[ In\]
</dt> <dd>

Typ: **UINT**

Die Größe des Puffers der MIME-Typen.

</dd> <dt>

*wzMimeTypes* \[ out\]
</dt> <dd>

Typ: **WCHAR \***

Ein Zeiger, der die mime-Typen empfängt, die dem Codec zugeordnet sind.

</dd> <dt>

*pcchActual* \[ out\]
</dt> <dd>

Typ: **UINT \***

Die tatsächliche Puffergröße, die zum Abrufen aller mime-Typen erforderlich ist, die dem Codec zugeordnet sind.

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



 

 




