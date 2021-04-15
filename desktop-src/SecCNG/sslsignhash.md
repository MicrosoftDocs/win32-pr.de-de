---
description: Signiert einen Hash mit dem angegebenen privaten Schlüssel.
ms.assetid: 25e8ebc5-278d-4d1f-977a-c2fab07b790a
title: Sslsignhash-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslSignHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 339d0a27cb987557ff90cbd0f489813edb357b77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484627"
---
# <a name="sslsignhash-function"></a>Sslsignhash-Funktion

Die **sslsignhash** -Funktion signiert einen [*Hash*](/windows/desktop/SecGloss/h-gly) mit dem angegebenen [*privaten Schlüssel*](/windows/desktop/SecGloss/p-gly). Der Signatur Prozess wird auf dem Server ausgeführt.

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslSignHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _In_  PBYTE              pbHashValue,
  _In_  DWORD              cbHashValue,
  _Out_ PBYTE              pbSignature,
  _In_  DWORD              cbSignature,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hsslprovider* \[ in\]
</dt> <dd>

Das Handle für die Protokoll Anbieter Instanz des [*Secure Sockets Layer Protokolls*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*hprivatekey* \[ in\]
</dt> <dd>

Das Handle für den privaten Schlüssel, der zum Signieren des Hashwerts verwendet werden soll.

</dd> <dt>

*pbHashValue* \[ in\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der den zu Signier nden Hash enthält.

</dd> <dt>

*cbhashwert* \[ in\]
</dt> <dd>

Die Größe des *pbHashValue* -Puffers in Bytes.

</dd> <dt>

*pbSignature* \[ vorgenommen\]
</dt> <dd>

Die Adresse eines Puffers, der die Signatur des Hashwerts empfängt. Der *cbsignature* -Parameter enthält die Größe dieses Puffers. Legen Sie den *pbSignature* -Parameter auf **null** fest, um die erforderliche Größe des Puffers zu bestimmen. Die erforderliche Größe des Puffers wird im *pcbresult* -Parameter zurückgegeben.

</dd> <dt>

*cbsignature* \[ in\]
</dt> <dd>

Die Größe des *pbSignature* -Puffers in Bytes.

</dd> <dt>

*pcbresult* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Wert, der nach Abschluss die tatsächliche Anzahl der in den *pbSignature* -Puffer geschriebenen Bytes enthält.

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



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

