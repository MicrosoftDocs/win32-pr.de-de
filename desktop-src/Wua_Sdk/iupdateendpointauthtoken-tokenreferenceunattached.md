---
description: Ruft das XML-Format eines nicht angefügten Verweises auf das Token ab.
ms.assetid: D5D61ED7-68FB-4FC0-9C2A-90D3B1219351
title: 'Iupdateendpointauthtoken:: tokenreferenceunattached-Methode (updateendpointauth. h)'
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
ms.openlocfilehash: 7f9a25c444cf1ba8421d3787a9ead242750e5756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343325"
---
# <a name="iupdateendpointauthtokentokenreferenceunattached-method"></a>Iupdateendpointauthtoken:: tokenreferenceunattached-Methode

Ruft das XML-Format eines nicht angefügten Verweises auf das Token ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT TokenReferenceUnattached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psztokenreference* \[ vorgenommen\]
</dt> <dd>

Zeiger auf den nicht angefügten Tokenverweis.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg **S \_ OK** zurück. Andernfalls wird ein com-oder Windows-Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Ein nicht angefügter Verweis verweist auf eine referenece (z. b. das Zeichen, das das Token verwendet), das nicht in der Nachricht, in der sich das Token befindet, befindet.

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

 

 




