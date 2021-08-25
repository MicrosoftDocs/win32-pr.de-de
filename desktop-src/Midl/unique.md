---
title: Eindeutiges Attribut
description: Das \unique\-Attribut gibt einen eindeutigen Zeiger an.
ms.assetid: 0d668148-e65a-478f-9e47-2528d3caa84c
keywords:
- Eindeutiges Midl-Attribut
topic_type:
- apiref
api_name:
- unique
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57c176c9a246329b6193c97ca5ce356c2b433cb421b77b374e103778df1b79dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822030"
---
# <a name="unique-attribute"></a>Eindeutiges Attribut

Das **\[ eindeutige \]** Attribut gibt einen eindeutigen Zeiger an.

``` syntax
pointer_default(unique)

typedef [ unique [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef struct-or-union-declarator 
{
    [ unique [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...}

[ unique [[ , function-attribute-list ]] ] type-specifier ptr-decl function-name(
    [[ [ parameter-attribute-list ] ]] type-specifier [[declarator]]
    , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ unique [[ , parameter-attribute-list ]] ] type-specifier [[declarator]]
    , ...);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*type-attribute-list* 
</dt> <dd>

Gibt ein oder mehrere Attribute an, die für den Typ gelten. Gültige Typattribute sind **\[** [**handle**](handle.md) **\]** , switch **\[** [**\_ type**](switch-type.md) **\]** , transmit **\[** [**\_ as**](transmit-as.md) **\]** ; das Zeigerattribut **\[** [**ref**](ref.md) **\]** , **\[ unique \]** oder **\[** [**ptr**](ptr.md); und das **\]** **\[** [**\_ Kontexthandle**](context-handle.md)der Verwendungsattribute **\]** , **\[** [**Zeichenfolge**](string.md) **\]** und **\[** [**ignorieren**](ignore.md) **\]** . Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*Typspezifizierer* 
</dt> <dd>

Gibt einen [Basistyp,](midl-base-types.md) [**eine Struktur,**](struct.md) [**einen Union-,**](union.md) [**Enumerations-**](enum.md) oder Typbezeichner an. Eine optionale Speicherspezifikation kann dem *Typspezifizierer* vorangestellt werden.

</dd> <dt>

*deklarator und declarator-list* 
</dt> <dd>

Gibt C-Standarddeklaratoren an, z. B. Bezeichner, Zeigerdeklaratoren und Arraydeklaratoren. Weitere Informationen finden Sie unter [Array- und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**Arrays**](arrays-1.md). und [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers). Die *Deklaratorliste* besteht aus einem oder mehreren Deklaratoren, die durch Kommas getrennt sind. Der Parameternamenbezeichner im Funktionsdeklarator ist optional.

</dd> <dt>

*struct-or-union-declarator* 
</dt> <dd>

Gibt eine [**MIDL-Struktur**](struct.md) oder einen Union-Deklarator an. [](union.md)

</dd> <dt>

*field-attribute-list* 
</dt> <dd>

Gibt null oder mehr Feldattribute an, die für den Strukturmember, union-Member oder Funktionsparameter gelten. Gültige Feldattribute **\[** [**sind: zuerst \_ ist**](first-is.md) **\]** , der letzte **\[** [**\_ ist**](last-is.md) **\]** , die Länge **\[** [**\_ ist**](length-is.md) **\]** , max **\[** [**\_ ist**](max-is.md) **\]** , die Größe **\[** [**\_ ist**](size-is.md) **\]** ; die Verwendungsattribute **\[ Zeichenfolge \]**, **\[ ignorieren \]** und **\[ \_ \] Kontexthandle;** das Zeigerattribut **\[ ref \]**, **\[ eindeutig \]** oder **\[ ptr \]**; und der **\[ Union-Attributwechseltyp \_ \]**. Trennen Sie mehrere Feldattribute durch Kommas.

</dd> <dt>

*function-attribute-list* 
</dt> <dd>

Gibt null oder mehr Attribute an, die für die Funktion gelten. Gültige Funktionsattribute sind **\[** [**rückruf,**](callback.md) **\]** **\[** [**local,**](local.md) **\]** das Zeigerattribut **\[ ref, \]** **\[ eindeutig \]** oder **\[ ptr \]** und die Verwendungsattribute **\[ Zeichenfolge \]**, **\[ ignorieren \]** und **\[ \_ Kontexthandle \]**.

</dd> <dt>

*ptr-decl* 
</dt> <dd>

Gibt mindestens einen Zeigerdeklarator an, für den das **\[ eindeutige \]** Attribut gilt. Ein Zeigerdeklarator entspricht dem in C verwendeten Zeigerdeklarator. sie wird aus dem \* Bezeichner, Modifizierern wie **far** und dem Qualifizierer [**const**](const.md)erstellt.

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Gibt den Namen der Remoteprozedur an.

</dd> <dt>

*parameter-attribute-list* 
</dt> <dd>

Besteht aus null oder mehr Attributen, die für den angegebenen Parametertyp geeignet sind. Parameterattribute können die direktionalen Attribute **\[ in \]** und **\[ out \]** aufnehmen. Die Feldattribute **\[ sind zuerst \_ \]**, **\[ die letzte \_ ist \]**, die Länge ist , **\[ max \_ \]** **\[ \_ \] ist**, die Größe **\[ \_ \] ist**, und der **\[ \_ Schaltertyp; \]** das Zeigerattribut **\[ ref \]**, **eindeutig** oder [**ptr;**](ptr.md)und das **\[ \_ Kontexthandle \]** der Verwendungsattribute und die **\[ Zeichenfolge \]**. Das Verwendungsattribut **\[ ignore \]** kann nicht als Parameterattribut verwendet werden. Trennen Sie mehrere Attribute durch Kommas.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Zeigerattribute können als Typattribut angewendet werden. als Feldattribut, das für einen Strukturmember, union-Member oder Parameter gilt; oder als Funktionsattribut, das für den Funktionsrückgabetyp gilt. Das Zeigerattribut kann auch mit dem **\[** [**\_ Zeigerstandardschlüsselwort**](pointer-default.md) angezeigt **\]** werden.

Ein eindeutiger Zeiger weist die folgenden Merkmale auf:

-   Kann den Wert **NULL** aufweisen.
-   Kann während eines Aufrufs von **NULL** in nicht **NULL,** von nicht **NULL** in **NULL** oder von einem Wert ungleich **NULL** in einen anderen geändert werden.
-   Kann neuen Arbeitsspeicher auf dem Client zuordnen. Wenn der eindeutige Zeiger von **NULL** in nicht **NULL** geändert wird, werden die vom Server zurückgegebenen Daten in den neuen Speicher geschrieben.
-   Kann vorhandenen Arbeitsspeicher auf dem Client verwenden, ohne neuen Arbeitsspeicher zu belegen. Wenn sich ein eindeutiger Zeiger während eines Aufrufs von einem Wert ungleich **NULL** in einen anderen ändert, wird davon ausgegangen, dass der Zeiger auf ein Datenobjekt desselben Typs zeigt. Vom Server zurückgegebene Daten werden in vorhandenen Speicher geschrieben, der durch den Wert des eindeutigen Zeigers vor dem Aufruf angegeben wird.
-   Kann den Arbeitsspeicher auf dem Client verwaist. Arbeitsspeicher, auf den von einem eindeutigen Zeiger ungleich **NULL** verwiesen wird, wird möglicherweise nie freigegeben, wenn der eindeutige Zeiger während eines Aufrufs in **NULL** geändert wird und der Client keine andere Möglichkeit zum Dereferenzieren des Speichers hat.
-   Verursacht kein Aliasing. Wie der Speicher, auf den ein Verweiszeiger zeigt, kann der Speicher, auf den ein eindeutiger Zeiger zeigt, nicht von einem anderen Namen in der Funktion aus erreicht werden.

Die Stubs rufen die vom Benutzer bereitgestellten Speicherverwaltungsfunktionen [**midl \_ user \_ allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function) und [**midl \_ user \_ free**](/windows/desktop/Rpc/the-midl-user-free-function) auf, um Denk- und Zuordnungsspeicher frei zuzuweisen, der für eindeutige Zeiger und deren Verweise erforderlich ist.

Die folgenden Einschränkungen gelten für eindeutige Zeiger:

-   Das **\[ eindeutige \]** Attribut kann nicht auf Bindungshandleparameter ( [**handle \_ t**](handle-t.md)) und Kontexthandleparameter angewendet werden.
-   Das **\[ eindeutige \]** Attribut kann nicht auf **\[** [](out-idl.md) **\]** out-only-Zeigerparameter der obersten Ebene angewendet werden (Parameter, die nur über das **\[ \] richtungsorientierte** Out-Attribut verfügen).
-   Standardmäßig sind Zeiger der obersten Ebene in Parameterlisten **\[** [](ref.md) **\]** Verweiszeiger. Dies gilt auch dann, wenn die Schnittstelle den **Zeiger \_ default(unique)** angibt. Parameter der obersten Ebene in Parameterlisten müssen mit dem **\[ \] unique-Attribut** angegeben werden, um ein eindeutiger Zeiger zu sein.
-   Eindeutige Zeiger können nicht verwendet werden, um die Größe eines Arrays oder Union-Arm zu beschreiben, da eindeutige Zeiger den Wert **NULL** aufweisen können. Diese Einschränkung verhindert den Fehler, der auftritt, wenn ein **NULL-Wert** als Arraygröße oder Union-Arm-Größe verwendet wird.

## <a name="examples"></a>Beispiele

``` syntax
pointer_default(unique) 
 
typedef [unique, string] unsigned char * MY_STRING_TYPE; 
 
[unique] char * MyFunction([in, out, unique] long * plNumber);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Arrays**](arrays-1.md)
</dt> <dt>

[Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Array- und Sized-Pointer attribute](array-and-sized-pointer-attributes.md)
</dt> <dt>

[MIDL-Basistypen](midl-base-types.md)
</dt> <dt>

[**Rückruf**](callback.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**\_Kontexthandle**](context-handle.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[**\_first ist**](first-is.md)
</dt> <dt>

[**Handlebezeichner**](handle.md)
</dt> <dt>

[**handle \_ t**](handle-t.md)
</dt> <dt>

[**Ignorieren**](ignore.md)
</dt> <dt>

[**last \_ ist**](last-is.md)
</dt> <dt>

[**length \_ ist**](length-is.md)
</dt> <dt>

[**lokal**](local.md)
</dt> <dt>

[**max \_ ist**](max-is.md)
</dt> <dt>

[midl \_ user \_ allocate](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[midl \_ user \_ free](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**\_Zeigerstandard**](pointer-default.md)
</dt> <dt>

[**Ptr**](ptr.md)
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
</dt> </dl>

 

 