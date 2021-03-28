---
description: Enthält den Offline Status des Ordners.
ms.assetid: b50b130d-0675-49b5-b730-f67ea1c71d8c
title: Folder2. Offlinestatus-Eigenschaft (Shldisp. h)
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
ms.openlocfilehash: d456eae826e8a2e173b92fac4be716fb24bcb92d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977072"
---
# <a name="folder2offlinestatus-property"></a>Folder2. Offlinestatus (Eigenschaft)

Enthält den Offline Status des Ordners.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
iOfflineStatus = Folder2.OfflineStatus
```



## <a name="property-value"></a>Eigenschaftswert

Eine **ganze** Zahl, die auf einen der folgenden Werte festgelegt ist.

<dt>



 (OFS \_ ) Dirtycache)


</dt> <dd>

Der Server ist mit nicht synchronisierten Änderungen online.

</dd> <dt>



 (OFS \_ ) VSTE


</dt> <dd>

Das Offline Caching ist für diesen Ordner nicht aktiviert.

</dd> <dt>



 (OFS \_ ) Aufzu


</dt> <dd>

Der Server ist offline.

</dd> <dt>



 (OFS \_ ) Internet


</dt> <dd>

Der Server ist online.

</dd> <dt>



 (OFS \_ ) Serverback)


</dt> <dd>

Der Server ist offline, kann aber erreicht werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Offlinedateien müssen durch Ordneroptionen aktiviert werden, damit **Offlinestatus** ordnungsgemäß funktioniert. Wenn die Offlinedateien-Option nicht aktiviert ist, gibt die-Eigenschaft **OFS \_ inaktiv** zurück.

 

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die ordnungsgemäße Verwendung von **Offlinestatus** für JScript, VBScript und Visual Basic.

JScript


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



VBScript


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



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Folder2**](folder2-object.md)
</dt> <dt>

[**Ordner**](folder.md)
</dt> </dl>

 

 




