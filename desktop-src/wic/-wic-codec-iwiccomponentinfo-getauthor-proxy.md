---
description: Proxyfunktion für die GetAuthor-Methode.
ms.assetid: fb76009e-cc01-4dec-9403-04bf6b53db80
title: IWICComponentInfo_GetAuthor_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetAuthor_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c83d42f499c8f821f5b342f08749a2167aac9cc61334fe2fc2d9e9134b5e2b49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206671"
---
# <a name="iwiccomponentinfo_getauthor_proxy-function"></a>IWICComponentInfo-GetAuthor-Proxyfunktion \_ \_

Proxyfunktion für die [**GetAuthor-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getauthor)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICComponentInfo_GetAuthor_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchAuthor,
  _Inout_ WCHAR             *wzAuthor,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DIES \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\***

Zeiger auf dieses [**IWICComponentInfo-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)

</dd> <dt>

*cchAuthor* \[ In\]
</dt> <dd>

Typ: **UINT**

Die Größe des *wzAuthor-Puffers.*

</dd> <dt>

*wzAuthor* \[ in, out\]
</dt> <dd>

Typ: **WCHAR \***

Ein Zeiger, der den Namen des Autors der Komponente empfängt.

Die zurückgegebene Zeichenfolge ist gebietsschemaspezifisch, standardmäßig 1033.

</dd> <dt>

*pcchActual* \[ out\]
</dt> <dd>

Typ: **UINT \***

Ein Zeiger, der die tatsächliche Länge des Autorennamens der Komponente empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ausgeführt wird, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows NUR XP mit SP2, Windows \[ Vista-Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




