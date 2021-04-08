---
description: Gibt ein Handle für den Handshake-Hash zurück.
ms.assetid: c0f20084-c863-42cf-afdf-298c5a96eed9
title: Sslhashhandshake-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslHashHandshake
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 1dbfdbceb4242d389669a3eebf14260a3bb396fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960469"
---
# <a name="sslhashhandshake-function"></a>Sslhashhandshake-Funktion

Die **sslhashhandshake** -Funktion gibt ein Handle für den Handshake-Hash zurück.

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslHashHandshake(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_HASH_HANDLE hHandshakeHash,
  _Out_   PBYTE              pbInput,
  _In_    DWORD              cbInput,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hsslprovider* \[ in\]
</dt> <dd>

Das Handle für die Protokoll Anbieter Instanz des [*Secure Sockets Layer Protokolls*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*hhandshakehash* \[ in, out\]
</dt> <dd>

Das Handle für das Hash Objekt.

</dd> <dt>

*pbinput* \[ vorgenommen\]
</dt> <dd>

Die Adresse eines Puffers, der die Daten enthält, für die ein Hashwert erstellt werden soll.

</dd> <dt>

*cbinput* \[ in\]
</dt> <dd>

Die Größe des *pbinput* -Puffers in Bytes.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.

## <a name="remarks"></a>Bemerkungen

Die **sslhashhandshake** -Funktion ist eine von drei Funktionen, die verwendet werden, um einen Hash zu generieren, der während des SSL-Handshake verwendet wird.

1.  Die [**sslkreatehandshakehash**](sslcreatehandshakehash.md) -Funktion wird aufgerufen, um ein Hashhandle abzurufen.
2.  Die **sslhashhandshake** -Funktion wird beliebig oft mit dem Hashhandle aufgerufen, um dem Hash Daten hinzuzufügen.
3.  Die [**sslcomputefinishedhash**](sslcomputefinishedhash.md) -Funktion wird mit dem Hashhandle aufgerufen, um den Digest der Hash Daten zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

