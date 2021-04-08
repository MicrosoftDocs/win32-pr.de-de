---
title: Webviewfoldercontents. popupitemmenu-Methode (Shldisp. h)
description: Erstellt ein Kontextmenü für das angegebene Element und gibt die ausgewählte Befehls Zeichenfolge zurück.
ms.assetid: 3c07500c-2fe9-4976-a1a8-b128e75f9325
keywords:
- Popupitemmenu-Methode Legacy-Windows-Umgebungs Features
- Popupitemmenu-Methode Legacy-Windows-Umgebungs Funktionen, webviewfoldercontents-Objekt
- Webviewfoldercontents-Objekt Legacy Funktionen der Windows-Umgebung, Methode "popupitemmenu"
topic_type:
- apiref
api_name:
- WebViewFolderContents.PopupItemMenu
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41753814f103998185acc798a37447f22356d2aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740128"
---
# <a name="webviewfoldercontentspopupitemmenu-method"></a>Webviewfoldercontents. popupitemmenu-Methode

Erstellt ein Kontextmenü für das angegebene Element und gibt die ausgewählte Befehls Zeichenfolge zurück.

## <a name="syntax"></a>Syntax


```JScript
retVal = WebViewFolderContents.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*vitem* \[ in\]
</dt> <dd>

Typ: **Variant**

Das [**folderItem**](../shell/folderitem.md) -Objekt, für das das Kontextmenü erstellt wird.

</dd> <dt>

*VX* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Die horizontale Position des Menüs in Bildschirm Koordinaten.

</dd> <dt>

*Vy* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Die vertikale Position des Menüs in Bildschirm Koordinaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Geben Sie Folgendes ein: **[BSTR](/previous-versions/windows/desktop/automat/bstr) \** _

Wenn diese Methode zurückgegeben wird, enthält Sie die Befehls Zeichenfolge.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die ordnungsgemäße Verwendung von _ *popupitemmenu** für JScript Embedded in HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsPopupItemMenuJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            var szCommand;

            szCommand = FileList.PopupItemMenu(objFolderItem);
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



 

