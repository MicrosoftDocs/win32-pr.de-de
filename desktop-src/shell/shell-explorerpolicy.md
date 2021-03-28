---
description: Ruft den Wert für eine angegebene Windows Internet Explorer-Richtlinie ab.
ms.assetid: 47E17F6A-ED43-44cd-AF77-A6E49865E1B5
title: Shell. explorerpolicy-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ExplorerPolicy
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: fea5192990b8c19c8ddfe8ffad6efe21b98625c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980864"
---
# <a name="shellexplorerpolicy-method"></a>Shell. explorerpolicy-Methode

Ruft den Wert für eine angegebene Windows Internet Explorer-Richtlinie ab.

## <a name="syntax"></a>Syntax


```JScript
retVal = Shell.ExplorerPolicy(
  bstrPolicyName
)
```


```VB

Shell.ExplorerPolicy( _
  ByVal bstrPolicyName As BSTR _
) As Variant
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstraupolicyname* \[ in\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine **Zeichenfolge** , die den Namen der Richtlinie angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Typ: **Variant \** _

Der Wert, der dem angegebenen Richtlinien Namen zugeordnet ist.

### <a name="vb"></a>VB

Typ: _*Variant \**_

Der Wert, der dem angegebenen Richtlinien Namen zugeordnet ist.

## <a name="remarks"></a>Bemerkungen

Netzwerkadministratoren können die Computerumgebung Ihrer Benutzer durch Festlegen von Richtlinien steuern und verwalten.

Der angegebene Wertname muss im Unterschlüssel "_ *HKEY \_ Current \_ User **\\** Software **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Policies **\\** Explorer**" angegeben werden. Wenn der Wertname nicht vorhanden ist, gibt die Methode **null** zurück.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird die ordnungsgemäße Verwendung von **explorerpolicy** für JScript, VBScript und Visual Basic veranschaulicht.

JScript


```JScript
<script language="JScript">
    function fnIShellDispatch4ExplorerPolicyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;
        
        vReturn = objShell.ExplorerPolicy("ValueName");
        alert(vReturn);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
     function fnIShellDispatch4ExplorerPolicyVB()
        dim objShell
        dim vReturn
        
        set objShell = CreateObject("shell.application")
            vReturn = objShell.ExplorerPolicy("ValueName")
            alert(vReturn)
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnIShellDispatch4ExplorerPolicyVB()
    Dim objShell As Shell
    Dim vReturn  As Variant
    
    Set objShell = New Shell
        vReturn = objShell.ExplorerPolicy("ValueName")
        Debug.Print vReturn
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 6,0 oder höher)</dt> </dl> |



 

 
