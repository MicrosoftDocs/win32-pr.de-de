---
description: Gibt einen Wert zurück, der angibt, ob ein bestimmter Dienst ausgeführt wird.
ms.assetid: 91f3fba1-7aa5-423a-bc37-49db230c79db
title: IShellDispatch2. isservicerunning-Methode (Shldisp. h)
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
ms.openlocfilehash: f39cd7da3d9959830208ab971b636e146e549775
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978048"
---
# <a name="ishelldispatch2isservicerunning-method"></a>IShellDispatch2. isservicerunning-Methode

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

*sservicename* \[ in\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine **Zeichenfolge** , die den Namen des Dienstanbieter enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Typ: **Variant \** _

Gibt _ *true** zurück, wenn der von *sservicename* angegebene Dienst ausgeführt wird. andernfalls **false**.

### <a name="vb"></a>VB

Typ: **Variant \** _

Gibt _ *true** zurück, wenn der von *sservicename* angegebene Dienst ausgeführt wird. andernfalls **false**.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird implementiert und über die [**Shell. isservicerunning**](./shell-isservicerunning.md) -Methode aufgerufen.

Diese Methode ist zurzeit nicht in Microsoft Visual Basic verfügbar.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird die Verwendung von **isservicerunning** veranschaulicht, um zu bestimmen, ob der Themes-Dienst für eine Anwendung ausgeführt wird. Die Verwendung wird für JScript und VBScript angezeigt.

JScript


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



VBScript


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



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



 

 
