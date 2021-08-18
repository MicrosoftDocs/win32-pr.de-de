---
description: 'Gibt das Handle entweder an einen Kryptografiedienstanbieter (Cryptographic Service Provider, CSP) oder an einen CNG-Schlüssel (Cryptography API: Next Generation) frei.'
ms.assetid: 76cbf8ae-c4ab-43d9-b06d-ea0b2a66368a
title: FreeCryptProvFromCertEx-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeCryptProvFromCertEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: b887fd7cd37e8963430378590552273b0856dc2cf73e9d0da15ab41a5a622447
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006738"
---
# <a name="freecryptprovfromcertex-function"></a>FreeCryptProvFromCertEx-Funktion

Die **FreeCryptProvFromCertEx-Funktion** gibt das Handle entweder an einen [*Kryptografiedienstanbieter (Cryptographic Service Provider,*](../secgloss/c-gly.md) CSP) oder an einen CNG-Schlüssel (Cryptography API: Next Generation) frei.

> [!Note]  
> Dieser Funktion ist keine Headerdatei oder Importbibliothek zugeordnet. Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Headerdatei erstellen und die [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um dynamisch eine Verknüpfung mit Mssign32.dll herzustellen.

 

## <a name="syntax"></a>Syntax


```C++
void WINAPI FreeCryptProvFromCertEx(
  _In_     BOOL                            fAcquired,
  _In_     HCRYPTPROV_OR_NCRYPT_KEY_HANDLE hProv,
           DWORD                           dwKeySpec,
  _In_opt_ LPWSTR                          pwszCapiProvider,
  _In_     DWORD                           dwProviderType,
  _In_opt_ LPWSTR                          pwszTmpContainer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fAcquired* \[ In\]
</dt> <dd>

Ein -Wert, der angibt, ob das Anbieterhandle aus dem [*Zertifikat*](../secgloss/c-gly.md)bezogen wurde.

</dd> <dt>

*hProv* \[ In\]
</dt> <dd>

Ein Handle für einen CAPICOM-CSP oder ein Handle für einen CNG-Schlüssel.

</dd> <dt>

*dwKeySpec* 
</dt> <dd>

Die Adresse einer **DWORD-Variablen,** die zusätzliche Informationen zum Schlüssel empfängt. Dies kann einer der folgenden Werte sein.



| Wert                                                                                                                                                                                | Bedeutung                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <dt>**AT \_ KEYEXCHANGE**</dt> </dl>                     | Das Schlüsselpaar ist ein Schlüsselaustauschpaar.<br/>                                                                  |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <dt>**AT \_ SIGNATURE**</dt> </dl>                           | Das Schlüsselpaar ist ein Signaturpaar.<br/>                                                                     |
| <span id="CERT_NCRYPT_KEY_SPEC"></span><span id="cert_ncrypt_key_spec"></span><dl> <dt>**CERT \_ NCRYPT \_ KEY \_ SPEC**</dt> </dl> | Der Schlüssel ist ein CNG-Schlüssel.<br/> **Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.<br/> |



 

</dd> <dt>

*pwszCapiProvider* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge für den Anbieternamen.

</dd> <dt>

*dwProviderType* \[ In\]
</dt> <dd>

Gibt den CSP-Typ an. Dies kann 0 (null) oder einer der [Kryptografieanbietertypen sein.](cryptographic-provider-types.md) Wenn dieser Member 0 (null) ist, ist der Schlüsselcontainer einer der CNG-Schlüsselspeicheranbieter.

</dd> <dt>

*pwszTmpContainer* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge für den Namen des temporären Schlüsselcontainers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
