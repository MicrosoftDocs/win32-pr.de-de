---
description: Führt ein Verb für eine Auflistung von FolderItem-Objekten aus. Diese Methode ist eine Erweiterung der InvokeVerb-Methode, die eine zusätzliche Steuerung des Vorgangs über einen Satz von Flags ermöglicht.
ms.assetid: 2c02985d-8877-4a02-a232-6aeb1716928c
title: FolderItems2.InvokeVerbEx-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems2.InvokeVerbEx
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 94d62de132a61bb357acac77aea41d2278ba1eb4453afa826ac32be90095ab25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860149"
---
# <a name="folderitems2invokeverbex-method"></a>FolderItems2.InvokeVerbEx-Methode

Führt ein Verb für eine Auflistung von [**FolderItem-Objekten**](folderitem.md) aus. Diese Methode ist eine Erweiterung der [**InvokeVerb-Methode,**](folderitem-invokeverb.md) die eine zusätzliche Steuerung des Vorgangs über einen Satz von Flags ermöglicht.

## <a name="syntax"></a>Syntax


```JScript
iRetVal = FolderItems2.InvokeVerbEx(
  [ vVerb ],
  [ vArgs ]
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*vVerb* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Eine **Variante** mit der Verbzeichenfolge, die dem auszuführenden Befehl entspricht. Wenn kein Verb angegeben wird, wird das Standardverb ausgeführt.

</dd> <dt>

*vArgs* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Eine **Variante,** die aus einer Zeichenfolge mit mindestens einem Argument für den von *vVerb angegebenen Befehl besteht.* Das Format dieser Zeichenfolge hängt vom jeweiligen Verb ab.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Ein Verb ist eine Zeichenfolge, die verwendet wird, um eine bestimmte Aktion anzugeben, die einem Element oder einer Auflistung von Elementen zugeordnet ist. In der Regel wird durch aufrufen eines Verbs eine zugehörige Anwendung gestartet. Wenn Sie z. B. das **geöffnete** Verb für eine .txt-Datei aufrufen, wird die Datei normalerweise mit einem Text-Editor geöffnet, in der Regel microsoft Editor. Weitere Informationen zu Verben finden Sie unter [Starten von Anwendungen](launch.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **InvokeVerbEx** verwendet, um das Standardverb ("open") für **Arbeitsplatz.** Die richtige Verwendung wird für JScript, VBScript und Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnFolderItems2InvokeVerbExJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder;
        var ssfDRIVES = 17;
        
        objFolder = objShell.NameSpace(ssfDRIVES);
        if (objFolder != null)
        {
            var objFolderItems2;
            
            objFolderItems2 = objFolder.Items();
            if (objFolderItems2 != null)
            {
                objFolderItems2.InvokeVerbEx();
            }
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnFolderItems2InvokeVerbExVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfDRIVES
                
            ssfWINDOWS = 17
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems2
                        
                set objFolderItems2 = objFolder.Items()
                if (not objFolderItems2 is nothing) then
                    objFolderItems2.InvokeVerbEx
                end if
                set objFolderItems2 = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub fnFolderItems2InvokeVerbExVB()
    Dim objShell      As Shell
    Dim objFolder     As Folder2
    Dim ssfDRIVES     As Long
    
    ssfDRIVES = 17
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfDRIVES)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems2 As FolderItems
            
            Set objFolderItems2 = objFolder.Items
                If (Not objFolderItems2 Is Nothing) Then
                    objFolderItems2.InvokeVerbEx
                End If
            Set objFolderItems2 = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**FolderItems2**](folderitems2-object.md)
</dt> <dt>

[**InvokeVerb**](folderitem-invokeverb.md)
</dt> </dl>

 

 




