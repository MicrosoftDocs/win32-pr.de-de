---
description: Konvertiert eine Datei-URL in einen Microsoft MS-DOS-Pfad.
ms.assetid: c35988ad-6cf8-41ec-bee9-e3bb982310ee
title: MF | atepathfromurl-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreatePathFromURL
api_type:
- DllExport
api_location:
- mfplat.dll
ms.openlocfilehash: c1838a3b09dc5375588d562aa503d555a186e394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345784"
---
# <a name="mfcreatepathfromurl-function"></a>MF | atepathfromurl-Funktion

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Stattdessen sollten Anwendungen [**pathkreatefromurl**](/windows/win32/api/shlwapi/nf-shlwapi-pathcreatefromurla)aufrufen.\]

Konvertiert eine Datei-URL in einen Microsoft MS-DOS-Pfad.

## <a name="syntax"></a>Syntax


```C++
HRESULT MFCreatePathFromURL(
  _In_opt_ LPCWSTR pwszFileURL,
  _Out_    LPWSTR  *ppwszFilePath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwszfileurl* \[ in, optional\]
</dt> <dd>

Eine NULL terminierte Zeichenfolge, die die URL enthält. Die maximale Länge der Zeichenfolge ist die Internet-maximale **\_ URL- \_ \_ Länge**.

</dd> <dt>

*ppwszfilepath* \[ vorgenommen\]
</dt> <dd>

Empfängt eine NULL-terminierte Zeichenfolge, die die URL enthält. Der Aufrufer muss die Zeichenfolge durch Aufrufen von [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)freigeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Funktion gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                  | Beschreibung                                                                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Funktion wurde erfolgreich ausgeführt. <br/>                                                                         |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Ungültiges Argument. Die im *pwszfileurl* -Parameter angegebene Zeichenfolge kann nicht in einen Pfad konvertiert werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Funktion verfügt über keine zugeordnete Import Bibliothek. Um diese Funktion aufzurufen, müssen Sie die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mfplat.dll zu verknüpfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Mfplat.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Funktionen](media-foundation-functions.md)
</dt> </dl>

 

 
