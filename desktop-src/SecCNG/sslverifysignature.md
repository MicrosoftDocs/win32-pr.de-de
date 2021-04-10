---
description: Überprüft die angegebene Signatur mit dem angegebenen Hash und dem öffentlichen Schlüssel.
ms.assetid: fa274851-15f2-4be0-9e2f-4cdced36daff
title: Sslverifysignature-Funktion (sslprovider. h)
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
ms.openlocfilehash: cb2a50a7f16062f271a89b6061e3f2fa2dd16685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862323"
---
# <a name="sslverifysignature-function"></a>Sslverifysignature-Funktion

Die **sslverifysignature** -Funktion überprüft die angegebene Signatur mit dem angegebenen [*Hash*](/windows/desktop/SecGloss/h-gly) und dem [*öffentlichen Schlüssel*](/windows/desktop/SecGloss/p-gly).

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

*hsslprovider* \[ in\]
</dt> <dd>

Das Handle für die Protokoll Anbieter Instanz des [*Secure Sockets Layer Protokolls*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*hpublickey* \[ in\]
</dt> <dd>

Das Handle für den öffentlichen Schlüssel.

</dd> <dt>

*pbHashValue* \[ in\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der den Hash enthält, der zum Überprüfen der Signatur verwendet werden soll.

</dd> <dt>

*cbhashwert* \[ in\]
</dt> <dd>

Die Größe des *pbHashValue* -Puffers in Bytes.

</dd> <dt>

*pbSignature* \[ in\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die zu überprüfende Signatur enthält.

</dd> <dt>

*cbsignature* \[ in\]
</dt> <dd>

Die Größe des *pbSignature* -Puffers in Bytes.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. die folgenden:



| Rückgabecode/-wert                                                                                                                                                    | BESCHREIBUNG                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt> </dl> | Eines der bereitgestellten Handles ist ungültig.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die **sslverifysignature** -Funktion wird derzeit nicht von Windows aufgerufen. Diese Funktion ist ein erforderlicher Bestandteil der SSL-Anbieter Schnittstelle und sollte vollständig implementiert werden, um die Vorwärtskompatibilität zu gewährleisten.

Die aktuellen Implementierungen der Serverseite der TLS-Verbindung ( [*Transport Layer Security Protocol*](/windows/desktop/SecGloss/t-gly) ) aufrufen die [**ncryptverifysignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) -Funktion während der Client Authentifizierung, um die Zertifikat Verifizierungs Nachricht zu verarbeiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

