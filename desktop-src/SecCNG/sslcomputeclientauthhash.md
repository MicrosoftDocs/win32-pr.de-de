---
description: Berechnet einen Hash, der während der Zertifikatauthentifizierung verwendet werden soll.
ms.assetid: f4a12464-8ad6-4bf9-8b6e-49bdf5332b66
title: SslComputeClientAuthHash-Funktion (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeClientAuthHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 59d1a4d8491175acb0f833cbafb430faae9b36b38a179970b7a99d6b0077591d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907161"
---
# <a name="sslcomputeclientauthhash-function"></a>SslComputeClientAuthHash-Funktion

Die **SslComputeClientAuthHash-Funktion** berechnet einen [*Hash*](/windows/desktop/SecGloss/h-gly) für die Verwendung während der [*Zertifikatauthentifizierung.*](/windows/desktop/SecGloss/c-gly)

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslComputeClientAuthHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _In_  NCRYPT_HASH_HANDLE hHandshakeHash,
  _In_  LPCWSTR            pszAlgId,
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

Das Handle der SSL-Protokollanbieterinstanz [*(Secure Sockets Layer Protocol).*](/windows/desktop/SecGloss/s-gly)

</dd> <dt>

*hMasterKey* \[ In\]
</dt> <dd>

Das Handle des [*Hauptschlüsselobjekts.*](/windows/desktop/SecGloss/m-gly)

</dd> <dt>

*hHandshakeHash* \[ In\]
</dt> <dd>

Das Handle des hash des bisher berechneten Handshakes.

</dd> <dt>

*pszAlgId* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Unicode-Zeichenfolge, die den angeforderten [*kryptografischen Algorithmus*](/windows/desktop/SecGloss/c-gly)identifiziert. Dies kann einer der [**CNG-Standardalgorithmusbezeichner**](cng-algorithm-identifiers.md) oder der Bezeichner für einen anderen registrierten Algorithmus sein.

</dd> <dt>

*pbOutput* \[ out\]
</dt> <dd>

Die Adresse eines Puffers, der den [*Schlüssel BLOB*](/windows/desktop/SecGloss/k-gly)empfängt. Der *cbOutput-Parameter* enthält die Größe dieses Puffers. Wenn dieser Parameter **NULL** ist, wird von dieser Funktion die erforderliche Größe in Bytes in das **DWORD-Objekt** gesetzt, auf das der *parameter "pwResult"* zeigt.

</dd> <dt>

*cbOutput* \[ In\]
</dt> <dd>

Die Länge des *pbOutput-Puffers* in Bytes.

</dd> <dt>

*resultsResult* \[ out\]
</dt> <dd>

Ein Zeiger auf einen **DWORD-Wert,** der die Länge des in den *pbOutput-Puffer* geschriebenen Hashs in Bytes angibt.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. folgende.



| Rückgabecode/-wert                                                                                                                                                    | Beschreibung                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NTE \_ UNGÜLTIGES \_ HANDLE**</dt> <dt>0x80090026L</dt> </dl> | Einer der angegebenen Handles ist ungültig.<br/> |



 

## <a name="remarks"></a>Hinweise

Die **SslComputeClientAuthHash-Funktion** berechnet den Hash, der in der Zertifikatüberprüfungsmeldung des SSL-Handshakes gesendet wird. Der Hashwert wird berechnet, indem ein Hash erstellt wird, der das Hauptgeheimnis mit einem Hash aller vorherigen gesendeten oder empfangenen Handshakenachrichten enthält. Weitere Informationen zur SSL-Handshakesequenz finden Sie unter [Beschreibung des ssl-Handshakes (Secure Sockets Layer).](https://support.microsoft.com/kb/257591)

Die Art und Weise, in der der Hash berechnet wird, hängt vom verwendeten Protokoll und der verwendeten Verschlüsselungssammlung ab. Darüber hinaus hängt der Hash vom Typ des verwendeten Clientauthentifizierungsschlüssels ab. Der *pszAlgId-Parameter* gibt den Typ des Schlüssels an, der für die Clientauthentifizierung verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

