---
description: Legt den Auswahl Zustand eines Elements in der Ansicht fest.
title: Shellfolderview. SelectItem-Methode (Shldisp. h)
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
ms.openlocfilehash: d44633983075cdf22581bce05cfb7c073f422084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217690"
---
# <a name="shellfolderviewselectitem-method"></a>Shellfolderview. SelectItem-Methode

Legt den Auswahl Zustand eines Elements in der Ansicht fest.

## <a name="syntax"></a>Syntax


```JScript
ShellFolderView.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*vitem* \[ in\]
</dt> <dd>

Typ: **Variant \** _

Das [_ *folderItem* *](folderitem.md) -Objekt, für das der Auswahl Zustand festgelegt wird.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Type: **Integer**

Ein Satz von Flags, die den neuen Auswahl Zustand angeben. Dabei kann es sich um einen oder mehrere der folgenden Werte handeln:

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

Versetzen Sie das Element in den Bearbeitungsmodus.

</dd> <dt>



 (4)


</dt> <dd>

Deaktivieren Sie alle Elemente außer dem angegebenen Element.

</dd> <dt>



 (8)


</dt> <dd>

Stellen Sie sicher, dass das Element in der Ansicht angezeigt wird.

</dd> <dt>



 (16)


</dt> <dd>

Gibt dem Element den Fokus.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

[**FocusedItem**](shellfolderview-focuseditem.md) kann nur auf dem lokalen System aufgerufen werden. Es funktioniert nicht, wenn es auf einer Webseite über HTTP oder UNC ausgeführt wird.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Methode in JScript Embedded in HTML.


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



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4,71 oder höher)</dt> </dl> |



 

 




