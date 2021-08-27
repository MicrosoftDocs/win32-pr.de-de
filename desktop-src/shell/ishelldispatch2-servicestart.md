---
description: 'IShellDispatch2.ServiceStart-Methode: Startet einen benannten Dienst.'
ms.assetid: 3af57cdc-f449-433d-a9e1-119038045e4c
title: IShellDispatch2.ServiceStart-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ServiceStart
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f48d13e593898b7b4f91fc9246745b183b928ffaa0a799100990a327a3f670ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090340"
---
# <a name="ishelldispatch2servicestart-method"></a>IShellDispatch2.ServiceStart-Methode

Startet einen benannten Dienst.

## <a name="syntax"></a>Syntax


```JScript
retVal = IShellDispatch2.ServiceStart(
  sServiceName,
  vPersistent
)
```


```VB

IShellDispatch2.ServiceStart( _
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

Legen Sie diese Einstellung auf **TRUE** fest, damit der Dienst während des Systemstarts automatisch vom Dienststeuerungs-Manager gestartet wird. Legen Sie diese Einstellung auf **FALSE** fest, um die Dienstkonfiguration unverändert zu lassen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Typ: **\* Variant**

Gibt **true** zurück, wenn erfolgreich. andernfalls **FALSE.**

### <a name="vb"></a>VB

Typ: **\* Variant**

Gibt **true** zurück, wenn erfolgreich. andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Diese Methode wird implementiert und über die [**Shell.ServiceStart-Methode**](./shell-servicestart.md) aufgerufen.

Die Methode gibt **FALSE** zurück, wenn der Dienst bereits gestartet wurde. Vor dem Aufrufen dieser Methode können Sie [**Shell.IsServiceRunning**](./shell-isservicerunning.md) aufrufen, um den Status des Diensts zu ermitteln.

Diese Methode ist in Microsoft Visual Basic derzeit nicht verfügbar.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird die Verwendung von **ServiceStart** zum Starten des Messenger-Diensts gezeigt. Die Verwendung wird für JScript und VBScript angezeigt.

JScript:


```JScript
<script language="JScript">
    function fnServiceStartJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStart("Messenger", true);
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnServiceStartVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStart("Messenger", true)

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



 

 
