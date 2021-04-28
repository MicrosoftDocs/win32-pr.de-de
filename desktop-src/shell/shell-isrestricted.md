---
description: 'Shell.IsRestricted-Methode: Ruft die Einschränkungseinstellung einer Gruppe aus der Registrierung ab.'
ms.assetid: C4B3B5C0-7445-483a-885F-5283BD4D4B39
title: Shell.IsRestricted-Methode (Shldisp.h)
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
ms.openlocfilehash: 3e428c914cf95d282fd721071009efc70fcb3a4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104258"
---
# <a name="shellisrestricted-method"></a>Shell.IsRestricted-Methode

Ruft die Einschränkungseinstellung einer Gruppe aus der Registrierung ab.

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

*sGroup* \[ In\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine **Zeichenfolge,** die den Gruppennamen enthält. Dieser Wert ist der Name eines Registrierungsunterschlüssels, unter dem die Einschränkung überprüft werden soll.

</dd> <dt>

*sRestriction* \[ In\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine **Zeichenfolge,** die die Einschränkung enthält, deren Wert abgerufen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Typ: **\* Integer**

Der Wert der Einschränkung. Wenn die angegebene Einschränkung nicht gefunden wird, ist der Rückgabewert 0.

### <a name="vb"></a>VB

Typ: **\* Integer**

Der Wert der Einschränkung. Wenn die angegebene Einschränkung nicht gefunden wird, ist der Rückgabewert 0.

## <a name="remarks"></a>Bemerkungen

**IsRestricted** sucht zunächst unter dem folgenden Schlüssel nach einem Unterschlüsselnamen, der *sGroup* entspricht.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
```

Einschränkungen werden als Werte der einzelnen Richtlinienunterschlüssel deklariert. Wenn die in *sRestriction* benannte Einschränkung im Unterschlüssel mit dem Namen in *sGroup* gefunden wird, gibt **IsRestricted** den aktuellen Wert der Einschränkung zurück. Wenn die Einschränkung unter **HKEY \_ LOCAL \_ MACHINE** nicht gefunden wird, wird derselbe Unterschlüssel unter **HKEY CURRENT USER \_ \_ überprüft.**

Diese Methode ist derzeit in Microsoft Visual Basic.

## <a name="examples"></a>Beispiele

Die folgenden Beispiele zeigen die Verwendung von **IsRestricted,** um den Datenwert der Einschränkung **"undockwithoutlogon"** aus dem **Unterschlüssel System** abzurufen. Die Verwendung wird für JScript und VBScript angezeigt.

Jscript:


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



Vbscript:


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



## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



 

 
