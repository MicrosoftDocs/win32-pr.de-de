---
description: Berechnet den geheimen Hauptschlüssel des Secure Sockets Layer Protokolls (SSL).
ms.assetid: c9408eb3-711d-42c3-a4ba-e388689da34e
title: Sslgeneratemasterkey-Funktion (sslprovider. h)
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
ms.openlocfilehash: ae8b357743cabf652721d3666c177990568718e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393806"
---
# <a name="sslgeneratemasterkey-function"></a>Sslgeneratemasterkey-Funktion

Die **sslgeneratemasterkey** -Funktion berechnet den geheimen Hauptschlüssel des [*Secure Sockets Layer Protokolls*](/windows/desktop/SecGloss/s-gly) (SSL).

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

*hsslprovider* \[ in\]
</dt> <dd>

Das Handle für die SSL-Protokoll Anbieter Instanz.

</dd> <dt>

*hprivatekey* \[ in\]
</dt> <dd>

Das Handle für den [*privaten Schlüssel*](/windows/desktop/SecGloss/p-gly) , der im Austausch verwendet wird.

</dd> <dt>

*hpublickey* \[ in\]
</dt> <dd>

Das Handle für den [*öffentlichen Schlüssel*](/windows/desktop/SecGloss/p-gly) , der im Austausch verwendet wird.

</dd> <dt>

*phmasterkey* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf das Handle des generierten [*Haupt Schlüssels*](/windows/desktop/SecGloss/m-gly).

</dd> <dt>

*dwprotocol* \[ in\]
</dt> <dd>

Einer der [**CNG-SSL-Anbieter Protokoll-Bezeichnerwerte**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .

</dd> <dt>

*dwciphersuite* \[ in\]
</dt> <dd>

Einer der [**Cipher Suite-Bezeichnerwerte des CNG-SSL-Anbieters**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .

</dd> <dt>

*pparameterlist* \[ in\]
</dt> <dd>

Ein Zeiger auf ein Array von [**ncryptbuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) -Puffern, die Informationen enthalten, die als Teil des Schlüsselaustausch Vorgangs verwendet werden. Der genaue Satz Puffer ist abhängig vom verwendeten Protokoll und der Verschlüsselungs Sammlung. Die Liste enthält mindestens Puffer, die den vom Client und vom Server bereitgestellten Zufallswert enthalten.

</dd> <dt>

*pboutput* \[ vorgenommen\]
</dt> <dd>

Die Adresse eines Puffers, der den geheimen Hauptschlüssel empfängt, der mit dem öffentlichen Schlüssel des Servers verschlüsselt ist. Der *cboutput* -Parameter enthält die Größe dieses Puffers. Wenn dieser Parameter **null** ist, gibt diese Funktion die erforderliche Größe in Byte in dem **DWORD** -Element zurück, auf das durch den *pcbresult* -Parameter verwiesen wird.

> [!Note]  
> Dieser Puffer wird verwendet, wenn ein RSA-Schlüsselaustausch durchgeführt wird.

 

</dd> <dt>

*cboutput* \[ in\]
</dt> <dd>

Die Größe des *pboutput* -Puffers in Bytes.

</dd> <dt>

*pcbresult* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen **DWORD** -Wert, in den die Anzahl der in den *pboutput* -Puffer geschriebenen Bytes aufgenommen werden soll.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Gibt an, ob diese Funktion für den Client seitigen oder serverseitigen Schlüsselaustausch verwendet wird.



| Wert                                                                                                                                                                                                                                                      | Bedeutung                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <dt>**NCrypt \_ SSL \_ - \_ clientflag**</dt> <dt>0x00000001</dt> </dl> | Gibt einen Client seitigen Schlüsselaustausch an.<br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <dt>**NCrypt \_ SSL \_ - \_ Serverflag**</dt> <dt>0x00000002</dt> </dl> | Gibt einen serverseitigen Schlüsselaustausch an.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. die folgenden:



| Rückgabecode/-wert                                                                                                                                                       | BESCHREIBUNG                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**Ernte \_ Kein Arbeits \_ Speicher**</dt> <dt>0x8009000el</dt> </dl>         | Es ist nicht genügend Arbeitsspeicher verfügbar, um erforderliche Puffer zuzuordnen.<br/> |
| <dl> <dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt> </dl>    | Eines der bereitgestellten Handles ist ungültig.<br/>                     |
| <dl> <dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt> </dl> | Der Parameter " *phmasterkey* " oder " *hpublickey* " ist ungültig.<br/>     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

