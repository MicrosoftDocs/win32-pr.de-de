---
description: Signiert einen Hash mithilfe des angegebenen privaten Schlüssels.
ms.assetid: 25e8ebc5-278d-4d1f-977a-c2fab07b790a
title: SslSignHash-Funktion (Sslprovider.h)
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
ms.openlocfilehash: c57da628aac5c4043abe79491b90bb64d9fa3644199c96ba1e2ad93440f7c11b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905619"
---
# <a name="sslsignhash-function"></a>SslSignHash-Funktion

Die **SslSignHash-Funktion** signiert einen [*Hash*](/windows/desktop/SecGloss/h-gly) mithilfe des angegebenen [*privaten Schlüssels.*](/windows/desktop/SecGloss/p-gly) Der Signierungsprozess wird auf dem Server ausgeführt.

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

*hSslProvider* \[ In\]
</dt> <dd>

Das Handle für die SSL-Protokollanbieterinstanz [*(Secure Sockets Layer Protocol).*](/windows/desktop/SecGloss/s-gly)

</dd> <dt>

*hPrivateKey* \[ In\]
</dt> <dd>

Das Handle für den privaten Schlüssel, der zum Signieren des Hashs verwendet werden soll.

</dd> <dt>

*pbHashValue* \[ In\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der den zu signierenden Hash enthält.

</dd> <dt>

*cbHashValue* \[ In\]
</dt> <dd>

Die Größe des *pbHashValue-Puffers* in Bytes.

</dd> <dt>

*pbSignature* \[ out\]
</dt> <dd>

Die Adresse eines Puffers, der die Signatur des Hash empfängt. Der *cbSignature-Parameter* enthält die Größe dieses Puffers. Um die erforderliche Größe des Puffers zu bestimmen, legen Sie den *parameter pbSignature* auf **NULL** fest. Die erforderliche Größe des Puffers wird im *parameter pwResult* zurückgegeben.

</dd> <dt>

*cbSignature* \[ In\]
</dt> <dd>

Die Größe des *pbSignature-Puffers* in Bytes.

</dd> <dt>

*resultsResult* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Wert, der nach Abschluss die tatsächliche Anzahl von Bytes enthält, die in den *pbSignature-Puffer* geschrieben wurden.

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



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

