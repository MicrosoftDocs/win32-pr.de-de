---
description: Erstellt einen temporären Container im Kryptografiedienstanbieter (kryptografischen Service Provider, CSP) und lädt einen privaten Schlüssel aus dem Arbeitsspeicher in den Container.
ms.assetid: 9388b49b-fad4-4499-a391-fe58ed672552
title: Pvkprivatekeyacquirecontextfrommemory-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkPrivateKeyAcquireContextFromMemory
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 1552d1e35845ffb7407d11d6e520b914ab805d50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348488"
---
# <a name="pvkprivatekeyacquirecontextfrommemory-function"></a>Pvkprivatekeyacquirecontextfrommemory-Funktion

> [!IMPORTANT]
> Diese API ist veraltet. Microsoft kann diese API in zukünftigen Versionen entfernen.

 

Die **pvkprivatekeyacquirecontextfrommemory** -Funktion erstellt einen temporären Container im [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) und lädt einen [*privaten Schlüssel*](../secgloss/p-gly.md) aus dem Arbeitsspeicher in den Container.

> [!Note]  
> Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek. Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.

 

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI PvkPrivateKeyAcquireContextFromMemory(
  _In_        LPCWSTR    pwszProvName,
  _In_        DWORD      dwProvType,
  _In_        BYTE       *pbData,
  _In_        DWORD      cbData,
  _In_        HWND       hwndOwner,
  _In_        LPCWSTR    pwszKeyName,
  _Inout_opt_ DWORD      *pdwKeySpec,
  _Out_       HCRYPTPROV *phCryptProv,
  _Out_       LPTSTR     *ppwszTmpContainer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwszprovname* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des CSP enthält, dessen Typ in *dwprovtype* angefordert wird.

</dd> <dt>

*dwprovtype* \[ in\]
</dt> <dd>

Ein **DWORD** -Wert für den CSP-Typ. Weitere Informationen zu CSP-Typen finden Sie unter [Typen von Kryptografieanbietern](cryptographic-provider-types.md).

</dd> <dt>

*pbData* \[ in\]
</dt> <dd>

Ein Zeiger auf einen Puffer, um die Kontext Daten zu empfangen. Der Aufrufer muss diese Ressource bereitstellen.

</dd> <dt>

*cbData* \[ in\]
</dt> <dd>

Ein **DWORD** -Wert, der die Größe des *pbData* -Puffers in Bytes angibt. Der Aufrufer muss diesen Wert angeben.

</dd> <dt>

*hwndOwner* \[ in\]
</dt> <dd>

Wenn ein Kennwort zum Entschlüsseln der Kontext Daten erforderlich ist, auf die durch den *pbData* -Parameter verwiesen wird, ist dieser Parameter ein Handle für das übergeordnete Dialogfeld. Andernfalls ist der Wert **null**.

</dd> <dt>

*pwszkeyname* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des abzurufenden Schlüssels enthält.

</dd> <dt>

*pdwkeyspec* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf einen **DWORD** -Wert, der den Typ des Schlüssels angibt. Mögliche Werte sind **bei \_ keyexchange** oder **bei \_ Signatur**.

</dd> <dt>

*phcryptprov* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf ein Handle für den CSP.

</dd> <dt>

*ppwsztmpcontainer* \[ vorgenommen\]
</dt> <dd>

Die Adresse eines Zeigers auf eine NULL-terminierte Zeichenfolge für den temporären Container Namen. Die **pvkprivatekeyacquirecontextfrommemory** -Funktion stellt den Puffer für diese Zeichenfolge bereit und initialisiert sie. Beim Aufrufen von **pvkprivatekeyacquirecontextfrommemory** sollte die Adresse auf einen **null** -Wert zeigen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg gibt diese Funktion " **true**" zurück. Die **pvkprivatekeyacquirecontextfrommemory** -Funktion gibt **false** zurück, wenn Sie fehlschlägt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
