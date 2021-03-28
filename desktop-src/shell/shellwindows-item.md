---
description: Ruft ein InternetExplorer-Objekt ab, das das Shellfenster darstellt.
ms.assetid: 32390f35-f83a-45d9-a240-282da7cb2b13
title: Shellwindows. Item-Methode (Exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows.Item
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ccdb73deb1d97d9c6e1ad8c335db3c58d796a299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216417"
---
# <a name="shellwindowsitem-method"></a>Shellwindows. Item-Methode

Ruft ein [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) -Objekt ab, das das Shellfenster darstellt.

## <a name="syntax"></a>Syntax


```JScript
retVal = ShellWindows.Item(
  [ iIndex ]
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iIndex* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Der nullbasierte Index des abzurufenden Elements. Dieser Wert muss kleiner sein als der Wert der [**count**](shellwindows-count.md) -Eigenschaft. Wenn dieser Wert weggelassen wird, wird der Standardwert 0 verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***

Ein Objekt Verweis auf das [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) -Objekt, das das Shellfenster darstellt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das- [**Element**](folderitemverbs-item.md) verwendet, um das [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) -Objekt abzurufen, das das erste shellfensterelement darstellt. Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

JScript


```JavaScript
<script language="JScript">
    function fnShellWindowsItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Windows();
        if (objShellWindows != null)
        {
            var objIE;
            objIE = objShellWindows.Item();

            if (objIE != null)
            {
                alert(objIE.path());
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellWindowsItemVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Windows()

        if (not objShellWindows is nothing) then
            dim objIE
            set objIE = objShellWindows.Item

            if (not objIE is nothing) then
                Wscript.Echo objIE.path
            end if

            set objIE = nothing
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellWindowsItemVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Windows()

    If (Not objShellWindows Is Nothing) Then
        Dim objIE As InternetExplorer
        Set objIE = objShellWindows.Item

        If (Not objIE Is Nothing) Then
            Debug.Print objIE.Path
        End If

        Set objIE = Nothing
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Exdisp. h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4,71 oder höher)</dt> </dl> |



 

 
