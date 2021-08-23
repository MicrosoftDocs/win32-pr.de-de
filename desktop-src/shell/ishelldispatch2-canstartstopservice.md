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
ms.openlocfilehash: bae0ed1a6f60a363a360c8824d5b41f17b89f9040d3354b9e3011e0269e9d9e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032238"
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

## <a name="remarks"></a>Hinweise

Diese Methode wird implementiert und über die [**Shell.CanStartStopService-Methode**](./shell-canstartstopservice.md) aufgerufen.

Diese Methode ist derzeit in Microsoft Visual Basic.

## <a name="examples"></a>Beispiele

Die folgenden Beispiele zeigen die Verwendung von **CanStartStopService** für JScript und VBScript.

JScript:


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



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



 

 
