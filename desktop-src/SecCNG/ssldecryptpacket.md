---
description: Entschlüsselt ein einzelnes SSL-Paket (Secure Sockets Layer Protocol).
ms.assetid: 22a7dd2b-d023-47b9-8f76-1c17c2dd6466
title: SslDecryptPacket-Funktion (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslDecryptPacket
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 0b058fbb01183ccf0582c0fa196bec71bfaffa2e8a44739c1ea5fb01a8148174
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906702"
---
# <a name="ssldecryptpacket-function"></a>SslDecryptPacket-Funktion

Die **SslDecryptPacket-Funktion** entschlüsselt ein einzelnes [*SSL-Paket (Secure Sockets Layer Protocol).*](/windows/desktop/SecGloss/s-gly)

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslDecryptPacket(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_KEY_HANDLE  hKey,
  _In_    PBYTE              *pbInput,
  _In_    DWORD              cbInput,
  _Out_   PBYTE              pbOutput,
  _In_    DWORD              cbOutput,
  _Out_   DWORD              *pcbResult,
  _In_    ULONGLONG          SequenceNumber,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSslProvider* \[ In\]
</dt> <dd>

Das Handle der SSL-Protokollanbieterinstanz.

</dd> <dt>

*hKey* \[ in, out\]
</dt> <dd>

Das Handle für den Schlüssel, der zum Entschlüsseln des Pakets verwendet wird.

</dd> <dt>

*pbInput* \[ In\]
</dt> <dd>

Ein Zeiger auf den Puffer, der das zu entschlüsselnde Paket enthält.

</dd> <dt>

*cbInput* \[ In\]
</dt> <dd>

Die Länge des *pbInput-Puffers* in Bytes.

</dd> <dt>

*pbOutput* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der das entschlüsselte Paket enthalten soll.

</dd> <dt>

*cbOutput* \[ In\]
</dt> <dd>

Die Länge (Bytes) des *pbOutput-Puffers.*

</dd> <dt>

*resultsResult* \[ out\]
</dt> <dd>

Die Anzahl der Bytes, die in den *pbOutput-Puffer* geschrieben wurden.

</dd> <dt>

*SequenceNumber* \[ In\]
</dt> <dd>

Die Sequenznummer, die diesem Paket entspricht.

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

Die Länge des Pakets kann 0 (null) sein, z. B. wenn eine "HelloRequest"-Nachricht entschlüsselt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

