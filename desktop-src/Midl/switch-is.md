---
title: switch_is-Attribut
description: Das \_ \switch is\-Attribut gibt den Ausdruck oder Bezeichner an, der als Union-Diskriminant fungiert, der das Union-Element auswählt.
ms.assetid: 93552bdf-6a14-47ce-877e-32ed976bb895
keywords:
- switch_is-Attribut MIDL
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

Der **\[ Schalter \_ ist \]** das -Attribut, das den Ausdruck oder Bezeichner angibt, der als Union-Diskriminant fungiert, der das Union-Element auswählt.

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

Gibt einen von MIDL unterstützten C-Sprachausdruck an. Fast alle C-Sprachausdrücke werden unterstützt. Der MIDL-Compiler unterstützt bedingte Ausdrücke, logische Ausdrücke, relationale Ausdrücke und arithmetische Ausdrücke. MIDL lässt keine Funktionsaufrufe in Ausdrücken zu und lässt keine Operatoren vor und nach dem Inkrement sowie vor und nach der Dekrementierung zu.

</dd> <dt>

*field-attr-list* 
</dt> <dd>

Gibt null oder mehr Feldattribute an, die für einen Union-Member gelten. Gültige Feldattribute **\[** [**sind: zuerst \_ ist**](first-is.md) **\]** , last **\[** [**\_ ist**](last-is.md) **\]** , length **\[** [**\_ ist**](length-is.md) **\]** , max **\[** [**\_ ist**](max-is.md) **\]** , size **\[** [**\_ ist**](size-is.md) **\]** ; die Verwendungsattribute **\[** [**Zeichenfolge**](string.md) **\]** , **\[** [**ignorieren**](ignore.md) **\]** und **\[** [**\_ Kontexthandle;**](context-handle.md) **\]** das Zeigerattribut **\[** [**ref**](ref.md) **\]** , **\[** [**eindeutig**](unique.md) **\]** oder **\[** [**ptr;**](ptr.md)und für **\]** Member, die selbst Unions sind, der Union-Attributswitchtyp **\[** [**\_**](switch-type.md) **\]** . Trennen Sie mehrere Feldattribute durch Kommas.

</dd> <dt>

*union-type-specifier* 
</dt> <dd>

Gibt den [](union.md) Union-Typbezeichner an. Eine optionale Speicherspezifikation kann dem *Typspezifizierer* vorangestellt werden.

</dd> <dt>

*deklarator und declarator-list* 
</dt> <dd>

Gibt einen C-Standarddeklarator an, z. B. einen Bezeichner, einen Zeigerdeklarator und einen Arraydeklarator. (Funktionsdeklaratoren und Bitfelddeklarationen sind in Unions, die in Remoteprozeduraufrufen übertragen werden, nicht zulässig. Diese Deklaratoren sind in Unions zulässig, die nicht übertragen werden.) Trennen Sie mehrere Deklaratoren durch Kommas.

</dd> <dt>

*function-attribute-list* 
</dt> <dd>

Gibt null oder mehr Attribute an, die für die Funktion gelten. Gültige Funktionsattribute sind **\[** [**rückruf,**](callback.md) **\]** **\[** [**local,**](local.md) **\]** das Zeigerattribut **\[ ref, \]** **\[ eindeutig \]** oder **\[ ptr \]** und die Verwendungsattribute **\[ Zeichenfolge \]**, **\[ ignorieren \]** und **\[ \_ Kontexthandle \]**.

</dd> <dt>

*Typspezifizierer* 
</dt> <dd>

Gibt einen [Basistyp,](midl-base-types.md) [**eine Struktur,**](struct.md) [**einen Union-,**](union.md) [**Enumerations-**](enum.md) oder Typbezeichner an. Eine optionale Speicherspezifikation kann dem *Typspezifizierer* vorangestellt werden.

</dd> <dt>

*Zeigerdeklarator* 
</dt> <dd>

Gibt null oder mehr Zeigerdeklaratoren an. Ein Zeigerdeklarator entspricht dem in C verwendeten Zeigerdeklarator. sie wird aus dem \* Bezeichner, Modifizierern wie **far** und dem Qualifizierer [**const**](const.md)erstellt.

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Gibt den Namen der Remoteprozedur an.

</dd> <dt>

*param-attr-list* 
</dt> <dd>

Gibt null oder mehr Attribute an, die für den angegebenen Parametertyp geeignet sind. Parameterattribute können die direktionalen Attribute **\[ in \]** und **\[ aus \]** aufnehmen, die Feldattribute **\[ sind zuerst \_ \]**, die letzte **\[ \_ ist \]**, die Länge ist , max **\[ \_ \]** **\[ \_ ist \]**, die Größe **\[ \_ ist \]**, und der **\[ \_ Schaltertyp \]**; das Zeigerattribut **\[ ref \]**, **\[ eindeutig \]** oder **\[ ptr \]**; und das **\[ \_ Kontexthandle \]** der Verwendungsattribute und die **\[ Zeichenfolge \]**. Das Verwendungsattribut **\[ ignore \]** kann nicht als Parameterattribut verwendet werden. Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*union-type* 
</dt> <dd>

Identifiziert den [](union.md) Union-Typspezifizierer.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das diskriminante, dem Switch zugeordnete **\[ \_ Attribut is \]** muss auf der gleichen logischen Ebene wie die Union definiert werden:

-   Wenn die Union ein Parameter ist, muss die Union-Unterscheidung ein anderer Parameter sein.
-   Wenn die Union ein Feld einer -Struktur ist, muss der diskriminante ein anderes Feld derselben Struktur sein.

Die Sequenz in einer Struktur oder einer Funktionsparameterliste ist nicht von Bedeutung. Die Union kann der Diskriminanz entweder vorangehen oder ihr folgen.

Der **\[ Schalter is \_ attribute \]** kann als Feldattribut oder als Parameterattribut angezeigt werden.

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

[**\_Kontexthandle**](context-handle.md)
</dt> <dt>

[Gekapselte Unions](encapsulated-unions.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[**\_first ist**](first-is.md)
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

[Nicht gekapselte Unions](nonencapsulated-unions.md)
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

 

 




