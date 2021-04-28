---
description: 'ShellFolderView.SelectItem-Methode: Legt den Auswahlzustand eines Elements in der Ansicht fest.'
title: ShellFolderView.SelectItem-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.SelectItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 91c39d4c-56c3-4c2b-93e8-9f782ca0aa93
ms.openlocfilehash: c8cbff0da4da55d9621bfeb01f26c5ed62fe230a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116748"
---
# <a name="shellfolderviewselectitem-method"></a>ShellFolderView.SelectItem-Methode

Legt den Auswahlzustand eines Elements in der Ansicht fest.

## <a name="syntax"></a>Syntax


```JScript
ShellFolderView.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*vItem* \[ In\]
</dt> <dd>

Typ: **\* Variant**

Das [**FolderItem-Objekt,**](folderitem.md) für das der Auswahlzustand festgelegt wird.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Typ: **Integer**

Ein Satz von Flags, die den neuen Auswahlzustand angeben. Dies kann einer oder mehrere der folgenden Werte sein.

<dt>



  (0)


</dt> <dd>

Deaktivieren Sie das Element.

</dd> <dt>



 (1)


</dt> <dd>

Wählen Sie das Element aus.

</dd> <dt>



 (3)


</dt> <dd>

Setzen Sie das Element in den Bearbeitungsmodus.

</dd> <dt>



 (4)


</dt> <dd>

Deaktivieren Sie alle Elemente bis auf das angegebene Element.

</dd> <dt>



 (8)


</dt> <dd>

Stellen Sie sicher, dass das Element in der Ansicht angezeigt wird.

</dd> <dt>



 (16)


</dt> <dd>

Geben Sie dem Element den Fokus.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

[**FocusedItem**](shellfolderview-focuseditem.md) kann nur auf dem lokalen System aufgerufen werden. Sie funktioniert nicht, wenn sie auf einer Webseite über HTTP oder UNC ausgeführt wird.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Methode in JScript, eingebettet in HTML.


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewSelectItemJ()
    {
        var objFolder;
        
        objFolder = WebOC.Document.Folder;
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.Self;
            if (objFolderItem != null)
            {
                WebOC.Document.SelectItem(objFolderItem, 16);
                alert("item selected");
            }
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
        height=400>
</object>
<br><br>
<INPUT id=SelectItem 
       type=button 
       value=SelectItem 
       name=SelectItem 
       onclick="fnShellFolderViewSelectItemJ()">
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



 

 




