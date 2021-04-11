---
title: ptr-Attribut
description: Das Attribut \ PTR \ legt einen Zeiger als vollständigen Zeiger fest.
ms.assetid: a1233a25-b651-4a01-8abf-a64dc9ee168e
keywords:
- PTR-Attribut-Mittel l
topic_type:
- apiref
api_name:
- ptr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2d8b2ee2e3ea4daccd1c4fa37ff1c1f1899dd3c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314799"
---
# <a name="ptr-attribute"></a>ptr-Attribut

Das **\[ ptr \]** -Attribut legt einen Zeiger als vollständigen Zeiger fest.

``` syntax
pointer_default(ptr)

typedef [ ptr [ , type-attribute-list ] ] type-specifier declarator-list; 

typedef [ struct | union ]
{
    [ ptr [ , field-attribute-list ] ] type-specifier declarator-list;
    ...
}

[ ptr [ , function-attribute-list ] ] type-specifier ptr-decl function-name(
    [ [ parameter-attribute-list ] ] type-specifier [standard-declarator]
    , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ ptr [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
    , ...);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Type-Attribute-List* 
</dt> <dd>

Gibt ein oder mehrere Attribute an, die auf den Typ angewendet werden. Gültige Typattribute sind **\[** [**handle**](handle.md) **\]** , **\[** [**\_ Switchtyp**](switch-type.md) **\]** , über **\[** [**Tragung \_ als**](transmit-as.md) **\]** ; Zeiger Attribut Verweis **\[** [](ref.md) **\]** , **\[** [**eindeutig**](unique.md)oder **\[ ptr \]**; und die Verwendungs Attribute **\[** [**Kontext \_ handle**](context-handle.md) **\]** , **\[** [**String**](string.md) **\]** und **\[** [**Ignore**](ignore.md) **\]** . Trennen Sie mehrere Attribute durch Kommas.

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

Gibt 0 (null) oder mehr Feld Attribute an, die für den Struktur-oder Union-Member oder Funktionsparameter gelten. Gültige Feld Attribute sind **\[** [**First \_ is**](first-is.md) **\]** , **\[** [**Last \_ is**](last-is.md) **\]** , **\[** [**length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ is**](size-is.md), **\]** die Usage-Attribute **\[** [**String**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** und **\[** [**context \_ handle**](context-handle.md), **\]** das Zeiger Attribut **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** oder **\[ \] ptr** und der Typ des Union-Attribut **\[** [**Schalters \_**](switch-type.md) **\]** . Trennen Sie mehrere Feld Attribute durch Kommas.

</dd> <dt>

*Function-Attribute-List* 
</dt> <dd>

Gibt 0 (null) oder mehr Attribute an, die für die Funktion gelten. Gültige Funktions Attribute sind **\[** [**Callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** das Zeiger Attribut **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** oder **\[ \] ptr** und die Zeichenfolge der Verwendungs Attribute **\[** [**Zeichenfolge**](string.md) **\]** , **\[** [**ignorieren**](ignore.md) **\]** und **\[** [**Kontext \_ handle**](context-handle.md) **\]** .

</dd> <dt>

*PTR-decl* 
</dt> <dd>

Gibt mindestens einen zeigerdeklarator an, auf den das **\[ ptr \]** -Attribut angewendet wird. Ein zeigerdeklarator ist derselbe wie der in C verwendete zeigerdeklarator. Sie wird aus dem Kenn \* Zeichner, den Modifizierern, z. b. **weit**, und dem Qualifizierer " [**Konstanten**](const.md)" erstellt.

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Remote Prozedur an.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

Besteht aus null oder mehr Attributen, die für den angegebenen Parametertyp geeignet sind. Parameter Attribute können die direktionalen Attribute [**ein-und**](in.md) [**Auslagern**](out-idl.md). die Feld Attribute [**\_ sind zuerst**](first-is.md), "Last", "length", " [**Max \_ is**](max-is.md)" [**\_**](last-is.md), "size" und " [**Switch \_ Type**](switch-type.md)", "Pointer Attribute [**ref**](ref.md)", " [**Unique**](unique.md)" oder " **\[ ptr \]**" und das [**Kontext \_ handle**](context-handle.md) und die [**Zeichenfolge**](string.md)der Verwendungs Attribute. [**\_**](length-is.md) [**\_**](size-is.md) Das Usage-Attribut " [**Ignore**](ignore.md) " kann nicht als Parameter Attribut verwendet werden. Trennen Sie mehrere Attribute durch Kommas.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der durch das **\[ ptr \]** -Attribut festgelegte vollständige Zeiger nähert sich der vollständigen Funktionalität des C-sprach Zeigers. Der vollständige Zeiger kann den Wert **null** aufweisen und sich während des Aufrufes von **null** in einen nicht-**null**-Wert ändern. Speicher, auf den von vollständigen Zeigern verwiesen wird, kann von anderen Namen in der Anwendung erreicht werden, die Aliasing und Zyklen unterstützen Diese Funktionalität erfordert während eines Remote Prozedur Aufrufes mehr Aufwand, um die Daten zu identifizieren, auf die der Zeiger verweist, um zu bestimmen, ob der Wert **null** ist, und um zu ermitteln, ob zwei Zeiger auf dieselben Daten zeigen.

Vollständige Zeiger verwenden für:

-   Remote Rückgabewerte.
-   Doppelte Zeiger, wenn die Größe eines Ausgabe Parameters nicht bekannt ist.
-   **Null** -Zeiger.

Vollständige (und eindeutige) Zeiger können nicht verwendet werden, um die Größe eines Arrays oder einer Union zu beschreiben, da diese Zeiger den Wert **null** haben können. Diese Einschränkung durch das Mittel l verhindert einen Fehler, der auftreten kann, wenn ein **null** -Wert als Größe verwendet wird.

Bei Verweis-und eindeutigen Zeigern wird davon ausgegangen, dass keine Daten gelöscht werden. Ein gerichtetes Diagramm, das durch das Starten eines eindeutigen oder Verweis Zeigers abgerufen wird und nur eindeutige Verweise oder Verweis Zeiger enthält, enthält weder eine erneute Konvergenz noch Zyklen.

Um Aliasing zu vermeiden, sollten alle Zeiger Werte von einem Eingabe Zeiger der gleichen Klasse des Zeigers abgerufen werden. Wenn mehr als ein Zeiger auf denselben Speicherort verweist, müssen alle Zeiger vollständig Zeiger sein.

In einigen Fällen können vollständige und eindeutige Zeiger gemischt werden. Einem vollständigen Zeiger kann der Wert eines eindeutigen Zeigers zugewiesen werden, solange die Zuweisung nicht gegen die Einschränkungen bei der Änderung des Werts eines eindeutigen Zeigers verstößt. Wenn Sie jedoch einen eindeutigen Zeiger auf den Wert eines vollständigen Zeigers zuweisen, können Sie Aliasing auslösen.

Das Kombinieren von vollständigen und eindeutigen Zeigern kann Aliasing verursachen, wie im folgenden Beispiel gezeigt:

``` syntax
typedef struct 
{ 
    [ptr] short * pdata;          // full pointer  
} GRAPH_NODE_TYPE; 
 
typedef struct 
{ 
    [unique] graph_node * left;   // unique pointer  
    [unique] graph_node * right;  // unique pointer 
} TREE_NODE_TYPE; 
 
// application code: 
short a = 5; 
TREE_NODE_TYPE * t; 
GRAPH_NODE_TYPE g, h; 
 
g.pdata = h.pdata = &a; 
t->left = &g; 
t->right = &h; 
// t->left->pdata == t->right->pdata == &a
```

Obwohl "t->Left" und "t->right" auf eindeutige Speicherorte verweisen, sind "t->Left->pData" und "t->right->pData" ein Alias. Aus diesem Grund müssen Aliasing-Unterstützungs Algorithmen allen Zeigern folgen (einschließlich eindeutiger Verweis Zeiger und Verweis Zeiger), die schließlich möglicherweise einen vollständigen Zeiger erreichen.

## <a name="examples"></a>Beispiele

``` syntax
pointer_default(ptr) 
 
typedef [ptr, string] unsigned char * MY_STRING_TYPE; 
 
[ptr] char * MyFunction([in, out, unique] long * plNumber);
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

[**ref**](ref.md)
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

 

 