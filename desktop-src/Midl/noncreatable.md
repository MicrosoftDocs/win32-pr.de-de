---
title: noncreatable-Attribut
description: Das Attribut \ nicht erstellbar \ definiert ein Objekt, das nicht allein instanziiert werden kann.
ms.assetid: 75d7b978-0f82-4e8a-89c2-ffd5b9a691d6
keywords:
- nicht mit einem Attribut in der Mitte
topic_type:
- apiref
api_name:
- noncreatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2aa54be3416087c06651a4bb58902a0469e8f0c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314810"
---
# <a name="noncreatable-attribute"></a>noncreatable-Attribut

Das **\[ nicht \]** Erstell Bare Attribut definiert ein Objekt, das nicht allein instanziiert werden kann.

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

*coclass-Attribute-List* 
</dt> <dd>

Andere Attribute, die auf die-Klasse angewendet werden.

</dd> <dt>

*Name der Co-Klasse* 
</dt> <dd>

Der Name der Klasse.

</dd> <dt>

*coclass-Interface-List* 
</dt> <dd>

Eine Liste der Schnittstellen für die-Klasse.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie das **\[ nicht \]** Erstell Bare Attribut in einer [**Co-Klasse**](coclass.md) -Anweisung, um Benutzern mitzuteilen, dass Sie kein neues Objekt dieser Klasse auf oberster Ebene erstellen können – d. h. durch Aufrufen von **CreateInstance** oder **CoCreateInstance**. Die Instanziierung eines Objekts dieser Klasse erfordert einen Methoden aufrufan ein anderes Objekt. In Microsoft Excel ist das "Cell"-Objekt z. b. nicht Erstell Bar und muss von einem Microsoft Excel-Arbeitsblatt Objekt abgerufen werden.

Methoden, die Instanzen von nicht erstellbar baren Klassen zurückgeben, sollten den exakten Typ des Objekts anstelle von **Variant** -oder **IDispatch** -Typen zurückgeben \* .

### <a name="typeflag-representation"></a>TYPEFLAG-Darstellung:

Das Fehlen von TYPEFLAG " \_ f".

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

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 