---
title: switch_is-Attribut
description: Der \switch is\-Attribut gibt den Ausdruck oder Bezeichner an, der bzw. der als Union diskriminant dient, der \_ den Union-Member auswählt.
ms.assetid: 93552bdf-6a14-47ce-877e-32ed976bb895
keywords:
- switch_is MIDL-Attribut
topic_type:
- apiref
api_name:
- switch_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1975dcf38a04fc127de199e7cc663c8af41b63e6ce8f92d38be2115316ed0727
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382841"
---
# <a name="switch_is-attribute"></a>switch \_ is attribute

Der **\[ Schalter \_ \] is-Attribut** gibt den Ausdruck oder Bezeichner an, der bzw. der als Union-Diskriminant dient, der den Union-Member auswählt.

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

*struct-tag* 
</dt> <dd>

Gibt ein optionales Tag für eine -Struktur an.

</dd> <dt>

*limited-expr* 
</dt> <dd>

Gibt einen von MIDL unterstützten C-Sprachausdruck an. Fast alle C-Sprachausdrücke werden unterstützt. Der MIDL-Compiler unterstützt bedingte Ausdrücke, logische Ausdrücke, relationale Ausdrücke und arithmetische Ausdrücke. MIDL lässt keine Funktionsaufrufe in Ausdrücken zu und lässt keine Prä- und Nachinkrementoperatoren sowie Prä- und Nachdekrementoperatoren zu.

</dd> <dt>

*field-attr-list* 
</dt> <dd>

Gibt null oder mehr Feldattribute an, die für ein Union-Element gelten. Zu den gültigen Feldattributen zählen zuerst ist , last ist , length ist , max ist , size ist ; die Verwendungsattribute string , ignore und context **\[** [**\_**](first-is.md)handle; das **\]** **\[** [**\_**](last-is.md) **\]** **\[** [**\_**](length-is.md) **\]** **\[** [**\_**](max-is.md) **\]** **\[** [**\_**](size-is.md) **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** **\[** [**\_**](context-handle.md) **\]** Zeigerattribut **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md), **\]** oder **\[** [**ptr;**](ptr.md) **\]** **\[** [**\_**](switch-type.md) **\]** und für Member, die selbst Unions sind, wird der Union-Attributschaltertyp verwendet. Trennen Sie mehrere Feldattribute durch Kommas.

</dd> <dt>

*union-type-specifier* 
</dt> <dd>

Gibt den [**Union-Typbezeichner**](union.md) an. Eine optionale Speicherspezifikation kann dem *Typspezifizierer vorangestellt werden.*

</dd> <dt>

*Deklarator und Deklaratorliste* 
</dt> <dd>

Gibt einen C-Standarddeklarator an, z. B. einen Bezeichner, einen Zeigerdeklarator und einen Arraydeklarator. (Funktionsdeklaratoren und Bitfelddeklarationen sind in Unions, die in Remoteprozeduraufrufen übertragen werden, nicht zulässig. Diese Deklaratoren sind in Unions zulässig, die nicht übertragen werden.) Trennen Sie mehrere Deklaratoren durch Kommas.

</dd> <dt>

*function-attribute-list* 
</dt> <dd>

Gibt null oder mehr Attribute an, die für die Funktion gelten. Gültige Funktionsattribute sind rückruf , local, das **\[** [](callback.md) **\]** **\[** [](local.md) **\]** Zeigerattribut **\[ ref, \]** **\[ \] unique** oder **\[ \]** **\[ ptr \]** und die Verwendungsattribute **\[ \]** **\[ \_ \]** Zeichenfolge , ignorieren und Kontexthand handle .

</dd> <dt>

*Typspezifizierer* 
</dt> <dd>

Gibt einen [Basistyp, eine](midl-base-types.md) [**Struktur,**](struct.md)eine [**Union,**](union.md) [**einen enum-Typ**](enum.md) oder einen Typbezeichner an. Eine optionale Speicherspezifikation kann dem *Typspezifizierer vorangestellt werden.*

</dd> <dt>

*Zeigerdeklarator* 
</dt> <dd>

Gibt null oder mehr Zeigerdeklaratoren an. Ein Zeigerdeklarator ist mit dem in C verwendeten Zeigerdeklarator identisch. sie wird aus dem \* Designator, Modifizierern wie **far** und dem Qualifizierer [**const erstellt.**](const.md)

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Gibt den Namen der Remoteprozedur an.

</dd> <dt>

*param-attr-list* 
</dt> <dd>

Gibt null oder mehr Attribute an, die für den angegebenen Parametertyp geeignet sind. Parameterattribute können die direktionalen Attribute **\[ \] in** **\[ \]** **\[ \_ \]** **\[ \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ \]** **\[ \]** und aus **\[ \_ \]** übernehmen, die Feldattribute sind zuerst , last ist , length ist , max ist , size ist , und **\[ switch \_ type, \]** das Zeigerattribut **\[ ref, \]** unique oder **\[ ptr \]** sowie das Kontexthand handle und die Zeichenfolge der Verwendungsattribute. Das ignorierte **\[ \] Verwendungsattribut** kann nicht als Parameterattribut verwendet werden. Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*union-type* 
</dt> <dd>

Identifiziert den [](union.md) Union-Typspezifizierer.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die dem Switch zugeordnete Diskriminanz **\[ \_ muss \]** auf der gleichen logischen Ebene wie die Union definiert werden:

-   Wenn die Union ein Parameter ist, muss die Union diskriminant ein anderer Parameter sein.
-   Wenn die Union ein Feld einer -Struktur ist, muss die Diskriminanz ein anderes Feld derselben Struktur sein.

Die Sequenz in einer Struktur oder einer Funktionsparameterliste ist nicht von Bedeutung. Die Union kann entweder dem Diskriminanten voran- oder folgen.

Der **\[ Schalter ist \_ ein \]** Attribut, das als Feldattribut oder als Parameterattribut angezeigt werden kann.

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

[MIDL-Basistypen](midl-base-types.md)
</dt> <dt>

[**Rückruf**](callback.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**Kontexthand \_ handle**](context-handle.md)
</dt> <dt>

[Gekapselte Unions](encapsulated-unions.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[**ersten \_ ist**](first-is.md)
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

[Nicht kapselte Unions](nonencapsulated-unions.md)
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

[**Union**](union.md)
</dt> <dt>

[**Einzigartige**](unique.md)
</dt> </dl>

 

 




