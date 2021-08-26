---
title: Strukturen (RPC)
description: Beschreibung der verschiedenen Typen von Strukturen im Remoteprozeduraufruf (RPC).
ms.assetid: edaf547d-d3d1-443c-93dd-8e036bc42944
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1783508a834ce2fa3d93d3db04edc1de362d6f888c29511c1eb6852cce0e83ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017410"
---
# <a name="structures-rpc"></a>Strukturen (RPC)

Es gibt mehrere Kategorien von Strukturen, die im Hinblick auf aktionen, die für das Marshalling erforderlich sind, progressiv komplizierter werden. Sie beginnen mit einer einfachen Struktur, die als Ganzes blockkopiert werden kann, und fahren mit einer komplexen Struktur fort, die feldweise gewartet werden muss.

-   [Einfache Struktur](#simple-structure)
-   [Einfache Struktur mit Zeigern](#simple-structure-with-pointers)
-   [Konforme Struktur](#conformant-structure)
-   [Konforme Struktur mit Zeigern](#conformant-structure-with-pointers)
-   [Konforme unterschiedliche Struktur (mit oder ohne Zeiger)](#conformant-varying-structure-with-or-without-pointers)
-   [Hard Structure](#hard-structure)
-   [Komplexe Struktur](#complex-structure)
-   [Beschreibung des Strukturmemberlayouts](#structure-member-layout-description)

> [!Note]  
> Im Vergleich zu Arraykategorien wird deutlich, dass nur Strukturen mit einer Größe von bis zu 64.000 beschrieben werden können (die Größe ist für den flachen Teil der Struktur), dass es keine Entsprechung von SM- und LG-Arrays gibt.

 

**Elemente, die strukturenverbreitet sind**

-   **Ausrichtung**

    Die erforderliche Ausrichtung des Puffers, bevor dasMarshaling der Struktur aufheben wird. Gültige Werte sind 0, 1, 3 und 7 (die tatsächliche Ausrichtung minus 1).

-   **\_Arbeitsspeichergröße**

    Größe der Struktur im Arbeitsspeicher in Bytes; für konforme Strukturen enthält diese Größe nicht die Größe des Arrays.

-   **\_Offset zu \_ \_ Arraybeschreibung**

    Offset vom aktuellen Formatzeichenfolgenzeiger zur Beschreibung des konformen Arrays, das in einer -Struktur enthalten ist.

-   **\_Elementlayout**

    Beschreibung der einzelnen Elemente der -Struktur. Die NDR-Routinen müssen diesen Teil der Formatzeichenfolge eines Typs nur untersuchen, wenn eine Endiantransformation erforderlich ist oder der Typ eine komplexe Struktur ist.

-   **\_Zeigerlayout**

    Weitere Informationen finden Sie im Abschnitt [Zeigerlayout.](pointer-layout-tfs.md)

## <a name="simple-structure"></a>Einfache Struktur

Eine einfache Struktur enthält nur Basistypen, feste Arrays und andere einfache Strukturen. Das Hauptmerkmal der einfachen Struktur ist, dass sie als Ganzes blockkopiert werden kann.

``` syntax
FC_STRUCT alignment<1> 
memory_size<2> 
member_layout<> 
FC_END
```

## <a name="simple-structure-with-pointers"></a>Einfache Struktur mit Zeigern

Eine einfache Struktur mit Zeigern enthält nur Basistypen, Zeiger, feste Arrays, einfache Strukturen und andere einfache Strukturen mit Zeigern. Da das Layout<> nur bei einer Endianess-Konvertierung besucht werden muss, wird es am Ende der Beschreibung platziert.

``` syntax
FC_PSTRUCT alignment<1> 
memory_size<2> 
pointer_layout<> 
member_layout<> 
FC_END
```

## <a name="conformant-structure"></a>Konforme Struktur

Eine konforme Struktur enthält nur Basistypen, feste Arrays und einfache Strukturen und muss entweder eine konforme Zeichenfolge oder ein konformes Array enthalten. Dieses Array kann tatsächlich in einer anderen konformen Struktur oder konformen Struktur mit Zeigern enthalten sein, die in diese Struktur eingebettet sind.

``` syntax
FC_CSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
member_layout<> 
FC_END
```

## <a name="conformant-structure-with-pointers"></a>Konforme Struktur mit Zeigern

Eine konforme Struktur mit Zeigern enthält nur Basistypen, Zeiger, feste Arrays, einfache Strukturen und einfache Strukturen mit Zeigern. Eine konforme Struktur muss ein konformes Array enthalten. Dieses Array kann tatsächlich in einer anderen konformen Struktur oder konformen Struktur mit Zeigern enthalten sein, die in diese Struktur eingebettet sind.

``` syntax
FC_CPSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
pointer_layout<> 
member_layout<> FC_END
```

## <a name="conformant-varying-structure-with-or-without-pointers"></a>Konforme unterschiedliche Struktur (mit oder ohne Zeiger)

Eine konforme unterschiedliche Struktur enthält nur einfache Typen, Zeiger, feste Arrays, einfache Strukturen und einfache Strukturen mit Zeigern. Eine konforme, unterschiedliche Struktur muss entweder eine konforme Zeichenfolge oder ein array mit unterschiedlichen Übereinstimmungen enthalten. Die konforme Zeichenfolge oder das Array kann tatsächlich in einer anderen konformen Struktur oder konformen Struktur mit Zeigern enthalten sein, die in diese Struktur eingebettet sind.

``` syntax
FC_CVSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
[pointer_layout<>] 
layout<> 
FC_END
```

## <a name="hard-structure"></a>Hard Structure

Die harte Struktur war ein Konzept, das darauf abzielte, harte Nachteile im Zusammenhang mit der Verarbeitung komplexer Strukturen zu beseitigen. Sie wird aus einer Beobachtung abgeleitet, dass eine komplexe Struktur in der Regel nur eine oder zwei Bedingungen aufweist, die blockkopieren und daher ihre Leistung im Vergleich zu einer einfachen Struktur verbessern. Die Ursache sind in der Regel Unions oder Enumerationsfelder.

Eine harte Struktur ist eine -Struktur, die eine Enumeration16, eine Endauffüllung im Arbeitsspeicher oder eine Union als letztes Element aufweist. Diese drei Elemente verhindern, dass die Struktur in eine der vorherigen Strukturkategorien fällt, die einen geringen Interpretationsaufwand und ein maximales Optimierungspotenzial haben, sie jedoch nicht in die sehr kostspielige komplexe Strukturkategorie zwingen.

enum16 darf nicht dazu führen, dass sich die Speicher- und Kabelgrößen der Struktur unterscheiden. Die Struktur darf weder ein konformes Array noch Zeiger haben (es sei denn, sie ist Teil der Union). Die einzigen anderen zulässigen Member sind Basistypen, feste Arrays und einfache Strukturen.

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

Der \_ Enumerationsoffset<2> Felds stellt den Offset vom Anfang der Struktur im Arbeitsspeicher zu einer Enumeration16 bereit, wenn sie eine enthält. Andernfalls ist der \_ Enumerationsoffset<2> Feld –1.

Die \_ Kopiergröße<2> Felds gibt die Gesamtzahl der Bytes in der Struktur an, die vom Block in den Puffer kopiert werden können. Diese Summe umfasst weder eine nachfolgende Union noch eine Endauffüllung im Arbeitsspeicher. Dieser Wert ist auch die Menge, in der der Pufferzeiger nach der Kopie erhöht werden soll.

Das Feld mem \_ copy \_ incr<2> ist die Anzahl der Bytes, die der Speicherzeiger nach dem Blockkopiervorgang erhöht werden soll, bevor eine nachfolgende Union verarbeitet wird. Das Erhöhen um diesen Betrag (nicht durch die \_ Kopiergröße<2> Bytes) ergibt einen ordnungsgemäßen Speicherzeiger auf alle nachgestellten Unionen.

## <a name="complex-structure"></a>Komplexe Struktur

Eine komplexe Struktur ist jede Struktur, die ein oder mehrere Felder enthält, die entweder verhindern, dass die Struktur blockkopiert wird, oder für die während des Marshallings oder Desmarshalings zusätzliche Überprüfungen durchgeführt werden müssen (z. B. gebundene Überprüfungen für eine Enumeration). Die folgenden NDR-Typen fallen in diese Kategorie:

-   [einfache Typen:](simple-types-tfs.md)ENUM16, \_ \_ INT3264 (nur auf 64-Bit-Plattformen), ein integraler \[ [ **Mit-Bereich**](/windows/desktop/Midl/range)\]
-   Ausrichtungsabstand am Ende der Struktur
-   Schnittstellenzeiger (sie verwenden einen eingebetteten komplexen )
-   ignorierte Zeiger (die sich auf das Ignorieren von \[ [](/windows/desktop/Midl/ignore) \] Attributen und FC \_ IGNORE-Token beziehen)
-   komplexe Arrays, unterschiedliche Arrays, Zeichenfolgenarrays
-   Mehrdimensionale konforme Arrays mit mindestens einer nicht fixierten Dimension
-   Unions
-   -Elemente, die mit Als übertragen definiert \[ [**\_**](/windows/desktop/Midl/transmit-as) \] \[ [**sind, stellen \_ als**](/windows/desktop/Midl/represent-as) \] , \[ [**Wire \_ Marshal**](/windows/desktop/Midl/wire-marshal) \] , User \[ [**\_ Marshal**](/windows/desktop/Midl/user-marshal) dar.\]
-   Eingebettete komplexe Strukturen
-   Auffüllen am Ende der Struktur

Eine komplexe Struktur weist die folgende Formatbeschreibung auf:

``` syntax
FC_BOGUS_STRUCT alignment<1> 
memory_size<2> 
offset_to_conformant_array_description<2> 
offset_to_pointer_layout<2> 
member_layout<> 
FC_END 
[pointer_layout<>]
```

Die \_ Arbeitsspeichergröße<2> Feld entspricht der Größe der Struktur im Arbeitsspeicher in Bytes.

Wenn die Struktur ein konformes Array enthält, stellt der Offset zur Beschreibung des \_ \_ konformen \_ \_ Arrays<2> Feld den Offset zur Beschreibung des konformen Arrays bereit, andernfalls 0 (null).

Wenn die Struktur Zeiger aufweist, stellt der Offset \_ zum \_ \_ Zeigerlayout<2> Feld den Offset über das Layout der Struktur zum Zeigerlayout bereit, andernfalls ist dieses Feld 0 (null).

Das \_ Zeigerlayout<> Feld einer komplexen Struktur wird etwas anders behandelt als bei anderen Strukturen. Das \_ Zeigerlayout<> Feld einer komplexen Struktur enthält nur Beschreibungen der tatsächlichen Zeigerfelder in der Struktur selbst. Zeiger, die in eingebetteten Arrays, Unions oder Strukturen enthalten sind, werden im Zeigerlayout der komplexen Struktur<> Feld nicht \_ beschrieben.

> [!Note]  
> Dies steht im Gegensatz zu anderen -Strukturen, die die Beschreibung aller Zeiger duplizieren, die in eingebetteten Arrays oder Strukturen in ihrem eigenen Zeigerlayout<> Feld enthalten \_ sind.

 

Das Format des Zeigerlayouts einer komplexen Struktur unterscheidet sich ebenfalls grundlegend. Da es nur Beschreibungen der tatsächlichen Zeigermember enthält und eine komplexe Struktur jeweils ein Feld gemarshallt und nicht gemarshallt wird, enthält das \_ Zeigerlayout<> Feld einfach die Zeigerbeschreibung aller Zeigermember. Es gibt keine FC \_ PP-Anfangs- und keines der üblichen \_ Zeigerlayouts<> Informationen.

## <a name="structure-member-layout-description"></a>Beschreibung des Strukturmemberlayouts

Die Layoutbeschreibung einer Struktur enthält mindestens eines der folgenden Formatzeichen:

-   Eines der Basistypzeichen, z. B. FC \_ CHAR usw.
-   Ausrichtungsdirektiven. Es gibt drei Formatzeichen, die die Ausrichtung des Arbeitsspeicherzeigers angeben: FC \_ ALIGNM2, FC \_ ALIGNM4 und FC \_ ALIGNM8.
    > [!Note]  
    > Es gibt auch Pufferausrichtungstoken, FC \_ ALIGNB2 bis FC \_ ALIGNM8; diese werden nicht verwendet.

     

-   Speicherauffüllung. Diese treten nur am Ende der Beschreibung einer Struktur auf und geben die Anzahl der Bytes der Auffüllung im Arbeitsspeicher vor dem konformen Array in der Struktur an: FC \_ STRUCTPADn, wobei n die Anzahl der Bytes der Auffüllung ist.
-   Alle eingebetteten Nichtbasistypen (beachten Sie jedoch, dass im Strukturlayout nie ein konformes Array auftritt). Dies weist eine 4-Byte-Beschreibung auf:

    ``` syntax
    FC_EMBEDDED_COMPLEX memory_pad<1> 
    offset_to_description<2>,
    ```

    , wobei nicht garantiert wird, dass der Offset 2 Byte ausgerichtet ist.

    Speicherpad \_<1> ist eine Auffüllung, die im Arbeitsspeicher vor dem komplexen Feld benötigt wird.

    Offset \_ zur Beschreibung<\_ 2> ist ein relativer Typoffset zum eingebetteten Typ.

Es kann auch ein \_ FC-PAD vor dem beendenden \_ FC-ENDE vorhanden sein, wenn dies erforderlich ist, um sicherzustellen, dass die Formatzeichenfolge an einer 2-Byte-Grenze nach dem FC-ENDE ausgerichtet \_ wird.

 

 