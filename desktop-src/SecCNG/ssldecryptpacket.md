---
description: Entschlüsselt ein einzelnes Secure Sockets Layer Protocol (SSL)-Paket.
ms.assetid: 22a7dd2b-d023-47b9-8f76-1c17c2dd6466
title: Ssldecryptpacket-Funktion (sslprovider. h)
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
ms.openlocfilehash: cd568596b7e780242c0ff8d9c522a9e1758c60b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959429"
---
# <a name="ssldecryptpacket-function"></a>Ssldecryptpacket-Funktion

die **ssldecryptpacket** -Funktion entschlüsselt ein einzelnes [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) (SSL)-Paket.

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

*hsslprovider* \[ in\]
</dt> <dd>

Das Handle der SSL-Protokoll Anbieter Instanz.

</dd> <dt>

*HKEY* \[ in, out\]
</dt> <dd>

Das Handle für den Schlüssel, der zum Entschlüsseln des Pakets verwendet wird.

</dd> <dt>

*pbinput* \[ in\]
</dt> <dd>

Ein Zeiger auf den Puffer, der das Paket enthält, das entschlüsselt werden soll.

</dd> <dt>

*cbinput* \[ in\]
</dt> <dd>

Die Länge des *pbinput* -Puffers in Bytes.

</dd> <dt>

*pboutput* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der das entschlüsselte Paket enthalten soll.

</dd> <dt>

*cboutput* \[ in\]
</dt> <dd>

Die Länge (Bytes) des *pboutput* -Puffers.

</dd> <dt>

*pcbresult* \[ vorgenommen\]
</dt> <dd>

Die Anzahl der in den *pboutput* -Puffer geschriebenen Bytes.

</dd> <dt>

*Sequencennummer* \[ in\]
</dt> <dd>

Die Sequenznummer, die diesem Paket entspricht.

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

Die Länge des Pakets kann NULL sein, z. b. Wenn eine "hellorequest"-Meldung entschlüsselt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

