---
description: Proxyfunktion für die GetSpecVersion-Methode.
ms.assetid: 363e55c2-d6e8-4ddc-a063-c5be08232a67
title: IWICComponentInfo_GetSpecVersion_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetSpecVersion_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a29b57e84b7cf9ceee67ac4f64ac090e697366fbe0698a891c8fbcc87e3ff5b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206583"
---
# <a name="iwiccomponentinfo_getspecversion_proxy-function"></a>IWICComponentInfo \_ \_ GetSpecVersion-Proxyfunktion

Proxyfunktion für die [**GetSpecVersion-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getspecversion)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICComponentInfo_GetSpecVersion_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchSpecVersion,
  _Inout_ WCHAR             *wzSpecVersion,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*THIS \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\***

Zeiger auf dieses [**IWICComponentInfo-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)

</dd> <dt>

*cchSpecVersion* \[ In\]
</dt> <dd>

Typ: **UINT**

Die Größe des *wzSpecVersion-Puffers.*

</dd> <dt>

*wzSpecVersion* \[ in, out\]
</dt> <dd>

Typ: **WCHAR \***

Wenn diese Methode zurückgegeben wird, enthalten Sie eine kulturinvariante Zeichenfolge der Spezifikationsversion der Komponente. Das Versionsformular ist NN.NN.NN.NN.

</dd> <dt>

*pcchActual* \[ out\]
</dt> <dd>

Typ: **UINT \***

Ein Zeiger, der die tatsächliche Länge der Spezifikationsversion der Komponente empfängt.

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



 

 




