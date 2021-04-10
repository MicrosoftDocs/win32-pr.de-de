---
description: Berechnet einen Hash, der während der Zertifikat Authentifizierung verwendet werden soll.
ms.assetid: f4a12464-8ad6-4bf9-8b6e-49bdf5332b66
title: Sslcomputeclientauthhash-Funktion (sslprovider. h)
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
ms.openlocfilehash: faea1699657efd92049068e48ff361c48242e9c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215555"
---
# <a name="sslcomputeclientauthhash-function"></a>Sslcomputeclientauthhash-Funktion

Die **sslcomputeclientauthhash** -Funktion berechnet einen [*Hash*](/windows/desktop/SecGloss/h-gly) , der während der [*Zertifikat*](/windows/desktop/SecGloss/c-gly) Authentifizierung verwendet werden soll.

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

*hsslprovider* \[ in\]
</dt> <dd>

Das Handle der Protokoll Anbieter Instanz des [*Secure Sockets Layer Protokolls*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*hmasterkey* \[ in\]
</dt> <dd>

Das Handle des [*Hauptschlüssel*](/windows/desktop/SecGloss/m-gly) Objekts.

</dd> <dt>

*hhandshakehash* \[ in\]
</dt> <dd>

Das Handle des Hashwerts des bisher berechneten Handshakes.

</dd> <dt>

*pszalgid* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge, die den angeforderten [*Kryptografiealgorithmus*](/windows/desktop/SecGloss/c-gly)identifiziert. Hierbei kann es sich um einen der Standard- [**CNG-Algorithmus**](cng-algorithm-identifiers.md) -IDs oder den Bezeichner für einen anderen registrierten Algorithmus handeln.

</dd> <dt>

*pboutput* \[ vorgenommen\]
</dt> <dd>

Die Adresse eines Puffers, der das [*Schlüsselblob*](/windows/desktop/SecGloss/k-gly)empfängt. Der *cboutput* -Parameter enthält die Größe dieses Puffers. Wenn dieser Parameter **null** ist, fügt diese Funktion die erforderliche Größe (in Bytes) in das **DWORD** ein, auf das durch den *pcbresult* -Parameter verwiesen wird.

</dd> <dt>

*cboutput* \[ in\]
</dt> <dd>

Die Länge des *pboutput* -Puffers in Bytes.

</dd> <dt>

*pcbresult* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen **DWORD** -Wert, der die Länge des in den *pboutput* -Puffer geschriebenen Hashs in Bytes angibt.

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
| <dl> <dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt> </dl> | Eines der angegebenen Handles ist ungültig.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die **sslcomputeclientauthhash** -Funktion berechnet den Hash, der in der Zertifikat Überprüfungs Nachricht des SSL-Handshakes gesendet wird. Der Hashwert wird berechnet, indem ein Hashwert erstellt wird, der den geheimen Hauptschlüssel mit einem Hash aller zuvor gesendeten oder empfangenen Hand Shake Nachrichten enthält. Weitere Informationen zur SSL-Handshake-Sequenz finden Sie unter [Beschreibung des Secure Sockets Layer (SSL) Handshake](https://support.microsoft.com/kb/257591).

Die Art und Weise, in der der Hashwert berechnet wird, hängt vom verwendeten Protokoll und der verwendeten Verschlüsselungs Sammlung ab. Außerdem hängt der Hash vom Typ des verwendeten Client Authentifizierungs Schlüssels ab. der *pszalgid* -Parameter gibt den Schlüsseltyp an, der für die Client Authentifizierung verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

