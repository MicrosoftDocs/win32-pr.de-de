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
ms.openlocfilehash: 579748ae3b2e650e53e0f903b2ba2342e0ab9e522ae84c06c1ae4e13398c8762
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090350"
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

Gibt **TRUE** zurück, wenn der von *sServiceName* angegebene Dienst ausgeführt wird. andernfalls **FALSE.**

### <a name="vb"></a>VB

Typ: **\* Variant**

Gibt **TRUE** zurück, wenn der von *sServiceName* angegebene Dienst ausgeführt wird. andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Diese Methode wird implementiert und über die [**Shell.IsServiceRunning-Methode**](./shell-isservicerunning.md) aufgerufen.

Diese Methode ist in Microsoft Visual Basic derzeit nicht verfügbar.

## <a name="examples"></a>Beispiele

Die folgenden Beispiele zeigen die Verwendung von **IsServiceRunning,** um zu bestimmen, ob der Themes-Dienst für eine Anwendung ausgeführt wird. Die Verwendung wird für JScript und VBScript angezeigt.

JScript:


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



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



 

 
