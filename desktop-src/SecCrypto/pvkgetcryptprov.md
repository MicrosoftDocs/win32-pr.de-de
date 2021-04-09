---
description: Ruft ein Handle für einen Kryptografiedienstanbieter (CSP) basierend auf einer Datei mit einem privaten Schlüssel oder einem Schlüssel Container Namen ab.
ms.assetid: 82cdaa6f-e747-4c9d-8d2d-5fa206891eed
title: Pvkgetcryptprov-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkGetCryptProv
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 026b31d021dc6ff2569ad9ce8f17d2e7f0d17b29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869000"
---
# <a name="pvkgetcryptprov-function"></a>Pvkgetcryptprov-Funktion

> [!IMPORTANT]
> Diese API ist veraltet. Microsoft kann diese API in zukünftigen Versionen entfernen.

 

Die **pvkgetcryptprov** -Funktion Ruft ein Handle für einen [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP) basierend auf einer Datei mit einem [*privaten Schlüssel*](../secgloss/p-gly.md) oder einem Schlüssel Container Namen ab.

> [!Note]  
> Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek. Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI PvkGetCryptProv(
  _In_      HWND       hwnd,
  _In_      LPCWSTR    pwszCaption,
  _In_      LPCWSTR    pwszCapiProvider,
  _In_      DWORD      dwProviderType,
  _In_      LPCWSTR    pwszPvkFile,
  _In_      LPCWSTR    pwszKeyContainerName,
  _Out_     DWORD      *pdwKeySpec,
  _Out_opt_ LPWSTR     *ppwszTmpContainer,
  _Out_     HCRYPTPROV *phCryptProv
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* \[ in\]
</dt> <dd>

Wenn ein Kennwort erforderlich ist, um die Datei mit dem privaten Schlüssel zu entschlüsseln, ist dieser Parameter ein Handle für das übergeordnete Element des Kennwort-Dialog Felds. Andernfalls ist der Wert **null**.

</dd> <dt>

*pwszcaption* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge für die Dialogfeld Beschriftung.

</dd> <dt>

*pwszcapiprovider* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge für den CSP-Namen.

</dd> <dt>

*dwprovidertype* \[ in\]
</dt> <dd>

Ein **DWORD** -Wert, der den Typ des Kryptografieanbieters darstellt. Weitere Informationen finden Sie unter [Typen von Kryptografieanbietern](cryptographic-provider-types.md).

</dd> <dt>

*pwszpvkfile* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen einer Datei mit einem privaten Schlüssel enthält.

</dd> <dt>

*pwszkeycontainername* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge für den Namen des privaten Schlüssel Containers.

</dd> <dt>

*pdwkeyspec* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen **DWORD** -Wert für den Typ des Schlüssels des Containers, der mit " *phcryptprov* " und " *ppwsztmpcontainer*" zurückgegeben wird.

</dd> <dt>

*ppwsztmpcontainer* \[ Out, optional\]
</dt> <dd>

Die Adresse eines Zeigers auf eine NULL-terminierte Zeichenfolge für den temporären Schlüssel Container Namen. Die **pvkgetcryptprov** -Funktion stellt den temporären Container bereit und initialisiert diesen. Wenn **pvkgetcryptprov** aufgerufen wird, sollte die Adresse auf einen **null** -Wert zeigen.

</dd> <dt>

*phcryptprov* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf ein Handle für den CSP.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.

Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

## <a name="remarks"></a>Bemerkungen

Die **pvkgetcryptprov** -Funktion versucht zunächst, das Anbieter Handle aus dem Schlüssel Container Namen zu erhalten, der durch den *pwszkeycontainername* -Parameter angegeben wird. Wenn Sie **null** für den *pwszkeycontainername* -Parameter übergeben, versucht **pvkgetcryptprov** , den Anbieter aus der Datei mit dem privaten Schlüssel zu erhalten, die im *pwszpvkfile* -Parameter angegeben ist.

Wenn Sie die Verwendung des CSP abgeschlossen haben, können Sie das Anbieter Handle und den temporären Schlüssel Container durch Aufrufen der [**pvkfreecryptprov**](pvkfreecryptprov.md) -Funktion freigeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
