---
description: Gibt einen SSL-Sitzungsschlüssel (Secure Sockets Layer Protocol) oder einen öffentlichen kurzlebigen Schlüssel in einem serialisierten BLOB zurück.
ms.assetid: c978e6ac-a535-4625-8598-4aa16484dcad
title: Sslexportkey-Funktion (sslprovider. h)
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
ms.openlocfilehash: c5fcbcfa1a8b6c1aa9922b98a7699bdf2bf4b0fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959428"
---
# <a name="sslexportkey-function"></a>Sslexportkey-Funktion

Die **sslexportkey** -Funktion gibt einen SSL- [*Sitzungsschlüssel*](/windows/desktop/SecGloss/s-gly) ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ) oder einen öffentlichen kurzlebigen Schlüssel in einem serialisierten [*BLOB*](/windows/desktop/SecGloss/b-gly)zurück.

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

*hsslprovider* \[ in\]
</dt> <dd>

Das Handle der SSL-Protokoll Anbieter Instanz.

</dd> <dt>

*HKEY* \[ in\]
</dt> <dd>

Das Handle des zu exportierenden Schlüssels.

Wenn Sie keinen Schlüssel angeben, legen Sie diesen Parameter auf **null** fest.

> [!Note]  
> Ein *HKEY* -Handle wird durch Aufrufen der [**sslopenprivatekey**](sslopenprivatekey.md) -Funktion abgerufen. Handles, die von der [**ncryptopenkey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) -Funktion abgerufen werden, werden nicht unterstützt.

 

</dd> <dt>

*pszblobtype* \[ in\]
</dt> <dd>

Eine mit NULL endenden Unicode-Zeichenfolge, die einen Bezeichner enthält, der den Typ des zu exportierenden BLOBs angibt. Dies kann einer der folgenden Werte sein:



| Wert                                                                                                                                                                                      | Bedeutung                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <dt>**bcrypt \_ dh \_ Public \_ BLOB**</dt> </dl>    | Exportieren Sie einen Diffie-Hellman [*öffentlichen Schlüssel*](/windows/desktop/SecGloss/p-gly). Der *pboutput* -Puffer empfängt eine [**bcrypt \_ DH-Schlüssel- \_ \_ BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) -Struktur, auf die die Schlüsseldaten unmittelbar folgen.<br/>                                                                                                               |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <dt>**bcrypt \_ eccpublic- \_ BLOB**</dt> </dl>     | Exportieren eines öffentlichen Schlüssels der [*elliptischen Kurve Kryptografie*](/windows/desktop/SecGloss/e-gly) (ECC). Der *pboutput* -Puffer empfängt eine [**bcrypt \_ ecckey- \_ blobstruktur**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) , die direkt auf die Schlüsseldaten folgt.<br/>                                                          |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <dt>**bcrypt \_ - \_ Schlüssel- \_ BLOB nicht transparent**</dt> </dl> | Exportieren Sie einen symmetrischen Schlüssel in einem Format, das für einen einzelnen [*Kryptografiedienstanbieter*](/windows/desktop/SecGloss/c-gly) (CSP) spezifisch ist. Nicht transparente BLOBs sind nicht übertragbar und müssen mit demselben *Kryptografiedienstanbieter* (CSP) importiert werden, der das BLOB generiert hat.<br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <dt>**bcrypt \_ rsapublic- \_ BLOB**</dt> </dl>     | Exportieren Sie einen öffentlichen RSA-Schlüssel. Der *pboutput* -Puffer empfängt eine [**bcrypt \_ rsaKey- \_ BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) -Struktur, auf die die Schlüsseldaten unmittelbar folgen.<br/>                                                                                                                                                                                                |



 

</dd> <dt>

*pboutput* \[ Out, optional\]
</dt> <dd>

Die Adresse eines Puffers, der das [*Schlüsselblob*](/windows/desktop/SecGloss/k-gly)empfängt. Der *cboutput* -Parameter enthält die Größe dieses Puffers. Wenn dieser Parameter **null** ist, fügt diese Funktion die erforderliche Größe (in Bytes) in das **DWORD** ein, auf das durch den *pcbresult* -Parameter verwiesen wird.

</dd> <dt>

*cboutput* \[ in\]
</dt> <dd>

Die Größe des *pboutput* -Puffers in Bytes.

</dd> <dt>

*pcbresult* \[ vorgenommen\]
</dt> <dd>

Die Adresse einer **DWORD** -Variablen, die die Anzahl von Bytes empfängt, die in den *pboutput* -Puffer kopiert werden. Wenn der *pboutput* -Parameter beim Aufrufen der-Funktion auf **null** festgelegt ist, wird die erforderliche Größe für den *pboutput* -Puffer in Bytes in dem **DWORD** zurückgegeben, auf das von diesem Parameter verwiesen wird.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. die folgenden:



| Rückgabecode/-wert                                                                                                                                                    | BESCHREIBUNG                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt> </dl> | Eines der bereitgestellten Handles ist ungültig.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die **sslexportkey** -Funktion ermöglicht das Transportieren von Sitzungs Schlüsseln von einem Prozess zu einem anderen und das Exportieren des öffentlichen Teils eines kurzlebigen Schlüssels.

Beim Exportieren von Sitzungs Schlüsseln ist der BLOB-Typ nicht transparent, was bedeutet, dass das BLOB-Format irrelevant ist, solange die Funktionen **sslexportkey** und [**sslimportkey**](sslimportkey.md) Sie interpretieren können.

Beim Exportieren des öffentlichen Teils eines kurzlebigen Schlüssels muss der BLOB-Typ der geeignete Typ sein, z. b. " **NCrypt \_ dh \_ Public \_ BLOB** " oder " **NCrypt \_ eccpublic \_ BLOB**".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

