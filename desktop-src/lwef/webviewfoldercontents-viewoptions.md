---
title: WebViewFolderContents.ViewOptions-Eigenschaft (Shldisp.h)
description: Ruft einen Satz von ShellFolderViewOptions-Flags ab, die die aktuellen Optionen der Ansicht angeben.
ms.assetid: 96edb144-e532-4ab5-99ae-d945e211d744
keywords:
- ViewOptions-Eigenschaft Legacy Windows-Umgebungsfeatures
- ViewOptions-Eigenschaft Legacy Windows Umgebungsfeatures , WebViewFolderContents-Objekt
- WebViewFolderContents-Objekt Legacy Windows Umgebungsfeatures , ViewOptions-Eigenschaft
topic_type:
- apiref
api_name:
- WebViewFolderContents.ViewOptions
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c897c75eab32962a18981c605c8465630aaf7b0c6b7d3e3f9a4fbe8e3d75d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607740"
---
# <a name="webviewfoldercontentsviewoptions-property"></a>WebViewFolderContents.ViewOptions-Eigenschaft

Ruft einen Satz von [**ShellFolderViewOptions-Flags**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) ab, die die aktuellen Optionen der Ansicht angeben.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
objViewOptions = WebViewFolderContents.ViewOptions
```



## <a name="property-value"></a>Eigenschaftswert

Eine Variable vom Typ [IDispatch,](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) die das Ansichtsoptionenobjekt empfängt.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Eigenschaft in JScript eingebettet in HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsViewOptionsJ()
    {
        var nViewOptions;

        nViewOptions = FileList.ViewOptions;
        if (nViewOptions != "")
        {
            alert(nViewOptions);
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



 

