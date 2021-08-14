---
description: 'IShellDispatch2.ServiceStop-Methode: Beendet einen benannten Dienst.'
ms.assetid: f4cd0e2c-4ecc-4e9f-a0b5-d2a8a739f0e2
title: IShellDispatch2.ServiceStop-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ServiceStop
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 71bc0502d45e4092decfe1b712ed11f75a02bf50d112436ad1d21f9e02c17e72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118221021"
---
# <a name="ishelldispatch2servicestop-method"></a>IShellDispatch2.ServiceStop-Methode

Beendet einen benannten Dienst.

## <a name="syntax"></a>Syntax


```JScript
retVal = IShellDispatch2.ServiceStop(
  sServiceName,
  vPersistent
)
```


```VB

IShellDispatch2.ServiceStop( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*sServiceName* \[ In\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine **Zeichenfolge,** die den Namen des Diensts enthält.

</dd> <dt>

*vPersistent* \[ In\]
</dt> <dd>

Typ: **Variant**

Legen Sie diese Einstellung auf **TRUE** fest, damit der Dienst vom Dienststeuerungs-Manager gestartet wird, wenn [**ServiceStart**](ishelldispatch2-servicestart.md) aufgerufen wird. Um die Dienstkonfiguration unverändert zu lassen, legen Sie *vPersistent* auf **false** fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Typ: **\* Variant**

Gibt **true** zurück, wenn erfolgreich. andernfalls **FALSE.**

### <a name="vb"></a>VB

Typ: **\* Variant**

Gibt **true** zurück, wenn erfolgreich. andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Diese Methode wird implementiert und über die [**Shell.ServiceStop-Methode**](./shell-servicestop.md) aufgerufen.

Die Methode gibt **FALSE** zurück, wenn der Dienst bereits beendet wurde. Vor dem Aufrufen dieser Methode können Sie [**Shell.IsServiceRunning**](./shell-isservicerunning.md) aufrufen, um den Status des Diensts zu ermitteln.

Diese Methode ist derzeit in Microsoft Visual Basic nicht verfügbar.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird die Verwendung von **ServiceStop** zum Beenden des Messenger-Diensts gezeigt. Die Verwendung wird für JScript und VBScript angezeigt.

JScript:


```JScript
<script language="JScript">
    function fnServiceStopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStop("Messenger", true);
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnServiceStopVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStop("Messenger", true)

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



 

 
