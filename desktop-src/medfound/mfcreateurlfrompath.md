---
description: Konvertiert einen Microsoft MS-DOS-Pfad in eine kanonische URL.
ms.assetid: 1186b970-9ae1-4020-b999-55157cff1741
title: MFCreateURLFromPath-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateURLFromPath
api_type:
- DllExport
api_location:
- mfplat.dll
ms.openlocfilehash: f9da3dd84d54bb514b7dda519db3de376b2ebb2bd2088d8fc8e18b4f2b848231
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739248"
---
# <a name="mfcreateurlfrompath-function"></a>MFCreateURLFromPath-Funktion

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Stattdessen sollten Anwendungen [UrlCreateFromPath aufrufen.](/windows/desktop/api/shlwapi/nf-shlwapi-urlcreatefrompatha)\]

Konvertiert einen Microsoft MS-DOS-Pfad in eine kanonische URL.

## <a name="syntax"></a>Syntax


```C++
HRESULT MFCreateURLFromPath(
  _In_opt_ LPCWSTR pwszFilePath,
  _Out_    LPWSTR  *ppwszFileURL
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwszFilePath* \[ in, optional\]
</dt> <dd>

Eine auf NULL beendete Zeichenfolge, die den Pfad enthält. Die maximale Länge der Zeichenfolge ist **INTERNET \_ MAX URL \_ \_ LENGTH.**

</dd> <dt>

*ppwszFileURL* \[ out\]
</dt> <dd>

Empfängt eine auf NULL beendete Zeichenfolge, die die URL enthält. Der Aufrufer muss die Zeichenfolge durch Aufrufen von [**CoTaskMemFree freigibt.**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt ein **HRESULT zurück.** Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                             | Beschreibung                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Die im *pwszFilePath-Parameter übergebene Zeichenfolge* hat bereits das URL-Format. In diesem Fall wird *pszFilePath* ohne Änderung einfach in *ppszFileURL* kopiert.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Die Funktion wurde erfolgreich ausgeführt. <br/>                                                                                                                                       |



 

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek zugeordnet. Zum Aufrufen dieser Funktion müssen Sie die [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um dynamisch eine Verknüpfung mit Mfplat.dll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Mfplat.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Funktionen](media-foundation-functions.md)
</dt> </dl>

 

 
