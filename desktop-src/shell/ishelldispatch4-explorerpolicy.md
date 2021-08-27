---
description: 'IShellDispatch4.ExplorerPolicy-Methode: Ruft den Wert für eine angegebene Windows Internet Explorer Richtlinie ab.'
ms.assetid: 490c3e18-b606-456a-9016-dc4f7bad2bc3
title: IShellDispatch4.ExplorerPolicy-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.ExplorerPolicy
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 16187fedde4a454ffaa5415ade08e61f5d0abca145caa7b5c8e29fa9f3b00cdd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111500"
---
# <a name="ishelldispatch4explorerpolicy-method"></a>IShellDispatch4.ExplorerPolicy-Methode

Ruft den Wert für eine angegebene Windows Internet Explorer Richtlinie ab.

## <a name="syntax"></a>Syntax


```JScript
retVal = IShellDispatch4.ExplorerPolicy(
  bstrPolicyName
)
```


```VB

IShellDispatch4.ExplorerPolicy( _
  ByVal bstrPolicyName As BSTR _
) As Variant
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrPolicyName* \[ In\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine **Zeichenfolge,** die den Namen der Richtlinie angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Typ: **\* Variant**

Der Wert, der dem angegebenen Richtliniennamen zugeordnet ist.

### <a name="vb"></a>VB

Typ: **\* Variant**

Der Wert, der dem angegebenen Richtliniennamen zugeordnet ist.

## <a name="remarks"></a>Hinweise

Netzwerkadministratoren können die Computerumgebung ihrer Benutzer steuern und verwalten, indem sie Richtlinien festlegen.

Der angegebene Wertname muss sich im Unterschlüssel **HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Policies** \\ **Explorer** befinden. Wenn der Wertname nicht vorhanden ist, gibt die Methode **NULL** zurück.

## <a name="examples"></a>Beispiele

Die folgenden Beispiele zeigen die ordnungsgemäße Verwendung von **ExplorerPolicy** für JScript, VBScript und Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnIShellDispatch4ExplorerPolicyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;
        
        vReturn = objshell.ExplorerPolicy("ValueName");
        alert(vReturn);
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
     function fnIShellDispatch4ExplorerPolicyVB()
        dim objShell
        dim vReturn
        
        set objShell = CreateObject("shell.application")
            vReturn = objshell.ExplorerPolicy("ValueName")
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
        vReturn = objshell.ExplorerPolicy("ValueName")
        Debug.Print vReturn
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 6.0 oder höher)</dt> </dl> |



 

 
