---
description: Ruft die Einschränkungs Einstellung einer Gruppe aus der Registrierung ab.
ms.assetid: 04275c5f-c3ed-4962-882f-2cce0258a9f4
title: IShellDispatch2. IsRestricted-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.IsRestricted
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f666a9ed3407d12eb9cf2c28ae062a9886d7a2cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978065"
---
# <a name="ishelldispatch2isrestricted-method"></a>IShellDispatch2. IsRestricted-Methode

Ruft die Einschränkungs Einstellung einer Gruppe aus der Registrierung ab.

## <a name="syntax"></a>Syntax


```JScript
iRetVal = IShellDispatch2.IsRestricted(
  sGroup,
  sRestriction
)
```


```VB

IShellDispatch2.IsRestricted( _
  ByVal sGroup As BSTR, _
  ByVal sRestriction As BSTR _
) As Integer
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*sgroup* \[ in\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine **Zeichenfolge** , die den Gruppennamen enthält. Dieser Wert ist der Name eines Registrierungs unter Schlüssels, unter dem die Einschränkung überprüft werden soll.

</dd> <dt>

*seinschränkung* \[ in\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine **Zeichenfolge** , die die Einschränkung enthält, deren Wert abgerufen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Typ: **Integer \** _

Der Wert der Einschränkung. Wenn die angegebene Einschränkung nicht gefunden wird, ist der Rückgabewert 0.

### <a name="vb"></a>VB

Type: _*Integer \**_

Der Wert der Einschränkung. Wenn die angegebene Einschränkung nicht gefunden wird, ist der Rückgabewert 0.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird implementiert und über die [_ *Shell. IsRestricted* *](./shell-isrestricted.md) -Methode aufgerufen.

**IsRestricted** sucht zuerst nach einem Unterschlüssel Namen, der mit *sgroup* unter dem folgenden Schlüssel übereinstimmt.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
```

Einschränkungen werden als Werte der einzelnen Richtlinien Unterschlüssel deklariert. Wenn die in *seinschränkung* benannte Einschränkung in dem Unterschlüssel mit dem Namen in *sgroup* gefunden wird, gibt **IsRestricted** den aktuellen Wert der Einschränkung zurück. Wenn die Einschränkung unter **HKEY \_ local \_ Machine** nicht gefunden wird, wird unter **HKEY \_ Current \_ User** der gleiche Unterschlüssel geprüft.

Diese Methode ist zurzeit nicht in Microsoft Visual Basic verfügbar.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird die Verwendung von **IsRestricted** zum Abrufen des Daten Werts der **undockwithoutlogon** -Einschränkung aus dem **System** Unterschlüssel veranschaulicht. Die Verwendung wird für JScript und VBScript angezeigt.

JScript


```JScript
<script language="JScript">
    function fnIsRestricedJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var lReturn;
        
        lReturn = objShell.IsRestricted("system", "undockwithoutlogon");
        document.write(lReturn);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnIsRestricedVB()
        dim objShell
        dim lReturn

        set objShell = CreateObject("shell.application")

        lReturn = objShell.IsRestricted("system", "undockwithoutlogon")
        document.write(lReturn)

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



 

 
