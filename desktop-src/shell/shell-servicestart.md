---
description: 'Shell.ServiceStart-Methode: Startet einen benannten Dienst.'
ms.assetid: 72214E80-38A2-4a57-B555-942902BAFC3D
title: Shell.ServiceStart-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ServiceStart
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: afdc1e7cac8d50de08e21cfad5cb492b5b51dcb647e963b4c003e9600a924244
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709550"
---
# <a name="shellservicestart-method"></a>Shell.ServiceStart-Methode

Startet einen benannten Dienst.

## <a name="syntax"></a>Syntax


```JScript
retVal = Shell.ServiceStart(
  sServiceName,
  vPersistent
)
```


```VB

Shell.ServiceStart( _
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

Legen Sie auf **TRUE** fest, damit der Dienst während des Systemstarts automatisch vom Dienststeuerungs-Manager gestartet wird. Legen Sie auf **FALSE fest,** um die Dienstkonfiguration unverändert zu lassen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Typ: **\* Variant**

Gibt **true zurück,** wenn erfolgreich; andernfalls **FALSE.**

### <a name="vb"></a>VB

Typ: **\* Variant**

Gibt **true zurück,** wenn erfolgreich; andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Die -Methode **gibt FALSE** zurück, wenn der Dienst bereits gestartet wurde. Vor dem Aufrufen dieser Methode können Sie [**Shell.IsServiceRunning**](./shell-isservicerunning.md) aufrufen, um den Status des Diensts zu ermitteln.

Diese Methode ist derzeit in Microsoft Visual Basic.

## <a name="examples"></a>Beispiele

Die folgenden Beispiele zeigen die Verwendung von **ServiceStart zum** Starten des Messenger-Diensts. Die Verwendung wird für JScript VBScript angezeigt.

JScript:


```JScript
<script language="JScript">
    function fnServiceStartJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStart("Messenger", true);
    }
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
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



 

 
