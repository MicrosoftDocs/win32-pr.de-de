---
description: Signiert die angegebene Datei und gibt einen Zeiger auf die signierten Daten zurück.
ms.assetid: 9921ffae-2299-4bf2-b76d-77f7f6afb663
title: SignerSignEx-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSignEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 0b880cc02053d5a90089cffc721b057c6fce9f34b8be6517c12ef59fef9e0ed4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898323"
---
# <a name="signersignex-function"></a>SignerSignEx-Funktion

Die **SignerSignEx-Funktion** signiert die angegebene Datei und gibt einen Zeiger auf die signierten Daten zurück.

> [!Note]  
> Dieser Funktion ist keine Headerdatei oder Importbibliothek zugeordnet. Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Headerdatei erstellen und die [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um dynamisch eine Verknüpfung mit Mssign32.dll herzustellen.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI SignerSignEx(
  _In_     DWORD                 dwFlags,
  _In_     SIGNER_SUBJECT_INFO   *pSubjectInfo,
  _In_     SIGNER_CERT           *pSignerCert,
  _In_     SIGNER_SIGNATURE_INFO *pSignatureInfo,
  _In_opt_ SIGNER_PROVIDER_INFO  *pProviderInfo,
  _In_opt_ LPCWSTR               pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES     psRequest,
  _In_opt_ LPVOID                pSipData,
  _Out_    SIGNER_CONTEXT        **ppSignerContext
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Ändert das Verhalten dieser Funktion.

Wenn es sich bei der zu signierten Datei um eine portierbare ausführbare Datei (Portable Executable, PE) handelt, kann dies 0 (null) oder eine Kombination aus einem oder mehreren der folgenden Werte sein. Diese Bezeichner werden in Mssip.h definiert.



| Wert                                                                                                                                                                                                                                                                                    | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPC_EXC_PE_PAGE_HASHES_FLAG"></span><span id="spc_exc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_ EXC \_ PE \_ PAGE \_ HASHES \_ FLAG**</dt> <dt>0x10</dt> </dl>                    | Schließen Sie Seitenhashes beim Erstellen indirekter SIP-Daten für die PE-Datei aus. Dieses Flag hat Vorrang vor dem **FLAG SPC \_ INC PE \_ PAGE \_ \_ HASHES \_ FLAG.**<br/> Wenn weder das **SPC \_ EXC \_ PE PAGE \_ \_ HASHES \_ FLAG** noch das **SPC INC PE PAGE \_ \_ \_ \_ HASHES FLAG \_ Flag** angegeben ist, wird der mit der [**WintrustSetDefaultIncludePEPageHashes-Funktion**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) festgelegte Wert für diese Einstellung verwendet. Die Standardeinstellung für diese Einstellung ist das Ausschließen von Seitenhashes beim Erstellen indirekter SIP-Daten für PE-Dateien.<br/> **Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.<br/> |
| <span id="SPC_INC_PE_IMPORT_ADDR_TABLE_FLAG"></span><span id="spc_inc_pe_import_addr_table_flag"></span><dl> <dt>**SPC \_ INC \_ PE \_ IMPORT \_ ADDR TABLE \_ \_ FLAG**</dt> <dt>0x20</dt> </dl> | Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_DEBUG_INFO_FLAG"></span><span id="spc_inc_pe_debug_info_flag"></span><dl> <dt>**SPC \_ INC \_ PE DEBUG INFO \_ \_ \_ FLAG**</dt> <dt>0x40</dt> </dl>                       | Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_RESOURCES_FLAG"></span><span id="spc_inc_pe_resources_flag"></span><dl> <dt>**SPC \_ INC \_ PE \_ RESOURCES \_ FLAG**</dt> <dt>0x80</dt> </dl>                           | Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_PAGE_HASHES_FLAG"></span><span id="spc_inc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_ INC \_ PE \_ PAGE \_ HASHES \_ FLAG**</dt> <dt>0x100</dt> </dl>                   | Einschließen von Seitenhashes beim Erstellen indirekter SIP-Daten für die PE-Datei.<br/> **Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

*pSubjectInfo* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**SIGNER \_ SUBJECT \_ INFO-Struktur,**](signer-subject-info.md) die das zu signierende Subjekt angibt.

</dd> <dt>

*pSignerCert* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**SIGNER \_ CERT-Struktur,**](signer-cert.md) die das Zertifikat angibt, das zum Erstellen der digitalen Signatur verwendet werden soll.

</dd> <dt>

*pSignatureInfo* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**SIGNER \_ SIGNATURE \_ INFO-Struktur,**](signer-signature-info.md) die Informationen über die digitale Signatur enthält.

</dd> <dt>

*pProviderInfo* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine [**SIGNER \_ PROVIDER \_ INFO-Struktur,**](signer-provider-info.md) die die Informationen des [*Kryptografiedienstanbieters (Cryptographic Service Provider,*](../secgloss/c-gly.md) CSP) und des privaten Schlüssels angibt, die zum Erstellen der digitalen Signatur verwendet werden.

Wenn der Wert dieses Parameters **NULL** ist, muss der Wert des *pSignerCert-Parameters* ein Zertifikat angeben, das einem CSP zugeordnet ist.

</dd> <dt>

*pwszHttpTimeStamp* \[ in, optional\]
</dt> <dd>

Die URL eines Zeitstempelservers.

</dd> <dt>

*psRequest* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf ein Array von [**CRYPT \_ ATTRIBUTE-Strukturen,**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) die einer Sign-Anforderung hinzugefügt werden. Dieser Parameter wird ignoriert, wenn der *pwszHttpTimeStamp-Parameter* keinen gültigen Wert enthält, der nicht **NULL** ist.

</dd> <dt>

*pSipData* \[ in, optional\]
</dt> <dd>

Ein 32-Bit-Wert, der als zusätzliche Daten an DIE SIP-Funktionen übergeben wird. Das Format und der Inhalt dieser werden vom SIP-Anbieter definiert.

</dd> <dt>

*ppSignerContext* \[ out\]
</dt> <dd>

Die Adresse eines Zeigers auf die [**SIGNER \_ CONTEXT-Struktur,**](signer-context.md) die das signierte [*BLOB*](../secgloss/b-gly.md)enthält. Wenn Sie die **SIGNER \_ CONTEXT-Struktur** nicht mehr verwenden, können Sie die **SIGNER \_ CONTEXT-Struktur** freigeben, indem Sie die [**SignerFreeSignerContext-Funktion**](signerfreesignercontext.md) aufrufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt die Funktion S \_ OK zurück.

Wenn die Funktion fehlschlägt, wird ein **HRESULT-Wert** zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte.](common-hresult-values.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerFreeSignerContext**](signerfreesignercontext.md)
</dt> </dl>

 

 
