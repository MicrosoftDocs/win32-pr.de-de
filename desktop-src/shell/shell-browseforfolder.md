---
description: Erstellt ein Dialogfeld, das dem Benutzer ermöglicht, einen Ordner auszuwählen, und gibt dann das Ordner Objekt des ausgewählten Ordners zurück.
title: Shell. Browse forfolder-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.BrowseForFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 4cc44e5a-3578-448b-9b19-1b71e1ae2cb9
ms.openlocfilehash: 7e14dffbfb9ab3e18bd4d8e11ffaf4768ad53131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042504"
---
# <a name="shellbrowseforfolder-method"></a>Shell. Browse forfolder-Methode

Erstellt ein Dialogfeld, das dem Benutzer ermöglicht, einen Ordner auszuwählen, und gibt dann das [**Ordner**](folder.md) Objekt des ausgewählten Ordners zurück.

## <a name="syntax"></a>Syntax


```JScript
retVal = Shell.BrowseForFolder(
  Hwnd,
  sTitle,
  iOptions,
  [ vRootFolder ]
)
```


```VB

Shell.BrowseForFolder( _
  ByVal Hwnd As Integer, _
  ByVal sTitle As BSTR, _
  ByVal iOptions As Integer, _
  [ ByVal vRootFolder As Variant ] _
) As FOLDER
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* \[ in\]
</dt> <dd>

Type: **Integer**

Das Handle für das übergeordnete Fenster des Dialog Felds. Dieser Wert kann auch 0 sein.

</dd> <dt>

*stitle* \[ in\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Ein **Zeichen** folgen Wert, der den Titel darstellt, der im Dialogfeld **Durchsuchen** angezeigt wird.

</dd> <dt>

*ioptions* \[ in\]
</dt> <dd>

Type: **Integer**

Ein **ganzzahliger** Wert, der die Optionen für die Methode enthält. Dies kann 0 (null) sein oder eine Kombination der Werte sein, die unter dem **ulflags** -Member der [**Browseinfo**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) -Struktur aufgeführt sind.

</dd> <dt>

*vrootfolder* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Der Stamm Ordner, der im Dialogfeld verwendet werden soll. Der Benutzer kann nicht in der Struktur nach oben navigieren als in diesem Ordner. Wenn dieser Wert nicht angegeben wird, ist der Stamm Ordner, der im Dialogfeld verwendet wird, der Desktop. Bei diesem Wert kann es sich um eine Zeichenfolge handeln, die den Pfad des Ordners oder einen der [**shellspecialfolderconstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) -Werte angibt. Beachten Sie, dass die in **shellspecialfolderconstants** gefundenen Konstanten Namen in Visual Basic verfügbar sind, jedoch nicht in VBScript oder JScript. In diesen Fällen müssen die numerischen Werte an ihrer Stelle verwendet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Typ: **Ordner \* \***

Ein Objekt Verweis auf das [**Ordner**](folder.md) Objekt des ausgewählten Ordners.

### <a name="vb"></a>VB

Typ: **Ordner \* \***

Ein Objekt Verweis auf das [**Ordner**](folder.md) Objekt des ausgewählten Ordners.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **browsforfolder** verwendet, um ein Durchsuchen-Fenster mit dem Titel "example" im Windows-Ordner anzuzeigen. Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

JScript


```JScript
<script language="JScript">
    function fnShellBrowseForFolderJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36;
        var objFolder;
        
        objFolder = objShell.BrowseForFolder(0, "Example", 0, ssfWINDOWS);
        if (objFolder != null)
        {
            // Add code here.
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellBrowseForFolderVB()
        dim objShell
        dim ssfWINDOWS
        dim objFolder
        
        ssfWINDOWS = 36
        set objShell = CreateObject("shell.application")
            set objFolder = objShell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
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
        Set objFolder = objShell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
            If (Not objFolder Is Nothing) Then
                'Add code here
            End If
        Set objFolder = Nothing
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



 

 
