---
description: Führt die angegebene System Steuerungsanwendung aus.
title: Ishelldispatch. controlpanelitem-Methode (Shldisp. h)
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
ms.openlocfilehash: 72164ff76cbcf15703bc91160e6211b38015f989
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527353"
---
# <a name="ishelldispatchcontrolpanelitem-method"></a>Ishelldispatch. controlpanelitem-Methode

Führt die angegebene System Steuerungsanwendung aus. Wenn die Anwendung bereits geöffnet ist, wird die laufende Instanz aktiviert.

> [!Note]  
> Ab Windows Vista sind die meisten System Steuerungsanwendungen shellelemente und können nicht mit dieser Funktion geöffnet werden. Wenn Sie diese System Steuerungsanwendungen öffnen möchten, übergeben Sie den kanonischen Namen an control.exe. Zum Beispiel:
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

*bstrindir* \[ in\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Der Dateiname der System Steuerungsanwendung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Diese Methode gibt keinen Wert zurück.

### <a name="vb"></a>VB

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird implementiert und über die [**Shell. controlpanelitem**](shell-controlpanelitem.md) -Methode aufgerufen.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird [**controlpanelitem**](shell-controlpanelitem.md) verwendet, um das Element **Anzeigeeigenschaften** der Systemsteuerung auszuführen. Die Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

JScript


```JScript
<script language="JScript">
    function fnShellControlPanelItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Shell_ControlPanelItem("desk.cpl");
    }
</script>
```



VBScript


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



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4,71 oder höher)</dt> </dl> |



 

 
