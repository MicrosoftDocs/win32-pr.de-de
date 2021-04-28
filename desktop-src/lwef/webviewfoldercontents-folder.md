---
title: WebViewFolderContents.Folder-Eigenschaft (Shldisp.h)
description: 'WebViewFolderContents.Folder-Eigenschaft: Ruft ein Folder-Objekt ab, das die Ansicht darstellt.'
ms.assetid: 1d81c27a-1e48-4c0a-b74d-c63af43a909d
keywords:
- Ordnereigenschaft Legacy-Windows-Umgebungsfeatures
- Ordnereigenschaft Legacy-Windows-Umgebungsfeatures , WebViewFolderContents-Objekt
- WebViewFolderContents-Objekt Legacy-Windows-Umgebungsfeatures , Folder-Eigenschaft
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
ms.openlocfilehash: e88fd7a54971fa088bdddbc78d3d8df4af610875
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102698"
---
# <a name="webviewfoldercontentsfolder-property"></a>WebViewFolderContents.Folder-Eigenschaft

Ruft ein [**Folder-Objekt**](../shell/folder.md) ab, das die Sicht darstellt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
Folder = WebViewFolderContents.Folder
```



## <a name="property-value"></a>Eigenschaftswert

Ein -Objekt, das das [**Folder-Objekt**](../shell/folder.md) empfängt.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Eigenschaft in JScript, eingebettet in HTML.


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



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

