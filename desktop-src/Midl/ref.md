---
title: ref-Attribut
description: Das Attribut \ Ref \ identifiziert einen Verweis Zeiger. Es wird lediglich verwendet, um eine Dereferenzierungsebene darzustellen.
ms.assetid: db4ff938-0f38-4f77-bb65-f728ffd609e0
keywords:
- Verweis Attribut-Mittel l
topic_type:
- apiref
api_name:
- ref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82bc5762eea78b3ce73ab3db58e9bb567b051675
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858185"
---
# <a name="ref-attribute"></a>ref-Attribut

Das **\[ ref \]** -Attribut identifiziert einen Verweis Zeiger. Es wird lediglich verwendet, um eine Dereferenzierungsebene darzustellen.

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

*Type-Attribute-List* 
</dt> <dd>

Gibt ein oder mehrere Attribute an, die auf den Typ angewendet werden. Gültige Typattribute sind **\[** [**handle**](handle.md) **\]** , **\[** [**\_ Switchtyp**](switch-type.md) **\]** , über **\[** [**Tragung \_ als**](transmit-as.md) **\]** ; Zeiger Attribute **\[ ref \]**, **\[** [**Unique**](unique.md) **\]** oder **\[** [**ptr**](ptr.md) **\]** ; und die Verwendungs Attribute **\[** [**Kontext \_ handle**](context-handle.md) **\]** , **\[** [**String**](string.md) **\]** und **\[** [**Ignore**](ignore.md) **\]** . Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*Typspezifizierer* 
</dt> <dd>

Gibt einen [Basistyp](midl-base-types.md), eine [**Struktur**](struct.md), eine [**Union**](union.md)oder einen Aufzählungstyp [**oder einen**](enum.md) Typbezeichner an. Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden.

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

Gibt 0 (null) oder mehr Feld Attribute an, die für die Struktur, den Union-Member oder den Funktionsparameter gelten. Gültige Feld Attribute sind **\[** [**First \_ is**](first-is.md) **\]** , **\[** [**Last \_ is**](last-is.md) **\]** , **\[** [**length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ is**](size-is.md), **\]** die Usage-Attribute **\[** [**String**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** und **\[** [**context \_ handle**](context-handle.md), **\]** das Zeiger Attribut **\[ ref \]**, **\[** [**Unique**](unique.md) **\]** oder **\[** [**ptr**](ptr.md) **\]** und der Typ des Union-Attribut **\[** [**Schalters \_**](switch-type.md) **\]** . Trennen Sie mehrere Feld Attribute durch Kommas.

</dd> <dt>

*Function-Attribute-List* 
</dt> <dd>

Gibt 0 (null) oder mehr Attribute an, die für die Funktion gelten. Gültige Funktions Attribute sind **\[** [**Callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** das Zeiger Attribut **\[ ref \]**, **\[** [**Unique**](unique.md) **\]** oder **\[** [**ptr**](ptr.md) **\]** und die Zeichenfolge der Verwendungs Attribute **\[** [**Zeichenfolge**](string.md) **\]** , **\[** [**ignorieren**](ignore.md) **\]** und **\[** [**Kontext \_ handle**](context-handle.md) **\]** .

</dd> <dt>

*PTR-decl* 
</dt> <dd>

Gibt mindestens einen zeigerdeklarator an, auf den das **\[ ref \]** -Attribut angewendet wird. Ein zeigerdeklarator ist derselbe wie der in C verwendete zeigerdeklarator. Sie wird aus dem Kenn \* Zeichner, den Modifizierern, z. b. **weit**, und dem Qualifizierer " [**Konstanten**](const.md)" erstellt.

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Remote Prozedur an.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

Besteht aus null oder mehr Attributen, die für den angegebenen Parametertyp geeignet sind. Parameter Attribute können die direktionalen **\[** [**Attribute ein**](in.md) **\]** -und **\[** [](out-idl.md) **\]** ausschalten. die Feld Attribute **\[** [**\_ sind zuerst**](first-is.md), "Last", " **\]** **\[** [**\_**](last-is.md) **\]** **\[** [**length \_**](length-is.md)" **\]** , " **\[** [**Max \_ is**](max-is.md)" **\]** , "size" und " **\[** [**\_**](size-is.md) **\]** **\[** [**Switch \_ Type**](switch-type.md)", **\]** das Zeiger Attribut " **\[ \] ref**", " **\[** [**Unique**](unique.md)" **\]** oder " **\[** [**ptr**](ptr.md)" **\]** und das **\[** [**Kontext \_ handle**](context-handle.md) und die **\]** **\[** [**Zeichenfolge**](string.md) **\]** der Verwendungs Attribute Das Usage-Attribut " **\[** [**Ignore**](ignore.md) " **\]** kann nicht als Parameter Attribut verwendet werden. Trennen Sie mehrere Attribute durch Kommas.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Ein Zeiger Attribut kann als Type-Attribut, als Feld Attribut, das auf einen Strukturmember, Union-Member oder Parameter angewendet wird, angewendet werden. oder als Funktions Attribut, das für den Funktions Rückgabetyp gilt. Das Zeiger Attribut kann auch mit dem **\[** [**Zeiger \_ default**](pointer-default.md) - **\]** Schlüsselwort angezeigt werden.

Ein Verweis Zeiger hat die folgenden Eigenschaften:

-   Verweist immer auf einen gültigen Speicherplatz. hat nie den Wert **null**. Ein Verweis Zeiger kann immer dereferenziert werden.
-   Ändert sich nie während eines Aufrufes. Ein Verweis Zeiger zeigt vor und nach dem-Befehl immer auf den gleichen Speicher auf dem Client.
-   Weist keinen neuen Arbeitsspeicher auf dem Client zu. Die vom Server zurückgegebenen Daten werden in den vorhandenen Speicher geschrieben, der durch den Wert des Verweis Zeigers vor dem-Befehl angegeben wird.
-   Führt nicht zum Aliasing. Speicher, auf den von einem Verweis Zeiger verwiesen wird, kann nicht von einem anderen Namen in der Funktion erreicht werden.

Ein Verweis Zeiger kann nicht als Typ eines Zeigers verwendet werden, der von einer Funktion zurückgegeben wird.

Wenn für einen Zeiger Parameter der obersten Ebene kein Attribut angegeben ist, wird es als Verweis Zeiger behandelt.

## <a name="examples"></a>Beispiele

``` syntax
[unique] char * GetFirstName( 
    [in, ref] char * pszFullName);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Mikro**](arrays-1.md)
</dt> <dt>

[Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md)
</dt> <dt>

[Mittel l-Basis Typen](midl-base-types.md)
</dt> <dt>

[**Rückruf**](callback.md)
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

[**vorgenommen**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**Größe \_ :**](size-is.md)
</dt> <dt>

[**Zeichenfolge**](string.md)
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
</dt> </dl>

 

 