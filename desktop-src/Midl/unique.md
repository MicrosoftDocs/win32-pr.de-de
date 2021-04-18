---
title: Eindeutiges Attribut
description: Das Attribut \ Unique \ gibt einen eindeutigen Zeiger an.
ms.assetid: 0d668148-e65a-478f-9e47-2528d3caa84c
keywords:
- Unique-attributmittell
topic_type:
- apiref
api_name:
- unique
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95b839a2abdd546842ef0d33d45a31428af840f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106338453"
---
# <a name="unique-attribute"></a>Eindeutiges Attribut

Das **\[ Unique \]** -Attribut gibt einen eindeutigen Zeiger an.

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

*Type-Attribute-List* 
</dt> <dd>

Gibt ein oder mehrere Attribute an, die auf den Typ angewendet werden. Gültige Typattribute sind **\[** [**handle**](handle.md) **\]** , **\[** [**\_ Switchtyp**](switch-type.md) **\]** , über **\[** [**Tragung \_ als**](transmit-as.md) **\]** ; Zeiger Attribut Verweis **\[** [](ref.md) **\]** , **\[ eindeutig \]** oder **\[** [**ptr**](ptr.md) **\]** ; und die Verwendungs Attribute **\[** [**Kontext \_ handle**](context-handle.md) **\]** , **\[** [**String**](string.md) **\]** und **\[** [**Ignore**](ignore.md) **\]** . Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*Typspezifizierer* 
</dt> <dd>

Gibt einen [Basistyp](midl-base-types.md), eine [**Struktur**](struct.md), eine [**Union**](union.md), einen [**Enumeration**](enum.md) -Typ oder einen Typbezeichner an. Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden.

</dd> <dt>

*Deklarator und Deklarator-List* 
</dt> <dd>

Gibt Standard-C-Deklaratoren an, z. b. Bezeichner, Zeiger Deklaratoren und Array Deklaratoren. Weitere Informationen finden Sie unter [Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**Arrays**](arrays-1.md)und [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers). Die *declarator-List* besteht aus einem oder mehreren Deklaratoren, die durch Kommas getrennt sind. Der Parameter-Name-Bezeichner im funktionsdedeclarator ist optional.

</dd> <dt>

*struct-or-Union-declarator* 
</dt> <dd>

Gibt eine mittlerer l- [**Struktur**](struct.md) oder einen [**Union**](union.md) -Deklarator an.

</dd> <dt>

*Field-Attribute-List* 
</dt> <dd>

Gibt 0 (null) oder mehr Feld Attribute an, die für den Strukturmember, den Union-Member oder den Funktionsparameter gelten. Gültige Feld Attribute sind **\[** [**First \_ is**](first-is.md) **\]** , **\[** [**Last \_ is**](last-is.md) **\]** , **\[** [**length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ is**](size-is.md), **\]** die Usage-Attribute **\[ \] String**, **\[ Ignore \]** und **\[ context \_ handle \]**, das Zeiger Attribut **\[ ref \]**, **\[ Unique \]** oder **\[ ptr \]** und der Typ **\[ \_ \]** des Union-Attribut Schalters. Trennen Sie mehrere Feld Attribute durch Kommas.

</dd> <dt>

*Function-Attribute-List* 
</dt> <dd>

Gibt 0 (null) oder mehr Attribute an, die für die Funktion gelten. Gültige Funktions Attribute sind **\[** [**Callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** das Zeiger Attribut **\[ ref \]**, **\[ Unique \]** oder **\[ \] ptr** und die Zeichenfolge der Verwendungs Attribute **\[ Zeichenfolge \]**, **\[ ignorieren \]** und **\[ Kontext \_ handle \]**.

</dd> <dt>

*PTR-decl* 
</dt> <dd>

Gibt mindestens einen zeigerdeklarator an, für den das **\[ eindeutige \]** Attribut gilt. Ein zeigerdeklarator ist derselbe wie der in C verwendete zeigerdeklarator. Sie wird aus dem Kenn \* Zeichner, den Modifizierern, z. b. **weit**, und dem Qualifizierer " [**Konstanten**](const.md)" erstellt.

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Remote Prozedur an.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

Besteht aus null oder mehr Attributen, die für den angegebenen Parametertyp geeignet sind. Parameter Attribute können die direktionalen Attribute **\[ \] ein-und** **\[ \] ausschalten. die** **\[ \] Feld Attribute** **\[ \_ sind \] zuerst**  **\[ \_ \]** **\[ \_ , " \]** Last", "length", " **\[ Max \_ \] is**", " **\[ size" und " \_ Switch Type", das Zeiger Attribut "ref", "Unique" oder "PTR" und das Kontext Handle und die Zeichenfolge der Verwendungs Attribute \]** **\[ \_ \]** **\[ \_ \]** **\[ \]** [](ptr.md) Das Usage-Attribut " **\[ Ignore \]** " kann nicht als Parameter Attribut verwendet werden. Trennen Sie mehrere Attribute durch Kommas.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Zeiger Attribute können als Type-Attribut angewendet werden. als Feld Attribut, das für einen Strukturmember, ein Union-Member oder einen-Parameter gilt. oder als Funktions Attribut, das für den Funktions Rückgabetyp gilt. Das Zeiger Attribut kann auch mit dem **\[** [**Zeiger \_ default**](pointer-default.md) - **\]** Schlüsselwort angezeigt werden.

Ein eindeutiger Zeiger weist die folgenden Eigenschaften auf:

-   Der Wert kann **null** sein.
-   Kann während eines Aufrufes von **null** in einen nicht-**null**-Wert, von einem nicht-**null** -Wert in **null** oder von einem nicht-**null** -Wert zu einem anderen ändern.
-   Auf dem Client kann neuer Arbeitsspeicher belegt werden. Wenn der eindeutige Zeiger von **null** in einen nicht-**null**-Wert geändert wird, werden die vom Server zurückgegebenen Daten in den neuen Speicher geschrieben.
-   Kann vorhandenen Arbeitsspeicher auf dem Client verwenden, ohne neuen Arbeitsspeicher zuzuordnen. Wenn sich ein eindeutiger Zeiger während eines Aufrufes von einem nicht-**null** -Wert in einen anderen ändert, wird davon ausgegangen, dass der Zeiger auf ein Datenobjekt desselben Typs verweist. Die vom Server zurückgegebenen Daten werden in den vorhandenen Speicher geschrieben, der durch den Wert des eindeutigen Zeigers vor dem-Befehl angegeben wird.
-   Der Arbeitsspeicher auf dem Client kann verwaisten. Der Speicher, auf den von einem eindeutigen Zeiger ungleich **null** verwiesen wird, wird möglicherweise nie freigegeben, wenn der eindeutige Zeiger während eines-Aufrufes in **null** ändert und der Client nicht über eine andere Möglichkeit zur Dereferenzierung des Speichers verfügt.
-   Führt nicht zum Aliasing. Wie der Speicher, auf den ein Verweis Zeiger zeigt, kann der Speicher, auf den von einem eindeutigen Zeiger verwiesen wird, nicht von einem anderen Namen in der Funktion erreicht werden.

Mit den stubaten werden die vom Benutzer bereitgestellten Speicherverwaltungsfunktionen " [**mittlere \_ Benutzer \_**](/windows/desktop/Rpc/the-midl-user-allocate-function) Zuordnungen" und " [**mittlere \_ Benutzer" \_ frei**](/windows/desktop/Rpc/the-midl-user-free-function) gegeben, um den für eindeutige Zeiger und deren Verweise erforderlichen Arbeitsspeicher zuzuordnen und deren Freigabe aufzuheben.

Die folgenden Einschränkungen gelten für eindeutige Zeiger:

-   Das **\[ Unique \]** -Attribut kann nicht auf Parameter für Bindungs handle ( [**handle \_ t**](handle-t.md)) und Kontext Handle angewendet werden.
-   Das **\[ Unique \]** -Attribut kann nicht auf **\[** [**out**](out-idl.md) **\]** -only-Zeiger Parameter (Parameter, die nur über das **\[ out \]** -direktionale Attribut verfügen) angewendet werden.
-   Standardmäßig sind Zeiger der obersten Ebene in Parameterlisten **\[** [**ref**](ref.md) - **\]** Zeiger. Dies gilt auch, wenn die Schnittstelle **Zeiger \_ Standard (eindeutig)** angibt. Parameter der obersten Ebene in Parameterlisten müssen mit dem **\[ Unique \]** -Attribut angegeben werden, damit es sich um einen eindeutigen Zeiger handelt.
-   Eindeutige Zeiger können nicht verwendet werden, um die Größe eines Arrays oder eines Union-Arm zu beschreiben, da eindeutige Zeiger den Wert **null** haben können. Diese Einschränkung verhindert den Fehler, der sich ergibt, wenn ein **null** -Wert als Array Größe oder Union-Arm-Größe verwendet wird.

## <a name="examples"></a>Beispiele

``` syntax
pointer_default(unique) 
 
typedef [unique, string] unsigned char * MY_STRING_TYPE; 
 
[unique] char * MyFunction([in, out, unique] long * plNumber);
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

[**Handle \_ t**](handle-t.md)
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

[mittlere Benutzer Zuordnungen \_ \_](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[mittlerer l- \_ Benutzer \_ kostenlos](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[**vorgenommen**](out-idl.md)
</dt> <dt>

[**Zeiger \_ Standard**](pointer-default.md)
</dt> <dt>

[**ptr**](ptr.md)
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
</dt> </dl>

 

 