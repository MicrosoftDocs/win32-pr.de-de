---
title: Union-Attribut
description: Das Union-Schlüsselwort wird in Funktionen angezeigt, die sich auf diskriminierte Unions beziehen.
ms.assetid: 135a6581-e03e-4b90-9fd8-15690820dbd0
keywords:
- Union-Attribut-Mittel l
topic_type:
- apiref
api_name:
- union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc683472d67775c4a2900695246d5f9ca920ca32
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104516299"
---
# <a name="union-attribute"></a>Union-Attribut

Das **Union** -Schlüsselwort wird in Funktionen angezeigt, die sich auf diskriminierte Unions beziehen.

``` syntax
/* Encapsulated union*/
typedef [[ [type-attribute-list] ]] union [[ struct-name ]] switch (switch-type switch-name) [[ union-name ]] 
{
  C-style-case-list 
  [[ [ field-attribute-list <> ] ]] type-specifier <> declarator-list <>;

        ...
}

/* Non-encapsulated union*/
typedef [switch_type(switch-type) [[ , type-attr-list ]] ] union [[ tag ]] 
{ 
    [ case ( limited-expr-list) ]
  [[ [ field-attribute-list ] ]] type-specifier declarator-list;
  [[ [ default ]
  [[ [ field-attribute-list ] ]] type-specifier declarator-list;
  ]]
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Type-Attribute-List* 
</dt> <dd>

Gibt 0 (null) oder mehr Attribute an, die für den Union-Typ gelten. Gültige Typattribute sind **\[** [**handle**](handle.md) **\]** , über **\[** [**tragen \_ als**](transmit-as.md) **\]** ; das Zeiger Attribut **\[** [**eindeutig**](unique.md) **\]** oder **\[** [**ptr**](ptr.md) **\]** ; und das **\[** [**Kontext \_ handle**](context-handle.md) der Verwendungs Attribute **\]** und **\[** [**Ignore**](ignore.md) **\]** . Gekapselte Unions können auch das Attribut " **\[** [**ref**](ref.md) **\]** Pointer Type" aufweisen. Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*Struktur Name* 
</dt> <dd>

Gibt ein optionales Tag an, das die vom Mittelwert Compiler generierte Struktur benennt.

</dd> <dt>

*Switch-Type* 
</dt> <dd>

Gibt einen [**int**](int.md)-, [**char**](char-idl.md)-, [**Enumeration**](enum.md) -Typ oder einen Bezeichner an, der zu einem dieser Typen aufgelöst wird.

</dd> <dt>

*SwitchName* 
</dt> <dd>

Gibt den Namen der Variablen vom Typ *Switch-Type* an, der als Union-diskriminant fungiert.

</dd> <dt>

*Union-Name* 
</dt> <dd>

Gibt einen optionalen Bezeichner an, der die Union in der Struktur benennt, die vom-Mittell-Compiler generiert wird und die die Union und die Diskriminante enthält.

</dd> <dt>

*C-Style-Case-List* 
</dt> <dd>

Liste von "**Case** *-Konstanten-expr* :"

</dd> <dt>

*begrenzte Ausdrucks Liste* 
</dt> <dd>

Gibt einen oder mehrere C-sprach Ausdrücke an. Der mittlerer l-Compiler unterstützt bedingte Ausdrücke, logische Ausdrücke, relationale Ausdrücke und arithmetische Ausdrücke. "Mittel l" lässt keine Funktionsaufrufe in Ausdrücken zu und lässt keine Inkrement-und Dekrementoperatoren zu. Einzelne Ausdrücke in der Liste sollten durch ein Komma getrennt werden.

</dd> <dt>

*Field-Attribute-List* 
</dt> <dd>

Gibt 0 (null) oder mehr Feld Attribute an, die für das Union-Element gelten. Gültige Feld Attribute sind **\[** [**First \_ is**](first-is.md), **\]** **\[** [**Last \_ is**](last-is.md) **\]** , **\[** [**length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ is**](size-is.md), **\]** die Usage **\[** -Attribut [**Zeichenfolge**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** und **\[** [**context \_ handle**](context-handle.md), **\]** das Zeiger Attribut **\[** [**Unique**](unique.md) **\]** oder **\[** [**ptr**](ptr.md) **\]** ; und für Member, die nicht gekapselte Unions sind, der **\[** [**\_ Switchtyp**](switch-type.md)des Union-Attributs **\]** . Nicht gekapselte Unions können auch das **\[** [**ref**](ref.md) - **\]** Zeiger Feld Attribut verwenden. Trennen Sie mehrere Feld Attribute durch Kommas.

</dd> <dt>

*Typspezifizierer* 
</dt> <dd>

Gibt einen [Basistyp](midl-base-types.md), eine [**Struktur**](struct.md), eine **Union**, einen [**Enumeration**](enum.md) -Typ oder einen Typbezeichner an. Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden.

</dd> <dt>

*Deklarator-List* 
</dt> <dd>

Ein oder mehrere Standard-C-Deklaratoren, wie z. b. Bezeichner, Zeiger Deklaratoren und Array Deklaratoren. (Funktions Deklaratoren und Bitfeld Deklarationen sind in Unions nicht zulässig, die in Remote Prozedur aufrufen übertragen werden. Mit der Ausnahme, dass Sie den [**/OSF**](-osf.md)-Compilerschalter verwenden, sind diese Deklaratoren in Unions zulässig, die nicht übertragen werden.) Trennen Sie mehrere Deklaratoren durch Kommas.

</dd> <dt>

*Tag* 
</dt> <dd>

Gibt ein optionales-Tag an.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Mittel l unterstützt zwei Typen von Unterscheidungs-Unions: [gekapselte Unions](encapsulated-unions.md) und [nicht gekapselt](nonencapsulated-unions.md) Die gekapselte Union ist mit früheren Implementierungen von RPC (NCA, Version 1) kompatibel. Die nicht gekapselte Union entfernt einige der Einschränkungen der gekapselten Union und bietet eine besser sichtbare Diskriminante als die gekapselte Union.

Die gekapselte Union wird durch das [**Switch**](switch.md) -Schlüsselwort und das Fehlen von anderen Union-bezogenen Schlüsselwörtern identifiziert.

Die nicht gekapselte Union, auch bekannt als Union, wird durch das vorhanden sein der **\[** [**Schalter \_ ist**](switch-is.md) **\]** und der **\[** [**\_ switchtypschlüsselwörter**](switch-type.md) identifiziert **\]** , die den Diskriminanten und dessen Typ identifizieren.

Wenn Sie **\[** [**in**](in.md), [**out**](out-idl.md) Unions verwenden, beachten Sie, **\]** dass das Ändern des Werts des Union-Schalters während des Aufrufes dazu führen kann, dass sich der Remote-Befehl von einem lokalen-Befehl unterscheidet. Bei der Rückgabe kopieren die Studs den **\[ in**- **, \] out** -Parameter in den Arbeitsspeicher, der bereits auf dem Client vorhanden ist. Wenn die Remote Prozedur den Wert des Union-Schalters ändert und folglich die Größe des Datenobjekts ändert, können die stubwerte den gültigen Speicher mit dem Wert **\[ out \]** überschreiben. Wenn der Union-Switch das Datenobjekt von einem Basistyp in einen Zeigertyp ändert, können die Stub den gültigen Arbeitsspeicher überschreiben, wenn Sie den Zeiger Referenten in den Speicher Speicherort kopieren, der durch den Wert **\[ in \]** einem Basistyp angegeben wird.

Die Form der Unions muss plattformübergreifend identisch sein, um die Konnektivität zu gewährleisten.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Gekapselt Unions](encapsulated-unions.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[Nicht gekapselt Unions](nonencapsulated-unions.md)
</dt> <dt>

[**vorgenommen**](out-idl.md)
</dt> <dt>

[**Switch \_ ist**](switch-is.md)
</dt> <dt>

[**\_Switchtyp**](switch-type.md)
</dt> </dl>

 

 




