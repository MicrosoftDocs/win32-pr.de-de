---
description: 'IShellDispatch2.IsServiceRunning-Methode: Gibt einen Wert zurück, der angibt, ob ein bestimmter Dienst ausgeführt wird.'
ms.assetid: 91f3fba1-7aa5-423a-bc37-49db230c79db
title: IShellDispatch2.IsServiceRunning-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.IsServiceRunning
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e8ad792f1669a8ebcfa411c58b34da214ccf69a7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117088"
---
# <a name="ishelldispatch2isservicerunning-method"></a>IShellDispatch2.IsServiceRunning-Methode

Gibt einen Wert zurück, der angibt, ob ein bestimmter Dienst ausgeführt wird.

## <a name="syntax"></a>Syntax


```JScript
retVal = IShellDispatch2.IsServiceRunning(
  sServiceName
)
```


```VB

IShellDispatch2.IsServiceRunning( _
  ByVal sServiceName As BSTR _
) As Variant
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*sServiceName* \[ In\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine **Zeichenfolge,** die den Namen des Diensts enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Typ: **\* Variant**

Gibt **TRUE zurück,** wenn der von *sServiceName angegebene Dienst* ausgeführt wird. andernfalls **FALSE.**

### <a name="vb"></a>VB

Typ: **\* Variant**

Gibt **TRUE zurück,** wenn der von *sServiceName angegebene Dienst* ausgeführt wird. andernfalls **FALSE.**

## <a name="remarks"></a>Bemerkungen

Diese Methode wird implementiert und über die [**Shell.IsServiceRunning-Methode aufgerufen.**](./shell-isservicerunning.md)

Diese Methode ist derzeit in Microsoft Visual Basic.

## <a name="examples"></a>Beispiele

Die folgenden Beispiele zeigen die Verwendung von **IsServiceRunning,** um zu bestimmen, ob der Themes-Dienst für eine Anwendung ausgeführt wird. Die Verwendung wird für JScript und VBScript angezeigt.

Jscript:


```JScript
<script language="JScript">
    function fnIsServiceRunningJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
    
        bReturn = objShell.IsServiceRunning("Themes");
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnIsServiceRunningVB()
        dim objShell
        dim bReturn
    
        set objShell = CreateObject("shell.application")
    
        bReturn = objShell.IsServiceRunning("Themes")
    
        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



 

 
