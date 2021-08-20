---
description: Proxyfunktion für die GetCLSID-Methode.
ms.assetid: c6a8d752-590f-43d6-bac8-72b5bd259ad0
title: IWICComponentInfo_GetCLSID_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetCLSID_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a50fe02c96991e592f8195599b02dfadc2fea65335162a1133be22096239d81a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117668413"
---
# <a name="iwiccomponentinfo_getclsid_proxy-function"></a>IWICComponentInfo \_ \_ GetCLSID-Proxyfunktion

Proxyfunktion für die [**GetCLSID-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getclsid)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICComponentInfo_GetCLSID_Proxy(
  _In_  IWICComponentInfo *THIS_PTR,
  _Out_ CLSID             *pclsid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*THIS \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\***

Zeiger auf dieses [**IWICComponentInfo-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)

</dd> <dt>

*pclsid* \[ out\]
</dt> <dd>

Typ: **CLSID \***

Ein Zeiger, der die CLSID der Komponente empfängt.

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



 

 




