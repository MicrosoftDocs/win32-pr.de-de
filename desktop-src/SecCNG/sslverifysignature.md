---
description: Überprüft die angegebene Signatur mithilfe des angegebenen Hashs und des öffentlichen Schlüssels.
ms.assetid: fa274851-15f2-4be0-9e2f-4cdced36daff
title: SslVerifySignature-Funktion (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslVerifySignature
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: b020f41822185dfc9e4e2513fc9e299bc35d9bbb258aaeddf6f1e1e8ea7b8cf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905659"
---
# <a name="sslverifysignature-function"></a>SslVerifySignature-Funktion

Die **SslVerifySignature-Funktion** überprüft die angegebene Signatur mithilfe des angegebenen [*Hashs*](/windows/desktop/SecGloss/h-gly) und des [*öffentlichen Schlüssels.*](/windows/desktop/SecGloss/p-gly)

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslVerifySignature(
  _In_ NCRYPT_PROV_HANDLE hSslProvider,
  _In_ NCRYPT_KEY_HANDLE  hPublicKey,
  _In_ PBYTE              pbHashValue,
  _In_ DWORD              cbHashValue,
  _In_ PBYTE              pbSignature,
  _In_ DWORD              cbSignature,
  _In_ DWORD              dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSslProvider* \[ In\]
</dt> <dd>

Das Handle für die SSL-Protokollanbieterinstanz [*(Secure Sockets Layer Protocol).*](/windows/desktop/SecGloss/s-gly)

</dd> <dt>

*hPublicKey* \[ In\]
</dt> <dd>

Das Handle für den öffentlichen Schlüssel.

</dd> <dt>

*pbHashValue* \[ In\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der den Hash enthält, der zum Überprüfen der Signatur verwendet werden soll.

</dd> <dt>

*cbHashValue* \[ In\]
</dt> <dd>

Die Größe des *pbHashValue-Puffers* in Bytes.

</dd> <dt>

*pbSignature* \[ In\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die zu überprüfende Signatur enthält.

</dd> <dt>

*cbSignature* \[ In\]
</dt> <dd>

Die Größe des *pbSignature-Puffers* in Bytes.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. folgende.



| Rückgabecode/-wert                                                                                                                                                    | BESCHREIBUNG                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NTE \_ UNGÜLTIGES \_ HANDLE**</dt> <dt>0x80090026L</dt> </dl> | Einer der bereitgestellten Handles ist ungültig.<br/> |



 

## <a name="remarks"></a>Hinweise

Die **SslVerifySignature-Funktion** wird derzeit nicht von Windows aufgerufen. Diese Funktion ist ein erforderlicher Teil der SSL-Anbieterschnittstelle und sollte vollständig implementiert werden, um die Vorwärtskompatibilität sicherzustellen.

Aktuelle Implementierungen der Serverseite der [*TLS-Verbindung (Transport Layer Security Protocol)*](/windows/desktop/SecGloss/t-gly) rufen die [**NCryptVerifySignature-Funktion**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) während der Clientauthentifizierung auf, um die Zertifikatüberprüfungsmeldung zu verarbeiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

