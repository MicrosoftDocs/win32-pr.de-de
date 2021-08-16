---
title: propget-Attribut
description: Das \propget\-Attribut gibt eine Eigenschaftenaccessorfunktion an. Die Eigenschaft muss den gleichen Namen wie die Funktion aufweisen.
ms.assetid: 0b76ece3-e19b-4c80-883c-ff414bc2e435
keywords:
- PROPGET-Attribut MIDL
topic_type:
- apiref
api_name:
- propget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aaa55521042adc07f4242a44060e2442f087e609d0e3995d8c77457c8653c66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383335"
---
# <a name="propget-attribute"></a>propget-Attribut

Das **\[ propget-Attribut \]** gibt eine Eigenschaftenaccessorfunktion an. Die Eigenschaft muss den gleichen Namen wie die Funktion aufweisen.

``` syntax
[propget [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*optional-property-attributes* 
</dt> <dd>

Null oder mehr Eigenschaftsattribute.

</dd> <dt>

*rückgabetyp* 
</dt> <dd>

Der Typ der von der Remoteprozedur zurückgegebenen Daten.

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Der Name der Remoteprozedur.

</dd> <dt>

*parameters* 
</dt> <dd>

Null oder mehr Parameter für die Remoteprozedur.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Eine Funktion, die über das Propget-Attribut verfügt, sollte auch als letzten Parameter einen Zeigertyp mit den **\[** [](out-idl.md) **\]** Out- und **\[** [**Retval-Attributen**](retval.md) **\]** aufweisen. Wenn der letzte Parameter nicht über die \[ Attribute out, retval \] verfügt, wird der Rückgabewert der Funktion als \[ out- retval-Parameter \] behandelt. Beispielsweise eine Funktion mit dem Prototyp

``` syntax
[propget] short MyFunction([in] long aLongValue);
```

wird als behandelt.

``` syntax
[propget] HRESULT MyFunction([in] long aLongValue, [out,retval] short *outValue);
```

Höchstens eines von **\[ propget, \]** **\[** [**propput**](propput.md) **\]** und **\[** [**propputref**](propputref.md) kann für eine Funktion angegeben **\]** werden.

Wenn das **\[** [**lcid-Attribut**](lcid.md) **\]** in der Parameterliste einer Funktion verwendet wird, die einen Parameter mit dem **\[** [**propput-Attribut**](propput.md) **\]** enthält, muss der **\[ \] lcid-Parameter** vor dem letzten Parameter liegen.

### <a name="flags"></a>Flags

INVOKE \_ PROPERTYGET

## <a name="examples"></a>Beispiele

``` syntax
interface MyInterface : IDispatch                         
{                
    [propget, 
     helpstring("A meaningful comment.")] HRESULT Method1(
         [out, retval] int* ReturnVal); 

    [propput, 
     helpstring("Another meaningful comment.")] HRESULT Method1(
         [in] int Value);
        
    [propget, 
     helpstring("A meaningful comment."), id(1)] HRESULT Method2(
         [out, retval] YourInterface** ReturnVal); 

    [propputref, 
     helpstring("Another meaningful comment."), 
     id(1)] HRESULT Method2([in] YourPoint* Point);
}                 
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[BEISPIEL FÜR ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**Retval**](retval.md)
</dt> <dt>

[**Propput**](propput.md)
</dt> <dt>

[**Propputref**](propputref.md)
</dt> <dt>

[**Typeflags**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 