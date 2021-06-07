---
UID: NS:directml.DML_RANDOM_GENERATOR_OPERATOR_DESC
title: DML_RANDOM_GENERATOR_OPERATOR_DESC
description: Füllt einen Ausgabe tensor mit deterministisch generierten, pseudo-zufälligen, gleichmäßig verteilten Bits. Dieser Operator kann optional auch einen aktualisierten internen Generatorzustand ausgeben, der bei nachfolgenden Ausführungen des Operators verwendet werden kann.
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
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417186"
---
# <a name="dml_random_generator_operator_desc-structure-directmlh"></a>DML_RANDOM_GENERATOR_OPERATOR_DESC-Struktur (directml.h)

Füllt einen Ausgabe tensor mit deterministisch generierten, pseudo-zufälligen, gleichmäßig verteilten Bits. Dieser Operator kann optional auch einen aktualisierten internen Generatorzustand ausgeben, der bei nachfolgenden Ausführungen des Operators verwendet werden kann.

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

Beim erstmaligen Initialisieren des Eingabezustands des Generators sollte in der Regel der 128-Bit-Zähler (die ersten vier UINT32-Werte mit 32 Bit) mit 0 initialisiert werden. Der Schlüssel kann beliebig ausgewählt werden. unterschiedliche Schlüsselwerte erzeugen unterschiedliche Sequenzen von Zahlen. Der Wert für den Schlüssel wird in der Regel mithilfe eines vom Benutzer bereitgestellten *Ausgangswerts* generiert.

`OutputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Ausgabe-Tensor, der die resultierenden Pseudozufallswerte enthält. Dieser Tensor kann eine beliebige Größe haben.

`OutputStateTensor`

Typ: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler Ausgabe-Tensor, der den aktualisierten internen Generatorzustand enthält. Falls angegeben, verwendet dieser Operator den *InputStateTensor,* um einen entsprechenden aktualisierten Generatorzustand zu berechnen, und schreibt das Ergebnis in den *OutputStateTensor.* In der Regel speichern Aufrufer dieses Ergebnis und stellen es bei einer nachfolgenden Ausführung dieses Operators als Eingabezustand zur Verfügung.

`Type`

Typ: **[DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)**

Einer der Werte aus der [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md) Enumeration, der den Typ des generators angibt, der verwendet werden soll. Derzeit ist der einzige gültige Wert **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, der Pseudozufallszahlen gemäß dem [4x32-10-Algorithmus](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf)generiert.

## <a name="remarks"></a>Hinweise
Bei jeder Ausführung dieses Operators sollte der 128-Bit-Zähler erhöht werden. Wenn *OutputStateTensor* angegeben wird, erhöht dieser Operator den Zähler in Ihrem Namen mit dem richtigen Wert und schreibt das Ergebnis in *den OutputStateTensor.* Die Menge, um die sie erhöht werden soll, hängt von der Anzahl der generierten 32-Bit-Ausgabeelemente und vom Typ des Generators ab.

Für **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10** sollte der 128-Bit-Zähler bei jeder Ausführung um erhöht `ceil(outputSize / 4)` werden, wobei die Anzahl der Elemente im `outputSize` *OutputTensor* ist.

Stellen Sie sich ein Beispiel vor, bei dem der Wert des 128-Bit-Indikators derzeit und `0x48656c6c'6f46726f'6d536561'74746c65` die Größe des OutputTensor `{3,3,20,7219}` ist. Nachdem dieser Operator einmal ausgeführt wurde, sollte der Zähler um 324.855 erhöht werden (die Anzahl der generierten Ausgabeelemente geteilt durch 4, aufgerundet), was zu einem Zählerwert von `0x48656c6c'6f46726f'6d536561'746f776e` führt. Dieser aktualisierte Wert sollte dann als Eingabe für die nächste Ausführung dieses Operators angegeben werden.

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

## <a name="requirements"></a>Requirements (Anforderungen)
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |