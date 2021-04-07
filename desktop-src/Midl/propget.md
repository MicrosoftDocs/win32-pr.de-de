---
title: propget-Attribut
description: Das Attribut \ Propget \ gibt eine eigenschaftenaccessorfunktion an. Die-Eigenschaft muss den gleichen Namen wie die Funktion aufweisen.
ms.assetid: 0b76ece3-e19b-4c80-883c-ff414bc2e435
keywords:
- Propget-Attribut-Mittel l
topic_type:
- apiref
api_name:
- propget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6337409e021670c282400d38b97543687fa81c2a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038834"
---
# <a name="propget-attribute"></a>propget-Attribut

Das **\[ propget \]** -Attribut gibt eine eigenschaftenaccessorfunktion an. Die-Eigenschaft muss den gleichen Namen wie die Funktion aufweisen.

``` syntax
[propget [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*optionale-Property-Attribute* 
</dt> <dd>

NULL oder mehr Eigenschafts Attribute.

</dd> <dt>

*Rückgabetyp* 
</dt> <dd>

Der Typ der Daten, die von der Remote Prozedur zurückgegeben werden.

</dd> <dt>

*function-name* 
</dt> <dd>

Der Name der Remote Prozedur.

</dd> <dt>

*parameters* 
</dt> <dd>

NULL oder mehr Parameter für die Remote Prozedur.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Eine Funktion, die über das Propget-Attribut verfügt, sollte auch, als letzten Parameter, einen Zeigertyp mit den Attributen " **\[** [**out**](out-idl.md) " **\]** und " **\[** [**retval**](retval.md) **\]** " aufweisen. Wenn der letzte Parameter nicht die \[ Attribute out, retval hat \] , wird der Rückgabewert der Funktion als " \[ out", "retval"-Parameter behandelt \] . Beispielsweise eine Funktion mit dem Prototyp

``` syntax
[propget] short MyFunction([in] long aLongValue);
```

wird behandelt als

``` syntax
[propget] HRESULT MyFunction([in] long aLongValue, [out,retval] short *outValue);
```

Für eine Funktion kann höchstens ein **\[ propget \]**-, **\[** [**PROPPUT**](propput.md) **\]** -und **\[** [**PROPPUTREF**](propputref.md) -Konstruktor **\]** angegeben werden.

Wenn das **\[** [**LCID**](lcid.md) - **\]** Attribut in der Parameterliste einer Funktion verwendet wird, die einen Parameter mit dem **\[** [**PROPPUT**](propput.md) - **\]** Attribut enthält, muss der **\[ LCID \]** -Parameter den Wert Second bis The Last aufweisen.

### <a name="flags"></a>Flags

\_PropertyGet aufrufen

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

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**vorgenommen**](out-idl.md)
</dt> <dt>

[**retval**](retval.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**FUNCFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 