---
description: Ruft ein Handle für einen Kryptografiedienstanbieter (Cryptographic Service Provider, CSP) basierend auf einer Datei mit einem privaten Schlüssel oder einem Schlüsselcontainernamen ab.
ms.assetid: 82cdaa6f-e747-4c9d-8d2d-5fa206891eed
title: PvkGetCryptProv-Funktion
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
ms.openlocfilehash: 5ba60ca31bf75e355126484608bfe9650b00fea60eaf876022e2de2bf5030470
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901320"
---
# <a name="pvkgetcryptprov-function"></a>PvkGetCryptProv-Funktion

> [!IMPORTANT]
> Diese API ist veraltet. Microsoft kann diese API in zukünftigen Versionen entfernen.

 

Die **PvkGetCryptProv-Funktion** ruft ein Handle für einen Kryptografiedienstanbieter [](../secgloss/p-gly.md) (Cryptographic [*Service Provider,*](../secgloss/c-gly.md) CSP) basierend auf einer Datei mit einem privaten Schlüssel oder einem Schlüsselcontainernamen ab.

> [!Note]  
> Dieser Funktion ist keine Headerdatei oder Importbibliothek zugeordnet. Zum Aufrufen dieser Funktion müssen Sie eine benutzerdefinierte Headerdatei erstellen und die [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um eine dynamische Verknüpfung mit Mssign32.dll.

 

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

*hwnd* \[ In\]
</dt> <dd>

Wenn zum Entschlüsseln der Datei mit dem privaten Schlüssel ein Kennwort erforderlich ist, ist dieser Parameter ein Handle für das übergeordnete Element des Dialogfelds "Kennwort". andernfalls ist es **NULL.**

</dd> <dt>

*pwszCaption* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge für die Beschriftung des Dialogfelds.

</dd> <dt>

*pwszCapiProvider* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge für den CSP-Namen.

</dd> <dt>

*dwProviderType* \[ In\]
</dt> <dd>

Ein **DWORD-Wert,** der den Kryptografieanbietertyp darstellt. Weitere Informationen finden Sie unter [Kryptografieanbietertypen](cryptographic-provider-types.md).

</dd> <dt>

*pwszPvkFile* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen einer Datei mit privatem Schlüssel enthält.

</dd> <dt>

*pwszKeyContainerName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge für den Containernamen des privaten Schlüssels.

</dd> <dt>

*pdwKeySpec* \[ out\]
</dt> <dd>

Ein Zeiger auf einen **DWORD-Wert** für den Schlüsseltyp des Containers, der mit *phCryptProv* und *ppwszTmpContainer zurückgegeben wird.*

</dd> <dt>

*ppwszTmpContainer* \[ out, optional\]
</dt> <dd>

Die Adresse eines Zeigers auf eine auf NULL beendete Zeichenfolge für den temporären Schlüsselcontainernamen. Die **PvkGetCryptProv-Funktion** stellt den temporären Container zur Und initialisiert den Container. Beim Aufrufen **von PvkGetCryptProv** sollte die Adresse auf einen **NULL-Wert** verweisen.

</dd> <dt>

*phCryptProv* \[ out\]
</dt> <dd>

Ein Zeiger auf ein Handle für den CSP.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird **S \_ OK zurückgegeben.**

Wenn bei der Methode ein Fehler auftritt, wird ein **HRESULT-Wert** zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

## <a name="remarks"></a>Hinweise

Die **PvkGetCryptProv-Funktion** versucht zunächst, das Anbieterhandle aus dem Schlüsselcontainernamen zu erhalten, der durch den *pwszKeyContainerName-Parameter angegeben* wird. Wenn Sie **NULL für** den *pwszKeyContainerName-Parameter* übergeben, versucht **PvkGetCryptProv,** den Anbieter aus der datei mit dem privaten Schlüssel zu erhalten, die im *pwszPvkFile-Parameter angegeben* ist.

Wenn Sie die Verwendung des CSP abgeschlossen haben, geben Sie das Anbieterhandler und den temporären Schlüsselcontainer frei, indem Sie die [**PvkFreeCryptProv-Funktion**](pvkfreecryptprov.md) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
