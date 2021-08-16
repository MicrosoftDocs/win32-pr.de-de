---
description: Enthält den Offlinestatus des Ordners.
ms.assetid: b50b130d-0675-49b5-b730-f67ea1c71d8c
title: Folder2.OfflineStatus-Eigenschaft (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.OfflineStatus
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a2664a99fb103b41bd3b5040b3876b0cb92b8f9c010f420f93af7eb62a6f32bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860247"
---
# <a name="folder2offlinestatus-property"></a>Folder2.OfflineStatus-Eigenschaft

Enthält den Offlinestatus des Ordners.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
iOfflineStatus = Folder2.OfflineStatus
```



## <a name="property-value"></a>Eigenschaftswert

Eine **ganze Zahl,** die auf einen der folgenden Werte festgelegt ist.

<dt>



 (OFS \_ DIRTYCACHE)


</dt> <dd>

Der Server ist mit nicht synchronisierten Änderungen online.

</dd> <dt>



 (OFS \_ INACTIVE)


</dt> <dd>

Die Offlinezwischenspeicherung ist für diesen Ordner nicht aktiviert.

</dd> <dt>



 (OFS \_ OFFLINE)


</dt> <dd>

Der Server ist offline.

</dd> <dt>



 (OFS \_ ONLINE)


</dt> <dd>

Der Server ist online.

</dd> <dt>



 (OFS \_ SERVERBACK)


</dt> <dd>

Der Server ist offline, kann aber erreicht werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

> [!Note]  
> Offlinedateien müssen über Ordneroptionen aktiviert werden, damit **OfflineStatus** ordnungsgemäß funktioniert. Wenn die Offlinedateien Option nicht aktiviert ist, gibt die Eigenschaft **OFS \_ INACTIVE** zurück.

 

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die ordnungsgemäße Verwendung von **OfflineStatus** für JScript, VBScript und Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnOfflineStatusJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("\\\\server\\share\\folder");
        if (objFolder2 != null)
        {
            var nReturn;

            nReturn = objFolder2.OfflineStatus;
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnOfflineStatusVB()
        dim objShell
        dim objFolder2
       
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("\\server\share\folder")

        if (not objFolder2 is nothing) then
            dim nReturn

            nReturn = objFolder2.OfflineStatus
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub fnOfflineStatusVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("\\server\share\folder")

    If (Not objFolder2 Is Nothing) Then
        Dim nReturn As Integer
        
        nReturn = objFolder2.OfflineStatus()
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Folder2**](folder2-object.md)
</dt> <dt>

[**Ordner**](folder.md)
</dt> </dl>

 

 




