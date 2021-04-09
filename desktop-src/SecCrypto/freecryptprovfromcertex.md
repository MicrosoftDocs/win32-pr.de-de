---
description: 'Gibt das Handle entweder für einen Kryptografiedienstanbieter (kryptografischen Service Provider, CSP) oder für einen CNG-Schlüssel (Cryptography API: Next Generation) frei.'
ms.assetid: 76cbf8ae-c4ab-43d9-b06d-ea0b2a66368a
title: Freecryptprovfromcertex-Funktion
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
ms.openlocfilehash: 1be6270ebf9320a9c7527736b9fc4894cd50de9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867420"
---
# <a name="freecryptprovfromcertex-function"></a>Freecryptprovfromcertex-Funktion

Die **freecryptprovfromcertex** -Funktion gibt das Handle entweder für einen [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) oder für einen CNG-Schlüssel (Cryptography API: Next Generation) frei.

> [!Note]  
> Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek. Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.

 

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

*facettrot* \[ in\]
</dt> <dd>

Ein-Wert, der angibt, ob das Anbieter Handle aus dem [*Zertifikat*](../secgloss/c-gly.md)abgerufen wurde.

</dd> <dt>

*hprov* \[ in\]
</dt> <dd>

Ein Handle für einen CAPICOM-CSP oder ein Handle für einen CNG-Schlüssel.

</dd> <dt>

*dwkeyspec* 
</dt> <dd>

Die Adresse einer **DWORD** -Variablen, die zusätzliche Informationen über den Schlüssel empfängt. Dies kann einer der folgenden Werte sein:



| Wert                                                                                                                                                                                | Bedeutung                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <dt>**bei \_ keyexchange**</dt> </dl>                     | Das Schlüsselpaar ist ein Schlüsselaustausch Paar.<br/>                                                                  |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <dt>**bei \_ Signatur**</dt> </dl>                           | Das Schlüsselpaar ist ein Signatur Paar.<br/>                                                                     |
| <span id="CERT_NCRYPT_KEY_SPEC"></span><span id="cert_ncrypt_key_spec"></span><dl> <dt>**Zertifikat- \_ NCrypt- \_ Schlüssel \_ Spezifikation**</dt> </dl> | Der Schlüssel ist ein CNG-Schlüssel.<br/> **Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.<br/> |



 

</dd> <dt>

*pwszcapiprovider* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge für den Anbieter Namen.

</dd> <dt>

*dwprovidertype* \[ in\]
</dt> <dd>

Gibt den CSP-Typ an. Dies kann NULL oder einer der [kryptografieanbiettypen](cryptographic-provider-types.md)sein. Wenn dieser Member 0 (null) ist, ist der Schlüssel Container einer der CNG-Schlüsselspeicher Anbieter.

</dd> <dt>

*pwsztmpcontainer* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge für den Namen des temporären Schlüssel Containers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
