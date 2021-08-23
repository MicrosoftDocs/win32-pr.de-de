---
description: Proxyfunktion für die GetFriendlyName-Methode.
ms.assetid: 8ac8f954-c2b9-47a2-88fe-b56710b5630c
title: IWICComponentInfo_GetFriendlyName_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetFriendlyName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 5af41c00945550fc9e833b9324e22f522aa7a5e73dacd109d76159d5dd0173db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965249"
---
# <a name="iwiccomponentinfo_getfriendlyname_proxy-function"></a>IWICComponentInfo \_ GetFriendlyName-Proxyfunktion \_

Proxyfunktion für die [**GetFriendlyName-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getfriendlyname)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICComponentInfo_GetFriendlyName_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchFriendlyName,
  _Inout_ WCHAR             *wzFriendlyName,
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

*cchFriendlyName* \[ In\]
</dt> <dd>

Typ: **UINT**

Die Größe des *wzFriendlyName-Puffers.*

</dd> <dt>

*wzFriendlyName* \[ in, out\]
</dt> <dd>

Typ: **WCHAR \***

Ein Zeiger, der den Benutzerfreundlichen Namen der Komponente empfängt.

Die zurückgegebene Zeichenfolge ist locale-spezifisch und standardmäßig 1033.

</dd> <dt>

*pcchActual* \[ out\]
</dt> <dd>

Typ: **UINT \***

Ein Zeiger, der die tatsächliche Länge des Benutzerfreundlichnamens der Komponente empfängt.

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



 

 




