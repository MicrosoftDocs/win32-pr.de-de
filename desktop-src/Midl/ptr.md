---
title: ptr-Attribut
description: Das Attribut \ptr\ bezeichnet einen Zeiger als vollständigen Zeiger.
ms.assetid: a1233a25-b651-4a01-8abf-a64dc9ee168e
keywords:
- ptr-Attribut MIDL
topic_type:
- apiref
api_name:
- ptr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53e9b85be5e9073a272dafd63a2a01ba64f440f90cc5d9c41f44260f235f9ab5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927420"
---
# <a name="ptr-attribute"></a>ptr-Attribut

Das **\[ ptr-Attribut \]** bestimmt einen Zeiger als vollständigen Zeiger.

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

*type-attribute-list* 
</dt> <dd>

Gibt ein oder mehrere Attribute an, die für den Typ gelten. Gültige Typattribute sind handle , switch type , transmit as , das **\[** [](handle.md) **\]** **\[** [**\_**](switch-type.md) **\]** **\[** [**\_**](transmit-as.md) **\]** Zeigerattribut **\[** [**ref,**](ref.md) **\]** unique oder **\[** [](unique.md) **\[ ptr \]** sowie **\[** [**\_**](context-handle.md) **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** das Kontexthand handle für die Verwendungsattribute , string und ignore . Trennen Sie mehrere Attribute durch Kommas.

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

Gibt null oder mehr Feldattribute an, die für den Struktur- oder Union-Member oder Funktionsparameter gelten. Zu den gültigen Feldattributen zählen zuerst ist , last ist , length ist , max ist , size ist ; die Verwendungsattribute string , ignore und context **\[** [**\_**](first-is.md)handle; das **\]** **\[** [**\_**](last-is.md) **\]** **\[** [**\_**](length-is.md) **\]** **\[** [**\_**](max-is.md) **\]** **\[** [**\_**](size-is.md) **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** **\[** [**\_**](context-handle.md) **\]** Zeigerattribut **\[** [**ref,**](ref.md) **\]** **\[** [**unique**](unique.md) **\]** oder **\[ ptr \]** und der Union-Attributschaltertyp **\[** [**\_**](switch-type.md) **\]** . Trennen Sie mehrere Feldattribute durch Kommas.

</dd> <dt>

*function-attribute-list* 
</dt> <dd>

Gibt null oder mehr Attribute an, die für die Funktion gelten. Gültige Funktionsattribute sind rückruf , local, das **\[** [](callback.md) **\]** **\[** [](local.md) **\]** Zeigerattribut **\[** [**ref,**](ref.md) **\]** unique oder **\[** [](unique.md) **\]** **\[ \] ptr** und die Verwendungsattribute **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** **\[** [**\_**](context-handle.md) **\]** Zeichenfolge , ignorieren und Kontexthand handle .

</dd> <dt>

*ptr-decl* 
</dt> <dd>

Gibt mindestens einen Zeigerdeklarator an, auf den das **\[ ptr-Attribut \]** angewendet wird. Ein Zeigerdeklarator ist mit dem in C verwendeten Zeigerdeklarator identisch. sie wird aus dem \* Designator, Modifizierern wie **far** und dem Qualifizierer [**const erstellt.**](const.md)

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Gibt den Namen der Remoteprozedur an.

</dd> <dt>

*parameter-attribute-list* 
</dt> <dd>

Besteht aus 0 (null) oder mehr Attributen, die für den angegebenen Parametertyp geeignet sind. Parameterattribute können die direktionalen Attribute [**in und aus**](in.md) [**übernehmen.**](out-idl.md) Die [**Feldattribute \_**](first-is.md)sind zuerst , die letzte ist [**, \_**](last-is.md)die Länge ist [**, \_**](length-is.md) [**max \_ ist**](max-is.md), die Größe ist , und der Switchtyp [**, \_**](switch-type.md)das Zeigerattribut [**ref,**](ref.md) [**unique**](unique.md)oder **\[ ptr \]** und das Kontexthand handle und die Zeichenfolge der [**Verwendungsattribute \_**](context-handle.md) [**.**](string.md) [**\_**](size-is.md) Das ignorierte [**Verwendungsattribut**](ignore.md) kann nicht als Parameterattribut verwendet werden. Trennen Sie mehrere Attribute durch Kommas.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der vollständige Zeiger, der vom **\[ \] ptr-Attribut** angegeben wird, nähert sich der vollständigen Funktionalität des C-Sprachzeigers. Der vollständige Zeiger kann den Wert **NULL haben** und sich während des Aufrufs von **NULL** in Nicht-NULL **ändern.** Storage, auf die durch vollständige Zeiger verwiesen wird, können durch andere Namen in der Anwendung erreicht werden, die Aliasing und Zyklen unterstützen. Diese Funktion erfordert mehr Aufwand während eines Remoteprozeduraufrufs, um die Daten zu identifizieren, auf die der Zeiger verwiesen wird, um zu bestimmen, ob der Wert **NULL** ist, und um zu ermitteln, ob zwei Zeiger auf dieselben Daten zeigen.

Verwenden Sie vollständige Zeiger für:

-   Remote-Rückgabewerte.
-   Doppelte Zeiger, wenn die Größe eines Ausgabeparameters nicht bekannt ist.
-   **NULL-Zeiger.**

Vollständige (und eindeutige) Zeiger können nicht verwendet werden, um die Größe eines Arrays oder einer Union zu beschreiben, da diese Zeiger den Wert **NULL haben können.** Diese Einschränkung durch MIDL verhindert einen  Fehler, der bei Verwendung eines NULL-Werts als Größe entstehen kann.

Es wird davon ausgegangen, dass Verweis- und eindeutige Zeiger kein Aliasing von Daten verursachen. Ein gerichtetes Diagramm, das von einem eindeutigen - oder Verweiszeiger aus ermittelt wird und nur eindeutigen - oder Verweiszeigern folgt, enthält weder Reconvergence noch Zyklen.

Um Aliasing zu vermeiden, sollten alle Zeigerwerte von einem Eingabezeiger derselben Zeigerklasse erhalten werden. Wenn mehr als ein Zeiger auf denselben Speicherort zeigt, müssen alle diese Zeiger vollständige Zeiger sein.

In einigen Fällen können vollständige und eindeutige Zeiger gemischt werden. Einem vollständigen Zeiger kann der Wert eines eindeutigen Zeigers zugewiesen werden, solange die Zuweisung nicht gegen die Einschränkungen zum Ändern des Werts eines eindeutigen Zeigers verstößt. Wenn Sie jedoch einem eindeutigen Zeiger den Wert eines vollständigen Zeigers zuweisen, können Sie aliasing verursachen.

Das Kombinieren von vollständigen und eindeutigen Zeigern kann aliasing verursachen, wie im folgenden Beispiel gezeigt:

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

Obwohl "t->left" und "t->right" auf eindeutige Speicherorte zeigen, werden "t->left->pdata" und "t->right->pdata" als Alias verwendet. Aus diesem Grund müssen Aliasing-Unterstützungsalgorithmen allen Zeigern (einschließlich eindeutiger und Referenzzeiger) folgen, die letztendlich einen vollständigen Zeiger erreichen können.

## <a name="examples"></a>Beispiele

``` syntax
pointer_default(ptr) 
 
typedef [ptr, string] unsigned char * MY_STRING_TYPE; 
 
[ptr] char * MyFunction([in, out, unique] long * plNumber);
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

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
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

[**Zeiger \_ standard**](pointer-default.md)
</dt> <dt>

[**ref**](ref.md)
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

 

 