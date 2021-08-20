---
description: Proxyfunktion für die GetColors-Methode.
ms.assetid: 31590de3-f35c-4253-9a80-2f59c795bf3f
title: IWICPalette_GetColors_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetColors_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fca361a2e7385b4e3fb0757e28d25472ac84bc3fd4bb8d028406c51514ef9da7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118033546"
---
# <a name="iwicpalette_getcolors_proxy-function"></a>IWICPalette \_ \_ GetColors-Proxyfunktion

Proxyfunktion für die [**GetColors-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolors)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICPalette_GetColors_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _In_  UINT        colorCount,
  _Out_ WICColor    *pColors,
  _Out_ UINT        *pcActualColors
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*THIS \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***

Zeiger auf dieses [**IWICPalette-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)

</dd> <dt>

*colorCount* \[ In\]
</dt> <dd>

Typ: **UINT**

Die Größe des *pColors-Arrays.*

</dd> <dt>

*pColors* \[ out\]
</dt> <dd>

Typ: **WICColor \***

Zeiger, der die Farben der Palette empfängt.

</dd> <dt>

*pcActualColors* \[ out\]
</dt> <dd>

Typ: **UINT \***

Die tatsächliche Größe, die zum Abrufen der Palettenfarben erforderlich ist.

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



 

 




