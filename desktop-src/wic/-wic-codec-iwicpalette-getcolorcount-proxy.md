---
description: Proxyfunktion für die GetColorCount-Methode.
ms.assetid: 2ad87383-4d30-4df0-b43a-95fdad1d59f9
title: IWICPalette_GetColorCount_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetColorCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 18d06760c696bb3e95dc638bea31d02228a108b9866e213013243ad4eeec441e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206329"
---
# <a name="iwicpalette_getcolorcount_proxy-function"></a>IWICPalette \_ \_ GetColorCount-Proxyfunktion

Proxyfunktion für die [**GetColorCount-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolorcount)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICPalette_GetColorCount_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _Out_ UINT        *pcCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*THIS \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***

Zeiger auf dieses [**IWICPalette-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)

</dd> <dt>

*pcCount* \[ out\]
</dt> <dd>

Typ: **UINT \***

Zeiger, der die Anzahl der Farben in der Farbtabelle empfängt.

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



 

 




