---
title: out-Attribut
description: Das Attribut \ out \ identifiziert Zeiger Parameter, die von der aufgerufenen Prozedur an die aufrufenden Prozeduren zurückgegeben werden (vom Server an den Client).
ms.assetid: f92ef78a-321b-460e-a18a-b63a5e199ad0
keywords:
- Out-Attribut, Mittel l
topic_type:
- apiref
api_name:
- out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b590cadeb12a77cff859991efb6356393072823
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340903"
---
# <a name="out-attribute"></a>out-Attribut

Das \[ **out** - \] Attribut identifiziert Zeiger Parameter, die von der aufgerufenen Prozedur an die aufrufenden Prozeduren zurückgegeben werden (vom Server an den Client).

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ out [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Function-Attribute-List* 
</dt> <dd>

Gibt 0 (null) oder mehr Attribute an, die für die Funktion gelten. Gültige Funktions Attribute sind \[ [**Callback**](callback.md) \] , \[ [**local**](local.md), \] das Zeiger Attribut \[ [**ref**](ref.md) \] , \[ [**Unique**](unique.md) \] oder \[ [**ptr**](ptr.md) \] und die Zeichenfolge der Verwendungs Attribute \[ [**Zeichenfolge**](string.md) \] , \[ [**ignorieren**](ignore.md) \] und \[ [**Kontext \_ handle**](context-handle.md) \] .

</dd> <dt>

*Typspezifizierer* 
</dt> <dd>

Gibt einen [ \_ Basistyp](midl-base-types.md), eine [**Struktur**](struct.md), eine [**Union**](union.md)oder einen Aufzählungstyp [**oder einen**](enum.md) Typbezeichner an. Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden.

</dd> <dt>

*Zeiger-Deklarator* 
</dt> <dd>

Gibt 0 (null) oder mehr Zeiger Deklaratoren an. Ein zeigerdeklarator ist derselbe wie der in C verwendete zeigerdeklarator. Sie wird aus dem Kenn \* Zeichner, den Modifizierern, z. b. **weit**, und dem Qualifizierer " [**Konstanten**](const.md)" erstellt.

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Remote Prozedur an.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

Gibt NULL oder mehr Attribute an, die für einen angegebenen Parametertyp geeignet sind. Parameter Attribute mit dem \[ **out** - \] Attribut können auch das direktionale Attribut annehmen \[  \] . die Feld Attribute \[ [**\_ sind zuerst**](first-is.md) \] , " \[ [**Last \_**](last-is.md)" \] , " \[ [**length \_**](length-is.md)" \] , " \[ [**Max \_ is**](max-is.md)" \] , "size" und " \[ [**\_**](size-is.md) \] \[ [**Switch \_ Type**](switch-type.md)", \] das Zeiger Attribut " \[ [**ref**](ref.md)" \] , " \[ [**Unique**](unique.md)" \] oder " \[ [**ptr**](ptr.md)" \] und das \[ [**Kontext \_ handle**](context-handle.md) \] und die \[ [**Zeichenfolge**](string.md) \] der Verwendungs Attribute Das Usage-Attribut " \[ [**Ignore**](ignore.md) " \] kann nicht als Parameter Attribut verwendet werden. Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*Deklarator* 
</dt> <dd>

Gibt die Standard Deklaratoren an, z. b. Bezeichner, Zeiger Deklaratoren und Array Deklaratoren. Weitere Informationen finden Sie unter [Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**Arrays**](arrays-1.md)und [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers). Der parameterdeklarator im funktionsdedeclarator (z. b. der Parameter Name) ist optional.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das \[ **out** \] -Attribut gibt an, dass ein Parameter, der als Zeiger und die zugehörigen Daten im Arbeitsspeicher fungiert, von der aufgerufenen Prozedur an die aufrufende Prozedur zurückgegeben werden soll.

Das \[ **out** - \] Attribut muss ein Zeiger sein. DCE-IDL-Compiler erfordern das vorhanden sein eines expliziten \* als zeigerdeklarator in der Parameter Deklaration. Microsoft IDL bietet eine Erweiterung, die diese Anforderung löscht und ein Array oder einen zuvor definierten Zeigertyp zulässt.

Ein verknüpftes Attribut \[ [**in**](in.md) \] gibt an, dass der Parameter von der aufrufenden Prozedur an die aufgerufene Prozedur übergeben wird. Die \[ **in** \] -und \[ **out** - \] Attribute geben die Richtung an, in der die Parameter übermittelt werden. Ein Parameter kann nur als " \[ nur **in** \] -only", " \[ **out**" \] oder " \[ **in**  \] ", "out" definiert werden.

\[  \] Es wird davon ausgegangen, dass ein out-only-Parameter nicht definiert ist, wenn die Remote Prozedur aufgerufen wird und der Speicher für das Objekt vom Server zugeordnet wird. Da Zeiger/Parameter der obersten Ebene immer auf einen gültigen Speicher zeigen und daher nicht **null** sein dürfen, \[ kann **out** \] nicht auf \[ [**eindeutige**](unique.md) \] oder \[ [**ptr**](ptr.md) - \] Zeiger der obersten Ebene angewendet werden. Parameter, die \[ **eindeutig** \] sind \[ , oder **ptr** - \] Zeiger müssen entweder \[ [**in**](in.md) - \] oder \[ **in**-, **out** - \] Parameter sein.

## <a name="examples"></a>Beispiele

``` syntax
HRESULT MyFunction([out] short * pcount);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Mikro**](arrays-1.md)
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

[**lassen**](ignore.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[**Letzter \_ ist**](last-is.md)
</dt> <dt>

[**Länge \_ ist**](length-is.md)
</dt> <dt>

[**nah**](local.md)
</dt> <dt>

[**Max \_ ist**](max-is.md)
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

[**Union**](union.md)
</dt> <dt>

[**gem**](unique.md)
</dt> </dl>

 

 