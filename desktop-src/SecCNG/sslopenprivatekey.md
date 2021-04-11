---
description: Öffnet ein Handle für einen privaten Schlüssel.
ms.assetid: 2406be2c-121c-4475-b193-d370a88641da
title: Sslopenprivatekey-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslOpenPrivateKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 6fd5c10ce6385e377c72d21f4557d27d2345737d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128804"
---
# <a name="sslopenprivatekey-function"></a>Sslopenprivatekey-Funktion

Die **sslopenprivatekey** -Funktion öffnet ein Handle für einen [*privaten Schlüssel*](/windows/desktop/SecGloss/p-gly).

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslOpenPrivateKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phPrivateKey,
  _In_  PCCERT_CONTEXT     pCertContext,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hsslprovider* \[ in\]
</dt> <dd>

Das Handle für die Protokoll Anbieter Instanz des [*Secure Sockets Layer Protokolls*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*phprivatekey* \[ vorgenommen\]
</dt> <dd>

Die Adresse eines Puffers, in den das Handle in den privaten Schlüssel geschrieben werden soll.

Wenn Sie die Verwendung des Schlüssels abgeschlossen haben, sollten Sie " *phprivatekey* " freigeben, indem Sie die [**sslfreeobject**](sslfreeobject.md) -Funktion aufrufen.

</dd> <dt>

*pcertcontext* \[ in\]
</dt> <dd>

Die Adresse des Zertifikats, aus dem der private Schlüssel abgerufen werden soll.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. die folgenden:



| Rückgabecode/-wert                                                                                                                                                       | BESCHREIBUNG                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**Ernte \_ Kein Arbeits \_ Speicher**</dt> <dt>0x8009000el</dt> </dl>         | Es ist nicht genügend Arbeitsspeicher verfügbar, um erforderliche Puffer zuzuordnen.<br/> |
| <dl> <dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt> </dl>    | Das *hsslprovider* -Handle ist ungültig.<br/>                       |
| <dl> <dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt> </dl> | Der Parameter " *phprivatekey* " oder " *pcertcontext* " ist **null**.<br/>   |



 

## <a name="remarks"></a>Bemerkungen

Der erhaltene private Schlüssel ist Teil eines [*öffentlichen/privaten Schlüssel Paars*](/windows/desktop/SecGloss/p-gly) innerhalb eines [*Zertifikats*](/windows/desktop/SecGloss/c-gly). Diese Funktion extrahiert lediglich den privaten Schlüssel aus dem Zertifikat, das durch den *pcertcontext* -Parameter angegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

