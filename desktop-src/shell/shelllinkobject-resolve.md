---
description: Sucht nach dem Ziel eines Shelllinks, auch wenn das Ziel verschoben oder umbenannt wurde.
ms.assetid: 60e119be-8e45-4f63-a381-cad048de0765
title: ShellLinkObject.Resolve-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Resolve
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: fdff3fd1a606b8dbec35476988497dd14892692a42e6502343716264873c184d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857493"
---
# <a name="shelllinkobjectresolve-method"></a>ShellLinkObject.Resolve-Methode

Sucht nach dem Ziel eines Shelllinks, auch wenn das Ziel verschoben oder umbenannt wurde.

## <a name="syntax"></a>Syntax


```JScript
iRetVal = ShellLinkObject.Resolve(
  fFlags
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fFlags* \[ In\]
</dt> <dd>

Typ: **Integer**

Flags, die die zu ergreifende Aktion angeben. Dies kann eine Kombination der folgenden Werte sein:

<dt>



 (1)


</dt> <dd>

Zeigt kein Dialogfeld an, wenn der Link nicht aufgelöst werden kann. Wenn dieses Flag festgelegt ist, gibt das obere Wort *fFlags* eine Time out-Dauer in Millisekunden an. Die Methode gibt zurück, wenn der Link nicht innerhalb der Time outdauer aufgelöst werden kann. Wenn das hohe Wort auf 0 (null) festgelegt ist, beträgt die Time outdauer standardmäßig 3.000 Millisekunden (3 Sekunden).

</dd> <dt>



 (4)


</dt> <dd>

Wenn sich der Link geändert hat, aktualisieren Sie den Pfad und die Liste der Bezeichner.

</dd> <dt>



 (8)


</dt> <dd>

Aktualisieren Sie die Linkinformationen nicht.

</dd> <dt>



 (16)


</dt> <dd>

Führen Sie die Suchhuristik nicht aus.

</dd> <dt>



 (32)


</dt> <dd>

Verwenden Sie keine Verteilte Linknachverfolgung.

</dd> <dt>



 (64)


</dt> <dd>

Deaktivieren Sie die Nachverfolgung verteilter Links. Standardmäßig verfolgt die Nachverfolgung verteilter Links Wechselmedien auf mehreren Geräten basierend auf dem Volumenamen nach. Außerdem wird der UNC-Pfad zum Nachverfolgen von Remotedateisystemen verwendet, deren Laufwerkbuchstaben geändert wurden. Wenn Sie dieses Flag festlegen, werden beide Nachverfolgungstypen deaktiviert.

</dd> <dt>



 (128)


</dt> <dd>

Rufen Sie den Windows Installer auf.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Methode ist in der Funktionalität im Wesentlichen identisch mit [**resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve). Weitere Informationen zur Linkauflösung finden Sie im Abschnitt "Hinweise" auf dieser Seite.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Methode für JScript, VBScript und Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellLinkObjectResolveJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.ParseName("Internet Explorer.lnk");
            if (objFolderItem != null)
            {
                var objShellLink;
                
                objShellLink = objFolderItem.GetLink;
                if (objShellLink != null)
                {
                    objShellLink.Resolve(1);
                }
            }
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellLinkObjectResolveVB()
        dim objShell
        dim objFolder
        dim ssfPROGRAMS
        
        ssfPROGRAMS = 2
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objFolderItem
                
                set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                    if (not objFolderItem is nothing) then
                        dim objShellLink
                        
                        set objShellLink = objFolderItem.GetLink
                            if (not objShellLink is nothing) then
                                objShellLink.Resolve(1)
                            end if
                        set objShellLink = nothing
                    end if
                set objFolderItem = nothing
            end if
        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellLinkObjectResolveVB()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                If (Not objFolderItem Is Nothing) Then
                    Dim objShellLink As ShellLinkObject
                    
                    Set objShellLink = objFolderItem.GetLink
                        If (Not objShellLink Is Nothing) Then
                            objShellLink.Resolve (1)
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional nur mit \[ SP3-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



 

 
