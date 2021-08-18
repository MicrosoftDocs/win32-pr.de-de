---
description: Gibt ein Handle für den Handshakehash zurück.
ms.assetid: c0f20084-c863-42cf-afdf-298c5a96eed9
title: SslHashHandshake-Funktion (Sslprovider.h)
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
ms.openlocfilehash: 5a21bdb3fd655e5c3b39249937f04a4122c64e6c6176c0d39ae1164e48863edb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906098"
---
# <a name="sslhashhandshake-function"></a>SslHashHandshake-Funktion

Die **SslHashHandshake-Funktion** gibt ein Handle für den Handshakehash zurück.

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

*hSslProvider* \[ In\]
</dt> <dd>

Das Handle für die SSL-Protokollanbieterinstanz [*(Secure Sockets Layer Protocol).*](/windows/desktop/SecGloss/s-gly)

</dd> <dt>

*hHandshakeHash* \[ in, out\]
</dt> <dd>

Das Handle für das Hashobjekt.

</dd> <dt>

*pbInput* \[ out\]
</dt> <dd>

Die Adresse eines Puffers, der die zu hashingden Daten enthält.

</dd> <dt>

*cbInput* \[ In\]
</dt> <dd>

Die Größe des *pbInput-Puffers* in Bytes.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt sie 0 (null) zurück.

## <a name="remarks"></a>Hinweise

Die **SslHashHandshake-Funktion** ist eine von drei Funktionen, die verwendet werden, um einen Hash zu generieren, der während des SSL-Handshakes verwendet wird.

1.  Die [**SslCreateHandshakeHash-Funktion**](sslcreatehandshakehash.md) wird aufgerufen, um ein Hashhandle abzurufen.
2.  Die **SslHashHandshake-Funktion** wird beliebig oft mit dem Hashhandle aufgerufen, um dem Hash Daten hinzuzufügen.
3.  Die [**SslComputeFinishedHash-Funktion**](sslcomputefinishedhash.md) wird mit dem Hashhandle aufgerufen, um den Digest der Hashdaten abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

