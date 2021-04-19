---
description: Konvertiert einen Microsoft MS-DOS-Pfad in eine kanonisierte URL.
ms.assetid: 1186b970-9ae1-4020-b999-55157cff1741
title: MF | ateurlfrompath-Funktion
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
ms.openlocfilehash: e43c2d7df299792d8b5be99226e9cfdbd11976a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348462"
---
# <a name="mfcreateurlfrompath-function"></a>MF | ateurlfrompath-Funktion

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Stattdessen sollten Anwendungen [urlkreatefrompath](/windows/desktop/api/shlwapi/nf-shlwapi-urlcreatefrompatha)aufrufen.\]

Konvertiert einen Microsoft MS-DOS-Pfad in eine kanonisierte URL.

## <a name="syntax"></a>Syntax


```C++
HRESULT MFCreateURLFromPath(
  _In_opt_ LPCWSTR pwszFilePath,
  _Out_    LPWSTR  *ppwszFileURL
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwszfilepath* \[ in, optional\]
</dt> <dd>

Eine NULL terminierte Zeichenfolge, die den Pfad enthält. Die maximale Länge der Zeichenfolge ist die Internet-maximale **\_ URL- \_ \_ Länge**.

</dd> <dt>

*ppwszfileurl* \[ vorgenommen\]
</dt> <dd>

Empfängt eine NULL-terminierte Zeichenfolge, die die URL enthält. Der Aufrufer muss die Zeichenfolge durch Aufrufen von [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)freigeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Funktion gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                             | Beschreibung                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Die im *pwszfilepath* -Parameter angegebene Zeichenfolge weist bereits das URL-Format auf. In diesem Fall wird *pszfilepath* einfach ohne Änderung in *ppszfileurl* kopiert.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Die Funktion wurde erfolgreich ausgeführt. <br/>                                                                                                                                       |



 

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

 

 
