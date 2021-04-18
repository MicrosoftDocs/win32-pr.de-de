---
title: Helpstringcontext-Attribut
description: Das Attribut \ helpstringcontext \ gibt einen 32-Bit-Hilfe Kontext Bezeichner in der Hilfedatei an. Sie können das Attribut \ helpstringcontext \ auf die Anweisungen Library, Interface, dispinterface, Module, Coclass, typedef, Properties, Parameters und Methods anwenden.
ms.assetid: 0ac41bd9-ccc6-4b5c-b925-63bff9254eed
keywords:
- Helpstringcontext-Attribut-Mittel l
topic_type:
- apiref
api_name:
- helpstringcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72ddded3beb768543f2f990aa9d656fba1fa8b98
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106340662"
---
# <a name="helpstringcontext-attribute"></a>Helpstringcontext-Attribut

Das **\[ helpstringcontext \]** -Attribut gibt einen 32-Bit-Hilfe Kontext Bezeichner in der Hilfedatei an. Sie können das **\[ helpstringcontext \]** -Attribut auf [**Library**](library.md), [**Interface**](interface.md), [**dispinterface**](dispinterface.md), [**Module**](module.md), [**Co-Klasse**](coclass.md), [**typedef**](typedef.md) -Anweisungen,-Eigenschaften,-Parameter und-Methoden anwenden.

``` syntax
[  helpstringcontext(contextid)[, optional-attribute-list]] idl-statement
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*ContextId* 
</dt> <dd>

Eine eindeutige ganze Zahl, die den Hilfetext identifiziert, der der aktuellen Mittel l-Anweisung zugeordnet ist.

</dd> <dt>

*optional-Attribut-List* 
</dt> <dd>

NULL oder mehr mittlere Attribute.

</dd> <dt>

*IDL-Anweisung* 
</dt> <dd>

Die Mittell-Anweisung, auf die das **\[ helpstringcontext \]** -Attribut angewendet wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **GetDocumentation2** -Funktionen in den Schnittstellen **ITypeLib2** und **ITypeInfo2** , um die Hilfe Zeichenfolge abzurufen.

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(. . .),
    helpstringcontext(103),
    version(1.0)
]
library Lines
{
    [
        uuid(. . .), 
        helpstringcontext(102),
        oleautomation,
        dual
    ]
    interface ILine : IDispatch
    {
        [propget, helpstringcontext(100)] HRESULT Color([out, retval] long* ReturnVal); 
        [propput, helpstringcontext(101)] HRESULT Color([in] long rgb);
    }
};
```

 

 




