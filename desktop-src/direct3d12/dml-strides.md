---
title: Verwenden von Schritten zum Ausdrücken von Auffüll-und Speicher Layout
description: Directml-Tensoren werden von Eigenschaften beschrieben, die als *Größen* und *Fortschritte* des Mandanten bezeichnet werden.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: b944b1a2600febe27f209bffcc0e355c6a9fc7db
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104548680"
---
# <a name="using-strides-to-express-padding-and-memory-layout"></a>Verwenden von Schritten zum Ausdrücken von Auffüll-und Speicher Layout

Directml-Tensoren &mdash; , die durch Direct3D 12-Puffer unterstützt werden, &mdash; werden durch Eigenschaften, die als *Größen* und *Fortschritte* des Mandanten bezeichnet werden, beschrieben. Die Tensor- *Größen* beschreiben die logischen Dimensionen des Mandanten. Ein 2D-tensorflow kann z. b. eine Höhe von 2 und eine Breite von 3 haben. Logisch hat der tensorflow 6 unterschiedliche Elemente, obwohl die Größen nicht angeben, wie diese Elemente im Arbeitsspeicher gespeichert werden. Die *Schritte* des Mandanten beschreiben das physische Speicher Layout der Tensor-Elemente.

## <a name="two-dimensional-2d-arrays"></a>Zweidimensionale (2D) Arrays

Angenommen, ein 2D-tensorflow hat eine Höhe von 2 und eine Breite von 3. die Daten bestehen aus Textzeichen. In C/C++ kann dies mit einem mehrdimensionalen Array ausgedrückt werden.

```cpp
constexpr int rows = 2;
constexpr int columns = 3;
char tensor[rows][columns];
tensor[0][0] = 'A';
tensor[0][1] = 'B';
tensor[0][2] = 'C';
tensor[1][0] = 'D';
tensor[1][1] = 'E';
tensor[1][2] = 'F';
```

Die logische Ansicht des obigen Tensors wird unten dargestellt.

```console
A B C
D E F
```

In C/C++ wird ein mehrdimensionales Array in Zeilen Hauptreihenfolge gespeichert. Das heißt, dass die aufeinander folgenden Elemente entlang der Width-Dimension im linearen Speicherbereich zusammenhängend gespeichert werden.

Offset:|0|1|2|3|4|5
-|-|-|-|-|-|-
Wert:|A|B|C|D|E|F

Der *Stride* -Wert einer Dimension ist die Anzahl der zu über springenden Elemente, um auf das nächste Element in dieser Dimension zuzugreifen. Mit Schritten wird das Layout des Tensors im Arbeitsspeicher ausgedrückt. Bei einer Zeilen Hauptreihenfolge ist der Stride der Width-Dimension immer 1, da angrenzende Elemente entlang der Dimension zusammenhängend gespeichert werden. Der Schritt der Height-Dimension hängt von der Größe der Width-Dimension ab. im obigen Beispiel ist der Abstand zwischen aufeinander folgenden Elementen entlang der Height-Dimension (z. b. A bis D) gleich der Breite des Tensors (in diesem Beispiel 3).

Um ein anderes Layout zu veranschaulichen, sollten Sie die Spalten Hauptreihenfolge in Erwägung gezogen Das heißt, dass die aufeinander folgenden Elemente entlang der Height-Dimension im linearen Speicherbereich zusammenhängend gespeichert werden. In diesem Fall ist der Höhen Sprung immer 1, und der Width-Stride ist 2 (die Größe der Height-Dimension).

Offset:|0|1|2|3|4|5
-|-|-|-|-|-|-
Wert:|Ein|D|B|E|C|F

## <a name="higher-dimensions"></a>Höhere Dimensionen

Wenn es um mehr als zwei Dimensionen geht, ist es unhandlich, auf ein Layout als Zeilen-Haupt-oder Spalten hauptverweis zu verweisen. Im weiteren Verlauf dieses Themas werden z. b. Begriffe und Bezeichnungen verwendet.

- 2D: die "HW" &mdash; -Höhe ist die Dimension mit der höchsten Ordnung (Row-Major).
- 2D: die Breite "Wh" &mdash; ist die Dimension mit der höchsten Ordnung (Spalten-Major).
- 3D: die Tiefe "DHW" &mdash; ist die Dimension mit der höchsten Ordnung, gefolgt von Höhe und Breite.
- 3D: die "WHD"- &mdash; Breite ist die Dimension mit der höchsten Ordnung, gefolgt von Höhe und dann Tiefe.
- 4D: "nchw" &mdash; die Anzahl der Bilder (Batch Größe), dann die Anzahl der Kanäle, die Höhe und die Breite.

Im Allgemeinen ist der *gepackte* Schritt einer Dimension gleich dem Produkt der Größen der Größen der unteren Reihenfolge. Beispielsweise ist der D-Stride mit dem Layout "DHW" gleich H * W; der H-Stride ist gleich W;. und der W-Stride ist gleich 1. Die Schritte werden als *gepackt* bezeichnet, wenn die gesamte physische Größe des Mandanten gleich der Gesamtgröße des Mandanten ist. Das heißt, es gibt keine zusätzlichen Leerzeichen und keine überlappenden Elemente.

Wir erweitern das 2D-Beispiel auf drei Dimensionen, sodass wir über einen tensorflow mit der Tiefe 2, Höhe 2 und Breite 3 verfügen (insgesamt 12 logische Elemente).

```console
A B C
D E F

G H I
J K L
```

Mit dem Layout "DHW" wird dieser tensorflow wie folgt gespeichert.

Offset:|0|1|2|3|4|5|6|7|8|9|10|11|
-|-|-|-|-|-|-|-|-|-|-|-|-|
Wert:|A|B|C|D|E|F|G|H|I|J|K|L|

- D-Stride = Height (2) * Width (3) = 6 (z. b. der Abstand zwischen ' A ' und ' G ').
- H-Stride = Width (3) = 3 (z. b. der Abstand zwischen "A" und "d").
- W-Stride = 1 (z. B. der Abstand zwischen "A" und "B").

Das Punktprodukt der Indizes/Koordinaten eines Elements und der Fortschritte gibt den Offset für dieses Element im Puffer an. Beispielsweise ist der Offset des H-Elements (d = 1, H = 0, w = 1) 7.

{1, 0, 1} ⋅ {6, 3, 1} = 1 * 6 + 0 * 3 + 1 * 1 = 7

## <a name="packed-tensors"></a>Gepackte Tensoren

In den obigen Beispielen werden *gepackte* Tensoren veranschaulicht. Ein tensorflow wird als *gepackt* bezeichnet, wenn die logische Größe des Tensors (in-Elementen) gleich der physischen Größe des Puffers (in-Elementen) ist und jedes Element über eine eindeutige Adresse/einen eindeutigen Offset verfügt. Beispielsweise wird ein 2x2x3-tensorflow verpackt, wenn der Puffer 12 Elemente in der Länge hat und kein Paar von Elementen denselben Offset im Puffer gemeinsam verwenden. Gepackte Tensoren sind der häufigste Fall. in den Schritten werden jedoch komplexere Speicher Layouts ermöglicht.

## <a name="broadcasting-with-strides"></a>Broadcasting mit Schritten

Wenn die Puffergröße eines Tensors (in-Elemente) kleiner als das Produkt seiner logischen Dimensionen ist, folgt es, dass es einige Überlappende Elemente gibt. Der übliche Fall hierfür wird als *Broadcast* bezeichnet. Dabei sind die Elemente einer Dimension ein Duplikat einer anderen Dimension. Betrachten wir beispielsweise das 2D-Beispiel. Nehmen wir an, dass wir einen Mandanten benötigen, der logisch 2x3 ist, aber die zweite Zeile ist mit der ersten Zeile identisch. So sieht das aus.

```console
A B C
A B C
```

Diese kann als gepackter HW/Row-Major-Tensor gespeichert werden. Ein kompakteres Speicher würde jedoch nur drei Elemente (a, B und C) enthalten und einen Höhen Sprung von 0 anstelle von 3. In diesem Fall beträgt die physische Größe des Tensors 3 Elemente, die logische Größe ist jedoch 6 Elemente.

Im Allgemeinen werden alle Elemente in den Dimensionen mit niedrigerer Reihenfolge in der übertragenen Dimension wiederholt, wenn der Stride-Wert einer Dimension 0 ist. Wenn der Mandanten z. b. nchw ist und der C-Stride den Wert 0 hat, weist jeder Kanal dieselben Werte auf H und W auf.

## <a name="padding-with-strides"></a>Padding mit Schritten

Ein tensorflow wird als *aufgefüllt* bezeichnet, wenn die physische Größe größer ist als die minimale Größe, die für seine Elemente benötigt wird. Wenn keine Broadcast-und überlappenden Elemente vorhanden sind, ist die Mindestgröße des Tensors (in Elementen) einfach das Produkt seiner Dimensionen. Sie können die-Hilfsfunktion verwenden `DMLCalcBufferTensorSize` (Weitere Informationen finden Sie unter [directml-Hilfsfunktionen](dml-helper-functions.md) für eine Auflistung dieser Funktion), um die *minimale* Puffergröße für Ihre directml-Tensoren zu berechnen.

Nehmen wir an, dass ein Puffer die folgenden Werte enthält (die x-Elemente geben Füll Werte an).

0|1|2|3|4|5|6|7|8|9|
-|-|-|-|-|-|-|-|-|-|
A|B|C|x|x|D|E|F|x|x

Der aufgefüllte tensorflow kann mithilfe eines Höhen Schrittes von 5 anstelle von 3 beschrieben werden. Anstelle von drei Elementen, um zur nächsten Zeile zu gelangen, ist der Schritt 5 Elemente (3 *echte* Elemente plus 2 Auffüll Elemente). Die Auffüll Zeichen sind z. b. in Computergrafiken üblich, um sicherzustellen, dass ein Bild über eine zweistufige Ausrichtung verfügt.

```console
A B C
D E F
```

## <a name="directml-buffer-tensor-descriptions"></a>Tensorflow-Beschreibungen für directml-Puffer

Directml kann mit einer Vielzahl von physischen tensorflow-Layouts arbeiten, da die [ **DML_BUFFER_TENSOR_DESC** Struktur](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) sowohl `Sizes` -als auch-Member enthält `Strides` . Einige Operator Implementierungen sind möglicherweise effizienter mit einem bestimmten Layout, sodass es nicht ungewöhnlich ist, die Speicherung von tensorflow-Daten zu ändern, um die Leistung zu verbessern.

Die meisten directml-Operatoren benötigen entweder 4D-oder 5D-Tensoren, und die Reihenfolge der Größen-und Schritte Werte ist fest. Wenn Sie die Reihenfolge der Größen und der Stride-Werte in einer Mandanten Beschreibung beheben, kann directml unterschiedliche physische Layouts ableiten.

**4D**
- [**DML_BUFFER_TENSOR_DESC:: sizes**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) = {N-Size, C-size, H-Size, W-size}
- [**DML_BUFFER_TENSOR_DESC::**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) Stride = {N-Stride, C-Stride, H-Stride, W-Stride}

**5D**
- **DML_BUFFER_TENSOR_DESC:: sizes** = {N-Size, C-size, D-Size, H-Size, W-size}
- **DML_BUFFER_TENSOR_DESC::** Stride = {N-Stride, C-Stride, D-Stride, H-Stride, W-Stride}

Wenn ein directml-Operator einen 4D-oder einen 5D-Tensor erfordert, aber die tatsächlichen Daten einen niedrigeren Rang aufweisen (z. b. 2D), sollten die führenden Dimensionen mit 1 s gefüllt werden. Beispielsweise wird ein "HW"-tensorflow mithilfe von **DML_BUFFER_TENSOR_DESC:: sizes** = {1, 1, H, W} festgelegt.

Wenn tensorflow-Daten in nchw/ncdhw gespeichert werden, ist es nicht erforderlich, **DML_BUFFER_TENSOR_DESC::-Schritte** festzulegen, es sei denn, Sie möchten Broadcasting oder Padding. Sie können das Feld "Schritte" auf festlegen `nullptr` . Wenn die tensorflow-Daten jedoch in einem anderen Layout, z. b. nhwc, gespeichert werden, benötigen Sie Schritte, um die Transformation von nchw zu diesem Layout auszudrücken.

Ein einfaches Beispiel ist die Beschreibung eines 2D-Tensors mit Höhe 3 und der Breite 5.

**Gepackte nchw (implizite Schritte)**
- **DML_BUFFER_TENSOR_DESC:: sizes** = {1, 1, 3, 5}
- **DML_BUFFER_TENSOR_DESC:: Schritte** = `nullptr`

**Gepackte nchw (explizite Schritte)**
- N-Stride = C-size * H-Size × W-size = 1 * 3 * 5 = 15
- C-Stride = H-Size * W-size = 3 * 5 = 15
- H-Stride = W-Size = 5
- W-Stride = 1
- **DML_BUFFER_TENSOR_DESC:: sizes** = {1, 1, 3, 5}
- **DML_BUFFER_TENSOR_DESC::-Schritte** = {15, 15, 5, 1}

**Gepacktes nhwc**
- N-Stride = H-Size * W-size × C-size = 3 * 5 * 1 = 15
- H-Stride = W-size × C-Size = 5 * 1 = 5
- W-Stride = C-Größe = 1
- C-Stride = 1
- **DML_BUFFER_TENSOR_DESC:: sizes** = {1, 1, 3, 5}
- **DML_BUFFER_TENSOR_DESC::-Schritte** = {15, 1, 5, 1}

## <a name="see-also"></a>Siehe auch

* [Directml-Hilfsfunktionen](dml-helper-functions.md)
* [DML_BUFFER_TENSOR_DESC Struktur](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc)
