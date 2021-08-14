---
description: Ruft den Typ des Endpunkttokens ab, z. B. ein WS-Security SAML (Security Assertion Markup Language) 1.1-Token.
ms.assetid: 1C6FFAD7-DC80-4957-96B4-FA0D954786DD
title: IUpdateEndpointAuthToken::TokenType-Methode (UpdateEndpointAuth.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenType
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: a4479adc05eba8160098bd60c349645c4e30853abc693396f18f69ec722a06d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118815291"
---
# <a name="iupdateendpointauthtokentokentype-method"></a>IUpdateEndpointAuthToken::TokenType-Methode

Ruft den Typ des Endpunkttokens ab, z. B. ein WS-Security SAML (Security Assertion Markup Language) 1.1-Token.

## <a name="syntax"></a>Syntax


```C++
HRESULT TokenType(
  [out] UpdateEndpointAuthTokenType *pTokenType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTokenType* \[ out\]
</dt> <dd>

Der Typ des Endpunkttokens.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **S \_ OK zurück,** wenn erfolgreich. Andernfalls wird ein COM- oder Windows zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional nur mit \[ SP3-Desktop-Apps\]<br/>                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000 Server nur mit \[ SP3-Desktop-Apps\]<br/>                |
| Header<br/>                   | <dl> <dt>UpdateEndpointAuth.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>UpdateEndpointAuth.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IUpdateEndpointAuthToken**](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




