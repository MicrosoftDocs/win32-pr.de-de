---
description: Ruft das XML-Format eines nicht angefügten Verweises auf das Token ab.
ms.assetid: D5D61ED7-68FB-4FC0-9C2A-90D3B1219351
title: IUpdateEndpointAuthToken::TokenReferenceUnattached-Methode (UpdateEndpointAuth.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenReferenceUnattached
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 2dada627d6e2b8832f4317c47e54a9c4417e14b821f6cd84bce44d9f53c99aaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049248"
---
# <a name="iupdateendpointauthtokentokenreferenceunattached-method"></a>IUpdateEndpointAuthToken::TokenReferenceUnattached-Methode

Ruft das XML-Format eines nicht angefügten Verweises auf das Token ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT TokenReferenceUnattached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszTokenReference* \[ out\]
</dt> <dd>

Zeiger auf den Nicht angefügten Tokenverweis.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg **S \_ OK** zurück. Andernfalls wird ein COM- oder Windows Fehlercode zurückgegeben.

## <a name="remarks"></a>Hinweise

Ein nicht angefügter Verweis verweist auf einen Verweis (z. B. die Signierung, die das Token verwendet), die sich nicht in der Nachricht befindet, in der sich das Token befindet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional nur mit \[ SP3-Desktop-Apps\]<br/>                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000 Server nur mit \[ SP3-Desktop-Apps\]<br/>                |
| Header<br/>                   | <dl> <dt>UpdateEndpointAuth.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>UpdateEndpointAuth.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IUpdateEndpointAuthToken**](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




