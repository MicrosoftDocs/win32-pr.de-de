---
title: ref-Attribut
description: Das Attribut \ref\ identifiziert einen Verweiszeiger. Es wird einfach verwendet, um eine Deskriptionsebene zu darstellen.
ms.assetid: db4ff938-0f38-4f77-bb65-f728ffd609e0
keywords:
- ref-Attribut MIDL
topic_type:
- apiref
api_name:
- ref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 916556bdee83817f512c2d86eef2d768c3f6dbddf06b39408da5c25a2ba10ed2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013668"
---
# <a name="ref-attribute"></a>ref-Attribut

Das **\[ ref-Attribut \]** identifiziert einen Verweiszeiger. Es wird einfach verwendet, um eine Deskriptionsebene zu darstellen.

``` syntax
pointer_default(ref)

typedef [ ref [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef [ struct | union ] 
{
    [ ref [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...}

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ ref [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
    , ...);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*type-attribute-list* 
</dt> <dd>

Gibt ein oder mehrere Attribute an, die für den Typ gelten. Gültige Typattribute sind handle, switch type , transmit as , die Zeigerattribute **\[** [](handle.md) **\]** **\[** [**\_**](switch-type.md) **\]** **\[** [**\_**](transmit-as.md) **\]** **\[ \] ref**, **\[** [**unique**](unique.md)oder **\]** **\[** [**ptr**](ptr.md) **\]** und **\[** [**\_**](context-handle.md) **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** die Kontexthand handle für die Verwendungsattribute , string und ignorieren . Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*Typspezifizierer* 
</dt> <dd>

Gibt einen [Basistyp, eine](midl-base-types.md) [**Struktur,**](struct.md)eine [**Union**](union.md)oder einen [**enum-Typ**](enum.md) oder Typbezeichner an. Eine optionale Speicherspezifikation kann dem *Typspezifizierer vorangestellt werden.*

</dd> <dt>

*Standarddeklarator* 
</dt> <dd>

Gibt einen C-Standarddeklarator an, z. B. einen Bezeichner, einen Zeigerdeklarator oder einen Arraydeklarator. Weitere Informationen finden Sie unter [Array- und Sized-Pointer Attribute,](array-and-sized-pointer-attributes.md) [**Arrays**](arrays-1.md)und [Arrays und Zeiger.](/windows/desktop/Rpc/arrays-and-pointers)

</dd> <dt>

*declarator-list* 
</dt> <dd>

Gibt C-Standarddeklaratoren an, z. B. Bezeichner, Zeigerdeklaratoren und Arraydeklaratoren. Weitere Informationen finden Sie unter [Array- und Sized-Pointer Attribute,](array-and-sized-pointer-attributes.md) [**Arrays**](arrays-1.md)und [Arrays und Zeiger.](/windows/desktop/Rpc/arrays-and-pointers) Die *Declaratorliste besteht* aus einem oder mehreren Deklaratoren, die durch Kommas getrennt sind. Der Parameternamenbezeichner im Funktionsdeklarator ist optional.

</dd> <dt>

*Feldattributliste* 
</dt> <dd>

Gibt null oder mehr Feldattribute an, die für die Struktur, den Union-Member oder den Funktionsparameter gelten. Zu den gültigen Feldattributen zählen zuerst ist , last ist , length ist , max ist , size ist ; die Verwendungsattribute string , ignore und context **\[** [**\_**](first-is.md)handle; das **\]** **\[** [**\_**](last-is.md) **\]** **\[** [**\_**](length-is.md) **\]** **\[** [**\_**](max-is.md) **\]** **\[** [**\_**](size-is.md) **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** **\[** [**\_**](context-handle.md) **\]** Zeigerattribut **\[ ref, \]** **\[** [**unique**](unique.md) **\]** oder **\[** [**ptr**](ptr.md)und der **\]** Union-Attributschaltertyp **\[** [**\_**](switch-type.md) **\]** . Trennen Sie mehrere Feldattribute durch Kommas.

</dd> <dt>

*function-attribute-list* 
</dt> <dd>

Gibt null oder mehr Attribute an, die für die Funktion gelten. Gültige Funktionsattribute sind **\[** [**rückruf**](callback.md), local, das **\]** **\[** [](local.md) **\]** Zeigerattribut **\[ ref, \]** **\[** [**unique**](unique.md)oder ptr und die **\]** **\[** [](ptr.md) **\]** Verwendungsattribute Zeichenfolge **\[** [](string.md) **\]** , **\[** [**ignorieren**](ignore.md) **\]** und **\[** [**\_ Kontexthand handle**](context-handle.md) **\]** .

</dd> <dt>

*ptr-decl* 
</dt> <dd>

Gibt mindestens einen Zeigerdeklarator an, für den das **\[ ref-Attribut \]** gilt. Ein Zeigerdeklarator ist mit dem in C verwendeten Zeigerdeklarator identisch. sie wird aus dem \* Designator, Modifizierern wie **far** und dem Qualifizierer [**const erstellt.**](const.md)

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Gibt den Namen der Remoteprozedur an.

</dd> <dt>

*parameter-attribute-list* 
</dt> <dd>

Besteht aus 0 (null) oder mehr Attributen, die für den angegebenen Parametertyp geeignet sind. Parameterattribute können die direktionalen Attribute in und aus nehmen. Die Feldattribute sind zuerst , last ist , length ist , max ist , size ist , und switch type, das Zeigerattribut **\[** [](in.md) **\]** **\[** [](out-idl.md) **\]** **\[** [**\_**](first-is.md) **\]** **\[** [**\_**](last-is.md) **\]** **\[** [**\_**](length-is.md) **\]** **\[** [**\_**](max-is.md) **\]** **\[** [**\_**](size-is.md) **\]** **\[** [**\_**](switch-type.md) **\]** **\[ ref, \]** **\[** [**unique**](unique.md)oder ptr **\]** **\[** [](ptr.md)sowie **\]** **\[** [**\_**](context-handle.md) **\]** **\[** [](string.md) **\]** das Kontexthand handle und die Zeichenfolge der Verwendungsattribute. Das ignorierte **\[** [**Verwendungsattribut**](ignore.md) **\]** kann nicht als Parameterattribut verwendet werden. Trennen Sie mehrere Attribute durch Kommas.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Ein Zeigerattribut kann als Typattribut als Feldattribut angewendet werden, das für einen Struktur member, union member oder parameter gilt. oder als Funktionsattribut, das für den Funktions-Rückgabetyp gilt. Das Zeigerattribut kann auch mit dem **\[** [**Standardschlüsselwort des \_ Zeigers angezeigt**](pointer-default.md) **\]** werden.

Ein Verweiszeiger hat die folgenden Merkmale:

-   Verweist immer auf gültigen Speicher. hat nie den Wert **NULL.** Ein Verweiszeiger kann immer dereferenziert werden.
-   Ändert sich während eines Aufrufs nie. Ein Verweiszeiger zeigt vor und nach dem Aufruf immer auf denselben Speicher auf dem Client.
-   Weist auf dem Client keinen neuen Arbeitsspeicher zu. Vom Server zurückgegebene Daten werden in vorhandenen Speicher geschrieben, der durch den Wert des Verweiszeigers vor dem Aufruf angegeben wird.
-   Verursacht kein Aliasing. Storage, auf die ein Verweiszeiger zeigt, kann von einem anderen Namen in der Funktion nicht erreicht werden.

Ein Verweiszeiger kann nicht als Typ eines Zeigers verwendet werden, der von einer Funktion zurückgegeben wird.

Wenn für einen Zeigerparameter der obersten Ebene kein Attribut angegeben wird, wird es als Verweiszeiger behandelt.

## <a name="examples"></a>Beispiele

``` syntax
[unique] char * GetFirstName( 
    [in, ref] char * pszFullName);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Arrays**](arrays-1.md)
</dt> <dt>

[Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Array- Sized-Pointer Attribute](array-and-sized-pointer-attributes.md)
</dt> <dt>

[MIDL-Basistypen](midl-base-types.md)
</dt> <dt>

[**Rückruf**](callback.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**Kontexthand \_ handle**](context-handle.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[**first \_ is**](first-is.md)
</dt> <dt>

[**Handlebezeichner**](handle.md)
</dt> <dt>

[**Ignorieren**](ignore.md)
</dt> <dt>

[**last \_ is**](last-is.md)
</dt> <dt>

[**length \_ ist**](length-is.md)
</dt> <dt>

[**lokal**](local.md)
</dt> <dt>

[**max \_ is**](max-is.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**Ptr**](ptr.md)
</dt> <dt>

[**size \_ ist**](size-is.md)
</dt> <dt>

[**Schnur**](string.md)
</dt> <dt>

[**Struktur**](struct.md)
</dt> <dt>

[**\_switch-Typ**](switch-type.md)
</dt> <dt>

[**übertragen \_ als**](transmit-as.md)
</dt> <dt>

[**Union**](union.md)
</dt> <dt>

[**Einzigartige**](unique.md)
</dt> </dl>

 

 