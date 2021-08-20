---
description: Erstellt einen temporären Container im Kryptografiedienstanbieter (Cryptographic Service Provider, CSP) und lädt einen privaten Schlüssel aus dem Arbeitsspeicher in den Container.
ms.assetid: 9388b49b-fad4-4499-a391-fe58ed672552
title: PvkPrivateKeyAcquireContextFromMemory-Funktion
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
ms.openlocfilehash: 3f22e6135fbad3ed4919ec44620f5b1234f17b21c27b0a3048848d258adabbd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117975864"
---
# <a name="pvkprivatekeyacquirecontextfrommemory-function"></a>PvkPrivateKeyAcquireContextFromMemory-Funktion

> [!IMPORTANT]
> Diese API ist veraltet. Microsoft kann diese API in zukünftigen Versionen entfernen.

 

Die **PvkPrivateKeyAcquireContextFromMemory-Funktion** erstellt einen temporären Container im [*Kryptografiedienstanbieter (Cryptographic Service Provider,*](../secgloss/c-gly.md) CSP) und lädt einen [*privaten Schlüssel*](../secgloss/p-gly.md) aus dem Arbeitsspeicher in den Container.

> [!Note]  
> Dieser Funktion ist keine Headerdatei oder Importbibliothek zugeordnet. Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Headerdatei erstellen und die [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um dynamisch eine Verknüpfung mit Mssign32.dll herzustellen.

 

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

*pwszProvName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des CSP enthält, dessen Typ in *dwProvType* angefordert wird.

</dd> <dt>

*dwProvType* \[ In\]
</dt> <dd>

Ein **DWORD-Wert** für den CSP-Typ. Weitere Informationen zu CSP-Typen finden Sie unter [Kryptografieanbietertypen.](cryptographic-provider-types.md)

</dd> <dt>

*pbData* \[ In\]
</dt> <dd>

Ein Zeiger auf einen Puffer, um die Kontextdaten zu empfangen. Der Aufrufer muss diese Ressource bereitstellen.

</dd> <dt>

*cbData* \[ In\]
</dt> <dd>

Ein **DWORD-Wert,** der die Größe des *pbData-Puffers* in Bytes angibt. Der Aufrufer muss diesen Wert angeben.

</dd> <dt>

*hwndOwner* \[ In\]
</dt> <dd>

Wenn zum Entschlüsseln der Kontextdaten, auf die der *pbData-Parameter* verweist, ein Kennwort erforderlich ist, ist dieser Parameter ein Handle für das übergeordnete Element des Dialogfelds. Andernfalls ist es **NULL.**

</dd> <dt>

*pwszKeyName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des abzurufenden Schlüssels enthält.

</dd> <dt>

*pdwKeySpec* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf einen **DWORD-Wert,** der den Typ des Schlüssels angibt. Mögliche Werte sind **AT \_ KEYEXCHANGE** oder **AT \_ SIGNATURE.**

</dd> <dt>

*phCryptProv* \[ out\]
</dt> <dd>

Ein Zeiger auf ein Handle für den CSP.

</dd> <dt>

*ppwszTmpContainer* \[ out\]
</dt> <dd>

Die Adresse eines Zeigers auf eine auf NULL endende Zeichenfolge für den temporären Containernamen. Die **PvkPrivateKeyAcquireContextFromMemory-Funktion** stellt den Puffer für diese Zeichenfolge bereit und initialisiert sie. Beim Aufrufen von **PvkPrivateKeyAcquireContextFromMemory** sollte die Adresse auf einen **NULL-Wert** verweisen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg gibt diese Funktion **TRUE** zurück. Die **PvkPrivateKeyAcquireContextFromMemory-Funktion** gibt **FALSE** zurück, wenn sie fehlschlägt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
