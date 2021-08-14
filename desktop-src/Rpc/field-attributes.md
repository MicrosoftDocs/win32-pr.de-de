---
title: Feldattribute
description: Feldattribute (Attribute, die auf Felder eines Arrays, einer Struktur, einer Union oder eines Zeichenarrays angewendet werden) und Remoteprozeduraufruf (RPC).
ms.assetid: 4508479d-ff0a-4698-94aa-588837032067
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e6d14bab0cf14710e91fceb466111c4af32d3d2828e4b7bdacc9494fa27b7d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929999"
---
# <a name="field-attributes"></a>Feldattribute

Feldattribute sind die Attribute, die auf Felder eines Arrays, einer Struktur, einer Union oder eines Zeichenarrays angewendet werden können:

-   **\[**[**ignore ,**](/windows/desktop/Midl/ignore) **\]** Größe **\[** [ **\_ ist**](/windows/desktop/Midl/size-is)**\]**
-   **\[**[**max \_ is**](/windows/desktop/Midl/max-is)**\]**
-   **\[**[**length \_ ist**](/windows/desktop/Midl/length-is)**\]**
-   **\[**[**ersten \_ ist**](/windows/desktop/Midl/first-is)**\]**
-   **\[**[**last \_ is**](/windows/desktop/Midl/last-is)**\]**
-   **\[**[**switch \_ ist**](/windows/desktop/Midl/switch-is)**\]**
-   **\[**[**Schnur**](/windows/desktop/Midl/string)**\]**
-   [Zeigerattribute](three-pointer-types.md)

Beispielsweise werden Feldattribute in Verbindung mit Arraydeklarationen verwendet, um entweder die Größe des Arrays oder den Teil des Arrays anzugeben, der gültige Daten enthält. Dies erfolgt durch Zuordnen eines anderen Parameters, Strukturfelds oder eines konstanten Ausdrucks zum Array.

Das **\[** [**ignore-Attribut**](/windows/desktop/Midl/ignore) **\]** bestimmt Zeigerfelder, die während des Marshallingprozesses ignoriert werden sollen. Ein solches ignoriertes Feld wird auf empfängerseitiger Seite auf **NULL** festgelegt.

MIDL bietet *konforme*, *variierende* und *offene Arrays.* Ein Array wird als konform bezeichnet, wenn seine Grenzen zur Laufzeit bestimmt werden. Die Größe ist ein Attribut, das die Obergrenze für die Zuordnungsgröße des Arrays und das Max is-Attribut die Obergrenze für den Wert eines gültigen **\[** [**\_**](/windows/desktop/Midl/size-is) **\]** **\[** [**\_**](/windows/desktop/Midl/max-is) **\]** Arrayindexes bestimmt. Weitere Informationen finden Sie unter **\[** [**Arrays.**](arrays.md) **\]**

Ein Array wird als varying bezeichnet, wenn seine Grenzen zur Kompilierzeit bestimmt werden, der Bereich der übertragenen Elemente jedoch zur Laufzeit bestimmt wird. Ein offenes Array (auch als konformes variierende Array bezeichnet) ist ein Array, dessen Obergrenze und Bereich der übertragenen Elemente zur Laufzeit bestimmt werden. Um den Bereich der übertragenen Elemente eines Arrays zu bestimmen, muss die Arraydeklaration eine Länge enthalten: , first **\[** [**\_**](/windows/desktop/Midl/length-is) **\]** **\[** [**\_ ist**](/windows/desktop/Midl/first-is) **\]** oder last **\[** [**\_ is**](/windows/desktop/Midl/last-is) **\]** attribute.

Das **\[ Length \_ \] is-Attribut** gibt die **\[ \_ \]** Anzahl der zu übertragenden Arrayelemente an, und das erste attribut ist der Index des ersten zu übertragenden Arrayelements. Das **\[ letzte \_ \] is-Attribut** gibt den Index des letzten zu übertragenden Arrayelements an.

Der **\[** [**Schalter ist \_ feldattribut**](/windows/desktop/Midl/switch-is) **\]** bezeichnet einen Union-Diskriminator. Wenn die Union ein Prozedurparameter ist, muss der Union-Diskriminator ein weiterer Parameter derselben Prozedur sein. Wenn die Union ein Feld einer -Struktur ist, muss der Diskriminator ein anderes Feld der -Struktur auf der gleichen Ebene wie das Union-Feld sein. Der Diskriminator muss ein boolescher [**Typ,**](/windows/desktop/Midl/boolean) [**char,**](/windows/desktop/Midl/char-idl) [**int**](/windows/desktop/Midl/int)oder [**enum-Typ**](/windows/desktop/Midl/enum) oder ein Typ sein, der in einen dieser Typen auflöset. Weitere Informationen finden Sie unter [Nonencapsulated Unions and](/windows/desktop/Midl/nonencapsulated-unions) switch is (Nicht kapselte Unions und **\[ Switch \_ ist \]**).

Das **\[** [**Zeichenfolgenfeldattribut**](/windows/desktop/Midl/string) gibt an, dass ein eindimensionales Zeichen oder Bytearray oder ein Zeiger auf ein auf Null terminiertes Zeichen oder einen Bytestream als Zeichenfolge behandelt **\]** werden soll. Das Zeichenfolgenattribut gilt nur für eindimensionale Arrays und Zeiger. Der Elementtyp ist auf [**char,**](/windows/desktop/Midl/char-idl) [**byte,**](/windows/desktop/Midl/byte) [**wchar \_ t**](/windows/desktop/Midl/wchar-t)oder einen benannten Typ beschränkt, der in einen dieser Typen auflöset.

Informationen zum Kontext, in dem Feldattribute angezeigt werden, finden Sie unter [MIDL-Arrays,](/windows/desktop/Midl/midl-arrays) [MIDL-Strukturen](/windows/desktop/Midl/midl-structures)und [MIDL-Unions.](/windows/desktop/Midl/midl-unions)

 

 