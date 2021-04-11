---
title: WebViewFolderContents.SelectedItems-Methode (Shldisp.h)
description: Ruft ein folderitems-Objekt ab, das alle ausgewählten Elemente in der Ansicht darstellt.
ms.assetid: 683acac4-f157-4a75-a3f8-c693887c1ea5
keywords:
- SelectedItems-Methode Legacy-Windows-Umgebungs Features
- SelectedItems-Methode Legacy-Windows-Umgebungs Features, webviewfoldercontents-Objekt
- Webviewfoldercontents-Objekt Legacy Funktionen der Windows-Umgebung, SelectedItems-Methode
topic_type:
- apiref
api_name:
- WebViewFolderContents.SelectedItems
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee4b7f34cdcabec637671af79775fc1fa546790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040917"
---
# <a name="webviewfoldercontentsselecteditems-method"></a>Webviewfoldercontents. SelectedItems-Methode

Ruft ein [**folderitems**](../shell/folderitems.md) -Objekt ab, das alle ausgewählten Elemente in der Ansicht darstellt.

## <a name="syntax"></a>Syntax


```JScript
retVal = WebViewFolderContents.SelectedItems()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Type: **[ **folderitems**](../shell/folderitems.md)\*\***

Ein Objekt Verweis auf das [**folderitems**](../shell/folderitems.md) -Objekt.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Methode für JScript Embedded in HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectedItemsJ()
    {
        var objFolderItems;

        objFolderItems = FileList.SelectedItems();
        if (objFolderItems != null)
        {
            alert(objFolderItems.Count);
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



 

