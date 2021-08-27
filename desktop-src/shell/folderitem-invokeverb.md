---
description: Führt ein Verb für das Element aus.
ms.assetid: 569bdc88-15ef-4d08-923c-4f41e5ae5a38
title: FolderItem.InvokeVerb-Methode (Shldisp.h)
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
ms.openlocfilehash: 1f6c45c67bd8863b6cf1169670a4d087f29e4441c48592f850a683af5ef0bc1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111790"
---
# <a name="folderiteminvokeverb-method"></a>FolderItem.InvokeVerb-Methode

Führt ein Verb für das Element aus.

## <a name="syntax"></a>Syntax


```JScript
FolderItem.InvokeVerb(
  [ vVerb ]
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*vVerb* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Eine Zeichenfolge, die das auszuführende Verb angibt. Dies muss einer der Werte sein, die von der -Eigenschaft des Elements [**FolderItemVerb.Name**](folderitemverb-name.md) werden. Wenn kein Verb angegeben wird, wird das Standardverb aufgerufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Ein Verb ist eine Zeichenfolge, die verwendet wird, um eine bestimmte Aktion anzugeben, die ein Element unterstützt. Das Aufrufen eines Verbs entspricht dem Auswählen eines Befehls im Kontextmenü eines Elements. In der Regel wird durch das Aufrufen eines Verbs eine zugehörige Anwendung gestartet. Wenn Sie beispielsweise das Verb "öffnen" für eine .txt-Datei aufrufen, wird die Datei mit einem Text-Editor geöffnet, in der Regel microsoft Editor. Weitere [Informationen zu Verben](launch.md) finden Sie unter Starten von Anwendungen.

Das [**FolderItemVerbs-Objekt**](folderitemverbs.md) stellt die Auflistung von Verben dar, die dem Element zugeordnet sind. Das Standardverb kann für verschiedene Elemente variieren, ist jedoch in der Regel "offen".

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **InvokeVerb verwendet,** um das Standardverb ("open" in diesem Fall) im Ordner Windows aufrufen. Die richtige Verwendung wird für JScript, VBScript und Visual Basic.

JScript:


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



Vbscript:


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**FolderItem**](folderitem.md)
</dt> <dt>

[**Verben**](folderitem-verbs.md)
</dt> <dt>

[**Doit**](folderitemverb-doit.md)
</dt> </dl>

 

 




