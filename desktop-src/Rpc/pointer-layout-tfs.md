---
title: Zeigerlayout
description: Zeigerlayout beschreibt Zeiger einer Struktur oder eines Arrays.
ms.assetid: 1a4984c1-97b9-4e95-a17e-851b67fa94a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6616cc7d1000b042c6039b2abf3f79d4900cd0e5fadac748881666610b139c57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019192"
---
# <a name="pointer-layout"></a>Zeigerlayout

Zeigerlayout beschreibt Zeiger einer Struktur oder eines Arrays.

## <a name="pointer_layout"></a>Zeigerlayout \_<>

Ein \_ Zeigerlayout<> Feld besteht aus den Formatzeichen FC \_ PP FC \_ PAD, gefolgt von einer oder mehreren Zeigerbeschreibungen, wie weiter unten beschrieben, und endet mit einem FC \_ END-Formatzeichen:

``` syntax
FC_PP
FC_PAD
{ pointer_instance_layout<> }*
FC_END
```

Ein \_ \_ Zeigerinstanzlayout<> Feld ist eine Formatzeichenfolge, die einzelne oder mehrere Instanzen von Zeigern beschreibt. Die folgenden Felder werden in diesen Deskriptoren verwendet:

-   Offset \_ im \_ Arbeitsspeicher

    Der Offset mit Vorzeichen zur Position des Zeigers im Arbeitsspeicher. Bei einem Zeiger, der sich in einer -Struktur befindet, ist dieser Offset ein negativer Offset vom Ende der Struktur (das Ende des nicht konformen Teils konformer Strukturen). bei Arrays ist der Offset vom Anfang des Arrays.

-   Offset \_ im \_ Puffer

    Der Offset mit Vorzeichen zur Position des Zeigers im Puffer. Bei einem Zeiger, der sich in einer -Struktur befindet, ist dieser Offset ein negativer Offset vom Ende der Struktur (das Ende des nicht konformanten Teils konformer Strukturen): Bei Arrays ist der Offset vom Anfang des Arrays.

-   Offset \_ zu \_ Array

    Offset von einer einschließenden Struktur zu dem eingebetteten Array, dessen Zeiger behandelt werden. Bei Arrays der obersten Ebene ist dieses Feld immer 0 (null).

-   Iterationen

    Gesamtzahl der Zeiger, die das gleiche Layout aufweisen,<> beschrieben.

-   increment

    Inkrementieren zwischen aufeinander folgenden Zeigern während eines REPEAT-Vorgangs.

-   Anzahl \_ der \_ Zeiger

    Anzahl verschiedener Zeiger in einer Wiederholungsinstanz.

-   \_Zeigerbeschreibung

    Zeigerbeschreibung.

Alle Zeigerinstanzlayouts verwenden die folgende Einzelzeigerinstanz \_<8>:

``` syntax
offset_to_pointer_in_memory<2> 
offset_to_pointer_in_buffer<2> 
pointer_description<4>
```

Es folgen Instanzdeskriptoren:

**Einzelne Instanz eines Zeigers auf einen einfachen Typ:**

``` syntax
FC_NO_REPEAT FC_PAD 
pointer_instance<8>
```

**Wiederholungszeiger korrigiert:**

``` syntax
FC_FIXED_REPEAT FC_PAD 
iterations<2> 
increment<2> 
offset_to_array<2> 
number_of_pointers<2>
{ pointer_instance<8> }*
```

**Variabler Wiederholungszeiger:**

``` syntax
FC_VARIABLE_REPEAT (FC_FIXED_OFFSET | FC_VARIABLE_OFFSET) 
increment<2> 
offset_to_array<2> 
number_of_pointers<2> 
{ pointer_instance<8> }*
```

Für feste Repeat- und Variable Repeat-Zeigerinstanzen gibt es eine Reihe von Offset- und Zeigerbeschreibungen für jeden Zeiger in der Wiederholungsinstanz.

## <a name="pointers-layout-design-issues"></a>Layoutentwurfsprobleme bei Zeigern

In diesem Abschnitt werden Probleme im Zusammenhang mit der Verarbeitung konformer Strukturen und eingebetteter Zeiger behandelt. Das Problem besteht darin, dass der Compiler Zeigerlayouts für Strukturen und Arrays mit einiger Redundanz generiert. Dies ist von Vorteil, da die Informationen nützlich sind und daher beispielsweise eine konforme Struktur ein Zeigerlayout durchgehen kann, um alle Zeiger aus der Struktur und aus dem konformen Array zu bedienen, das Teil der konformen Struktur ist. Es gibt jedoch einige eingebettete Situationen, in denen die NDR-Engine zusätzliche Aufgaben ausführen muss, um alle Zeigerlayouts in der richtigen Sequenz zu verarbeiten und jeden Zeiger genau einmal zu verarbeiten.

## <a name="what-the-compiler-generates"></a>Was der Compiler generiert

Jedes in diesem Abschnitt erläuterte Objekt verfügt über Zeiger, sodass beispielsweise eine konforme Struktur Zeiger im Strukturteil sowie in den Arrayelementen enthält. Das -Element ist eine einfache -Struktur mit einem Zeiger.

1.  Konforme Struktur, einzelne Ebene

    Der konforme Deskriptor verfügt über einen PP-Teil, in dem alle Zeiger sowohl aus der Struktur als auch aus dem Array beschrieben werden. Die Memberliste enthält FC \_ LONG anstelle eines Zeigers. Der CARRAY-Arraydeskriptor verfügt über Elemente durch die Verwendung eines eingebetteten \_ komplexen und überhaupt keine Zeigerdeskriptoren. Das Element verfügt weiterhin über einen einzelnen Zeigerdeskriptor. Zeigerlayout steht vor dem Elementlayout in einer konformen Struktur und einfachen Strukturdeskriptoren.

2.  Konforme Struktur, zwei oder mehr Ebenen

    Die PP-Beschreibung enthält Zeiger von allen Ebenen. Es verwendet dieselbe Arraybeschreibung wie die interne konforme Struktur. Die Memberliste enthält FC \_ LONG anstelle eines Zeigers. Eine eingebettete Struktur wird durch die Verwendung eines eingebetteten komplexen -Komplexes bezeichnet. Der konforme Strukturdeskriptor wird wie benutzbar wiederverwendet. Die Größe des flachen Teils der -Struktur ist ebenfalls vollständig. Dies bedeutet, dass die Strukturgröße der obersten Ebene die Flachgröße der eingebetteten Struktur enthalten würde.

3.  Komplexe Struktur, einzelne Ebene

    Zeigermember werden durch FC \_ POINTER markiert. Das Zeigerlayout ist so vereinfacht, dass für jeden FC POINTER-Eintrag in der Liste ein Zeigerdeskriptor (4 Bytes) vorhanden \_ ist. Das Zeigerlayout wird parallel zu einer Memberbegehung ausgeführt, d. h., ein FC POINTER bewirkt, dass \_ die nächste Zeigerbeschreibung verarbeitet wird. Das CARRAY-Array verfügt über ein Zeigerlayout mit allen Deskriptoren des Arrays und dann mithilfe eines eingebetteten komplexen Elements. Der Elementdeskriptor wird wiederverwendet. Die Größe des flachen Teils der Struktur ist abgeschlossen. Mit anderen Worten: Die Flachgröße der Struktur der obersten Ebene schließt die Flachgröße der eingebetteten Struktur ein. Das Elementlayout ist dem Zeigerlayout für komplexe Strukturen vorangestellt.

    Daher unterscheidet sich die Generierung konformer Arraybeschreibungen, je nachdem, ob es sich um ein Array innerhalb einer konformen Struktur oder innerhalb einer komplexen Struktur handelt.

4.  Komplexe Struktur, 2 oder mehr Ebenen, komplex in komplex

    Die komplexe Struktur der obersten Ebene verfügt über Memberzeiger, die eingebettete komplexe Struktur über ihre Memberzeiger. Der konforme Strukturdeskriptor wird wiederverwendet. Der Arraydeskriptor von oben ist das wiederverwendete Array aus der eingebetteten Struktur.

5.  Komplexe Struktur mit eingebetteter konformer Struktur

    Die konforme Struktur der obersten Ebene verfügt über Memberzeiger. Der konforme Strukturdeskriptor wird wie benutzbar wiederverwendet. Der Arraydeskriptor wird aus der eingebetteten konformen Struktur wiederverwendet. Mit anderen Worten, es weist keine Zeiger auf den Arraydeskriptor auf. Das Element verfügt über einen Zeigerdeskriptor.

6.  Arrays von Strukturen mit Zeigern

    Ein Array einfacher Strukturen mit Zeigern wird als SMFARRAY oder CARRAY generiert, je nachdem, ob das Array dimensioniert ist, aber in beiden Fällen verfügt es über ein Zeigerlayout, das vollständig ist (FIXED \_ REPEAT oder VARIABLE \_ REPEAT). Das Zeigerlayout steht vor dem Elementlayout.

    Ein Array komplexer Strukturen mit Zeigern wird als BOGUS ARRAY generiert, \_ unabhängig davon, ob es festgelegt oder dimensioniert ist und in beiden Fällen über kein Zeigerlayout verfügt.

## <a name="what-the-ndr-engine-does"></a>Leistung der NDR-Engine

In diesem Abschnitt wird das Verhalten der NDR-Engine beschrieben.

**Der Marshallingdurchlauf**

1.  Konforme Strukturen und eingebettete konforme Strukturen.

    Die Struktur der obersten Ebene verhält sich wie eine Struktur auf einer einzelnen Ebene.

2.  Eingebettete komplexe Struktur mit konformen Arrays

    Jede komplexe Struktur erzwingt, dass die äußere Struktur eine komplexe Struktur ist. Eingebettete Strukturen marshallen ihr Array nie. Jede Struktur durchläuft immer eingebettete Zeiger, indem einfach Member gemarshallt werden und ein Member ein FC \_ POINTER ist.

3.  Komplexe Struktur mit konformer Struktur

    Die oberste eingebettete konforme Struktur marshallt das konforme Array und alle Pointees. Die NDR-Engine stürzt niemals zu tiefer geschachtelten konformen Strukturen ab, sofern vorhanden. dies vereinfacht die Lösung, da eine konforme Struktur ein Blattobjekt im Hinblick auf das Marshalling eingebetteter Objekte ist. Die komplexe Struktur der obersten Ebene überspringt das Marshalling des Arrays.

**Aufheben desMarshalings, Auffüllens und Freigebens von Läufen**

Unmarshaling ist symmetrisch zum Marshalling. Der erste Vorgang, der für komplexe Strukturen ausgeführt wird, besteht darin, die Position der Pointees im Puffer durch Aufrufen der **NdrComplexStructBufferSize-Funktion** zu ermitteln. Anschließend werden pointes parallel entmarshalsiert, sodass das gleiche Schema für die korrekte Verwendung der Pointees entmarshalingt werden kann. Es sollte keine Verwirrung hinsichtlich der Größe von Objekten und Unions bestehen. Das Speicherbild sollte nicht nur für den Pufferinhalt für Objekte und Unions verwendet werden, deren Größe festgelegt ist.

Die Flags, die zum ordnungsgemäßen Marshalling und Aufheben des Marshallings verwendet werden, werden auf die gleiche Weise beim Auffüllen und Freigeben verwendet, um sicherzustellen, dass Pointees genau einmal ausgeführt werden.

**Endianesspass**

Zunächst ähnelt der Endianess-Pass dem Marshalling/Unmarshaling. zwei Durchläufe sind erforderlich, um komplexe Strukturen zu verarbeiten. Der erste Durchlauf konvertiert den flachen Teil und sucht die Position der Pointees im Puffer, ähnlich wie bei der Füllung dieses Vorgangs zum Aufheben desMarshalings. Der zweite Durchlauf konvertiert dann die Pointees.

Endianessdurchläufe unterscheiden sich wie folgt: Jede Struktur und jedes Element muss abgestuft werden, bis der Blattmember oder das Element ein einfacher Typ ist. Dies unterscheidet sich vom Unmarshaling. In unmarshaling ist es beispielsweise nie erforderlich, konforme Strukturen zu verarbeiten, die in konforme Strukturen eingebettet sind, oder ein beliebiges Element der konformen Struktur. Ein weiteres Problem besteht darin, dass die Konvertierung kein idempotenter Vorgang ist. Daher kann der Unmarshalingdurchlauf das Unmarshaling einiger Teile ohne Schaden wiederholen, während die Konvertierung ausschließlich einmal pro beliebigem einfachen Typ durchgeführt werden muss.

Daher kann der Endianess-Algorithmus wie folgt zusammengefasst werden. NDR verfügt über ein Konzept der konformen Struktur der obersten Ebene und ein Flag, um dies entsprechend zu kennzeichnen. Beim ersten Durchgehen, z. B. um den flachen Teil zu konvertieren und die Position der Zeiger zu erhalten, wird dieses Konzept nicht verwendet. NDR würde durch die flachen Teile aller Ebenen von Strukturen absteigen und nie in die Zeigerverarbeitung übersteigen. Schließlich würde NDR das Array auf oberster Ebene flach konvertieren.

Beim zweiten Durchgang wird das -Flag verwendet, um den Pass des eingebetteten Zeigers zu markieren, um zu vermeiden, dass tiefere Ebenen der konformen Strukturen und dann die am häufigsten konforme Struktur eintreten. Auf diese Weise würde das Flag das allgemeine Marshalling-/Unmarshalingverhalten erzwingen, wodurch vermieden wird, dass in tiefere Ebenen von konformen Strukturen absteigend.

Der zweite Durchgang für komplexe Strukturen mit konformen Arrays funktioniert wie folgt: Die komplexen Strukturen funktionieren wie folgt. Dies bedeutet, dass tiefere Ebenen niemals ihre konforme Größe oder ihre konformen Arrays betrachten oder überspringen würden und stattdessen einfach ihre Member durchlassen würden, ohne das Array zu berühren.

Bei komplexen Strukturen mit konformen Strukturen muss die konforme Struktur wissen, ob sie sich auf der obersten Ebene befindet und sich in einer komplexen Struktur befindet. Der flache Teil des Arrays wird von der am häufigsten konformen -Struktur verarbeitet. Im zweiten Durchgang würde die oberste konforme Struktur den flachen Teil überspringen und das Zeigerlayout durchgehen und zurückgeben. Die oberste komplexe Struktur würde ihren flachen Teil überspringen und auch das Zeigerlayout überspringen.

**Der robuste Aspekt der Endianess-Walks**

Die Exemplarische Endianess überprüft die üblichen Out-of-the-Buffer-Bedingungen und führt andere Überprüfungen nicht korrelierter Natur durch. Die Überprüfungen, die auf korrelierte Werte abzielen (z. B. das Größenargument im Vergleich zur konformen Größe), können nicht mit diesem Schritt ausgeführt werden. sie werden später ausgeführt, wenn dasMarshaling nicht mehr ausgeführt wird.

 

 




