---
description: 'IShellDispatch2.CanStartStopService-Methode: Bestimmt, ob der aktuelle Benutzer den benannten Dienst starten und beenden kann.'
ms.assetid: cbb54ae9-02e6-4243-a782-e9f125c21c0d
title: IShellDispatch2.CanStartStopService-Methode (Shldisp.h)
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
ms.openlocfilehash: 600cf7fafd556a9192c4b0de4089516bc6cca2a0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117128"
---
# <a name="ishelldispatch2canstartstopservice-method"></a>IShellDispatch2.CanStartStopService-Methode

Bestimmt, ob der aktuelle Benutzer den benannten Dienst starten und beenden kann.

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

*sServiceName* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine **Zeichenfolge,** die den Namen des Diensts enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Typ: **\* Variant**

Gibt **TRUE zurück,** wenn der Benutzer den Dienst starten und beenden kann. andernfalls **FALSE.**

### <a name="vb"></a>VB

Typ: **\* Variant**

Gibt **TRUE zurück,** wenn der Benutzer den Dienst starten und beenden kann. andernfalls **FALSE.**

## <a name="remarks"></a>Bemerkungen

Diese Methode wird implementiert und über die [**Shell.CanStartStopService-Methode**](./shell-canstartstopservice.md) aufgerufen.

Diese Methode ist derzeit in Microsoft Visual Basic.

## <a name="examples"></a>Beispiele

Die folgenden Beispiele zeigen die Verwendung von **CanStartStopService** für JScript und VBScript.

Jscript:


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



Vbscript:


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



## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



 

 
