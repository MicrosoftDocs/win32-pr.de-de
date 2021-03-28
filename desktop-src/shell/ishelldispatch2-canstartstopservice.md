---
description: Bestimmt, ob der aktuelle Benutzer den benannten Dienst starten und Abbrechen kann.
ms.assetid: cbb54ae9-02e6-4243-a782-e9f125c21c0d
title: IShellDispatch2. canstartstopservice-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.CanStartStopService
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 92655c2c561284f00204826e1848a75f00f4a04d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527329"
---
# <a name="ishelldispatch2canstartstopservice-method"></a>IShellDispatch2. canstartstopservice-Methode

Bestimmt, ob der aktuelle Benutzer den benannten Dienst starten und Abbrechen kann.

## <a name="syntax"></a>Syntax


```JScript
retVal = IShellDispatch2.CanStartStopService(
  sServiceName
)
```


```VB

IShellDispatch2.CanStartStopService( _
  ByVal sServiceName As String _
) As Variant
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*sservicename* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine **Zeichenfolge** , die den Namen des Dienstanbieter enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Typ: **Variant \** _

Gibt _ *true** zurück, wenn der Benutzer den Dienst starten und Abbrechen kann. andernfalls **false**.

### <a name="vb"></a>VB

Typ: **Variant \** _

Gibt _ *true** zurück, wenn der Benutzer den Dienst starten und Abbrechen kann. andernfalls **false**.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird implementiert und über die [**Shell. canstartstopservice**](./shell-canstartstopservice.md) -Methode aufgerufen.

Diese Methode ist zurzeit nicht in Microsoft Visual Basic verfügbar.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird die Verwendung von **canstartstopservice** für JScript und VBScript veranschaulicht.

JScript


```JScript
<script language="JScript">
    function fnCanStartStopServiceJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;

        bReturn = objShell.CanStartStopService("service name");
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnCanStartStopServiceVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.CanStartStopService("service name")

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



 

 
