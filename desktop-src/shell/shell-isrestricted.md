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
ms.openlocfilehash: 40e6c23f14b3c09a6cfe4885cc7b7bf877e3e4bfbf538645cf96b99ea451776f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968549"
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

## <a name="remarks"></a>Hinweise

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

In den folgenden Beispielen wird die Verwendung von **IsRestricted** zum Abrufen des Datenwerts der **Einschränkung undockwithoutlogon** aus dem **Unterschlüssel System** gezeigt. Die Verwendung wird für JScript VBScript angezeigt.

JScript:


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



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



 

 
