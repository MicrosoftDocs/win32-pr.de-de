---
description: Gibt das Handle für einen Kryptografiedienstanbieter (CSP) frei und löscht optional den temporären Container, der von der getcryptprovfromcert-Funktion erstellt wurde.
ms.assetid: 4462eef2-7056-4e48-aa96-c46f29b701d6
title: Freecryptprovfromcert-Funktion
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
ms.openlocfilehash: 8201de475a4224aea58267405ccde244e56d59f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867423"
---
# <a name="freecryptprovfromcert-function"></a>Freecryptprovfromcert-Funktion

> [!IMPORTANT]
> Diese API ist veraltet. Microsoft kann diese API in zukünftigen Versionen entfernen.

 

Die Funktion **freecryptprovfromcert** gibt das Handle für einen [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) frei und löscht optional den temporären Container, der von der [**getcryptprovfromcert**](getcryptprovfromcert.md) -Funktion erstellt wurde.

> [!Note]  
> Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek. Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.

 

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

*facettrot* \[ in\]
</dt> <dd>

Ein-Wert, der angibt, ob das Anbieter Handle aus dem [*Zertifikat*](../secgloss/c-gly.md)abgerufen wurde.

</dd> <dt>

*hprov* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**hcryptprov**](hcryptprov.md) -Struktur für den CSP.

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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
