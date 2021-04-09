---
title: Strukturen (RPC)
description: Beschreibung verschiedener Typen von Strukturen im Remote Prozedur Aufruf (RPC).
ms.assetid: edaf547d-d3d1-443c-93dd-8e036bc42944
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ccae91f703badd2e0153dfc3d8acff1ace562f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039335"
---
# <a name="structures-rpc"></a>Strukturen (RPC)

Es gibt mehrere Kategorien von Strukturen, die in Bezug auf die für das Marshalling erforderlichen Aktionen progressiv komplizierter sind. Sie beginnen mit einer einfachen Struktur, die als Ganzes blockiert werden kann, und fahren mit einer komplexen Struktur fort, bei der das Feld nach außen gewartet werden muss.

-   [Einfache Struktur](#simple-structure)
-   [Einfache Struktur mit Zeigern](#simple-structure-with-pointers)
-   [Konforme Struktur](#conformant-structure)
-   [Konforme Struktur mit Zeigern](#conformant-structure-with-pointers)
-   [Konforme unterschiedliche Struktur (mit oder ohne Zeiger)](#conformant-varying-structure-with-or-without-pointers)
-   [Harte Struktur](#hard-structure)
-   [Komplexe Struktur](#complex-structure)
-   [Beschreibung des Strukturmember-Layouts](#structure-member-layout-description)

> [!Note]  
> Im Vergleich zu Array Kategorien wird deutlich, dass nur Strukturen mit einer Größe von bis zu 64K beschrieben werden können (die Größe ist für den flachen Teil der Struktur), d. h. es gibt keine Entsprechung von SM-und LG-Arrays.

 

**Elemente, die von Strukturen gemeinsam sind**

-   **Richt**

    Die erforderliche Ausrichtung des Puffers vor dem Mars Hallen der-Struktur. Gültige Werte sind 0, 1, 3 und 7 (die tatsächliche Ausrichtung minus 1).

-   **Arbeitsspeicher \_ Größe**

    Größe der Struktur im Arbeitsspeicher in Bytes. für konforme Strukturen enthält diese Größe nicht die Größe des Arrays.

-   **\_Beschreibung für Offset zu \_ array \_**

    Offset vom aktuellen Format Zeichenfolgen-Zeiger auf die Beschreibung des konformen Arrays, das in einer-Struktur enthalten ist.

-   **Element \_ Layout**

    Beschreibung der einzelnen Elemente der Struktur. Die NDR-Routinen müssen diesen Teil der Format Zeichenfolge eines Typs nur untersuchen, wenn die Endian-Transformation erforderlich ist oder wenn der Typ eine komplexe Struktur ist.

-   **Zeiger \_ Layout**

    Weitere Informationen finden Sie im Abschnitt [Zeiger Layout](pointer-layout-tfs.md) .

## <a name="simple-structure"></a>Einfache Struktur

Eine einfache Struktur enthält nur Basis Typen, fixierte Arrays und andere einfache Strukturen. Die Hauptfunktion der einfachen Struktur ist, dass Sie als Ganzes blockiert werden kann.

``` syntax
FC_STRUCT alignment<1> 
memory_size<2> 
member_layout<> 
FC_END
```

## <a name="simple-structure-with-pointers"></a>Einfache Struktur mit Zeigern

Eine einfache Struktur mit Zeigern enthält nur Basis Typen, Zeiger, fixierte Arrays, einfache Strukturen und andere einfache Strukturen mit Zeigern. Da das Layout<> nur bei einer Endianess-Konvertierung besucht werden muss, wird es am Ende der Beschreibung platziert.

``` syntax
FC_PSTRUCT alignment<1> 
memory_size<2> 
pointer_layout<> 
member_layout<> 
FC_END
```

## <a name="conformant-structure"></a>Konforme Struktur

Eine konforme Struktur enthält nur Basis Typen, fixierte Arrays und einfache Strukturen und muss entweder eine konforme Zeichenfolge oder ein konformes Array enthalten. Dieses Array könnte sich in einer anderen konformen Struktur oder einer konformen Struktur mit Zeigern befinden, die in diese Struktur eingebettet sind.

``` syntax
FC_CSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
member_layout<> 
FC_END
```

## <a name="conformant-structure-with-pointers"></a>Konforme Struktur mit Zeigern

Eine konforme Struktur mit Zeigern enthält nur Basis Typen, Zeiger, fixierte Arrays, einfache Strukturen und einfache Strukturen mit Zeigern. eine konforme Struktur muss ein konformes Array enthalten. Dieses Array könnte sich in einer anderen konformen Struktur oder einer Übereinstimmung mit in dieser Struktur eingebetteten Zeigern befinden.

``` syntax
FC_CPSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
pointer_layout<> 
member_layout<> FC_END
```

## <a name="conformant-varying-structure-with-or-without-pointers"></a>Konforme unterschiedliche Struktur (mit oder ohne Zeiger)

Eine konforme, unterschiedliche Struktur enthält nur einfache Typen, Zeiger, fixierte Arrays, einfache Strukturen und einfache Strukturen mit Zeigern. eine konforme, unterschiedliche Struktur muss entweder eine konforme Zeichenfolge oder ein konforme Array enthalten. Die konforme Zeichenfolge oder das Array kann in einer anderen konformen Struktur oder einer konformen Struktur mit Zeigern enthalten sein, die in diese Struktur eingebettet sind.

``` syntax
FC_CVSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
[pointer_layout<>] 
layout<> 
FC_END
```

## <a name="hard-structure"></a>Harte Struktur

Die feste Struktur war ein Konzept, das auf die Vermeidung von schweren Strafen im Zusammenhang mit der Verarbeitung komplexer Strukturen abzielt. Sie wird von einer Beobachtung abgeleitet, dass eine komplexe Struktur in der Regel nur eine oder zwei Bedingungen hat, die das Kopieren von Blöcken verhindern und somit die Leistung im Vergleich zu einer einfachen Struktur beeinträchtigen. Die Übeltäter sind in der Regel Unions oder enumerationsfelder.

Eine feste Struktur ist eine Struktur, die über eine enum16, einen endleerraum im Arbeitsspeicher oder eine Union als letzten Member verfügt. Diese drei Elemente verhindern, dass die Struktur in eine der vorherigen Struktur Kategorien fällt, bei denen ein geringer Interpretations Aufwand und ein maximales Optimierungspotenzial auftreten, aber nicht in der sehr kostspieligen komplexen Struktur Kategorie erzwungen werden.

Der enum16 darf nicht bewirken, dass sich die Arbeitsspeicher-und Netzwerkgröße der Struktur unterscheiden. Die Struktur darf weder ein konformes Array noch einen Zeiger enthalten (es sei denn, ein Teil der Union); die einzigen zulässigen Member sind Basis Typen, fixierte Arrays und einfache Strukturen.

``` syntax
FC_HARD_STRUCTURE alignment<1> 
memory_size<2> 
reserved<4> 
enum_offset<2> 
copy_size<2> 
mem_copy_incr<2> 
union_description_offset<2>
member_layout<> 
FC_END
```

Das Enumeration \_ Offset<2> Feld gibt den Offset vom Anfang der Struktur im Arbeitsspeicher zu einem enum16 an, wenn es einen enthält. andernfalls ist der Enumeration- \_ Offset<2> Feld – 1.

Im \_ Feld kopiergröße<2> wird die Gesamtzahl der Bytes in der Struktur angezeigt, die in den bzw. aus dem Puffer in den Puffer kopiert werden kann. Diese Summe umfasst weder eine nachfolgende Union noch einen Endabstand im Speicher. Dieser Wert ist auch der Betrag, um den der Puffer Zeiger nach der Kopie inkrementiert werden soll.

Das Feld für die<der Arbeits \_ \_ Speicher-2> ist die Anzahl der Bytes, die der Speicher Zeiger nach dem Block Kopiervorgang erhöht werden soll, bevor eine nachfolgende Union verarbeitet wird. Das Inkrementieren um diesen Betrag (nicht nach Kopier \_ Größe<2> Bytes) ergibt einen korrekten Speicher Zeiger auf jede nachfolgende Union.

## <a name="complex-structure"></a>Komplexe Struktur

Eine komplexe Struktur ist jede Struktur, die ein oder mehrere Felder enthält, die entweder verhindern, dass die Struktur blockiert wird, oder für die während des Marshalling oder Unmarshalling eine zusätzliche Überprüfung durchgeführt werden muss (z. b. gebundene Prüfungen auf eine Enumeration). Die folgenden NDR-Typen fallen in diese Kategorie:

-   [einfache Typen](simple-types-tfs.md): ENUM16, \_ \_ INT3264 (nur auf 64-Bit-Plattformen), eine Ganzzahl mit dem \[ [ **Bereich**](/windows/desktop/Midl/range)\]
-   Ausrichtungs Abstände am Ende der Struktur
-   Schnittstellen Zeiger (Sie verwenden einen eingebetteten komplexen)
-   ignorierte Zeiger (die sich auf das \[ [**Ignore**](/windows/desktop/Midl/ignore) \] -Attribut und das FC- \_ ignoriertoken beziehen)
-   komplexe Arrays, unterschiedliche Arrays, Zeichen folgen Arrays
-   Mehrdimensionale konforme Arrays mit mindestens einer nicht fixierten Dimension
-   Unions
-   Elemente, die mit "über \[ [**tragen \_ als**](/windows/desktop/Midl/transmit-as)" definiert \] sind, \[ [**darstellen \_ als**](/windows/desktop/Midl/represent-as) \] , \[ [**Wire \_ Marshal**](/windows/desktop/Midl/wire-marshal) \] , \[ [**User \_ Marshal**](/windows/desktop/Midl/user-marshal)\]
-   eingebettete komplexe Strukturen
-   Auffüllen am Ende der Struktur

Eine komplexe Struktur hat die folgende Formatbeschreibung:

``` syntax
FC_BOGUS_STRUCT alignment<1> 
memory_size<2> 
offset_to_conformant_array_description<2> 
offset_to_pointer_layout<2> 
member_layout<> 
FC_END 
[pointer_layout<>]
```

Die Arbeitsspeicher \_ Größe<2> Feld ist die Größe der Struktur im Arbeitsspeicher in Bytes.

Wenn die Struktur ein konformes Array enthält, gibt die Offset \_ \_ - \_ zu \_ -konform-Array Beschreibung<2> Feld den Offset der Beschreibung des konformen Arrays an; andernfalls ist Sie 0 (null).

Wenn die Struktur Zeiger enthält, stellt das \_ \_ Layout zum Zeiger \_ Layout<2> Feld den Offset hinter dem Layout der Struktur für das Zeiger Layout bereit. andernfalls ist dieses Feld NULL.

Das Zeiger \_ Layout<> Feld einer komplexen Struktur wird etwas anders behandelt als bei anderen Strukturen. Das Zeiger \_ Layout<> -Feld einer komplexen Struktur enthält nur Beschreibungen der tatsächlichen Zeiger Felder in der Struktur selbst. Alle Zeiger, die in eingebetteten Arrays, Unions oder Strukturen enthalten sind, werden nicht im Feld Zeiger Layout<> der komplexen Struktur beschrieben \_ .

> [!Note]  
> Dies steht im Gegensatz zu anderen-Strukturen, die die Beschreibung von Zeigern duplizieren, die in eingebetteten Arrays oder Strukturen in Ihrem eigenen Zeiger \_ Layout<> Feld enthalten sind.

 

Das Format des Zeiger Layouts einer komplexen Struktur ist ebenfalls völlig unterschiedlich. Da es nur Beschreibungen der tatsächlichen Zeiger Elemente enthält und eine komplexe Struktur gemarshallt wird und ein Feld gleichzeitig gemarshallt wird, enthält das Zeiger \_ Layout<> Feld einfach die Zeiger Beschreibung aller Zeiger Elemente. Es gibt keine beginnende FC \_ -PP und keines der üblichen Zeiger \_ Layouts<> Informationen.

## <a name="structure-member-layout-description"></a>Beschreibung des Strukturmember-Layouts

Die layoutbeschreibung einer Struktur enthält mindestens eines der folgenden Formatzeichen:

-   Eines der Basistyps, wie z. b. FC \_ Char, usw.
-   Ausrichtungs Direktiven. Es gibt drei Formatzeichen, die die Ausrichtung des Speicher Zeigers angeben: FC \_ ALIGNM2, FC \_ ALIGNM4 und FC \_ ALIGNM8.
    > [!Note]  
    > Es gibt auch Puffer Ausrichtungs Token, FC \_ ALIGNB2 bis FC \_ ALIGNM8; diese werden nicht verwendet.

     

-   Arbeitsspeicher Auffüll Zeichen. Diese treten nur am Ende der Beschreibung einer Struktur auf und geben die Anzahl von Byte Auffüll Zeichen im Arbeitsspeicher vor dem konformen Array in der Struktur an: FC \_ structpadn, wobei n für die Anzahl der Byte Auffüll Zeichen steht.
-   Alle eingebetteten nicht-Basistyps (Beachten Sie jedoch, dass im Struktur Layout nie ein konformes Array auftritt). Dies hat eine 4-Byte-Beschreibung:

    ``` syntax
    FC_EMBEDDED_COMPLEX memory_pad<1> 
    offset_to_description<2>,
    ```

    , wenn der Offset nicht garantiert 2-Byte-ausgerichtet ist.

    \_das Speicher Pad<1> ist ein Abstand, der im Arbeitsspeicher vor dem komplexen Feld benötigt wird.

    Offset \_ zu \_ Beschreibung<2> ist ein relativer typoffset zum eingebetteten Typ.

Es kann auch ein FC \_ -Pad vor dem abschließenden FC-Ende vorhanden sein \_ , um sicherzustellen, dass die Format Zeichenfolge an einer 2-Byte-Grenze nach dem FC-Ende ausgerichtet wird \_ .

 

 