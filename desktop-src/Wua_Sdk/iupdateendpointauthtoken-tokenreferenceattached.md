---
description: Ruft das XML-Format eines angefügten Verweises auf das Token ab.
ms.assetid: F4329A2E-61FD-40E0-9E24-87C9A4585E55
title: 'Iupdateendpointauthtoken:: tokenreferenceattached-Methode (updateendpointauth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenReferenceAttached
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 9582c54c42e2416d5d7a98e85eba3151fd6769a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350462"
---
# <a name="iupdateendpointauthtokentokenreferenceattached-method"></a>Iupdateendpointauthtoken:: tokenreferenceattached-Methode

Ruft das XML-Format eines angefügten Verweises auf das Token ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT TokenReferenceAttached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psztokenreference* \[ vorgenommen\]
</dt> <dd>

Zeiger auf den Verweis auf ein angefügtes Token.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg **S \_ OK** zurück. Andernfalls wird ein com-oder Windows-Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Ein angefügter Verweis verweist auf eine referenece (z. b. das Zeichen, das das Token verwendet), das sich in derselben Nachricht befindet, in der sich das Token befindet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]<br/>                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]<br/>                |
| Header<br/>                   | <dl> <dt>Updateendpointauth. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Updateendpointauth. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Updateendpointauth. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iupdateendpointauthtoken**](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




