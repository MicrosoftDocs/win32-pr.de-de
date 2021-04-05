---
description: Ruft den Schlüssel ab, der zum Verschlüsseln der ausgehenden Nachrichten verwendet wird, die vom Token geschützt werden.
ms.assetid: 1ADBDFC8-E4D9-440B-B310-913213086283
title: 'Iupdateendpointauthtoken:: SigningKey-Methode (updateendpointauth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.SigningKey
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: ae9847eb698bfcf0402a550ecb54705c4b3f3a52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041785"
---
# <a name="iupdateendpointauthtokensigningkey-method"></a>Iupdateendpointauthtoken:: SigningKey-Methode

Ruft den Schlüssel ab, der zum Verschlüsseln der ausgehenden Nachrichten verwendet wird, die vom Token geschützt werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT SigningKey(
  [in, out, unique] BYTE  *pbKey,
  [in, out]         ULONG *pcbKeySize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbkey* \[ in, out\]
</dt> <dd>

Schlüssel, der zum Verschlüsseln der ausgehenden Nachricht verwendet wird.

</dd> <dt>

*pcbkeysize* \[ in, out\]
</dt> <dd>

Größe des Schlüssels, auf den durch den *pbkey* -Parameter verwiesen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg **S \_ OK** zurück. Andernfalls wird ein com-oder Windows-Fehlercode zurückgegeben.

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

 

 




