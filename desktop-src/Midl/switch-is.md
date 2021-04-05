---
title: switch_is-Attribut
description: Der \ Switch \_ is \ Attribute gibt den Ausdruck oder den Bezeichner an, der als uniondiskriminant fungiert, der das Unionmember auswählt.
ms.assetid: 93552bdf-6a14-47ce-877e-32ed976bb895
keywords:
- Switch_is Attribut-Mittel l
topic_type:
- apiref
api_name:
- switch_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c52661c4fa1ebce57011f4424901dd1ec18250f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103948222"
---
# <a name="switch_is-attribute"></a>Switch \_ ist Attribut

Der **\[ Switch \_ is \]** Attribute gibt den Ausdruck oder den Bezeichner an, der als uniondiskriminant fungiert, der das Unionmember auswählt.

``` syntax
typedef struct [[ struct-tag ]] 
{
    [ switch_is(limited-expr) [[ , field-attr-list ]] ] union-type-specifier declarator;
    ...
}

[[ [function-attribute-list] ]] type-specifier [[pointer-declarator]] function-name(
    [ switch_is(limited-expr) [[ , param-attr-list ]] ] union-type [[declarator]]
    , ...);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*struct-Tag* 
</dt> <dd>

Gibt ein optionales Tag für eine Struktur an.

</dd> <dt>

*Limited-expr* 
</dt> <dd>

Gibt einen von der Mittel l unterstützten C-sprach Ausdruck an. Fast alle C-sprach Ausdrücke werden unterstützt. Der mittlerer l-Compiler unterstützt bedingte Ausdrücke, logische Ausdrücke, relationale Ausdrücke und arithmetische Ausdrücke. Die Mittel l lässt keine Funktionsaufrufe in Ausdrücken zu und lässt keine Pre-und Post-Increment-und Pre-und Post-Dekrement-Operatoren zu.

</dd> <dt>

*Field-attr-List* 
</dt> <dd>

Gibt 0 (null) oder mehr Feld Attribute an, die für ein Union-Element gelten. Gültige Feld Attribute sind **\[** [**First \_ is**](first-is.md), **\]** **\[** [**Last \_ is**](last-is.md) **\]** , **\[** [**length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ is**](size-is.md), **\]** die Usage **\[** -Attribut [**Zeichenfolge**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** und **\[** das [**Kontext \_ handle**](context-handle.md), **\]** das Zeiger Attribut **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** oder **\[** [**ptr**](ptr.md) **\]** und für Member, die selbst Unions sind, der **\[** [**\_ Switchtyp**](switch-type.md)des Union-Attributs **\]** . Trennen Sie mehrere Feld Attribute durch Kommas.

</dd> <dt>

*Union-type-specifier* 
</dt> <dd>

Gibt den [**Union**](union.md) -Typbezeichner an. Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden.

</dd> <dt>

*Deklarator und Deklarator-List* 
</dt> <dd>

Gibt einen C-Standard Deklarator an, z. b. einen Bezeichner, einen zeigerdeklarator und einen Arraydeklarator. (Funktions Deklaratoren und Bitfeld Deklarationen sind in Unions nicht zulässig, die in Remote Prozedur aufrufen übertragen werden. Diese Deklaratoren sind in Unions zulässig, die nicht übertragen werden.) Trennen Sie mehrere Deklaratoren durch Kommas.

</dd> <dt>

*Function-Attribute-List* 
</dt> <dd>

Gibt 0 (null) oder mehr Attribute an, die für die Funktion gelten. Gültige Funktions Attribute sind **\[** [**Callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** das Zeiger Attribut **\[ ref \]**, **\[ Unique \]** oder **\[ \] ptr** und die Zeichenfolge der Verwendungs Attribute **\[ Zeichenfolge \]**, **\[ ignorieren \]** und **\[ Kontext \_ handle \]**.

</dd> <dt>

*Typspezifizierer* 
</dt> <dd>

Gibt einen [Basistyp](midl-base-types.md), eine [**Struktur**](struct.md), eine [**Union**](union.md), einen [**Enumeration**](enum.md) -Typ oder einen Typbezeichner an. Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden.

</dd> <dt>

*Zeiger-Deklarator* 
</dt> <dd>

Gibt 0 (null) oder mehr Zeiger Deklaratoren an. Ein zeigerdeklarator ist derselbe wie der in C verwendete zeigerdeklarator. Sie wird aus dem Kenn \* Zeichner, den Modifizierern, z. b. **weit**, und dem Qualifizierer " [**Konstanten**](const.md)" erstellt.

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Remote Prozedur an.

</dd> <dt>

*param-attr-List* 
</dt> <dd>

Gibt NULL oder mehr Attribute an, die für den angegebenen Parametertyp geeignet sind. Parameter Attribute können die direktionalen **\[ Attribute \] ein-und** **\[ \]** **\[ \]** **\[ \_ \]** **\[ \] ausschalten, die** Feld Attribute **\[ \_ \] sind zuerst** **\[ \_ \] , "** Last", "length", " **\[ Max \_ \] is**", " **\[ size" \_ und "Switch Type", das Zeiger Attribut "ref", "Unique" oder "PTR" und das Kontext Handle und die Zeichenfolge der Verwendungs Attribute \]** **\[ \]** **\[ \_ \]** **\[ \_ \]** **\[ \]** Das Usage-Attribut " **\[ Ignore \]** " kann nicht als Parameter Attribut verwendet werden. Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*Union-Type* 
</dt> <dd>

Identifiziert den [**Union**](union.md) -Typspezifizierer.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der dem **\[ Switch \_ \]** zugeordnete diskriminant muss auf derselben logischen Ebene wie die Union definiert werden:

-   Wenn die Union ein Parameter ist, muss der Union-diskriminant ein anderer Parameter sein.
-   Wenn die Union ein Feld einer Struktur ist, muss die Diskriminante ein anderes Feld derselben Struktur sein.

Die Sequenz in einer Struktur oder einer Funktionsparameter Liste ist nicht signifikant. Die Union kann dem Diskriminanten vorangestellt oder folgen.

Der **\[ Switch \_ is \]** -Attribut kann als Feld Attribut oder als Parameter Attribut angezeigt werden.

## <a name="examples"></a>Beispiele

``` syntax
typedef [switch_type(short)] union _WILLIE_UNION_TYPE 
{ 
    [case(24)] 
        float fMays; 
    [case(25)] 
        double dMcCovey; 
    [default] 
        ; 
} WILLIE_UNION_TYPE; 
 
typedef struct _WINNER_TYPE 
{ 
    [switch_is(sUniformNumber)] WILLIE_UNION_TYPE w; 
    short sUniformNumber; 
} WINNER_TYPE;
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mittel l-Basis Typen](midl-base-types.md)
</dt> <dt>

[**Rückruf**](callback.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**Kontext \_ handle**](context-handle.md)
</dt> <dt>

[Gekapselt Unions](encapsulated-unions.md)
</dt> <dt>

[**Enumeration**](enum.md)
</dt> <dt>

[**der erste \_ ist**](first-is.md)
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

[Nicht gekapselt Unions](nonencapsulated-unions.md)
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

 

 




