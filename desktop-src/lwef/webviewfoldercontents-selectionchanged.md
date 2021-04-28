---
title: WebViewFolderContents.SelectionChanged-Ereignis (Shldisp.h)
description: 'WebViewFolderContents.SelectionChanged-Ereignis: Tritt auf, wenn sich der Auswahlzustand eines Elements oder elements in der Ansicht geändert hat.'
ms.assetid: 46dfceec-aa81-4950-81e5-526a6e621271
keywords:
- SelectionChanged-Ereignis Legacy-Windows-Umgebungsfeatures
topic_type:
- apiref
api_name:
- SelectionChanged
api_location:
- Shell32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea6176cb2a1703d48cd2ddec8069c65d7efc978f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102658"
---
# <a name="webviewfoldercontentsselectionchanged-event"></a>WebViewFolderContents.SelectionChanged-Ereignis

Tritt ein, wenn sich der Auswahlzustand eines Elements oder elements in der Ansicht geändert hat.

## <a name="syntax"></a>Syntax


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
WebViewFolderContents.SelectionChanged = EventHandler;
```



## <a name="parameters"></a>Parameter

Dieser Ereignishandler verfügt über keine Parameter.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieses Ereignisses für JScript, das in HTML eingebettet ist.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectionChangedJ()
    {
        alert("SelectionChanged event was called");
    }
</script>

<script language="JavaScript" for="FileList" event="SelectionChanged">
    fnWebViewFolderContentsSelectionChangedJ();
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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 





