---
description: Führt einen SSL-Schlüsselaustausch Vorgang (Server Side Secure Sockets Layer Protocol) aus.
ms.assetid: 052e38ee-658c-47dc-8098-c9a1fd359e1c
title: Sslimportmasterkey-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslImportMasterKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e21c4cd0f6e51662124e02881b82c905dba68c9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362462"
---
# <a name="sslimportmasterkey-function"></a>Sslimportmasterkey-Funktion

Die **sslimportmasterkey** -Funktion führt einen serverseitigen [*Secure Sockets Layer Protokoll*](/windows/desktop/SecGloss/s-gly) (SSL)-Schlüsselaustausch Vorgang aus.

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslImportMasterKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _Out_ NCRYPT_KEY_HANDLE  *phMasterKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  PNCryptBufferDesc  pParameterList,
  _In_  PBYTE              pbEncryptedKey,
  _In_  DWORD              cbEncryptedKey,
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

*phmasterkey* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf das Handle, um den [*Hauptschlüssel*](/windows/desktop/SecGloss/m-gly)zu empfangen.

</dd> <dt>

*dwprotocol* \[ in\]
</dt> <dd>

Einer der [**CNG-SSL-Anbieter Protokoll-Bezeichnerwerte**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .

</dd> <dt>

*dwciphersuite* \[ in\]
</dt> <dd>

Einer der [**Cipher Suite-Bezeichner Werte des CNG-SSL-Anbieters**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .

</dd> <dt>

*pparameterlist* \[ in\]
</dt> <dd>

Ein Zeiger auf ein Array von [**ncryptbuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) -Puffern, die Informationen enthalten, die als Teil des Schlüsselaustausch Vorgangs verwendet werden. Der genaue Satz Puffer ist abhängig vom verwendeten Protokoll und der Verschlüsselungs Sammlung. Die Liste enthält mindestens Puffer, die den vom Client und vom Server bereitgestellten Zufallswert enthalten.

</dd> <dt>

*pbencryptedkey* \[ in\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der den verschlüsselten Schlüssel für den geheimen Hauptschlüssel enthält, der mit dem [*öffentlichen Schlüssel*](/windows/desktop/SecGloss/p-gly) des Servers verschlüsselt ist.

</dd> <dt>

*cbencryptedkey* \[ in\]
</dt> <dd>

Die Größe des *pbencryptedkey* -Puffers in Bytes.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Legen Sie diesen Parameter auf das **NCrypt- \_ SSL- \_ \_ Serverflag** fest, um anzugeben, dass es sich um einen Server

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. die folgenden:



| Rückgabecode/-wert                                                                                                                                                       | BESCHREIBUNG                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**Ernte \_ Kein Arbeits \_ Speicher**</dt> <dt>0x8009000el</dt> </dl>         | Es ist nicht genügend Arbeitsspeicher verfügbar, um erforderliche Puffer zuzuordnen.<br/> |
| <dl> <dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt> </dl>    | Eines der bereitgestellten Handles ist ungültig.<br/>                     |
| <dl> <dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt> </dl> | Der *phmasterkey* -Parameter ist **null**.<br/>                      |



 

## <a name="remarks"></a>Bemerkungen

Diese Funktion entschlüsselt den geheimen Hauptschlüssel, berechnet den SSL-Hauptschlüssel und gibt ein Handle für dieses Objekt an den Aufrufer zurück. Dieser Hauptschlüssel kann dann verwendet werden, um den SSL-Sitzungsschlüssel abzuleiten und den SSL-Handshake abzuschließen.

> [!Note]  
> Diese Funktion wird verwendet, wenn der [*RSA*](/windows/desktop/SecGloss/r-gly) -Schlüsselaustausch Algorithmus verwendet wird. Wenn [*dh*](/windows/desktop/SecGloss/d-gly) verwendet wird, ruft der Servercode stattdessen [**sslgeneratemasterkey**](sslgeneratemasterkey.md) auf.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

