---
title: Webviewfoldercontents. SelectItem-Methode (Shldisp. h)
description: Legt den Auswahl Zustand eines Elements in der Ansicht fest.
ms.assetid: c0e163ee-1951-476c-807a-781e26766d99
keywords:
- SelectItem-Methode Legacy Windows-Umgebungs Features
- SelectItem-Methode Legacy-Windows-Umgebungs Features, webviewfoldercontents-Objekt
- Webviewfoldercontents-Objekt Legacy Funktionen der Windows-Umgebung, SelectItem-Methode
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
ms.openlocfilehash: e491fb27db2d6e1e9b449be4aa2924684021539a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339935"
---
# <a name="webviewfoldercontentsselectitem-method"></a>Webviewfoldercontents. SelectItem-Methode

Legt den Auswahl Zustand eines Elements in der Ansicht fest.

## <a name="syntax"></a>Syntax


```JScript
WebViewFolderContents.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*vitem* \[ in\]
</dt> <dd>

Typ: **Variant \** _

Das [_ *folderItem* *](../shell/folderitem.md) -Objekt, für das der Auswahl Zustand festgelegt wird.

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

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Methode für JScript Embedded in HTML.


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
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4,71 oder höher)</dt> </dl> |



 

