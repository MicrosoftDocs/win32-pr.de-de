---
title: Feldattribute
description: Feldattribute (Attribute, die auf Felder eines Arrays, einer Struktur, einer Union oder eines Zeichenarrays angewendet werden) und Remote Procedure Call (RPC).
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

-   **\[**[**ignore**](/windows/desktop/Midl/ignore) **\]** , größe **\[** [ **\_ ist**](/windows/desktop/Midl/size-is)**\]**
-   **\[**[**max \_ ist**](/windows/desktop/Midl/max-is)**\]**
-   **\[**[**length \_ ist**](/windows/desktop/Midl/length-is)**\]**
-   **\[**[**\_first ist**](/windows/desktop/Midl/first-is)**\]**
-   **\[**[**last \_ ist**](/windows/desktop/Midl/last-is)**\]**
-   **\[**[**switch \_ ist**](/windows/desktop/Midl/switch-is)**\]**
-   **\[**[**Schnur**](/windows/desktop/Midl/string)**\]**
-   [Zeigerattribute](three-pointer-types.md)

Beispielsweise werden Feldattribute in Verbindung mit Arraydeklarationen verwendet, um entweder die Größe des Arrays oder den Teil des Arrays anzugeben, der gültige Daten enthält. Dazu wird dem Array ein anderer Parameter, ein Strukturfeld oder ein konstanter Ausdruck zugeordnet.

Das **\[** [](/windows/desktop/Midl/ignore) **\]** ignore-Attribut legt Zeigerfelder fest, die während des Marshallingprozesses ignoriert werden sollen. Ein solches ignoriertes Feld wird auf empfängerseitiger Seite auf **NULL** festgelegt.

MIDL stellt *konforme,* *unterschiedliche* und *offene* Arrays bereit. Ein Array wird als konform bezeichnet, wenn seine Grenzen zur Laufzeit bestimmt werden. Das **\[** [**Size \_ is-Attribut**](/windows/desktop/Midl/size-is) **\]** legt die Obergrenze für die Zuordnungsgröße des Arrays fest, und das **\[** [**max \_ is-Attribut**](/windows/desktop/Midl/max-is) **\]** legt die Obergrenze für den Wert eines gültigen Arrayindexes fest. Weitere Informationen finden Sie unter **\[** [**Arrays.**](arrays.md) **\]**

Ein Array wird als variierend bezeichnet, wenn seine Grenzen zur Kompilierzeit bestimmt werden, aber der Bereich der übertragenen Elemente zur Laufzeit bestimmt wird. Ein offenes Array (auch als konformes variierendes Array bezeichnet) ist ein Array, dessen Obergrenze und Bereich der übertragenen Elemente zur Laufzeit bestimmt werden. Um den Bereich der übertragenen Elemente eines Arrays zu bestimmen, muss die Arraydeklaration eine Länge von **\[** [**\_**](/windows/desktop/Midl/length-is) **\]** enthalten: , **\[** [**first \_ ist**](/windows/desktop/Midl/first-is) **\]** oder last **\[** [**\_ is**](/windows/desktop/Midl/last-is) **\]** attribute.

Das **\[ length \_ \] is-Attribut** gibt die Anzahl der zu übertragenden Arrayelemente an, und das **\[ erste \_ ist \]** das Attribut, das den Index des ersten zu übertragenden Arrayelements annimmt. Das **\[ attribut last \_ is \]** legt den Index des letzten zu übertragenden Arrayelements dar.

Der **\[** [**Schalter \_ ist**](/windows/desktop/Midl/switch-is) **\]** ein Feldattribut, das einen Union-Diskriminator bestimmt. Wenn die Union ein Prozedurparameter ist, muss der Union-Diskriminator ein anderer Parameter derselben Prozedur sein. Wenn die Union ein Feld einer Struktur ist, muss der Diskriminator ein anderes Feld der Struktur sein, das sich auf der gleichen Ebene wie das Union-Feld befindet. Der Diskriminator muss ein [**boolescher**](/windows/desktop/Midl/boolean), [**char-,**](/windows/desktop/Midl/char-idl) [**int-**](/windows/desktop/Midl/int)oder [**enum-Typ**](/windows/desktop/Midl/enum) oder ein Typ sein, der in einen dieser Typen aufgelöst wird. Weitere Informationen finden Sie unter [Nicht gekapselte Unions](/windows/desktop/Midl/nonencapsulated-unions) und **\[ Switch \_ \] ist**.

Das **\[** [](/windows/desktop/Midl/string) **\]** Zeichenfolgenfeldattribut legt fest, dass ein eindimensionales Zeichen oder Bytearray oder ein Zeiger auf ein null terminiertes Zeichen oder einen Bytestream als Zeichenfolge behandelt werden soll. Das Zeichenfolgenattribut gilt nur für eindimensionale Arrays und Zeiger. Der Elementtyp ist auf [**char,**](/windows/desktop/Midl/char-idl) [**byte,**](/windows/desktop/Midl/byte) [**wchar \_ t**](/windows/desktop/Midl/wchar-t)oder einen benannten Typ beschränkt, der in einen dieser Typen aufgelöst wird.

Informationen zum Kontext, in dem Feldattribute angezeigt werden, finden Sie unter [MIDL-Arrays,](/windows/desktop/Midl/midl-arrays) [MIDL-Strukturen](/windows/desktop/Midl/midl-structures)und [MIDL-Unions.](/windows/desktop/Midl/midl-unions)

 

 