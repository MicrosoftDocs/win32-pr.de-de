---
title: Arrays-Attribut
description: Arrays sind homogene Auflistungen von Daten, auf die über einen Index oder eine Element Nummer zugegriffen wird
ms.assetid: 375fb795-8f18-45b7-898c-99f1273746d8
keywords:
- Arrays-Attribut-Mittel l
topic_type:
- apiref
api_name:
- arrays
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e189eb1784a4ff24b799c7a4d4482d0f56b20e3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106337404"
---
# <a name="arrays-attribute"></a>Arrays-Attribut

Arrays sind homogene Auflistungen von Daten, auf die über einen Index oder eine Element Nummer zugegriffen wird

``` syntax
typedef [ [type-attr-list] ] type-specifier [pointer-decl] array-declarator;

typedef [ [type-attr-list] ] struct [ tag ] 
{
    [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
    ...
};

typedef [ [type-attr-list] ] union [ tag ] 
{
    [ case (limited-expression [ , ... ] ) ]
  [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
  [ [ default ]
  [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
  ]
};

[[ [function-attribute-list] ]] type-specifier [[pointer-decl]] function-name(
        [[ [param-attr-list] ]] type-specifier [[pointer-decl]] array-declarator
        , ...);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Type-attr-List* 
</dt> <dd>

Gibt 0 (null) oder mehr Attribute an, die für den Typ gelten. Gültige Typattribute sind [**\[ handle \]**](handle.md), [**\[ \_ Switchtyp \]**](switch-type.md) [**\[ , über \_ Tragung \] als**](transmit-as.md); Zeiger Attribut Verweis, [**\[ eindeutig \]**](unique.md)oder [**\[ \] ptr**](ptr.md); und die Verwendungs Attribute [**\[ Kontext \_ handle \]**](context-handle.md), [**\[ String \]**](string.md)und [**\[ Ignore \]**](ignore.md). [**\[ \]**](ref.md) Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*Typspezifizierer* 
</dt> <dd>

Gibt den Typbezeichner, Basistyp, [**Struktur**](struct.md), [**Union**](union.md)oder [**Enumeration**](enum.md) -Typ an. Die Typspezifikation kann eine optionale Speicher Spezifikation enthalten.

</dd> <dt>

*Zeiger-decl* 
</dt> <dd>

Gibt 0 (null) oder mehr Zeiger Deklaratoren an. Ein zeigerdeklarator ist derselbe wie der in C verwendete zeigerdeklarator, der aus dem Kenn Zeichner erstellt wurde **\*** , Modifizierer, z. b. **weit**, und der Qualifizierer [**Konstanten**](const.md).

</dd> <dt>

*Array-declarator* 
</dt> <dd>

Gibt den Namen des Arrays an, gefolgt von einem der folgenden Konstrukte für jede Dimension des Arrays: "**\[ \]**", " **\[\*\]** ", "**\[ ***Const1*** \]**" oder "**\[ ***Lower...*** Upper \]**"Where *Lower* und *Upper* sind konstante Werte, die die unteren und oberen Begrenzungen darstellen. Die *untere* Konstante muss zu 0 (null) ausgewertet werden.

</dd> <dt>

*Tag* 
</dt> <dd>

Gibt ein optionales Tag für die Struktur oder Union an.

</dd> <dt>

*Field-Attribute-List* 
</dt> <dd>

Gibt 0 (null) oder mehr Feld Attribute an, die für die Struktur, den Union-Member oder den Funktionsparameter gelten. Gültige Feld Attribute sind [**\[ First \_ is \]**](first-is.md), [**\[ Last \_ is \]**](last-is.md), [**\[ length \_ is \]**](length-is.md), [**\[ Max \_ is \]**](max-is.md), [**\[ size \_ is \]**](size-is.md), die Usage-Attribut [**\[ Zeichenfolge \]**](string.md)und [**\[ \] Ignore**](ignore.md); die Zeiger Attribute [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)und [**\[ ptr \]**](ptr.md)sowie der Typ [**\[ \_ \]**](switch-type.md)des Union-Attribut Schalters. Trennen Sie mehrere Feld Attribute durch Kommas. Beachten Sie, dass die oben aufgeführten Attribute **\[ First \_ is \]**, **\[ Last \_ is \]** und [**\[ Ignore \]**](ignore.md) für Unions nicht gültig sind.

</dd> <dt>

*eingeschränkter Ausdruck* 
</dt> <dd>

Gibt einen C-sprach Ausdruck an. Der mittlerer l-Compiler unterstützt bedingte Ausdrücke, logische Ausdrücke, relationale Ausdrücke und arithmetische Ausdrücke. "Mittel l" lässt keine Funktionsaufrufe in Ausdrücken zu und lässt keine Inkrement-und Dekrementoperatoren zu.

</dd> <dt>

*Function-Attribute-List* 
</dt> <dd>

Gibt 0 (null) oder mehr Attribute an, die für die Funktion gelten. Gültige Funktions Attribute sind [**\[ Callback \]**](callback.md), [**\[ local \]**](local.md), das Zeiger Attribut [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)oder [**\[ ptr \]**](ptr.md)sowie die [**\[ Zeichen \] Folge**](string.md)der Verwendungs Attribute und das [**\[ Kontext \_ handle \]**](context-handle.md).

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Remote Prozedur an.

</dd> <dt>

*param-attr-List* 
</dt> <dd>

Gibt die direktionalen Attribute und mindestens ein optionales Feld Attribut an, die auf den Array Parameter angewendet werden. Gültige Feld Attribute sind " [**\[ Max \_ is \]**](max-is.md)", " [**\[ size \_ \]**](size-is.md)", " [**\[ length \_ \]**](length-is.md)", " [**\[ First \_ is \]**](first-is.md)" und " [**\[ Last \_ \]**](last-is.md)".

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Arrays in der mittleren l verwenden einen Stil, der mit identisch ist, aber nicht genau mit C und C++ identisch ist. Weitere Informationen finden Sie unter [Mittel l-Arrays](midl-arrays.md).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

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
</dt> <dt>

[**gem**](unique.md)
</dt> </dl>

 

 




