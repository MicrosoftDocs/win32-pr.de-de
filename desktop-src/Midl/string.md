---
title: Zeichenfolgeattribut
description: Das Attribut \ String \ gibt an, dass das eindimensionale Char-, WCHAR \_ t-, Bytearray-Array oder der-Zeiger auf ein solches Array als Zeichenfolge behandelt werden muss.
ms.assetid: 379cd59e-7540-4188-9b5c-6c25a8928999
keywords:
- Zeichen folgen Attribut-Mittel l
topic_type:
- apiref
api_name:
- string
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae2bd3c56bcf09d1c47343f903653e9d83113b1d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948691"
---
# <a name="string-attribute"></a>Zeichenfolgeattribut

Das **\[ String \]** -Attribut gibt an, dass das eindimensionale [**char**](char-idl.md)-, [**WCHAR \_ t**](wchar-t.md)-, [**Bytearray**](byte.md) -Array oder der-Zeiger auf ein solches Array als Zeichenfolge behandelt werden muss. Die Zeichenfolge kann auch ein Array (oder ein Zeiger auf ein Array) der Konstrukte sein, deren Felder alle vom Typ **Byte** sind.

``` syntax
typedef [ string [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef [ struct | union ] 
{
    [ string [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...
};

[ string [[ , function-attribute-list ]] ] type-specifier ptr-decl function-name(
  [[ [ parameter-attribute-list ] ]] type-specifier [[standard-declarator]]
  , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ string [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
  , ...);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Type-Attribute-List* 
</dt> <dd>

Gibt ein oder mehrere Attribute an, die auf einen Typ angewendet werden. Gültige Typattribute sind **\[** [**handle**](handle.md) **\]** , **\[** [**\_ Switchtyp**](switch-type.md) **\]** , über **\[** [**Tragung \_ als**](transmit-as.md) **\]** ; Zeiger Attribut Verweis **\[** [](ref.md) **\]** , **\[** [**eindeutig**](unique.md) **\]** oder **\[** [**ptr**](ptr.md) **\]** ; und die Verwendungs Attribute **\[** [**Kontext \_ handle**](context-handle.md) **\]** , **\[ String \]** und **\[** [**Ignore**](ignore.md) **\]** . Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*Typspezifizierer* 
</dt> <dd>

Gibt einen [Basistyp](midl-base-types.md), [**Strukturtyp oder**](struct.md) Typbezeichner an. Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden.

</dd> <dt>

*Standard-declarator* 
</dt> <dd>

Gibt einen Standard-C-Deklarator an, z. b. einen Bezeichner, einen zeigerdeklarator oder einen Arraydeklarator. Weitere Informationen finden Sie unter [Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**Arrays**](arrays-1.md)und [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers).

</dd> <dt>

*Deklarator-List* 
</dt> <dd>

Gibt Standard-C-Deklaratoren an, z. b. Bezeichner, Zeiger Deklaratoren und Array Deklaratoren. Weitere Informationen finden Sie unter [Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**Arrays**](arrays-1.md)und [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers). Die *declarator-List* besteht aus einem oder mehreren Deklaratoren, die durch Kommas getrennt sind. Der Parameter-Name-Bezeichner im funktionsdedeclarator ist optional.

</dd> <dt>

*Field-Attribute-List* 
</dt> <dd>

Gibt 0 (null) oder mehr Feld Attribute an, die für die Struktur, den Union-Member oder den Funktionsparameter gelten. Die zwei gültigen Feld Attribute sind **\[** [**Max \_ is**](max-is.md) , **\]** und **\[** [**size \_ ist**](size-is.md), **\]** die **\[ Zeichenfolge \]** der Verwendungs Attribute, das **\[ ignorieren \]** und das **\[ Kontext \_ \] handle**, das Zeiger Attribut **\[** [**ref**](ref.md) **\]** , **\[ Unique \]** oder **\[** [**ptr**](ptr.md) **\]** und der **\[ \_ Typ \]** des Union-Attribut Schalters. Trennen Sie mehrere Feld Attribute durch Kommas.

</dd> <dt>

*Function-Attribute-List* 
</dt> <dd>

Gibt 0 (null) oder mehr Attribute an, die für die Funktion gelten. Gültige Funktions Attribute sind **\[** [**Callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** das Zeiger Attribut **\[ ref \]**, **\[ Unique \]** oder **\[ \] ptr** und die Zeichenfolge der Verwendungs Attribute **\[ Zeichenfolge \]**, **\[ ignorieren \]** und **\[ Kontext \_ handle \]**.

</dd> <dt>

*PTR-decl* 
</dt> <dd>

Gibt einen optionalen zeigerdeklarator an, auf den das **\[ Zeichen \]** folgen Attribut angewendet wird. Ein zeigerdeklarator ist derselbe wie der in C verwendete zeigerdeklarator. Sie wird aus dem Kenn \* Zeichner, den Modifizierern, z. b. **weit**, und dem Qualifizierer " [**Konstanten**](const.md)" erstellt.

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Remote Prozedur an.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

Besteht aus null oder mehr Attributen, die für den angegebenen Parametertyp geeignet sind. Parameter Attribute können die direktionalen **\[ Attribute \] ein-und** **\[ \] Auschecken**; die Feld Attribute **\[** [**Max \_ ist**](max-is.md) **\]** , und **\[** [**size \_ ist**](size-is.md) **\]** , das Zeiger Attribut **\[ ref \]**, **\[ Unique \]** oder **\[ ptr \]** und das **\[ Kontext \_ handle \]** und die **\[ Zeichenfolge \]** der Verwendungs Attribute. Das Usage-Attribut " **\[ Ignore \]** " kann nicht als Parameter Attribut verwendet werden. Trennen Sie mehrere Attribute durch Kommas.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn das **\[ Zeichen \]** folgen Attribut mit einem Array verwendet wird, dessen Begrenzungen zur Laufzeit bestimmt werden, müssen Sie auch **\[ \_ \] eine Size** -oder **\[ Max \_ is \]** -Attribut angeben, wie im folgenden Beispiel gezeigt:

``` syntax
/* a string that can hold up to MAX_STRING_LENGTH characters */
typedef [string, max_is(MAX_STRING_LENGTH)] char line[];
```

Das **\[ String \]** -Attribut kann nicht mit Attributen verwendet werden, die den Bereich der übertragenen Elemente angeben, z. b. **\[ First \_ is \]**, **\[ Last \_ is \]** und **\[ length \_ ist \]**.

Bei Verwendung in mehrdimensionalen Arrays gilt das **\[ Zeichen \]** folgen Attribut für das äußteste ganz rechts.

Verwenden Sie zum Definieren einer gezählten Zeichenfolge nicht das **\[ String \]** -Attribut. Verwenden Sie ein Zeichen Array oder einen Zeichen basierten Zeiger wie den folgenden:

``` syntax
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
} counted_string;
```

Das **\[ String \]** -Attribut gibt an, dass der Stub eine von der Sprache bereitgestellte Methode verwenden soll, um die Länge von Zeichen folgen zu bestimmen.

Beim Deklarieren von Zeichen folgen in C müssen Sie Speicherplatz für ein zusätzliches Zeichen zuweisen, das das Ende der Zeichenfolge markiert.

## <a name="examples"></a>Beispiele

``` syntax
/* a string type that can hold up to 80 characters */ 
typedef [string] char line[81]; 
 
HRESULT Proc1([in, string] char * pszName);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Mikro**](arrays-1.md)
</dt> <dt>

[Mittel l-Basis Typen](midl-base-types.md)
</dt> <dt>

[**Rückruf**](callback.md)
</dt> <dt>

[**Char**](char-idl.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**Kontext \_ handle**](context-handle.md)
</dt> <dt>

[**Enumeration**](enum.md)
</dt> <dt>

[**der erste \_ ist**](first-is.md)
</dt> <dt>

[**bewältigen**](handle.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**lassen**](ignore.md)
</dt> <dt>

[**Letzter \_ ist**](last-is.md)
</dt> <dt>

[**Länge \_ ist**](length-is.md)
</dt> <dt>

[**nah**](local.md)
</dt> <dt>

[**Max \_ ist**](max-is.md)
</dt> <dt>

[**Zeiger \_ Standard**](pointer-default.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**Größe \_ :**](size-is.md)
</dt> <dt>

[**struct**](struct.md)
</dt> <dt>

[**\_Switchtyp**](switch-type.md)
</dt> <dt>

[**übertragen \_ als**](transmit-as.md)
</dt> <dt>

[**Union**](union.md)
</dt> <dt>

[**gem**](unique.md)
</dt> <dt>

[**WCHAR \_ t**](wchar-t.md)
</dt> </dl>

 

 