---
title: WebViewFolderContents.Folder-Eigenschaft (Shldisp.h)
description: Ruft ein Ordner Objekt ab, das die Ansicht darstellt.
ms.assetid: 1d81c27a-1e48-4c0a-b74d-c63af43a909d
keywords:
- Ordner Eigenschaft Legacy-Windows-Umgebungs Features
- Ordner Eigenschaft Legacy Windows-Umgebungs Funktionen, webviewfoldercontents-Objekt
- Webviewfoldercontents-Objekt Legacy-Windows-Umgebungs Features, Ordner Eigenschaft
topic_type:
- apiref
api_name:
- WebViewFolderContents.Folder
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c0640d4e29b903b32a6c9ed1e0b1de9f458b132
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475423"
---
# <a name="webviewfoldercontentsfolder-property"></a>Webviewfoldercontents. Folder-Eigenschaft

Ruft ein [**Ordner**](../shell/folder.md) Objekt ab, das die Ansicht darstellt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
Folder = WebViewFolderContents.Folder
```



## <a name="property-value"></a>Eigenschaftswert

Ein Objekt, das das [**Ordner**](../shell/folder.md) Objekt empfängt.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Eigenschaft in JScript Embedded in HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsFolderJ()
    {
        var objFolder;

        objFolder = FileList.Folder;
        if (objFolder != null)
        {
            alert(objFolder.Title);
        }
    }
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4,71 oder höher)</dt> </dl> |



 

