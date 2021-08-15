---
description: 'ShellFolderView.Folder-Eigenschaft: Ruft ein Folder-Objekt ab, das die Ansicht darstellt.'
ms.assetid: 8f3e7827-f2a0-4ce9-b3e9-e6316ec58863
title: ShellFolderView.Folder-Eigenschaft (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.Folder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 40ff2dbed37aa8ceb80072870c78cee4e63cba3656550081be2c655cb6f6ddf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857709"
---
# <a name="shellfolderviewfolder-property"></a>ShellFolderView.Folder (Eigenschaft)

Ruft ein [**Folder-Objekt**](folder.md) ab, das die Sicht darstellt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
Folder = ShellFolderView.Folder
```



## <a name="property-value"></a>Eigenschaftswert

Objekt, das das [**Folder-Objekt**](folder.md) empfängt.

## <a name="remarks"></a>Hinweise

**Der** Ordner kann nur auf dem lokalen System aufgerufen werden. Sie funktioniert nicht, wenn sie auf einer Webseite über HTTP oder UNC ausgeführt wird.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Eigenschaft für JScript in HTML eingebetteten Dateien.


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewFolderJ()
    {
        var objFolder;
        
        objFolder = WebOC.Document.Folder;
        if (objFolder != null)
        {
            alert("Got Folder object");
        }
    }
    
    function fnLoad()
    {
        var webOC;
        
        webOC = document.all("WebOC");
        webOC.Navigate("C:\\");
    }
</script>

</head>
<body onload="fnLoad()">
<object id="WebOC" 
        classid="clsid:8856F961-340A-11D0-A96B-00C04FD705A2"
        width=400
        height=400 VIEWASTEXT>
</object>
<br><br>
<INPUT id=Folder 
       type=button 
       value=Folder 
       name=Folder 
       onclick="fnShellFolderViewFolderJ()">
</body>
</html>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 




