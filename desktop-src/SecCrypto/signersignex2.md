---
description: Signiert und Zeitstempel der angegebenen Datei, sodass mehrere Unterschriften zugelassen werden.
ms.assetid: 216EFFCF-CD23-484A-ADBF-94B5AD52289F
title: SignerSignEx2-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSignEx2
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: a03d326969ce1f447dc82708792bd3761e02a823
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217618"
---
# <a name="signersignex2-function"></a>SignerSignEx2-Funktion

Die **SignerSignEx2** -Funktion signiert und Zeitstempel für die angegebene Datei, sodass mehrere unterschiedliche Signaturen möglich sind.

> [!Note]  
> Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek. Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI SignerSignEx2(
  _In_       DWORD                  dwFlags,
  _In_       SIGNER_SUBJECT_INFO    *pSubjectInfo,
  _In_       SIGNER_CERT            *pSignerCert,
  _In_       SIGNER_SIGNATURE_INFO  *pSignatureInfo,
  _In_opt_   SIGNER_PROVIDER_INFO   *pProviderInfo,
  _In_opt_   DWORD                  dwTimestampFlags,
  _In_opt_   PCSTR                  pszTimestampAlgorithmOid,
  _In_opt_   PCWSTR                 pwszHttpTimeStamp,
  _In_opt_   PCRYPT_ATTRIBUTES      psRequest,
  _In_opt_   PVOID                  pSipData,
  _Out_      SIGNER_CONTEXT         **ppSignerContext,
  _In_opt_   PCERT_STRONG_SIGN_PARA pCryptoPolicy,
  _Reserved_ PVOID                  pReserved
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Ändert das Verhalten dieser Funktion.

Wenn es sich bei der zu Signier enden Datei um eine portable ausführbare Datei (PE) handelt, kann diese 0 (null) oder eine Kombination aus einem oder mehreren der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                                                                    | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPC_EXC_PE_PAGE_HASHES_FLAG"></span><span id="spc_exc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_ Exkl \_ PE \_ \_ Seitenhashes, \_ Flag**</dt> <dt>0x10</dt> </dl>                    | Ausschließen von Seitenhashes beim Erstellen von SIP-indirekten Daten für die PE-Datei. Dieses Flag hat Vorrang vor dem **Flag "SPC \_ Inc \_ PE \_ \_ Seitenhashes \_** ".<br/> Wenn weder der Befehl " **SPC \_ EXC \_ PE \_ Page \_ Hashes \_** " noch das Flag " **SPC \_ Inc \_ PE \_ Page \_ Hashes \_** Flag Flag" angegeben ist, wird der mit der [**wintrustsetdefaultincludegpgehashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) -Funktion festgelegte Wert für diese Einstellung verwendet. Der Standardwert für diese Einstellung besteht darin, Seitenhashes auszuschließen, wenn indirekte SIP-Daten für PE-Dateien erstellt werden.<br/> Dieser Wert wird in der Header Datei "mssip. h" definiert.<br/> **Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.<br/> |
| <span id="SPC_INC_PE_IMPORT_ADDR_TABLE_FLAG"></span><span id="spc_inc_pe_import_addr_table_flag"></span><dl> <dt>**SPC \_ Inkl \_ PE \_ Import \_ addr \_ - \_ Tabellenflag**</dt> <dt>0x20</dt> </dl> | Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_DEBUG_INFO_FLAG"></span><span id="spc_inc_pe_debug_info_flag"></span><dl> <dt>**SPC \_ Inc \_ PE \_ - \_ debuginfoflag \_**</dt> <dt>0x40</dt> </dl>                       | Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_RESOURCES_FLAG"></span><span id="spc_inc_pe_resources_flag"></span><dl> <dt>**SPC \_ Inkl \_ PE \_ Resources- \_ Flag**</dt> <dt>0x80</dt> </dl>                           | Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_PAGE_HASHES_FLAG"></span><span id="spc_inc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_ Inkl \_ . \_ \_ Seitenhashes- \_ Flag**</dt> <dt>0x100</dt> </dl>                   | Einschließen von Seitenhashes beim Erstellen von SIP-indirekten Daten für die PE-Datei.<br/> **Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.<br/> Dieser Wert wird in der Header Datei "mssip. h" definiert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SIG_APPEND"></span><span id="sig_append"></span><dl> <dt>**Sig \_**</dt> <dt>0x1000</dt> anfügen </dl>                                                                         | Die Signatur wird eingefügt. Wenn Sie dieses Flag festlegen, bevor eine Signatur hinzugefügt wurde, wird die generierte Signatur als äußere Signatur hinzugefügt. Wenn Sie dieses Flag nicht festlegen, ersetzt die generierte Signatur die äußere Signatur, wobei alle inneren Signaturen gelöscht werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

*psubjetinfo* \[ in\]
</dt> <dd>

Ein Zeiger auf die [**\_ \_ Informations**](signer-subject-info.md) Struktur des Signatur Gebers, die den Betreff angibt, der signiert werden soll.

</dd> <dt>

*psignercert* \[ in\]
</dt> <dd>

Zeiger auf eine [**Signatur Geber- \_ CERT**](signer-cert.md) -Struktur, die das Zertifikat angibt, das zum Erstellen der digitalen Signatur verwendet werden soll.

</dd> <dt>

*psignatureinfo* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**\_ Signatur \_**](signer-signature-info.md) Informationsstruktur, die Informationen zur digitalen Signatur enthält.

</dd> <dt>

*pproviderinfo* \[ in, optional\]
</dt> <dd>

Zeiger auf eine Informationsstruktur des [**Signatur Gebers \_ Anbieters \_**](signer-provider-info.md) , die die Informationen zum [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP) und zum privaten Schlüssel angibt, die zum Erstellen der digitalen Signatur verwendet werden.

Wenn der Wert dieses Parameters **null** ist, muss der *psignercert* -Parameter ein Zertifikat angeben, das einem CSP zugeordnet ist.

</dd> <dt>

*dwtimestampflags* \[ in, optional\]
</dt> <dd>

Flags, die an [**SignerTimeStampEx3**](signertimestampex3.md) übergeben werden, wenn der *pwszhttptimestamp* -Parameter nicht **null** ist. Dies kann einer der folgenden Werte sein:



| Wert                                                                                                                                                                                                          | Bedeutung                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <dt>**Signatur Geber- \_ Zeitstempel \_ Authenticode**</dt> </dl> | Standardwert. Gibt einen Authenticode-Zeitstempel an.<br/> |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <dt>**Signatur Geber- \_ Zeitstempel \_ Timestampserver**</dt> </dl>                | Gibt einen RFC 3161-Zeitstempel an.<br/>                    |



 

Dieser Parameter wird ignoriert, wenn der *pwszhttptimestamp* -Parameter **null** ist.

</dd> <dt>

*psztimestampalgorithmuid* \[ in, optional\]
</dt> <dd>

Der Objekt Bezeichner des Algorithmus, der zum Erstellen eines RFC 3161-Zeitstempels verwendet werden soll. Dieser Parameter wird bei Authenticode-Zeitstempeln ignoriert.

</dd> <dt>

*pwszhttptimestamp* \[ in, optional\]
</dt> <dd>

Die URL des Zeitstempel Servers.

</dd> <dt>

*psrequest* \[ in, optional\]
</dt> <dd>

Zeiger auf ein Array von [**crypt- \_ Attribut**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) Strukturen, die einer Signierungs Anforderung hinzugefügt werden. Dieser Parameter wird ignoriert, wenn der *pwszhttptimestamp* -Parameter keinen gültigen Wert enthält oder **null** ist.

</dd> <dt>

*psipdata* \[ in, optional\]
</dt> <dd>

Ein 32-Bit-Wert, der als zusätzliche Daten an SIP-Funktionen weitergeleitet wird. Das Format und der Inhalt dieser werden vom SIP-Anbieter definiert.

</dd> <dt>

*ppsignercontext* \[ vorgenommen\]
</dt> <dd>

Die Adresse eines Zeigers auf die [**Signatur Geber- \_ Kontext**](signer-context.md) Struktur, die das signierte [*BLOB*](../secgloss/b-gly.md)enthält. Wenn Sie mit der Verwendung der **Signatur Geber- \_ Kontext** Struktur fertig sind, können Sie die Signatur Geber- **\_ Kontext** Struktur durch Aufrufen der [**signerfreesignercontext**](signerfreesignercontext.md) -Funktion freigeben.

</dd> <dt>

*pcryptopolicy* \[ in, optional\]
</dt> <dd>

Falls vorhanden, ein Zeiger auf eine [**CERT \_ Strong \_ Sign \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) Structure-Struktur, die die Parameter enthält, die für die Überprüfung auf starke Signaturen verwendet werden. Wenn entweder ein Zertifikat oder die zugehörige Kette nicht bestanden wird, wird die Datei in keiner Weise geändert. Wenn eine URL zum Angeben einer Zeitstempel Stelle (Time Stamp Authority, TSA) übermittelt wird, wird diese Richtlinie auch auf den Zeitstempel angewendet.

</dd> <dt>

*erhaltene* 
</dt> <dd>

Reserviert. Dieser Wert muss **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion S \_ OK zurück.

Wenn die Funktion fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt. Mögliche Fehlercodes, die von dieser Funktion zurückgegeben werden, sind u. a. die folgenden. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).



| Rückgabecode                                                                                  | Beschreibung                                                                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Wenn Sie den Parameter " *dwtimestampflags* " auf den Signatur Geber- **\_ Zeitstempel \_ Authenticode** festgelegt haben, können Sie den *dwFlags* -Parameter nicht auf **sig \_ Append** festlegen.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Signersign**](signersign.md)
</dt> <dt>

[**Signersignetx**](signersignex.md)
</dt> <dt>

[**Signerfresignercontext**](signerfreesignercontext.md)
</dt> </dl>

 

 
