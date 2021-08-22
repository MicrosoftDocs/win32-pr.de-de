---
description: Berechnet den SSL-Hauptschlüssel (Secure Sockets Layer Protocol).
ms.assetid: c9408eb3-711d-42c3-a4ba-e388689da34e
title: SslGenerateMasterKey-Funktion (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGenerateMasterKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 4e1ca35493667cb6e7e3d5ba8b162a3d073d51fc397ce2e1a1da7ab7a380728d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906253"
---
# <a name="sslgeneratemasterkey-function"></a>SslGenerateMasterKey-Funktion

Die **SslGenerateMasterKey-Funktion** berechnet den GEHEIMEN SSL-Hauptschlüssel [*(Secure Sockets Layer Protocol).*](/windows/desktop/SecGloss/s-gly)

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslGenerateMasterKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _In_  NCRYPT_KEY_HANDLE  hPublicKey,
  _Out_ NCRYPT_KEY_HANDLE  *phMasterKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  PNCryptBufferDesc  pParameterList,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSslProvider* \[ In\]
</dt> <dd>

Das Handle für die SSL-Protokollanbieterinstanz.

</dd> <dt>

*hPrivateKey* \[ In\]
</dt> <dd>

Das Handle für den [*privaten Schlüssel,*](/windows/desktop/SecGloss/p-gly) der im Austausch verwendet wird.

</dd> <dt>

*hPublicKey* \[ In\]
</dt> <dd>

Das Handle für den [*öffentlichen Schlüssel,*](/windows/desktop/SecGloss/p-gly) der im Austausch verwendet wird.

</dd> <dt>

*phMasterKey* \[ out\]
</dt> <dd>

Ein Zeiger auf das Handle auf den generierten [*Hauptschlüssel.*](/windows/desktop/SecGloss/m-gly)

</dd> <dt>

*dwProtocol* \[ In\]
</dt> <dd>

Einer der [**CNG SSL Provider Protocol Identifier-Werte.**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx)

</dd> <dt>

*dwCipherSuite* \[ In\]
</dt> <dd>

Einer der [**CNG SSL Provider Cipher Suite Identifier-Werte.**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx)

</dd> <dt>

*pParameterList* \[ In\]
</dt> <dd>

Ein Zeiger auf ein Array von [**NCryptBuffer-Puffern,**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) die Informationen enthalten, die als Teil des Schlüsselaustauschvorgangs verwendet werden. Der genaue Satz von Puffern hängt vom verwendeten Protokoll und der verwendeten Verschlüsselungssammlung ab. Die Liste enthält mindestens Puffer, die die vom Client und server bereitgestellten Zufallswerte enthalten.

</dd> <dt>

*pbOutput* \[ out\]
</dt> <dd>

Die Adresse eines Puffers, der das Premastergeheimnis empfängt, das mit dem öffentlichen Schlüssel des Servers verschlüsselt ist. Der *cbOutput-Parameter* enthält die Größe dieses Puffers. Wenn dieser Parameter **NULL** ist, gibt diese Funktion die erforderliche Größe in Byte in dem **DWORD** zurück, auf das der *parameter "pwResult"* zeigt.

> [!Note]  
> Dieser Puffer wird beim Ausführen eines RSA-Schlüsselaustauschs verwendet.

 

</dd> <dt>

*cbOutput* \[ In\]
</dt> <dd>

Die Größe des *pbOutput-Puffers* in Bytes.

</dd> <dt>

*resultsResult* \[ out\]
</dt> <dd>

Ein Zeiger auf einen **DWORD-Wert,** in den die Anzahl der in den *pbOutput-Puffer* geschriebenen Bytes gesetzt werden soll.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Gibt an, ob diese Funktion für den clientseitigen oder serverseitigen Schlüsselaustausch verwendet wird.



| Wert                                                                                                                                                                                                                                                      | Bedeutung                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <dt>**NCRYPT \_ \_ \_ SSL-CLIENTFLAG-0x00000001**</dt> <dt></dt> </dl> | Gibt einen clientseitigen Schlüsselaustausch an.<br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <dt>**NCRYPT \_ \_ \_ SSL-SERVERFLAG-0x00000002**</dt> <dt></dt> </dl> | Gibt einen serverseitigen Schlüsselaustausch an.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. folgende.



| Rückgabecode/-wert                                                                                                                                                       | Beschreibung                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | Es ist nicht genügend Arbeitsspeicher verfügbar, um die erforderlichen Puffer zuzuordnen.<br/> |
| <dl> <dt>**NTE \_ UNGÜLTIGES \_ HANDLE**</dt> <dt>0x80090026L</dt> </dl>    | Einer der bereitgestellten Handles ist ungültig.<br/>                     |
| <dl> <dt>**NTE \_ UNGÜLTIGER \_ PARAMETER**</dt> <dt>0x80090027L</dt> </dl> | Der *parameter phMasterKey* oder *hPublicKey* ist ungültig.<br/>     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

