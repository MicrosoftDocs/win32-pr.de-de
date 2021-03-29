---
description: Beendet einen benannten Dienst.
ms.assetid: f4cd0e2c-4ecc-4e9f-a0b5-d2a8a739f0e2
title: IShellDispatch2. servicestop-Methode (Shldisp. h)
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
ms.openlocfilehash: 6a4a76c1f53309c14875eeaf6f3f4c0839a511bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978017"
---
# <a name="ishelldispatch2servicestop-method"></a>IShellDispatch2. servicestop-Methode

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

*sservicename* \[ in\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine **Zeichenfolge** , die den Namen des Dienstanbieter enthält.

</dd> <dt>

*vpersistent* \[ in\]
</dt> <dd>

Typ: **Variant**

Legen Sie diese Einstellung auf **true** fest, damit der Dienst vom Dienststeuerungs-Manager gestartet wird, wenn [**Servicestart**](ishelldispatch2-servicestart.md) aufgerufen wird. Legen Sie *vpersistenz* auf **false** fest, um die Dienst Konfiguration unverändert zu lassen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Typ: **Variant \** _

Gibt _ *true** zurück, wenn erfolgreich; andernfalls **false**.

### <a name="vb"></a>VB

Typ: **Variant \** _

Gibt _ *true** zurück, wenn erfolgreich; andernfalls **false**.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird implementiert und über die [**Shell. servicestop**](./shell-servicestop.md) -Methode aufgerufen.

Die Methode gibt **false** zurück, wenn der Dienst bereits beendet wurde. Bevor Sie diese Methode aufrufen, können Sie [**Shell. isservicerunning**](./shell-isservicerunning.md) aufrufen, um den Status des Dienstanbieter zu ermitteln.

Diese Methode ist zurzeit nicht in Microsoft Visual Basic verfügbar.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird gezeigt, wie **servicestop** verwendet wird, um den Messenger-Dienst zu verhindern. Die Verwendung wird für JScript und VBScript angezeigt.

JScript


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



VBScript


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



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



 

 
