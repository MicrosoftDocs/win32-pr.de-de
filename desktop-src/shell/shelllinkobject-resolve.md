---
description: Sucht das Ziel eines shelllinks, auch wenn das Ziel verschoben oder umbenannt wurde.
ms.assetid: 60e119be-8e45-4f63-a381-cad048de0765
title: Shelllinkobject. Resolve-Methode (Shldisp. h)
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
ms.openlocfilehash: b1cb0760f1ee19acfa10208711e73919fd084ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980800"
---
# <a name="shelllinkobjectresolve-method"></a>Shelllinkobject. Resolve-Methode

Sucht das Ziel eines shelllinks, auch wenn das Ziel verschoben oder umbenannt wurde.

## <a name="syntax"></a>Syntax


```JScript
iRetVal = ShellLinkObject.Resolve(
  fFlags
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fFlags* \[ in\]
</dt> <dd>

Type: **Integer**

Flags, die die auszuführende Aktion angeben. Dies kann eine Kombination der folgenden Werte sein:

<dt>



 (1)


</dt> <dd>

Wenn der Link nicht aufgelöst werden kann, wird kein Dialogfeld angezeigt. Wenn dieses Flag festgelegt ist, gibt das hochwertige Wort von *fFlags* eine Timeout Dauer in Millisekunden an. Die Methode gibt zurück, wenn der Link nicht innerhalb der Timeout Dauer aufgelöst werden kann. Wenn das höchst wertige Wort auf 0 (null) festgelegt ist, wird die Timeout Dauer standardmäßig auf 3000 Millisekunden (3 Sekunden) festgelegt.

</dd> <dt>



 (4)


</dt> <dd>

Wenn sich der Link geändert hat, aktualisieren Sie den Pfad und die Liste der Bezeichner.

</dd> <dt>



 (8)


</dt> <dd>

Aktualisieren Sie die Link Informationen nicht.

</dd> <dt>



 (16)


</dt> <dd>

Führen Sie die Suchheuristik nicht aus.

</dd> <dt>



 (32)


</dt> <dd>

Verwenden Sie die Nachverfolgung verteilter Links nicht.

</dd> <dt>



 (64)


</dt> <dd>

Deaktivieren Sie die Überwachung verteilter Links. Standardmäßig verfolgt die verteilte Link Verfolgung Wechselmedien auf der Grundlage des Volumenamens auf mehrere Geräte. Außerdem wird der UNC-Pfad verwendet, um Remote Dateisysteme zu verfolgen, deren Laufwerk Buchstabe geändert wurde. Wenn Sie dieses Flag festlegen, werden beide Arten der Nachverfolgung deaktiviert.

</dd> <dt>



 (128)


</dt> <dd>

Nennen Sie die Windows Installer.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Methode ist im Grunde identisch [**mit den zu**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve)lösenden Funktionen. Weitere Informationen zur Link Auflösung finden Sie im Abschnitt "Hinweise" auf dieser Seite.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Methode für JScript, VBScript und Visual Basic.

JScript


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



VBScript


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



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 2000 Professional mit SP3 \[ Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



 

 
