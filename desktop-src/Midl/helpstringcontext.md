---
title: helpstringcontext-Attribut
description: Das \helpstringcontext\-Attribut gibt einen 32-Bit-Hilfekontextbezeichner in der Hilfedatei an. Sie können das Attribut \helpstringcontext\ auf bibliothek, interface, dispinterface, module, coclass, typedef-Anweisungen, Eigenschaften, Parameter und Methoden anwenden.
ms.assetid: 0ac41bd9-ccc6-4b5c-b925-63bff9254eed
keywords:
- helpstringcontext-Attribut MIDL
topic_type:
- apiref
api_name:
- helpstringcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64e97ea0d7b41d87ef1d535d562f3b515dda4f59a67f6d5e35f97bed8b1f9ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807235"
---
# <a name="helpstringcontext-attribute"></a>helpstringcontext-Attribut

Das **\[ helpstringcontext-Attribut \]** gibt einen 32-Bit-Hilfekontextbezeichner in der Hilfedatei an. Sie können das **\[ \] helpstringcontext-Attribut** auf [**Bibliothek,**](library.md) [**Schnittstelle,**](interface.md) [**Dispinterface,**](dispinterface.md) [**Modul,**](module.md) [**Co-Klasse,**](coclass.md) [**Typedef-Anweisungen,**](typedef.md) Eigenschaften, Parameter und Methoden anwenden.

``` syntax
[  helpstringcontext(contextid)[, optional-attribute-list]] idl-statement
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Contextid* 
</dt> <dd>

Eine eindeutige ganze Zahl, die den Hilfetext identifiziert, der der aktuellen MIDL-Anweisung zugeordnet ist.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Null oder mehr MIDL-Attribute.

</dd> <dt>

*idl-statement* 
</dt> <dd>

Die MIDL-Anweisung, auf **\[ die \] das helpstringcontext-Attribut** angewendet wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Verwenden Sie **die GetDocumentation2-Funktionen** in den **Schnittstellen ITypeLib2** und **ITypeInfo2,** um die Hilfezeichenfolge abzurufen.

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

 

 




