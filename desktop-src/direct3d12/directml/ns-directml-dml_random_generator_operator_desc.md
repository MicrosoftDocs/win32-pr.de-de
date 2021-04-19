---
UID: NS:directml.DML_RANDOM_GENERATOR_OPERATOR_DESC
title: DML_RANDOM_GENERATOR_OPERATOR_DESC
description: Füllt einen Ausgabe Mandanten mit deterministisch generierten, pseudo zufälligen, gleichmäßig verteilten Bits. Dieser Operator kann optional auch einen aktualisierten internen Generator Status ausgeben, der während der nachfolgenden Ausführungen des Operators verwendet werden kann.
helpviewer_keywords:
- DML_RANDOM_GENERATOR_OPERATOR_DESC
- DML_RANDOM_GENERATOR_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RANDOM_GENERATOR_OPERATOR_DESC, DML_RANDOM_GENERATOR_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_RANDOM_GENERATOR_OPERATOR_DESC
- directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_RANDOM_GENERATOR_OPERATOR_DESC
ms.openlocfilehash: 19e01ec8dc47e65ace996deef5954c35e21bf5bb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106353243"
---
# <a name="dml_random_generator_operator_desc-structure-directmlh"></a>DML_RANDOM_GENERATOR_OPERATOR_DESC-Struktur (directml. h)

Füllt einen Ausgabe Mandanten mit deterministisch generierten, pseudo zufälligen, gleichmäßig verteilten Bits. Dieser Operator kann optional auch einen aktualisierten internen Generator Status ausgeben, der während der nachfolgenden Ausführungen des Operators verwendet werden kann.

Dieser Operator ist deterministisch und verhält sich so, als ob es sich um eine reine Funktion &mdash; handelt, deren Ausführung keine Nebeneffekte erzeugt und keinen globalen Zustand verwendet. Die von diesem Operator erzeugte pseudo zufällige Ausgabe ist ausschließlich von den Werten abhängig, die in *inputstatetensor* bereitgestellt werden.

Die von diesem Operator implementierten Generatoren sind nicht kryptografisch sicher. Daher sollte dieser Operator nicht für die Verschlüsselung, die Schlüsselgenerierung oder andere Anwendungen verwendet werden, die eine kryptografisch sichere Zufallszahlengenerierung erfordern.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

## <a name="syntax"></a>Syntax

```cpp
struct DML_RANDOM_GENERATOR_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputStateTensor;
  const DML_TENSOR_DESC* OutputTensor;
  _Maybenull_ const DML_TENSOR_DESC* OutputStateTensor;
  DML_RANDOM_GENERATOR_TYPE Type;
};
```

## <a name="members"></a>Member

`InputStateTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein eingabetensor, der den internen Generator Zustand enthält. Die Größe und das Format dieses Eingabe Mandanten hängt von der [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)ab.

Bei **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10** muss dieser tensorflow den Typ **UInt32** aufweisen und Übergrößen verfügen `{1,1,1,6}` . Die ersten 4 32-Bit-Werte enthalten einen monoton steigenden 128-Bit-Zählers. Die letzten 2 32-Bit-Werte enthalten den 64-Bit-Schlüsselwert für den Generator.

```
    Element        0       1       2       3       4       5
(32-bits each) |-------|-------|-------|-------|-------|-------|
                <--------128-bit counter------> <-64-bit key-->
```

Wenn Sie den Eingabe Zustand des Generators zum ersten Mal initialisieren, sollte der 128-bit-Counter (die ersten 4 32-Bit-UInt32-Werte) in der Regel mit 0 initialisiert werden. Der Schlüssel kann willkürlich ausgewählt werden. unterschiedliche Schlüsselwerte führen zu unterschiedlichen Zahlen Sequenzen. Der Wert für den Schlüssel wird normalerweise mit einem vom *Benutzer bereitgestellten* Startwert generiert.

`OutputTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Ausgabe-tensorflow, der die resultierenden Pseudo Zufallswerte enthält. Dieser Mandanten kann eine beliebige Größe aufweisen.

`OutputStateTensor`

Type: \_ maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler Ausgabe Mandanten, der den aktualisierten internen Generator Zustand enthält. Wenn angegeben, verwendet dieser Operator den *inputstatetensor* , um einen geeigneten aktualisierten Generator Zustand zu berechnen, und schreibt das Ergebnis in den *outputstatetensor*. In der Regel wird dieses Ergebnis von Aufrufern gespeichert und als Eingabe Zustand bei einer nachfolgenden Ausführung dieses Operators bereitgestellt.

`Type`

Typ: **[DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)**

Einer der Werte aus der [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md) Enumeration, die den Typ des zu verwendenden Generators angibt. Zurzeit ist der einzige gültige Wert **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, der nach dem " [philox 4x32-10"-Algorithmus](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf)Pseudozufallszahlen generiert.

## <a name="remarks"></a>Bemerkungen
Bei jeder Ausführung dieses Operators sollte der 128-Bit-Wert inkrementiert werden. Wenn *outputstatetensor* bereitgestellt wird, erhöht dieser Operator den Wert des Zählers mit dem korrekten Wert in Ihrem Namen und schreibt das Ergebnis in den *outputstatetensor*. Der Betrag, um den der Wert erhöht werden soll, hängt von der Anzahl der generierten 32-Bit-Ausgabe Elemente und vom Typ des Generators ab.

Für **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10** sollte der 128-Bit-Wert bei jeder Ausführung um inkrementiert werden `ceil(outputSize / 4)` , wobei `outputSize` die Anzahl der Elemente in *outputtensor* ist.

Sehen Sie sich ein Beispiel an, in dem der Wert des 128-Bit-Leistungs Zählers aktuell ist `0x48656c6c'6f46726f'6d536561'74746c65` , und die Größe von outputtensor ist `{3,3,20,7219}` . Nach dem einmaligen ausführen dieses Operators sollte der Leistungswert um 324.855 erhöht werden (die Anzahl der Ausgabe Elemente, dividiert durch 4, aufgerundet). Dies führt zu einem Leistungs Zählers `0x48656c6c'6f46726f'6d536561'746f776e` . Dieser aktualisierte Wert sollte dann als Eingabe für die nächste Ausführung dieses Operators angegeben werden.

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
`InputStateTensor` und `OutputStateTensor` müssen über die gleichen *Größen* verfügen.

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensorflow | Typ | Dimensionen | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| Inputstatetensor | Eingabe | {1, 1, 1, 6} | 4 | UINT32 |
| Outputtensor | Ausgabe | {D0, D1, D2, D3} | 4 | UINT32 |
| Outputstatetensor | Optionale Ausgabe | {1, 1, 1, 6} | 4 | UINT32 |

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |