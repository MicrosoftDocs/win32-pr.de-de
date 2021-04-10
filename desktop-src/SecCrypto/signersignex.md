---
description: Signiert die angegebene Datei und gibt einen Zeiger auf die signierten Daten zurück.
ms.assetid: 9921ffae-2299-4bf2-b76d-77f7f6afb663
title: Signersignetx-Funktion
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
ms.openlocfilehash: 9944a09459219ccac74f5fafc9424e9f85a01112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755561"
---
# <a name="signersignex-function"></a>Signersignetx-Funktion

Die **signersignetx** -Funktion signiert die angegebene Datei und gibt einen Zeiger auf die signierten Daten zurück.

> [!Note]  
> Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek. Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.

 

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

*dwFlags* \[ in\]
</dt> <dd>

Ändert das Verhalten dieser Funktion.

Wenn es sich bei der zu Signier enden Datei um eine portable ausführbare Datei (PE) handelt, kann diese 0 (null) oder eine Kombination aus einem oder mehreren der folgenden Werte sein. Diese Bezeichner sind in "mssip. h" definiert.



| Wert                                                                                                                                                                                                                                                                                    | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPC_EXC_PE_PAGE_HASHES_FLAG"></span><span id="spc_exc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_ Exkl \_ PE \_ \_ Seitenhashes, \_ Flag**</dt> <dt>0x10</dt> </dl>                    | Ausschließen von Seitenhashes beim Erstellen von SIP-indirekten Daten für die PE-Datei. Dieses Flag hat Vorrang vor dem **Flag "SPC \_ Inc \_ PE \_ \_ Seitenhashes \_** ".<br/> Wenn weder der Befehl " **SPC \_ EXC \_ PE \_ Page \_ Hashes \_** " noch das Flag " **SPC \_ Inc \_ PE \_ Page \_ Hashes \_** Flag Flag" angegeben ist, wird der mit der [**wintrustsetdefaultincludegpgehashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) -Funktion festgelegte Wert für diese Einstellung verwendet. Der Standardwert für diese Einstellung besteht darin, Seitenhashes auszuschließen, wenn indirekte SIP-Daten für PE-Dateien erstellt werden.<br/> **Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.<br/> |
| <span id="SPC_INC_PE_IMPORT_ADDR_TABLE_FLAG"></span><span id="spc_inc_pe_import_addr_table_flag"></span><dl> <dt>**SPC \_ Inkl \_ PE \_ Import \_ addr \_ - \_ Tabellenflag**</dt> <dt>0x20</dt> </dl> | Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_DEBUG_INFO_FLAG"></span><span id="spc_inc_pe_debug_info_flag"></span><dl> <dt>**SPC \_ Inc \_ PE \_ - \_ debuginfoflag \_**</dt> <dt>0x40</dt> </dl>                       | Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_RESOURCES_FLAG"></span><span id="spc_inc_pe_resources_flag"></span><dl> <dt>**SPC \_ Inkl \_ PE \_ Resources- \_ Flag**</dt> <dt>0x80</dt> </dl>                           | Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_PAGE_HASHES_FLAG"></span><span id="spc_inc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_ Inkl \_ . \_ \_ Seitenhashes- \_ Flag**</dt> <dt>0x100</dt> </dl>                   | Einschließen von Seitenhashes beim Erstellen von SIP-indirekten Daten für die PE-Datei.<br/> **Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

*psubjetinfo* \[ in\]
</dt> <dd>

Ein Zeiger auf die [**\_ \_ Info**](signer-subject-info.md) -Struktur des Signatur Gebers, die den Betreff angibt, der signiert werden soll.

</dd> <dt>

*psignercert* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**Signatur Geber \_**](signer-cert.md) -Zertifikat Struktur, die das Zertifikat angibt, das zum Erstellen der digitalen Signatur verwendet werden soll.

</dd> <dt>

*psignatureinfo* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**\_ Signatur \_**](signer-signature-info.md) Informationsstruktur, die Informationen zur digitalen Signatur enthält.

</dd> <dt>

*pproviderinfo* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine Informationsstruktur des [**Signatur Gebers \_ Anbieters \_**](signer-provider-info.md) , die die Informationen zum [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP) und zum privaten Schlüssel angibt, die zum Erstellen der digitalen Signatur verwendet werden.

Wenn der Wert dieses Parameters **null** ist, muss der Wert des *psignercert* -Parameters ein Zertifikat angeben, das einem CSP zugeordnet ist.

</dd> <dt>

*pwszhttptimestamp* \[ in, optional\]
</dt> <dd>

Die URL eines Zeitstempel Servers.

</dd> <dt>

*psrequest* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf ein Array von [**crypt- \_ Attribut**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) Strukturen, die einer Signierungs Anforderung hinzugefügt werden. Dieser Parameter wird ignoriert, wenn der *pwszhttptimestamp* -Parameter keinen gültigen Wert enthält, der nicht **null** ist.

</dd> <dt>

*psipdata* \[ in, optional\]
</dt> <dd>

Ein 32-Bit-Wert, der als zusätzliche Daten an SIP-Funktionen weitergeleitet wird. Das Format und der Inhalt dieser werden vom SIP-Anbieter definiert.

</dd> <dt>

*ppsignercontext* \[ vorgenommen\]
</dt> <dd>

Die Adresse eines Zeigers auf die [**Signatur Geber- \_ Kontext**](signer-context.md) Struktur, die das signierte [*BLOB*](../secgloss/b-gly.md)enthält. Wenn Sie mit der Verwendung der **Signatur Geber- \_ Kontext** Struktur fertig sind, können Sie die Signatur Geber- **\_ Kontext** Struktur durch Aufrufen der [**signerfreesignercontext**](signerfreesignercontext.md) -Funktion freigeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion S \_ OK zurück.

Wenn die Funktion fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Signersign**](signersign.md)
</dt> <dt>

[**Signerfresignercontext**](signerfreesignercontext.md)
</dt> </dl>

 

 
