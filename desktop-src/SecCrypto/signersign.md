---
description: Signiert die angegebene Datei.
ms.assetid: 5a59e663-057b-4380-aa14-536030e4051d
title: Signersign-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSign
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 9aa8ecc15e38c4a502b363898d5845cba5b0e47e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349340"
---
# <a name="signersign-function"></a>Signersign-Funktion

Die **signersign** -Funktion signiert die angegebene Datei.

> [!Note]  
> Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek. Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI SignerSign(
  _In_     SIGNER_SUBJECT_INFO   *pSubjectInfo,
  _In_     SIGNER_CERT           *pSignerCert,
  _In_     SIGNER_SIGNATURE_INFO *pSignatureInfo,
  _In_opt_ SIGNER_PROVIDER_INFO  *pProviderInfo,
  _In_opt_ LPCWSTR               pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES     psRequest,
  _In_opt_ LPVOID                pSipData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

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

Ein Zeiger auf eine Informationsstruktur des [**Signatur Gebers \_ Anbieters \_**](signer-provider-info.md) , die die Informationen zum [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP) und zum [*privaten Schlüssel*](../secgloss/p-gly.md) angibt, die zum Erstellen der digitalen Signatur verwendet werden.

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

[**Signersignetx**](signersignex.md)
</dt> </dl>

 

 
