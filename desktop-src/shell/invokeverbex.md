---
description: Führt ein Verb für ein shellelement aus.
ms.assetid: aac3f338-6074-4b1f-9b2f-e6206db52419
title: Shellfolderitem. invokeverbex-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem.InvokeVerbEx
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 627c2b40869ac9c509dcd645ec259de7db118235
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978160"
---
# <a name="shellfolderiteminvokeverbex-method"></a>Shellfolderitem. invokeverbex-Methode

Führt ein Verb für ein shellelement aus.

## <a name="syntax"></a>Syntax


```JScript
iRetVal = ShellFolderItem.InvokeVerbEx(
  [ vVerb ],
  [ vArgs ]
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*vverb* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Eine **Variante** , die die Verb Zeichenfolge enthält, die dem auszuführenden Befehl entspricht. Dabei muss es sich um einen der Werte handeln, die von der [**Name**](folderitemverb-name.md) -Eigenschaft des Elements zurückgegeben werden. Wenn kein Verb angegeben ist, wird das Standardverb ausgeführt.

</dd> <dt>

*vArgs* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Eine **Variante** , die aus einer Zeichenfolge mit einem oder mehreren Argumenten für den von *vverb* angegebenen Befehl besteht. Das Format dieser Zeichenfolge hängt von dem jeweiligen Verb ab.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Ein Verb ist eine Zeichenfolge, die verwendet wird, um eine bestimmte Aktion anzugeben, die ein Element unterstützt. Wenn Sie ein Verb aufrufen, wird in der Regel eine verwandte Anwendung gestartet. Wenn Sie z. b. das **geöffnete** Verb in einer txt-Datei aufrufen, wird die Datei normalerweise mit einem Text-Editor geöffnet, in der Regel Microsoft Notepad. Das [**folderitemverbs**](folderitemverbs.md) -Objekt stellt die Auflistung der Verben dar, die dem Element zugeordnet sind. Weitere Erläuterungen zu Verben finden Sie unter [Starten von Anwendungen](launch.md).

Diese Methode ähnelt [**invokeverb**](folderitem-invokeverb.md), aber Sie ermöglicht Ihnen, Argumente für den Befehl und den Befehl selbst anzugeben.

## <a name="examples"></a>Beispiele

Die folgenden Beispiele zeigen die ordnungsgemäße Verwendung dieser Methode in JScript, VBScript und Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnFolderItem2InvokeVerbExJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("NOTEPAD.EXE");
            if (objFolderItem != null)
            {
                objFolderItem.InvokeVerbEx("open", "c:\\autoexec.bat");
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFolderItemInvokeVerbExVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.Self
                if (not objFolderItem is nothing) then
                    objFolderItem.InvokeVerbEx()
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnFolderItem2InvokeVerbExVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem2 As Object
            
            Set objFolderItem2 = objFolder2.ParseName("NOTEPAD.EXE")
                If (Not objFolderItem2 Is Nothing) Then
                    objFolderItem2.InvokeVerbEx ("open")
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem2 = Nothing
        Else
            'Folder object returned nothing.
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

[**Shellfolderitem**](shellfolderitem-object.md)
</dt> <dt>

[**Invokeverb**](folderitem-invokeverb.md)
</dt> </dl>

 

 




