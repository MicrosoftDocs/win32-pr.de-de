---
description: Führt ein Verb für das Element aus.
ms.assetid: 569bdc88-15ef-4d08-923c-4f41e5ae5a38
title: FolderItem. invokeverb-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.InvokeVerb
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 259ff9613756940d5da8a37585dbf39fb2dc0a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524480"
---
# <a name="folderiteminvokeverb-method"></a>FolderItem. invokeverb-Methode

Führt ein Verb für das Element aus.

## <a name="syntax"></a>Syntax


```JScript
FolderItem.InvokeVerb(
  [ vVerb ]
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*vverb* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Eine Zeichenfolge, die das auszuführende Verb angibt. Dabei muss es sich um einen der Werte handeln, die von der [**FolderItemVerb.Name**](folderitemverb-name.md) -Eigenschaft des Elements zurückgegeben werden. Wenn kein Verb angegeben ist, wird das Standardverb aufgerufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Ein Verb ist eine Zeichenfolge, die verwendet wird, um eine bestimmte Aktion anzugeben, die ein Element unterstützt. Das Aufrufen eines Verbs entspricht dem Auswählen eines Befehls aus dem Kontextmenü eines Elements. Wenn Sie ein Verb aufrufen, wird in der Regel eine verwandte Anwendung gestartet. Wenn Sie z. b. das "Öffnen"-Verb in einer txt-Datei aufrufen, wird die Datei mit einem Text-Editor geöffnet, normalerweise Microsoft Notepad. Weitere Erläuterungen zu Verben finden Sie unter [Starten von Anwendungen](launch.md) .

Das [**folderitemverbs**](folderitemverbs.md) -Objekt stellt die Auflistung der Verben dar, die dem Element zugeordnet sind. Das Standardverb kann für unterschiedliche Elemente variieren, aber es ist in der Regel "geöffnet".

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **invokeverb** verwendet, um das Standard Verb (in diesem Fall "Öffnen") im Windows-Ordner aufzurufen. Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

JScript


```JScript
<script language="JScript">
    function fnFolderItemInvokeVerbJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.Self;
            if (objFolderItem != null)
            {
                var szReturn;
                
                objFolderItem.InvokeVerb();
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFolderItemInvokeVerbVB()
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
                    dim szReturn
                                
                    objFolderItem.InvokeVerb()
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
Private Sub fnFolderItemInvokeVerbVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.Self
                If (Not objFolderItem Is Nothing) Then
                    Dim szReturn As String
                    
                    objFolderItem.InvokeVerb
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Von folderItem**](folderitem.md)
</dt> <dt>

[**Verben**](folderitem-verbs.md)
</dt> <dt>

[**Doit**](folderitemverb-doit.md)
</dt> </dl>

 

 




