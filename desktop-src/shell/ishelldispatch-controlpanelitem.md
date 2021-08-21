---
description: Führt die angegebene Systemsteuerung Anwendung aus.
title: IShellDispatch.ControlPanelItem-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.ControlPanelItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9A9B6B3F-FBBC-4e76-8018-8858B6392276
ms.openlocfilehash: 89ea8431df7e8cac09a041bd9a16c805633cd3ec82a2cc506cb30fcf0f0cd39b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032258"
---
# <a name="ishelldispatchcontrolpanelitem-method"></a>IShellDispatch.ControlPanelItem-Methode

Führt die angegebene Systemsteuerung Anwendung aus. Wenn die Anwendung bereits geöffnet ist, wird die ausgeführte Instanz aktiviert.

> [!Note]  
> Ab Windows Vista sind die meisten Systemsteuerung Anwendungen Shellelemente und können nicht mit dieser Funktion geöffnet werden. Um diese Systemsteuerung Anwendungen zu öffnen, übergeben Sie den kanonischen Namen an control.exe. Zum Beispiel:
>
> ``` syntax
> control.exe /name Microsoft.Personalization
> ```

 

## <a name="syntax"></a>Syntax


```JScript
IShellDispatch.ControlPanelItem(
  bstrDir
)
```


```VB

IShellDispatch.ControlPanelItem( _
  ByVal bstrDir As BSTR _
)
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrDir* \[ In\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Der Dateiname der Systemsteuerung Anwendung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Diese Methode gibt keinen Wert zurück.

### <a name="vb"></a>VB

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode wird implementiert und über die [**Shell.ControlPanelItem-Methode**](shell-controlpanelitem.md) aufgerufen.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird [**ControlPanelItem**](shell-controlpanelitem.md) verwendet, um das **Anzeigeeigenschaften-Element** der Systemsteuerung auszuführen. Die Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

JScript:


```JScript
<script language="JScript">
    function fnShellControlPanelItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Shell_ControlPanelItem("desk.cpl");
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellControlPanelItemVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Shell_ControlPanelItem("desk.cpl")
       
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellControlPanelItemVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.Shell_ControlPanelItem ("desk.cpl")
    
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 
