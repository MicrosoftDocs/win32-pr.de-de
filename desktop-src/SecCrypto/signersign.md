---
description: Signiert die angegebene Datei.
ms.assetid: 5a59e663-057b-4380-aa14-536030e4051d
title: SignerSign-Funktion
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
ms.openlocfilehash: d9756fba3a931ddf09715b5086e613a9395c10c57c82fa18c64007aeb02b615c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117973134"
---
# <a name="signersign-function"></a>SignerSign-Funktion

Die **SignerSign-Funktion** signiert die angegebene Datei.

> [!Note]  
> Dieser Funktion ist keine Headerdatei oder Importbibliothek zugeordnet. Zum Aufrufen dieser Funktion müssen Sie eine benutzerdefinierte Headerdatei erstellen und die [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um eine dynamische Verknüpfung mit Mssign32.dll.

 

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

Ein Zeiger auf eine [**SIGNER \_ PROVIDER \_ INFO-Struktur,**](signer-provider-info.md) die den [](../secgloss/p-gly.md) Kryptografiedienstanbieter (Cryptographic [*Service Provider,*](../secgloss/c-gly.md) CSP) und informationen zum privaten Schlüssel angibt, die zum Erstellen der digitalen Signatur verwendet werden.

Wenn der Wert dieses Parameters **NULL ist,** muss der Wert des *pSignerCert-Parameters* ein Zertifikat angeben, das einem CSP zugeordnet ist.

</dd> <dt>

*pwszHttpTimeStamp* \[ in, optional\]
</dt> <dd>

Die URL eines Zeitstempelservers.

</dd> <dt>

*psRequest* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf ein Array von [**CRYPT \_ ATTRIBUTE-Strukturen,**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) die einer Vorzeichenanforderung hinzugefügt werden. Dieser Parameter wird ignoriert, wenn der *pwszHttpTimeStamp-Parameter* keinen gültigen Wert enthält, der nicht **NULL ist.**

</dd> <dt>

*pSipData* \[ in, optional\]
</dt> <dd>

Ein 32-Bit-Wert, der als zusätzliche Daten an DIE SIP-Funktionen übergeben wird. Das Format und der Inhalt dieses wird vom SIP-Anbieter definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt sie S \_ OK zurück.

Wenn die Funktion fehlschlägt, wird ein **HRESULT-Wert** zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
