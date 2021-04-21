---
UID: NS:directml.DML_RANDOM_GENERATOR_OPERATOR_DESC
title: DML_RANDOM_GENERATOR_OPERATOR_DESC
description: Füllt einen Ausgabe-Tensor mit deterministisch generierten, pseudo-zufälligen, gleichmäßig verteilten Bits. Dieser Operator kann optional auch einen aktualisierten internen Generatorzustand ausgeben, der bei nachfolgenden Ausführungen des Operators verwendet werden kann.
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
ms.openlocfilehash: 6807c3a1ac91716739075f51196a75ae76ca479b
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804066"
---
# <a name="dml_random_generator_operator_desc-structure-directmlh"></a>DML_RANDOM_GENERATOR_OPERATOR_DESC-Struktur (directml.h)

Füllt einen Ausgabe-Tensor mit deterministisch generierten, pseudo-zufälligen, gleichmäßig verteilten Bits. Dieser Operator kann optional auch einen aktualisierten internen Generatorzustand ausgeben, der bei nachfolgenden Ausführungen des Operators verwendet werden kann.

Dieser Operator ist deterministisch und verhält sich so, als wäre er eine reine &mdash; Funktion, d. h., seine Ausführung erzeugt keine Nebeneffekte und verwendet keinen globalen Zustand. Die von diesem Operator erzeugte Pseudozufallsausgabe hängt ausschließlich von den Werten ab, die im *InputStateTensor* bereitgestellt werden.

Die von diesem Operator implementierten Generatoren sind nicht kryptografisch sicher. daher sollte dieser Operator nicht für Verschlüsselung, Schlüsselgenerierung oder andere Anwendungen verwendet werden, die eine kryptografisch sichere Zufallszahlengenerierung erfordern.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

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

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Eingabe-Tensor, der den internen Generatorzustand enthält. Die Größe und das Format dieses Eingabe-Tensors hängen vom [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)ab.

Für **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10** muss dieser Tensor vom Typ **UINT32** sein und die Größe `{1,1,1,6}` aufweisen. Die ersten vier 32-Bit-Werte enthalten einen monoton ansteigenden 128-Bit-Indikator. Die letzten beiden 32-Bit-Werte enthalten den 64-Bit-Schlüsselwert für den Generator.

```
    Element        0       1       2       3       4       5
(32-bits each) |-------|-------|-------|-------|-------|-------|
                <--------128-bit counter------> <-64-bit key-->
```

Beim erstmaligen Initialisieren des Eingabezustands des Generators sollte in der Regel der 128-Bit-Zähler (die ersten vier UINT32-Werte mit 32 Bit) mit 0 initialisiert werden. Der Schlüssel kann beliebig ausgewählt werden. unterschiedliche Schlüsselwerte erzeugen unterschiedliche Sequenzen von Zahlen. Der Wert für den Schlüssel wird in der Regel mithilfe eines vom Benutzer bereitgestellten *Startwerts generiert.*

`OutputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Ausgabe tensor, der die resultierenden Pseudozufallswerte enthält. Dieser Tensor kann eine beliebige Größe haben.

`OutputStateTensor`

Typ: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler Ausgabe tensor, der den aktualisierten internen Generatorzustand enthält. Wenn angegeben, verwendet dieser Operator den *InputStateTensor,* um einen entsprechenden aktualisierten Generatorzustand zu berechnen, und schreibt das Ergebnis in *den OutputStateTensor.* In der Regel speichern Aufrufer dieses Ergebnis und geben es als Eingabezustand bei einer nachfolgenden Ausführung dieses Operators an.

`Type`

Typ: **[DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)**

Einer der Werte [](./ne-directml-dml_random_generator_type.md) aus der DML_RANDOM_GENERATOR_TYPE-Enum, der den Typ des zu verwendenden Generators angibt. Derzeit ist der einzige gültige Wert **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, der pseudozufälligkeitsbasierte Zahlen gemäß dem [Algorithmus Desox 4x32-10 generiert.](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf)

## <a name="remarks"></a>Hinweise
Bei jeder Ausführung dieses Operators sollte der 128-Bit-Zähler erhöht werden. Wenn *outputStateTensor* angegeben wird, erhöht dieser Operator den Zähler mit dem richtigen Wert in Ihrem Namen und schreibt das Ergebnis in *den OutputStateTensor.* Der Betrag, um den sie erhöht werden soll, hängt von der Anzahl der generierten 32-Bit-Ausgabeelemente und dem Typ des Generators ab.

Für **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10** sollte der 128-Bit-Leistungsindikator bei jeder Ausführung um erhöht werden, wobei die Anzahl der Elemente `ceil(outputSize / 4)` im `outputSize` *OutputTensor ist.*

Stellen Sie sich ein Beispiel vor, bei dem der Wert des 128-Bit-Leistungsindikators derzeit ist und die Größe des `0x48656c6c'6f46726f'6d536561'74746c65` OutputTensors `{3,3,20,7219}` ist. Nachdem dieser Operator einmal ausgeführt wurde, sollte der Zähler um 324.855 erhöht werden (die Anzahl der generierten Ausgabeelemente dividiert durch 4, aufgerundet), was zu einem Zählerwert von `0x48656c6c'6f46726f'6d536561'746f776e` führt. Dieser aktualisierte Wert sollte dann als Eingabe für die nächste Ausführung dieses Operators angegeben werden.

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.

## <a name="tensor-constraints"></a>Tensoreinschränkungen
`InputStateTensor`und `OutputStateTensor` müssen die gleichen Größen *aufweisen.*

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensor | Typ | Dimensionen | Unterstützte Dimensionsanzahlen | Unterstützte Datentypen |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputStateTensor | Eingabe | { 1, 1, 1, 6 } | 4 | UINT32 |
| OutputTensor | Ausgabe | { D0, D1, D2, D3 } | 4 | UINT32 |
| OutputStateTensor | Optionale Ausgabe | { 1, 1, 1, 6 } | 4 | UINT32 |

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |