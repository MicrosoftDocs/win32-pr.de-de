---
description: Gibt einen SSL-Sitzungsschlüssel (Secure Sockets Layer Protocol) oder einen öffentlichen kurzlebigen Schlüssel in ein serialisiertes BLOB zurück.
ms.assetid: c978e6ac-a535-4625-8598-4aa16484dcad
title: SslExportKey-Funktion (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslExportKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 073e922ce8c1a79e81d991c869743148b5a581503192a10dfb9cd6e64707d83e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906672"
---
# <a name="sslexportkey-function"></a>SslExportKey-Funktion

Die **SslExportKey-Funktion** gibt einen SSL-Sitzungsschlüssel [](/windows/desktop/SecGloss/s-gly) [*(Secure Sockets Layer Protocol)*](/windows/desktop/SecGloss/s-gly) oder einen öffentlichen kurzlebigen Schlüssel in ein serialisiertes [*BLOB*](/windows/desktop/SecGloss/b-gly)zurück.

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslExportKey(
  _In_      NCRYPT_PROV_HANDLE hSslProvider,
  _In_      NCRYPT_KEY_HANDLE  hKey,
  _In_      LPCWSTR            pszBlobType,
  _Out_opt_ PBYTE              pbOutput,
  _In_      DWORD              cbOutput,
  _Out_     DWORD              *pcbResult,
  _In_      DWORD              dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSslProvider* \[ In\]
</dt> <dd>

Das Handle der SSL-Protokollanbieterinstanz.

</dd> <dt>

*hKey* \[ In\]
</dt> <dd>

Das Handle des zu exportierende Schlüssels.

Wenn Sie keinen Schlüssel angeben, legen Sie diesen Parameter auf **NULL** fest.

> [!Note]  
> Ein *hKey-Handle* wird durch Aufrufen der [**SslOpenPrivateKey-Funktion**](sslopenprivatekey.md) abgerufen. Handles, die von der [**NCryptOpenKey-Funktion**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) abgerufen werden, werden nicht unterstützt.

 

</dd> <dt>

*pszBlobType* \[ In\]
</dt> <dd>

Eine auf NULL endende Unicode-Zeichenfolge, die einen Bezeichner enthält, der den Typ des zu exportierenden BLOB angibt. Dies kann einer der folgenden Werte sein.



| Wert                                                                                                                                                                                      | Bedeutung                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <dt>**ÖFFENTLICHES BCRYPT \_ \_ \_ DH-BLOB**</dt> </dl>    | Exportieren Sie einen Diffie-Hellman [*öffentlichen Schlüssel.*](/windows/desktop/SecGloss/p-gly) Der *pbOutput-Puffer* empfängt unmittelbar nach den Schlüsseldaten eine [**BCRYPT \_ DH KEY \_ \_ BLOB-Struktur.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob)<br/>                                                                                                               |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <dt>**BCRYPT \_ \_ ECCPUBLIC-BLOB**</dt> </dl>     | Exportieren Sie einen öffentlichen ECC-Schlüssel [*(Elliptic Curve Cryptography).*](/windows/desktop/SecGloss/e-gly) Der *pbOutput-Puffer* empfängt unmittelbar nach den Schlüsseldaten eine [**BCRYPT \_ \_ ECCKEY-BLOB-Struktur.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob)<br/>                                                          |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <dt>**BCRYPT \_ OPAQUE \_ KEY \_ BLOB**</dt> </dl> | Exportieren Sie einen symmetrischen Schlüssel in einem Format, das für einen einzelnen [*Kryptografiedienstanbieter (Cryptographic Service Provider,*](/windows/desktop/SecGloss/c-gly) CSP) spezifisch ist. Nicht transparente BLOBs sind nicht übertragbar und müssen mit demselben *Kryptografiedienstanbieter (Cryptographic Service Provider,* CSP) importiert werden, der das BLOB generiert hat.<br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <dt>**BCRYPT \_ \_ RSAPUBLIC-BLOB**</dt> </dl>     | Exportieren sie einen öffentlichen RSA-Schlüssel. Der *pbOutput-Puffer* empfängt eine [**BCRYPT \_ \_ RSAKEY-BLOB-Struktur**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) unmittelbar gefolgt von den Schlüsseldaten.<br/>                                                                                                                                                                                                |



 

</dd> <dt>

*pbOutput* \[ out, optional\]
</dt> <dd>

Die Adresse eines Puffers, der den [*Schlüssel BLOB*](/windows/desktop/SecGloss/k-gly)empfängt. Der *cbOutput-Parameter* enthält die Größe dieses Puffers. Wenn dieser Parameter **NULL** ist, wird von dieser Funktion die erforderliche Größe in Bytes in das **DWORD-Objekt** gesetzt, auf das der *parameter "pwResult"* zeigt.

</dd> <dt>

*cbOutput* \[ In\]
</dt> <dd>

Die Größe des *pbOutput-Puffers* in Bytes.

</dd> <dt>

*resultsResult* \[ out\]
</dt> <dd>

Die Adresse einer **DWORD-Variablen,** die die Anzahl der in den *pbOutput-Puffer* kopierten Bytes empfängt. Wenn der *pbOutput-Parameter* beim Aufruf der Funktion auf **NULL** festgelegt wird, wird die erforderliche Größe für den *pbOutput-Puffer* in Bytes in dem **DWORD** zurückgegeben, auf das dieser Parameter zeigt.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. folgende.



| Rückgabecode/-wert                                                                                                                                                    | BESCHREIBUNG                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NTE \_ UNGÜLTIGES \_ HANDLE**</dt> <dt>0x80090026L</dt> </dl> | Einer der bereitgestellten Handles ist ungültig.<br/> |



 

## <a name="remarks"></a>Hinweise

Die **SslExportKey-Funktion** ermöglicht das Übertragen von Sitzungsschlüsseln von einem Prozess in einen anderen sowie das Exportieren des öffentlichen Teils eines kurzlebigen Schlüssels.

Beim Exportieren von Sitzungsschlüsseln ist der BLOB-Typ nicht transparent, was bedeutet, dass das Format des BLOB irrelevant ist, solange sowohl die **SslExportKey-** als auch die [**SslImportKey-Funktion**](sslimportkey.md) es interpretieren können.

Beim Exportieren des öffentlichen Teils eines kurzlebigen Schlüssels muss der BLOB-Typ der entsprechende Typ sein, z. B. **NCRYPT \_ DH \_ PUBLIC \_ BLOB** oder **NCRYPT \_ ECCPUBLIC \_ BLOB**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

