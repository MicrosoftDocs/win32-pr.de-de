---
description: Ruft einen Satz von Flags ab, die die aktuellen Optionen der Ansicht angeben.
ms.assetid: 83a17033-bd7f-44de-a0c8-460d12c4825d
title: Shellfolderview. viewoptions-Eigenschaft (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.ViewOptions
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e336034e7d5037b8037c6fd0ef549fe5f87da312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994991"
---
# <a name="shellfolderviewviewoptions-property"></a>Shellfolderview. viewoptions (Eigenschaft)

Ruft einen Satz von Flags ab, die die aktuellen Optionen der Ansicht angeben.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
objViewOptions = ShellFolderView.ViewOptions
```



## <a name="property-value"></a>Eigenschaftswert

Eine Variable vom Typ [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , die das Ansichts Options Objekt empfängt. Enthält einen oder mehrere der folgenden Werte:

<dt>

<span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>

<span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>**Sfvvo \_ Showallobjects** (0x00000001)


</dt> <dd>

Die Option **alle Dateien anzeigen** ist aktiviert.

</dd> <dt>

<span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>

<span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>**Sfvvo \_ Showextensions** (0x00000002)


</dt> <dd>

Die Option **Erweiterungen für bekannte Dateitypen ausblenden** ist deaktiviert.

</dd> <dt>

<span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>

<span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>**Sfvvo \_ Showcompcolor** (0x00000008)


</dt> <dd>

Die Option **komprimierte Dateien und Ordner mit alternativer Farbe anzeigen** ist aktiviert.

</dd> <dt>

<span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>

<span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>**Sfvvo \_ Showsysfiles** (0x00000020)


</dt> <dd>

Die Option Ausgeblendete **Dateien nicht anzeigen** ist aktiviert.

</dd> <dt>

<span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>

<span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>**Sfvvo \_ WIN95CLASSIC** (0x00000040)


</dt> <dd>

Die Option für den **klassischen Stil** ist aktiviert.

</dd> <dt>

<span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>

<span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>**Sfvvo \_ Doubleclickinwebview** (0x00000080)


</dt> <dd>

Das **doppelklicken, um eine Element Option zu öffnen,** ist aktiviert.

</dd> <dt>

<span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>

<span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>**Sfvvo \_ Desktophtml** (0x00000200)


</dt> <dd>

Die Option **Active Desktop – View as Web Page** ist aktiviert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

[**FocusedItem**](shellfolderview-focuseditem.md) kann nur auf dem lokalen System aufgerufen werden. Es funktioniert nicht, wenn es auf einer Webseite über HTTP oder UNC ausgeführt wird.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Methode in JScript Embedded in HTML.


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewViewOptionsJ()
    {
        var objOptions;
        
        objOptions = WebOC.Document.ViewOptions;
        if (objOptions != null)
        {
            alert(objOptions);
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
<INPUT id=ViewOptions 
       type=button 
       value=ViewOptions 
       name=ViewOptions 
       onclick="fnShellFolderViewViewOptionsJ()">
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



 

 
