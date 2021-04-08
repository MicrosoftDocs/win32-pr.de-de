---
title: Attribut mit Anmerkungen versehen
description: Mit dem Attribut "\ Annotate \" können Sie eine SAL-Anmerkung-Zeichenfolge für die angegebene Methode, den Parameter oder das Strukturfeld angeben.
ms.assetid: D0A35DCD-BD2F-455B-A040-5D63E4572D83
keywords:
- Attribut-Mittell kommentieren
topic_type:
- apiref
api_name:
- annotate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 820310c6aca0e5269d6febff5dc7d3208413110c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "103732088"
---
# <a name="annotate-attribute"></a>Attribut mit Anmerkungen versehen

Mit dem Attribut " **\[ kommentieren \]** " können Sie eine SAL-Anmerkung-Zeichenfolge für die angegebene Methode, den Parameter oder das Strukturfeld angeben.

``` syntax
[ annotation(â€œstringâ€0,  [, function-attribute-list] ] function-declarator ;
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ annotation(â€œstringâ€) [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*string* 
</dt> <dd>

Die angegebene SAL-Anmerkung-Zeichenfolge.

</dd> <dt>

*Function-Attribute-List* 
</dt> <dd>

Gibt 0 (null) oder mehr Attribute an, die für die Funktion gelten. Gültige Funktions Attribute sind [**\[ Callback \]**](callback.md), die Zeiger Attribute [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)oder [**\[ ptr \]**](ptr.md)und die Verwendungs Attribute [**\[ Zeichenfolge \]**](string.md), [**\[ ignorieren \]**](ignore.md)und [**\[ Kontext \_ handle \]**](context-handle.md). Mehrere Attribute müssen durch Kommas getrennt werden.

</dd> <dt>

*Function-declarator* 
</dt> <dd>

Gibt den Typspezifizierer, den Funktionsnamen und die Parameterliste für die Funktion an.

</dd> <dt>

*Typspezifizierer* 
</dt> <dd>

Gibt einen **\_ Basistyp**, eine [**\[ Struktur \]**](struct.md) [](union.md), eine Union oder einen Aufzählungstyp oder einen Typbezeichner an. [**\[ \]**](enum.md) Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden.

</dd> <dt>

*Zeiger-Deklarator* 
</dt> <dd>

Gibt 0 (null) oder mehr Zeiger Deklaratoren an. Ein zeigerdeklarator ist mit dem in C verwendeten zeigerdeklarator identisch. Sie wird aus dem Kenn \* Zeichner, den Modifizierern, z. b. **weit**, und dem Qualifizierer " [**\[ Konstanten \]**](const.md)" erstellt.

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Remote Prozedur an.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

Gibt 0 (null) oder mehr für den Parametertyp geeignete Attribute an. Parameter Attribute mit dem [**\[ in \]**](in.md) -Attribut können auch das [**\[ \]**](unique.md) [**\[ \_ \]**](last-is.md) [**\[ \]**](ref.md) [**\[ \]**](out-idl.md)direktionale Attribut zurücknehmen. die Feld Attribute [**\[ \_ sind \] zuerst**](first-is.md) [**\[ \_ , " \]**](length-is.md)Last", "length", " [**\[ Max \_ \] is**](max-is.md)", " [**\[ size" und " \_ Switch Type", die Zeiger Attribute "ref", "Unique" oder "PTR" und das Kontext Handle und die Zeichenfolge der Verwendungs \]**](size-is.md) [**\[ \]**](string.md) [**\[ \_ \]**](switch-type.md) [**\[ \_ \]**](context-handle.md) [**\[ \]**](ptr.md) Das Usage-Attribut " [**\[ Ignore \]**](ignore.md) " kann nicht als Parameter Attribut verwendet werden. Mehrere Attribute müssen durch Kommas getrennt werden.

</dd> <dt>

*Deklarator* 
</dt> <dd>

Gibt Standard-C-Deklaratoren an, z. b. Bezeichner, Zeiger Deklaratoren und Array Deklaratoren. Weitere Informationen finden Sie unter [Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**\[ Arrays \]**](../rpc/arrays.md)und [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers). Der parameterdeklarator im funktionsdedeclarator (z. b. der Parameter Name) ist optional.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das **\[ kommentieren \]** -Attribut ermöglicht das Überschreiben von in der Mitte generierten SAL-Anmerkungen oder das Hinzufügen an Stellen, an denen die-Anmerkung nicht explizit eine Anmerkung generiert. Wenn [**/SAL**](-sal.md) nicht in der Befehlszeile angegeben ist, wird dieses Attribut ignoriert.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/sal**](-sal.md)
</dt> <dt>

[**/SAL \_ lokal**](-sal-local.md)
</dt> </dl>

 

 