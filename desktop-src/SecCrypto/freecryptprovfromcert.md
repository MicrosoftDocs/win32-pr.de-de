---
description: Gibt das Handle für einen Kryptografiedienstanbieter (Cryptographic Service Provider, CSP) frei und löscht optional den temporären Container, der von der GetCryptProvFromCert-Funktion erstellt wurde.
ms.assetid: 4462eef2-7056-4e48-aa96-c46f29b701d6
title: FreeCryptProvFromCert-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeCryptProvFromCert
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 8797a6f48bcfb973a6c07a4b05ae0d39bc3b4522ab6f7ae70a80eaa77081da44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006788"
---
# <a name="freecryptprovfromcert-function"></a>FreeCryptProvFromCert-Funktion

> [!IMPORTANT]
> Diese API ist veraltet. Microsoft kann diese API in zukünftigen Versionen entfernen.

 

Die **FreeCryptProvFromCert-Funktion** gibt das Handle für einen Kryptografiedienstanbieter (Cryptographic [*Service Provider,*](../secgloss/c-gly.md) CSP) frei und löscht optional den temporären Container, der von der [**GetCryptProvFromCert-Funktion erstellt**](getcryptprovfromcert.md) wurde.

> [!Note]  
> Dieser Funktion ist keine Headerdatei oder Importbibliothek zugeordnet. Zum Aufrufen dieser Funktion müssen Sie eine benutzerdefinierte Headerdatei erstellen und die [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um eine dynamische Verknüpfung mit Mssign32.dll.

 

## <a name="syntax"></a>Syntax


```C++
void WINAPI FreeCryptProvFromCert(
  _In_     BOOL       fAcquired,
  _In_     HCRYPTPROV hProv,
  _In_opt_ LPWSTR     pwszCapiProvider,
  _In_     DWORD      dwProviderType,
  _In_opt_ LPWSTR     pwszTmpContainer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fAcquired* \[ In\]
</dt> <dd>

Ein -Wert, der angibt, ob das Anbieterhand handle aus dem Zertifikat übernommen [*wurde.*](../secgloss/c-gly.md)

</dd> <dt>

*hProv* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**HCRYPTPROV-Struktur**](hcryptprov.md) für den CSP.

</dd> <dt>

*pwszCapiProvider* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge für den Anbieternamen.

</dd> <dt>

*dwProviderType* \[ In\]
</dt> <dd>

Gibt den CSP-Typ an. Dies kann 0 (null) oder einer der [Kryptografieanbietertypen sein.](cryptographic-provider-types.md) Wenn dieser Member 0 (null) ist, ist der Schlüsselcontainer einer der CNG-Schlüsselspeicheranbieter.

</dd> <dt>

*pwszTmpContainer* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge für den Namen des temporären Schlüsselcontainers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
