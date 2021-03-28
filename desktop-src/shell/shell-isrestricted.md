---
description: Ruft die Einschränkungs Einstellung einer Gruppe aus der Registrierung ab.
ms.assetid: C4B3B5C0-7445-483a-885F-5283BD4D4B39
title: Shell. IsRestricted-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.IsRestricted
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 2224a3ea4ea26cf39f2e15486de4f96afe5448d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216603"
---
# <a name="shellisrestricted-method"></a>Shell. IsRestricted-Methode

Ruft die Einschränkungs Einstellung einer Gruppe aus der Registrierung ab.

## <a name="syntax"></a>Syntax


```JScript
iRetVal = Shell.IsRestricted(
  sGroup,
  sRestriction
)
```


```VB

Shell.IsRestricted( _
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

_ *IsRestricted** sucht zuerst nach einem Unterschlüssel Namen, der mit *sgroup* unter dem folgenden Schlüssel übereinstimmt.

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



 

 
