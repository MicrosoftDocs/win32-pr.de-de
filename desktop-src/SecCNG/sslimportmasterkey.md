---
description: Führt einen serverseitigen SSL-Schlüsselaustauschvorgang (Secure Sockets Layer Protokoll) aus.
ms.assetid: 052e38ee-658c-47dc-8098-c9a1fd359e1c
title: SslImportMasterKey-Funktion (Sslprovider.h)
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
ms.openlocfilehash: 546cfeb39ac413b99b5b8021dc7dd6f0f57a89dbfb87880a63b0db2324cda0d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906061"
---
# <a name="sslimportmasterkey-function"></a>SslImportMasterKey-Funktion

Die **SslImportMasterKey-Funktion** führt einen serverseitigen Ssl-Schlüsselaustauschvorgang [*(Secure Sockets Layer*](/windows/desktop/SecGloss/s-gly) Protokoll) aus.

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

*hSslProvider* \[ In\]
</dt> <dd>

Das Handle für die SSL-Protokollanbieterinstanz.

</dd> <dt>

*hPrivateKey* \[ In\]
</dt> <dd>

Das Handle für den [*privaten Schlüssel, der*](/windows/desktop/SecGloss/p-gly) im Austausch verwendet wird.

</dd> <dt>

*phMasterKey* \[ out\]
</dt> <dd>

Ein Zeiger auf das Handle, um den [*Hauptschlüssel zu empfangen.*](/windows/desktop/SecGloss/m-gly)

</dd> <dt>

*dwProtocol* \[ In\]
</dt> <dd>

Einer der [**CNG SSL Provider Protocol Identifier-Werte.**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx)

</dd> <dt>

*dwCipherSuite* \[ In\]
</dt> <dd>

Einer der [**CNG SSL Provider Cipher Suite Identifiers-Werte.**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx)

</dd> <dt>

*pParameterList* \[ In\]
</dt> <dd>

Ein Zeiger auf ein Array von [**NCryptBuffer-Puffern,**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) die Informationen enthalten, die als Teil des Schlüsselaustauschs verwendet werden. Die genaue Gruppe von Puffern hängt vom verwendeten Protokoll und der verwendeten Verschlüsselungssammlung ab. Die Liste enthält mindestens Puffer, die die vom Client und Server bereitgestellten Zufallswerte enthalten.

</dd> <dt>

*pbEncryptedKey* \[ In\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der den verschlüsselten geheimen Premasterschlüssel enthält, der mit dem öffentlichen [*Schlüssel des*](/windows/desktop/SecGloss/p-gly) Servers verschlüsselt wurde.

</dd> <dt>

*cbEncryptedKey* \[ In\]
</dt> <dd>

Die Größe des *pbEncryptedKey-Puffers* in Bytes.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Legen Sie diesen Parameter auf **NCRYPT \_ SSL SERVER FLAG \_ \_ fest,** um anzugeben, dass es sich um einen Serveraufruf handelt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. folgende:



| Rückgabecode/-wert                                                                                                                                                       | Beschreibung                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | Es ist nicht genügend Arbeitsspeicher verfügbar, um erforderliche Puffer zu reservieren.<br/> |
| <dl> <dt>**NTE \_ UNGÜLTIGES \_ HANDLE**</dt> <dt>0x80090026L</dt> </dl>    | Eines der bereitgestellten Handles ist ungültig.<br/>                     |
| <dl> <dt>**NTE \_ UNGÜLTIGER \_ PARAMETER**</dt> <dt>0x80090027L</dt> </dl> | Der *phMasterKey-Parameter* ist **NULL.**<br/>                      |



 

## <a name="remarks"></a>Hinweise

Diese Funktion entschlüsselt das Prämastergeheimnis, berechnet das SSL-Hauptgeheimnis und gibt ein Handle für dieses Objekt an den Aufrufer zurück. Dieser Hauptschlüssel kann dann verwendet werden, um den SSL-Sitzungsschlüssel ableiten und den SSL-Handshake zu beenden.

> [!Note]  
> Diese Funktion wird verwendet, wenn der [*RSA-Schlüsselaustauschalgorithmus*](/windows/desktop/SecGloss/r-gly) verwendet wird. Wenn [*DH*](/windows/desktop/SecGloss/d-gly) verwendet wird, ruft der Servercode stattdessen [**SslGenerateMasterKey**](sslgeneratemasterkey.md) auf.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

