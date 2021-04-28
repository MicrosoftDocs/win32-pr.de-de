---
title: WebViewFolderContents.PopupItemMenu-Methode (Shldisp.h)
description: 'WebViewFolderContents.PopupItemMenu-Methode: Erstellt ein Kontextmenü für das angegebene Element und gibt die ausgewählte Befehlszeichenfolge zurück.'
ms.assetid: 3c07500c-2fe9-4976-a1a8-b128e75f9325
keywords:
- PopupItemMenu-Methode Legacy-Windows-Umgebungsfeatures
- PopupItemMenu-Methode Legacy-Windows-Umgebungsfeatures , WebViewFolderContents-Objekt
- WebViewFolderContents-Objekt Legacy-Windows-Umgebungsfeatures , PopupItemMenu-Methode
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
ms.openlocfilehash: c879e10097b334f0c2d4f98b1b76289d20ee4a93
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102638"
---
# <a name="webviewfoldercontentspopupitemmenu-method"></a>WebViewFolderContents.PopupItemMenu-Methode

Erstellt ein Kontextmenü für das angegebene Element und gibt die ausgewählte Befehlszeichenfolge zurück.

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

*vItem* \[ In\]
</dt> <dd>

Typ: **Variant**

Das [**FolderItem-Objekt,**](../shell/folderitem.md) für das das Kontextmenü erstellt wird.

</dd> <dt>

*vx* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Die horizontale Position des Menüs in Bildschirmkoordinaten.

</dd> <dt>

*vy* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Die vertikale Position des Menüs in Bildschirmkoordinaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[BSTR](/previous-versions/windows/desktop/automat/bstr)\***

Diese Methode gibt die Befehlszeichenfolge zurück.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die ordnungsgemäße Verwendung von **PopupItemMenu** für JScript, das in HTML eingebettet ist.


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



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

