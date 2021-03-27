---
description: Gibt einen Wert zurück, der angibt, ob ein bestimmter Dienst ausgeführt wird.
ms.assetid: FDC41C2D-7462-458f-BBE6-D97260C26B6C
title: Shell. isservicerunning-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.IsServiceRunning
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c3a65be4955c6f49e8e6baa49cd9dedb82fc5cc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865263"
---
# <a name="shellisservicerunning-method"></a>Shell. isservicerunning-Methode

Gibt einen Wert zurück, der angibt, ob ein bestimmter Dienst ausgeführt wird.

## <a name="syntax"></a>Syntax


```JScript
retVal = Shell.IsServiceRunning(
  sServiceName
)
```


```VB

Shell.IsServiceRunning( _
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

Diese Methode ist zurzeit nicht in Microsoft Visual Basic verfügbar.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird die Verwendung von **isservicerunning** veranschaulicht, um zu bestimmen, ob der Themes-Dienst für eine Anwendung ausgeführt wird. Die Verwendung wird für JScript und VBScript angezeigt.

JScript


```JScript
function fnIsServiceRunningJ()
{
    var objShell = new ActiveXObject("shell.application");
    var bReturn;

    bReturn = objShell.IsServiceRunning("Themes");
}
```



VBScript


```VB
function fnIsServiceRunningVB()
    dim objShell
    dim bReturn

    set objShell = CreateObject("shell.application")

    bReturn = objShell.IsServiceRunning("Themes")

    set objShell = nothing
end function
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



 

 
