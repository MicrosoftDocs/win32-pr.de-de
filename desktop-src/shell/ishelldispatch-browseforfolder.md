---
description: 'IShellDispatch.BrowseForFolder-Methode: Erstellt ein Dialogfeld, in dem der Benutzer einen Ordner auswählen und dann das Ordnerobjekt des ausgewählten Ordners zurückgibt.'
ms.assetid: 578C51C1-F59B-4604-A09B-62BA61225ABB
title: IShellDispatch.BrowseForFolder-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.BrowseForFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ee6202c7029e2c27684e15d96dd6c38680cb0678
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086688"
---
# <a name="ishelldispatchbrowseforfolder-method"></a>IShellDispatch.BrowseForFolder-Methode

Erstellt ein Dialogfeld, in dem der Benutzer einen Ordner auswählen und dann das Ordnerobjekt des ausgewählten [**Ordners zurückgibt.**](folder.md)

## <a name="syntax"></a>Syntax


```JScript
retVal = IShellDispatch.BrowseForFolder(
  Hwnd,
  sTitle,
  iOptions,
  [ vRootFolder ]
)
```


```VB

IShellDispatch.BrowseForFolder( _
  ByVal Hwnd As Integer, _
  ByVal sTitle As BSTR, _
  ByVal iOptions As Integer, _
  [ ByVal vRootFolder As Variant ] _
) As FOLDER
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*Hwnd* \[ In\]
</dt> <dd>

Typ: **Integer**

Das Handle für das übergeordnete Fenster des Dialogfelds. Dieser Wert kann auch 0 sein.

</dd> <dt>

*sTitle* \[ In\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Ein **Zeichenfolgenwert,** der den im Dialogfeld Durchsuchen **angezeigten Titel** darstellt.

</dd> <dt>

*iOptions* \[ In\]
</dt> <dd>

Typ: **Integer**

Ein **Ganzzahlwert,** der die Optionen für die Methode enthält. Dies kann 0 (null) oder eine Kombination der Werte sein, die unter dem **ulFlags-Element** der [**BROWSEINFO-Struktur aufgeführt**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) sind.

</dd> <dt>

*vRootFolder* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Der Stammordner, der im Dialogfeld verwendet werden soll. Der Benutzer kann in der Struktur nicht höher als in diesem Ordner suchen. Wenn dieser Wert nicht angegeben wird, ist der Stammordner, der im Dialogfeld verwendet wird, der Desktop. Dieser Wert kann eine Zeichenfolge sein, die den Pfad des Ordners oder einen der [**ShellSpecialFolderConstants-Werte angibt.**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) Beachten Sie, dass die konstanten Namen in **ShellSpecialFolderConstants** in Visual Basic, aber nicht in VBScript oder JScript verfügbar sind. In diesen Fällen müssen die numerischen Werte an ihrer Stelle verwendet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Typ: **\* \* FOLDER**

Ein Objektverweis auf das [**Folder-Objekt**](folder.md) des ausgewählten Ordners.

### <a name="vb"></a>VB

Typ: **\* \* FOLDER**

Ein Objektverweis auf das [**Folder-Objekt**](folder.md) des ausgewählten Ordners.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird implementiert und über die [**Shell.BrowseForFolder-Methode**](shell-browseforfolder.md) aufgerufen.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird **BrowseForFolder** verwendet, um ein Suchfenster mit dem Titel "Beispiel" anzuzeigen, das sich im Windows-Ordner befindet. Die Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

Jscript:


```JScript
<script language="JScript">
    function fnShellBrowseForFolderJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36;
        var objFolder;
        
        objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS);
        if (objFolder != null)
        {
            // Add code here.
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellBrowseForFolderVB()
        dim objShell
        dim ssfWINDOWS
        dim objFolder
        
        ssfWINDOWS = 36
        set objShell = CreateObject("shell.application")
            set objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
                if (not objFolder is nothing) then
                    'Add code here.
                end if
            set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellBrowseForFolderVB()
    Dim objShell   As Shell
    Dim ssfWINDOWS As Long
    Dim objFolder  As Folder
    
    ssfWINDOWS = 36
    Set objShell = New Shell
        Set objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
            If (Not objFolder Is Nothing) Then
                'Add code here
            End If
        Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 
