---
title: propputref-Attribut
description: Das Attribut \ propputref \ gibt eine Eigenschafts Einstellungs Funktion an, die einen Verweis anstelle eines Werts verwendet.
ms.assetid: 84f1cd08-3c42-4a6d-bb1d-0bfd3f4c33f2
keywords:
- propputref-Attribut-Mittel l
topic_type:
- apiref
api_name:
- propputref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead5ccf7f9dc6a59580b7c3e3576f3c7503ccafc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948617"
---
# <a name="propputref-attribute"></a>propputref-Attribut

Das **\[ PROPPUTREF \]** -Attribut gibt eine Eigenschafts Einstellungs Funktion an, die einen Verweis anstelle eines Werts verwendet.

``` syntax
[propputref [,optional-property-attributes]] return-type function-name( parameters);
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

Eine Funktion, die über das **\[ PROPPUTREF \]** -Attribut verfügt, muss auch, als letzten Parameter, einen Zeiger **\[** [**mit dem in**](in.md) -Attribut aufweisen **\]** .

Die-Eigenschaft muss den gleichen Namen wie die Funktion aufweisen. **\[** Für eine Funktion kann höchstens ein [**propget**](propget.md) **\]** -, **\[** [**PROPPUT**](propput.md) **\]** -und **\[ PROPPUTREF \]** -Attribut angegeben werden.

### <a name="flags"></a>Flags

\_propertyputref aufrufen

## <a name="examples"></a>Beispiele

``` syntax
interface InMyFace : IDispatch 
{
    [propget, 
     helpstring("A meaningful comment."), 
     id(1)] HRESULT Method2([out, retval] YourInterface** ReturnVal); 
    [propputref, 
     helpstring("Another meaningful comment."), 
     id(1)] HRESULT Method2([in] YourPoint* Point);
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**FUNCFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 