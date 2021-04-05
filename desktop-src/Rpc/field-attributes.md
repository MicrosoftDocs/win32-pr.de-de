---
title: Feldattribute
description: Feld Attribute (Attribute, die auf Felder eines Arrays, einer Struktur, einer Union oder eines Zeichen Arrays angewendet werden) und Remote Prozedur Aufruf (RPC).
ms.assetid: 4508479d-ff0a-4698-94aa-588837032067
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79b9421ddf4ea7e7bc4c70af0ecd826e2681875d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949054"
---
# <a name="field-attributes"></a>Feldattribute

Feld Attribute sind die Attribute, die auf Felder eines Arrays, einer Struktur, einer Union oder eines Zeichen Arrays angewendet werden können:

-   **\[**[**ignorieren**](/windows/desktop/Midl/ignore) **\]** , **\[** [ **Größe \_ ist**](/windows/desktop/Midl/size-is)**\]**
-   **\[**[**Max \_ ist**](/windows/desktop/Midl/max-is)**\]**
-   **\[**[**Länge \_ ist**](/windows/desktop/Midl/length-is)**\]**
-   **\[**[**der erste \_ ist**](/windows/desktop/Midl/first-is)**\]**
-   **\[**[**Letzter \_ ist**](/windows/desktop/Midl/last-is)**\]**
-   **\[**[**Switch \_ ist**](/windows/desktop/Midl/switch-is)**\]**
-   **\[**[**Schnür**](/windows/desktop/Midl/string)**\]**
-   [Zeiger Attribute](three-pointer-types.md)

Beispielsweise werden Feld Attribute in Verbindung mit Array Deklarationen verwendet, um entweder die Größe des Arrays oder den Teil des Arrays anzugeben, der gültige Daten enthält. Dies erfolgt durch Zuordnen eines anderen Parameters, Struktur Felds oder eines konstanten Ausdrucks zu dem Array.

Das **\[** [**Ignore**](/windows/desktop/Midl/ignore) -Attribut kennzeichnet **\]** Zeiger Felder, die während des Marshallingprozesses ignoriert werden. Ein ignoriertes Feld wird auf der Empfängerseite auf **null** festgelegt.

Die Mittel l stellt *konforme*, *abweichende* und *offene* Arrays bereit. Ein Array wird als konform bezeichnet, wenn seine Begrenzungen zur Laufzeit bestimmt werden. Die **\[** [**Größe \_ ist**](/windows/desktop/Midl/size-is) " **\]** Attribute" bezeichnet die obere Grenze der Zuordnungs Größe des Arrays, und das **\[** [**Maximum \_ is**](/windows/desktop/Midl/max-is) - **\]** Attribut legt die obere Grenze für den Wert eines gültigen Array Indexes fest. Weitere Informationen finden Sie unter **\[** [**Arrays**](arrays.md) **\]** .

Ein Array wird unterschiedlich aufgerufen, wenn seine Begrenzungen zur Kompilierzeit bestimmt werden, der Bereich der übertragenen Elemente jedoch zur Laufzeit bestimmt wird. Ein offenes Array (auch als konform bezeichnetes Array bezeichnet) ist ein Array, dessen obere Grenze und der Bereich der übertragenen Elemente zur Laufzeit bestimmt werden. Um den Bereich der übertragenen Elemente eines Arrays zu ermitteln, muss die Array Deklaration eine **\[** [**Länge \_**](/windows/desktop/Midl/length-is)von **\]** , das **\[** [**erste \_ ist**](/windows/desktop/Midl/first-is) **\]** oder das **\[** [**Letzte \_ is**](/windows/desktop/Midl/last-is) - **\]** Attribut enthalten.

Die **\[ Länge \_ ist \]** "Attribute" gibt die Anzahl der zu übertragenden Array Elemente an, **\[ \_ \]** und das erste Attribut bezeichnet den Index des ersten zu übertragenden Array Elements. Das **\[ Letzte \_ is \]** -Attribut kennzeichnet den Index des letzten Array Elements, das übertragen werden soll.

Der **\[** [**Switch \_ ist**](/windows/desktop/Midl/switch-is) **\]** ein Feld Attribut, das einen Union-Diskriminator bezeichnet. Wenn die Union ein Prozedur Parameter ist, muss der Union-Diskriminator ein weiterer Parameter der gleichen Prozedur sein. Wenn die Union ein Feld einer Struktur ist, muss es sich bei dem Diskriminator um ein anderes Feld der Struktur auf derselben Ebene wie das Union-Feld handeln. Der Diskriminator muss ein [**boolescher**](/windows/desktop/Midl/boolean), [**char**](/windows/desktop/Midl/char-idl)-, [**int**](/windows/desktop/Midl/int)- [**oder Enumerationstyp oder ein**](/windows/desktop/Midl/enum) Typ sein, der zu einem dieser Typen aufgelöst wird. Weitere Informationen finden Sie unter [nicht gekapselte Unions](/windows/desktop/Midl/nonencapsulated-unions) und **\[ Switch \_ ist \]**.

Das **\[** [**Zeichen**](/windows/desktop/Midl/string) folgen **\]** Feld Attribut gibt an, dass ein eindimensionales Zeichen oder Bytearray oder ein Zeiger auf ein mit Null endendes Zeichen oder einen Byte-Stream als Zeichenfolge behandelt werden soll. Das String-Attribut gilt nur für eindimensionale Arrays und Zeiger. Der Elementtyp ist auf [**char**](/windows/desktop/Midl/char-idl), [**Byte**](/windows/desktop/Midl/byte), [**WCHAR \_ t**](/windows/desktop/Midl/wchar-t)oder einen benannten Typ beschränkt, der in einen dieser Typen aufgelöst wird.

Informationen über den Kontext, in dem Feld Attribute angezeigt werden, finden Sie unter [Mittel l-Arrays](/windows/desktop/Midl/midl-arrays), [Mittel l-Strukturen](/windows/desktop/Midl/midl-structures)und [Mittel l-Unions](/windows/desktop/Midl/midl-unions).

 

 