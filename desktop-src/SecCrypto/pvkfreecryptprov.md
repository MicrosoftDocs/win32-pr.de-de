---
description: Gibt das Handle für einen Kryptografiedienstanbieter (CSP) frei und löscht optional den temporären Container, der von der pvkgetcryptprov-Funktion erstellt wurde.
ms.assetid: e7dcb5c5-dd80-4810-bf1f-4b7b921fa22c
title: Pvkfreecryptprov-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkFreeCryptProv
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 70ff29c968fe8f50c813f1da71b2e73a112f25f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349657"
---
# <a name="pvkfreecryptprov-function"></a>Pvkfreecryptprov-Funktion

> [!IMPORTANT]
> Diese API ist veraltet. Microsoft kann diese API in zukünftigen Versionen entfernen.

 

Die **pvkfreecryptprov** -Funktion gibt das Handle für einen [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) frei und löscht optional den temporären Container, der von der Funktion [**pvkgetcryptprov**](pvkgetcryptprov.md) erstellt wurde.

> [!Note]  
> Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek. Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.

 

## <a name="syntax"></a>Syntax


```C++
void WINAPI PvkFreeCryptProv(
  _In_     HCRYPTPROV hProv,
  _In_     LPCWSTR    pwszCapiProvider,
  _In_     DWORD      dwProviderType,
  _In_opt_ LPWSTR     pwszTmpContainer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprov* \[ in\]
</dt> <dd>

Ein Handle für den CSP.

</dd> <dt>

*pwszcapiprovider* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge für den CSP-Namen.

</dd> <dt>

*dwprovidertype* \[ in\]
</dt> <dd>

Ein **DWORD** -Wert, der den Typ des Kryptografieanbieters darstellt. Weitere Informationen finden Sie unter [Typen von Kryptografieanbietern](cryptographic-provider-types.md).

</dd> <dt>

*pwsztmpcontainer* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge für den temporären Schlüssel Container Namen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
