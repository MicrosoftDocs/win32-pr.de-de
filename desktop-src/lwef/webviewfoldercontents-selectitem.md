---
title: WebViewFolderContents.SelectItem-Methode (Shldisp.h)
description: 'WebViewFolderContents.SelectItem-Methode: Legt den Auswahlzustand eines Elements in der Ansicht fest.'
ms.assetid: c0e163ee-1951-476c-807a-781e26766d99
keywords:
- SelectItem-Methode – Legacy-Windows-Umgebungsfeatures
- SelectItem-Methode Legacy Windows Umgebungsfeatures , WebViewFolderContents-Objekt
- WebViewFolderContents-Objekt Legacy Windows Umgebungsfeatures, SelectItem-Methode
topic_type:
- apiref
api_name:
- WebViewFolderContents.SelectItem
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d144801e62962f4071b6c8e60147326908a9b4f7787e0d4ac549be9c51fa3c97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960620"
---
# <a name="webviewfoldercontentsselectitem-method"></a>WebViewFolderContents.SelectItem-Methode

Legt den Auswahlzustand eines Elements in der Ansicht fest.

## <a name="syntax"></a>Syntax


```JScript
WebViewFolderContents.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*vItem* \[ In\]
</dt> <dd>

Typ: **\* Variant**

Das [**FolderItem-Objekt,**](../shell/folderitem.md) für das der Auswahlzustand festgelegt wird.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Typ: **Ganze Zahl**

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

Versetzen Sie das Element in den Bearbeitungsmodus.

</dd> <dt>



 (4)


</dt> <dd>

Deaktivieren Sie alle außer dem angegebenen Element.

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

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Methode für JScript, die in HTML eingebettet sind.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectItemJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            FileList.SelectItem(objFolderItem, 1);
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
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

