---
description: Ruft ein-Objekt ab, das das übergeordnete Element des aktuellen-Objekts darstellt.
ms.assetid: 2FDEF8D3-3F5B-43ae-9812-83B4249D9CBB
title: Ishelldispatch. Parent-Eigenschaft (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Parent
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 051e6f323b9663b692410d81d85e55a404e99d56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130093"
---
# <a name="ishelldispatchparent-property"></a>Ishelldispatch. Parent-Eigenschaft

Ruft ein-Objekt ab, das das übergeordnete Element des aktuellen-Objekts darstellt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
objParent = IShellDispatch.Parent
```


```VB

Property Parent As Object
```





## <a name="property-value"></a>Eigenschaftswert

Eine Variable vom Typ [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , die das übergeordnete Objekt empfängt.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird implementiert, und der Zugriff erfolgt über die [**Shell. Parent**](shell-parent.md) -Eigenschaft.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird die Verwendung von **Parent** in JScript, VBScript und Visual Basic veranschaulicht.

JScript


```JScript
<script language="JScript">
    function fnShellParentJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objParent;

        objParent = objshell.Shell_Parent;
        if (objParent != null)
        {
            alert("Got parent property");
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellParentVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            if (not objShell is nothing) then
                dim objParent

                set objParent = objshell.Parent
                    if (not objParent is nothing) then
                        alert("Got parent property")
                    end if
                set objParent = nothing
            end if
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellParentVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        If (Not objShell Is Nothing) Then
            Dim objParent As Object
            
            Set objParent = objshell.Parent
                If (Not objParent Is Nothing) Then
                    Debug.Print "Got parent object"
                End If
            Set objParent = Nothing
        End If
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



 

 
