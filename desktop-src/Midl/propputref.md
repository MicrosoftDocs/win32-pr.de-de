---
title: propputref-Attribut
description: Das \propputref\-Attribut gibt eine Eigenschaftseinstellungsfunktion an, die einen Verweis anstelle eines Werts verwendet.
ms.assetid: 84f1cd08-3c42-4a6d-bb1d-0bfd3f4c33f2
keywords:
- PROPPUTREF-Attribut MIDL
topic_type:
- apiref
api_name:
- propputref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97e80b0baa4f78537142043b374c206ade0f3d51d7ca30c2f57e1c4ae4e9b695
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641963"
---
# <a name="propputref-attribute"></a>propputref-Attribut

Das **\[ \] propputref-Attribut** gibt eine Eigenschaftseinstellungsfunktion an, die einen Verweis anstelle eines Werts verwendet.

``` syntax
[propputref [,optional-property-attributes]] return-type function-name( parameters);
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

Eine Funktion, die über das **\[ propputref-Attribut \]** verfügt, muss als letzten Parameter auch einen Zeiger mit dem **\[** [**in-Attribut**](in.md) **\]** aufweisen.

Die Eigenschaft muss den gleichen Namen wie die Funktion aufweisen. Höchstens eines der **\[** [**Propget-,**](propget.md) **\]** **\[** [**Propput-**](propput.md) **\]** und **\[ Propputref-Attribute \]** kann für eine Funktion angegeben werden.

### <a name="flags"></a>Flags

INVOKE \_ PROPERTYPUTREF

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

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**In**](in.md)
</dt> <dt>

[BEISPIEL FÜR ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**Propput**](propput.md)
</dt> <dt>

[**Typeflags**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 