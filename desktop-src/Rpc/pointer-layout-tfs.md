---
title: Zeiger Layout
description: Das Zeiger Layout beschreibt Zeiger einer Struktur oder eines Arrays.
ms.assetid: 1a4984c1-97b9-4e95-a17e-851b67fa94a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f26a6639b0c4b56c911be1e688995aaf3fb9d2d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856639"
---
# <a name="pointer-layout"></a>Zeiger Layout

Das Zeiger Layout beschreibt Zeiger einer Struktur oder eines Arrays.

## <a name="pointer_layout"></a>Zeiger \_ Layout<>

Ein Zeiger \_ Layout<> Feld besteht aus der Format \_ \_ Zeichenfolge FC FC, gefolgt von einer oder mehreren Zeiger Beschreibungen, die später beschrieben werden, und endet mit einem FC- \_ endformatzeichen:

``` syntax
FC_PP
FC_PAD
{ pointer_instance_layout<> }*
FC_END
```

Ein \_ zeigerinstanzlayout \_<> Feld ist eine Format Zeichenfolge, die einzelne oder mehrere Instanzen von Zeigern beschreibt. Die folgenden Felder werden in diesen Deskriptoren verwendet:

-   Offset \_ im \_ Speicher

    Der Offset mit Vorzeichen für die Position des Zeigers im Arbeitsspeicher. Bei einem Zeiger in einer Struktur ist dieser Offset ein negativer Offset vom Ende der Struktur (das Ende des nicht konformen Teils der konformen Strukturen). für Arrays erfolgt der Offset vom Anfang des Arrays.

-   Offset \_ im \_ Puffer

    Der Offset mit Vorzeichen an der Position des Zeigers im Puffer. Bei einem Zeiger in einer Struktur ist dieser Offset ein negativer Offset vom Ende der Struktur (das Ende des nicht konformen Teils der konformen Strukturen): bei Arrays erfolgt der Offset vom Anfang des Arrays.

-   Offset \_ zu \_ Array

    Offset von einer einschließenden Struktur zum eingebetteten Array, dessen Zeiger behandelt werden. Bei Arrays der obersten Ebene ist dieses Feld immer 0 (null).

-   Iterationen

    Die Gesamtanzahl von Zeigern, die das gleiche Layout aufweisen<> beschrieben.

-   increment

    Inkrement zwischen aufeinander folgenden Zeigern während einer Wiederholung.

-   Anzahl \_ von \_ Zeigern

    Die Anzahl der unterschiedlichen Zeiger in einer Wiederholungs Instanz.

-   Zeiger \_ Beschreibung

    Zeiger Beschreibung.

Alle Zeiger instanzlayouts verwenden die folgende einzelne Zeiger \_ Instanz<8>:

``` syntax
offset_to_pointer_in_memory<2> 
offset_to_pointer_in_buffer<2> 
pointer_description<4>
```

Die folgenden Instanzdeskriptoren sind verfügbar:

**Einzelne Instanz eines Zeigers auf einen einfachen Typ:**

``` syntax
FC_NO_REPEAT FC_PAD 
pointer_instance<8>
```

**Wiederholungs Zeiger korrigiert:**

``` syntax
FC_FIXED_REPEAT FC_PAD 
iterations<2> 
increment<2> 
offset_to_array<2> 
number_of_pointers<2>
{ pointer_instance<8> }*
```

**Variabler Wiederholungs Zeiger:**

``` syntax
FC_VARIABLE_REPEAT (FC_FIXED_OFFSET | FC_VARIABLE_OFFSET) 
increment<2> 
offset_to_array<2> 
number_of_pointers<2> 
{ pointer_instance<8> }*
```

Für die wiederholten Wiederholungs-und Wiederholungs Zeiger Instanzen gibt es einen Satz von Offset-und Zeiger Beschreibungen für jeden Zeiger in der Wiederholungs Instanz.

## <a name="pointers-layout-design-issues"></a>Entwurfs Probleme beim Layout von Zeigern

In diesem Abschnitt werden Probleme im Zusammenhang mit der Verarbeitung von kompatiblen Strukturen und eingebetteten Zeigern behandelt. Das Problem besteht darin, dass der Compiler Zeiger Layouts für Strukturen und Arrays mit einiger Redundanz generiert. Dies ist von Vorteil, da die Informationen hilfreich sind. eine konforme Struktur kann z. b. ein Zeiger Layout durchlaufen, um alle Zeiger aus der Struktur zu bedienen, und aus dem konformen Array, das Teil der konformen Struktur ist. Es gibt jedoch einige eingebettete Situationen, bei denen die NDR-Engine zusätzliche Aufgaben ausführen muss, um alle Zeiger Layouts in der richtigen Reihenfolge zu verarbeiten, wobei jeder Zeiger genau einmal verarbeitet wird.

## <a name="what-the-compiler-generates"></a>Was der Compiler generiert

Jedes in diesem Abschnitt erörterte Objekt verfügt über Zeiger, z. b. enthält eine konforme Struktur Zeiger sowohl im Struktur Teil als auch in den Array Elementen. Das-Element ist eine einfache Struktur mit einem-Zeiger.

1.  Konforme Struktur, einzelne Ebene

    Der konforme Deskriptor verfügt über einen PP-Teil, in dem alle Zeiger sowohl aus der Struktur als auch aus dem Array beschrieben werden. Die Elementliste enthält den FC " \_ Long" an Stelle eines Zeigers. Die Beschreibung des caretzarararrays hat Elemente, die einen eingebetteten \_ komplexen und keinen Zeiger Deskriptoren verwenden. Das Element hat immer noch seinen einzelnen Zeiger Deskriptor. Das Zeiger Layout liegt vor dem Element Layout in einer konformen Struktur und einfachen Struktur Deskriptoren.

2.  Konforme Struktur, mindestens zwei Ebenen

    Die PP-Beschreibung enthält Zeiger von allen Ebenen. Die gleiche Array Beschreibung wird wieder verwendet wie die interne konforme Struktur. Die Elementliste enthält den FC " \_ Long" an Stelle eines Zeigers. Eine eingebettete Struktur kommt durch die Verwendung eines eingebetteten komplexen. Der konforme Struktur Deskriptor wird unverändert wieder verwendet. Die Größe des flachen Teils der Struktur wird ebenfalls vervollständigt, was bedeutet, dass die Struktur Größe der obersten Ebene die flache Größe der eingebetteten Struktur einschließt.

3.  Komplexe Struktur, einzelne Ebene

    Zeiger Elemente werden durch einen FC- \_ Zeiger gekennzeichnet. Das Zeiger Layout ist so vereinfacht, dass für jeden FC- \_ Zeiger Eintrag in der Liste ein Zeiger Deskriptor (4 Bytes) vorhanden ist. Das Zeiger Layout wird parallel zu einem Element Durchlauf durchlaufen, d. h. ein FC- \_ Zeiger bewirkt, dass die nächste Zeiger Beschreibung verarbeitet wird. Das CArray-Array weist das Zeiger Layout mit allen Deskriptoren des Arrays und dann das-Element durch die Verwendung eines eingebetteten komplexen auf. Der Element Deskriptor wird wieder verwendet. Die Größe des flachen Teils der Struktur wird beendet. Das heißt, die flache Größe der Struktur der obersten Ebene enthält die flache Größe der eingebetteten Struktur. Das Element Layout liegt vor dem Zeiger Layout für komplexe Strukturen.

    Daher unterscheidet sich die Beschreibung des konformen Arrays in Abhängigkeit davon, ob es sich um ein Array innerhalb einer konformen Struktur oder innerhalb einer komplexen Struktur handelt.

4.  Komplexe Struktur, mindestens zwei Ebenen, Komplex in Komplex

    Die komplexe Struktur der obersten Ebene verfügt über die Member-Zeiger, die eingebettete komplexe Struktur hat ihre Member-Zeiger. Der konforme Struktur Deskriptor wird wieder verwendet. Der Array Deskriptor von oben ist das wiederverwendete Array aus der eingebetteten-Struktur.

5.  Komplexe Struktur mit einer eingebetteten konformen Struktur

    Die oberste = ebenenkonforme Struktur verfügt über die Member-Zeiger. Der konforme Struktur Deskriptor wird unverändert wieder verwendet. Der Array Deskriptor wird aus der eingebetteten konformen Struktur wieder verwendet. Das heißt, es enthält keine Zeiger auf den Array Deskriptor. Das-Element hat seinen Zeiger Deskriptor.

6.  Arrays von Strukturen mit Zeigern

    Ein Array von einfachen Strukturen mit Zeigern wird als smfarray oder CArray generiert, abhängig davon, ob die Größe des Arrays groß ist. in beiden Fällen weist es jedoch ein gezeichtes Zeiger Layout auf (eine \_ wiederholte Wiederholung oder eine \_ wiederholte Variable). Das Zeiger Layout ist vor dem Element Layout.

    Ein Array komplexer Strukturen mit Zeigern wird \_ unabhängig davon, ob es sich um ein fester oder eine Größe handelt, als falsch Array generiert, und in beiden Fällen ist kein Zeiger Layout vorhanden.

## <a name="what-the-ndr-engine-does"></a>Funktionsweise der NDR-Engine

In diesem Abschnitt wird das Verhalten der NDR-Engine beschrieben.

**Der marshallingdurchlauf**

1.  Konforme Strukturen und eingebettete konforme Struktur.

    Die Struktur der obersten Ebene verhält sich wie eine Struktur mit einer Ebene.

2.  Eingebettete komplexe Struktur mit konformem Array

    Jede komplexe Struktur erzwingt, dass die äußere Struktur eine komplexe Struktur ist. Die eingebettete Struktur Marshalls nie das Array. Jede Struktur durchläuft immer eingebettete Zeiger, indem Member einfach gemarshallert werden und ein Member, der als FC- \_ Zeiger auftritt.

3.  Komplexe Struktur mit konformen Struktur

    Die am meisten eingebettete konforme Struktur marshallziert das konforme Array und alle pointierten. Die NDR-Engine wird nicht zu tieferen, in die Struktur eingefügten Strukturen herab laufen, wenn vorhanden. Dadurch wird die Lösung vereinfacht, da eine konforme Struktur ein Blatt Objekt ist, so weit das Marshalling von eingebetteten Objekten betrifft. Die komplexe Struktur der obersten Ebene überspringt das Marshalling von Arrays.

**Nicht Marshalling, übertragen und Freigeben von Durchläufen**

Das Marshalling ist symmetrisch zum Marshalling. der erste Vorgang, der für komplexe Strukturen durchführt, besteht darin, die Position des poinrats im Puffer zu ermitteln, indem die Funktion **ndrcomplexstructbuffersize** aufgerufen wird. Anschließend werden die pointees parallel entfernt. Dadurch wird das gleiche Schema zum ordnungsgemäßen Marshalling der pointierten für die Verwendung ermöglicht. Es sollte keine Verwirrung bezüglich der großen Objekte und Unions bestehen. das Speicher Abbild sollte nicht für Größen Objekte und Unions verwendet werden, sondern nur für den Pufferinhalt.

Die Flags, die verwendet werden, um das Marshalling und das Marshalling ordnungsgemäß durchzuführen, werden auf die gleiche Weise wie bei der Überprüfung und Freigabe verwendet, um sicherzustellen, dass pointierten genau einmal durchlaufen werden.

**Erfolgs Übergabe**

Zunächst ähnelt der gegen übergebene Pass einem Marshalling/Unmarshalling. zum Verarbeiten komplexer Strukturen sind zwei Durchgänge erforderlich. First Pass konvertiert den flachen Teil und findet die Position des pointierten im Puffer ähnlich der Art, wie bufsizing diesen Vorgang für das Marshalling durchführt. Der zweite Durchlauf konvertiert dann die pointierten.

Endianess-Pässe unterscheiden sich wie folgt: jede Struktur und jeder Member muss abgestuft werden, bis das Blatt Element oder Element ein einfacher Typ ist. Dies unterscheidet sich vom nicht Mars Hallen. beim nicht Marshalling gibt es z. b. nie eine Notwendigkeit, konforme Strukturen zu verarbeiten, die in konforme Strukturen eingebettet sind, oder ein beliebiges Member der konformen Struktur. Ein weiteres Problem ist, dass es sich bei der Konvertierung nicht um einen idempotenten Vorgang handelt – daher könnte der Unmarshalling-Durchlauf das rückgängig machen einiger Teile ohne Schaden wiederholen, während die Konvertierung für eine strikte einmal pro einfachen Typ durchgeführt werden muss.

Daher kann der-Algorithmus für die erneute Anmeldung wie folgt zusammengefasst werden. Der NDR hat eine Vorstellung von der Konzept Struktur der obersten Ebene und ein Flag, um dies nach Bedarf zu markieren. Wenn Sie das erste Mal durchlaufen, z. b. zum Konvertieren des flachen Teils und zum Abrufen der Position der poindanten, wird dieser Begriff nicht verwendet. Der NDR würde die flachen Teile aller Ebenen von Strukturen durchlaufen und nie die Zeiger Verarbeitung Unternehmen. Schließlich würde der NDR das Array auf der obersten Ebene in eine flache Konvertierung konvertieren.

Wenn Sie das zweite Mal durchlaufen, wird das-Flag verwendet, um die Übergabe des eingebetteten Zeigers zu markieren, um zu vermeiden, dass tiefere Ebenen der konformen Strukturen eingegeben werden, und dann die oberste konforme Struktur. Auf diese Weise würde das-Flag das gängige Marshalling/Unmarshalling-Verhalten erzwingen, um zu vermeiden, dass es zu tieferen Ebenen von konformen Strukturen absteigend wird.

Der zweite Durchlauf für komplexe Strukturen mit konformen Arrays funktioniert wie folgt: die komplexen Strukturen funktionieren in der üblichen Weise. Dies bedeutet, dass tiefere Ebenen nie Ihre konformen Größe oder Ihre konformen Arrays untersuchen oder überspringen und stattdessen einfach Ihre Member durchlaufen, ohne das Array zu berühren.

Bei komplexen Strukturen mit konformen Strukturen muss die konforme Struktur beachten, ob Sie die oberste Ebene ist und ob Sie sich in einer komplexen Struktur befindet. Der flache Teil des Arrays wird von der obersten konformen Struktur verarbeitet. Beim zweiten Durchlauf würde die am meisten übergebene Struktur den flachen Teil überspringen und das Zeiger Layout durchlaufen und zurückgeben. Die oberste komplexe Struktur würde den flachen Teil überspringen und auch das Zeiger Layout überspringen.

**Der robuste Aspekt der nicht Umwahl enden Exemplarische Vorgehensweise**

Der einstufige Durchlauf prüft auf die üblichen nicht korrelierten Bedingungen und führt andere Prüfungen in einer nicht korrelierten Art aus. Die Überprüfungen, die auf korrelierte Werte abzielen (z. b. das Größen Anpassungs Argument und die konformen Größe), können nicht mit diesem Schritt ausgeführt werden. Sie werden später, wenn das Marshalling erfolgt, ausgeführt.

 

 




