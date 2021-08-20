---
title: noncreatable-Attribut
description: Das Attribut \noncreatable\definiert ein Objekt, das nicht selbst instanziiert werden kann.
ms.assetid: 75d7b978-0f82-4e8a-89c2-ffd5b9a691d6
keywords:
- MIDL für nicht beschreibbare Attribute
topic_type:
- apiref
api_name:
- noncreatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e59c53d8e4c05d15d55a6ccd9d7fb2b5cd8783463d1f59d439c74240fdd93a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066940"
---
# <a name="noncreatable-attribute"></a>noncreatable-Attribut

Das **\[ nicht erstellbare Attribut \]** definiert ein Objekt, das nicht selbst instanziiert werden kann.

``` syntax
[
  coclass-attribute-list, 
    noncreatable
]
coclass coclass-name
{
  coclass-interface-list
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*coclass-attribute-list* 
</dt> <dd>

Andere Attribute, die für die -Klasse gelten.

</dd> <dt>

*coclass-name* 
</dt> <dd>

Der Name der Klasse.

</dd> <dt>

*coclass-interface-list* 
</dt> <dd>

Eine Liste der Schnittstellen für die -Klasse.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Use the **\[noncreatable\]** attribute on a [**coclass**](coclass.md) statement to indicate to users that they cannot create a new object of this class at the top level—that is, by calling **CreateInstance** or **CoCreateInstance**. Die Instanziierung eines Objekts dieser Klasse erfordert einen Methodenaufruf an ein anderes Objekt. In diesem Beispiel Microsoft Excel das "Cell"-Objekt nicht erstellt werden und muss aus einem Microsoft Excel erhalten werden.

Methoden, die Instanzen von nicht erstellbaren Klassen zurückgeben, sollten anstelle von **VARIANT-** oder **IDispatch-Typen** den genauen Typ des Objekts \* zurückgeben.

### <a name="typeflag-representation"></a>Typflagdarstellung:

Das Fehlen von TYPEFLAG \_ FCANCREATE.

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("This is MyCOClass"),
    noncreatable
]
coclass MyCoClass
{
    [default] interface IMyClass;
    [default, source] dispinterface IMyClassEvents;
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL-Dateibeispiel](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 