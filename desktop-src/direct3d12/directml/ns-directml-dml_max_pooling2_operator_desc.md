---
UID: NS:directml.DML_MAX_POOLING2_OPERATOR_DESC
title: DML_MAX_POOLING2_OPERATOR_DESC
description: Berechnet den Maximalen Wert für die Elemente innerhalb des gleitenden Fensters über den Eingabe-Tensor und gibt optional die Indizes der ausgewählten Höchstwerte zurück.
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
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
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_name:
- DML_MAX_POOLING2_OPERATOR_DESC
f1_keywords:
- DML_MAX_POOLING2_OPERATOR_DESC
- directml/DML_MAX_POOLING2_OPERATOR_DESC
ms.openlocfilehash: 06e4d7eb01abab9c412238e353a73607df02b219
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803667"
---
# <a name="dml_max_pooling2_operator_desc-structure-directmlh"></a>DML_MAX_POOLING2_OPERATOR_DESC-Struktur (directml.h)
Berechnet den Maximalen Wert für die Elemente innerhalb des gleitenden Fensters über den Eingabe-Tensor und gibt optional die Indizes der ausgewählten Höchstwerte zurück.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax
```cpp
struct DML_MAX_POOLING2_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  const DML_TENSOR_DESC *OutputIndicesTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *WindowSize;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  const UINT            *Dilations;
};
```



## <a name="members"></a>Member

`InputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Eingabe tensor von *Größen,* `{ BatchCount, ChannelCount, Height, Width }` wenn *InputTensor.DimensionCount* 4 und `{ BatchCount, ChannelCount, Depth, Height, Weight } ` *InputTensor.DimensionCount* 5 ist.


`OutputTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Ausgabe-Tensor, in den die Ergebnisse geschrieben werden sollen. Die Größen des Ausgabe-Tensors können wie folgt berechnet werden.

```cpp
OutputTensor->Sizes[0] = InputTensor->Sizes[0];
OutputTensor->Sizes[1] = InputTensor->Sizes[1];

for (UINT i = 0; i < DimensionCount; ++i) {
  UINT PaddedSize = InputTensor->Sizes[i + 2] + StartPadding[i] + EndPadding[i];
  OutputTensor->Sizes[i + 2] = (PaddedSize - WindowSizes[i]) / Strides[i] + 1;
}
```


`OutputIndicesTensor`

Typ: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler Ausgabe-Tensor von Indizes für den Eingabe tensor *InputTensor* der maximalen Werte, die im *OutputTensor* erstellt und gespeichert werden. Diese Indexwerte sind nullbasiert und behandeln den Eingabe-Tensor als zusammenhängendes eindimensionales Array. Wenn mehrere Elemente innerhalb des gleitenden Fensters den gleichen Wert aufweisen, werden die späteren gleichen Werte ignoriert, und der Index zeigt auf den ersten gefundenen Wert. *OutputTensor* und *OutputIndicesTensor* haben die gleichen Tensorgrößen.


`DimensionCount`

Typ: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Die Anzahl der räumlichen Dimensionen des Eingabe tensor *InputTensor*, die auch der Anzahl der Dimensionen des gleitenden *Fensters WindowSize* entspricht. Dieser Wert bestimmt auch die Größe der Arrays *Strides,* *StartPadding* und *EndPadding.* Sie sollte auf 2 festgelegt werden, wenn *InputTensor* 4D ist, und 3, wenn es sich um einen 5D-Tensor handelt.


`Strides`

Typ: \_ \_ Feldgröße \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Die Schritte für die Größendimensionen des gleitenden Fensters, wenn DimensionCount auf 2 oder auf `{ Height, Width }`  `{ Depth, Height, Width }` 3 festgelegt ist.


`WindowSize`

Typ: \_ \_ Feldgröße \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Die Dimensionen des gleitenden Fensters in `{ Height, Width }` , *wenn DimensionCount* auf 2 oder `{ Depth, Height, Width }` auf 3 festgelegt ist.


`StartPadding`

Typ: \_ \_ Feldgröße \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Die Anzahl der Auf padding-Elemente, die auf den Anfang jeder räumlichen Dimension des Eingabe tensor *InputTensor angewendet werden sollen.* Die Werte befinden sich in `{ Height, Width }` , *wenn DimensionCount* auf 2 oder `{ Depth, Height, Width }` auf 3 festgelegt ist.


`EndPadding`

Typ: \_ \_ Feldgröße \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Die Anzahl der Auf padding-Elemente, die auf das Ende jeder räumlichen Dimension des Eingabe tensor *InputTensor angewendet werden sollen.* Die Werte befinden sich in `{ Height, Width }` , *wenn DimensionCount* auf 2 oder `{ Depth, Height, Width }` auf 3 festgelegt ist.


`Dilations`

Typ: \_ \_ Feldgröße \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Die Werte für jede räumliche Dimension des Eingabe tensor *InputTensor,* mit dem ein Element innerhalb des gleitenden Fensters für jedes Element dieses Werts ausgewählt wird. Die Werte befinden sich in `{ Height, Width }` , *wenn DimensionCount* auf 2 oder `{ Depth, Height, Width }` auf 3 festgelegt ist.


## <a name="remarks"></a>Hinweise
**DML_MAX_POOLING2_OPERATOR_DESC** ersetzt die frühere Version DML_MAX_POOLING_OPERATOR1_DESC [durch](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) eine zusätzliche konstante *Arraydilierung*. Die beiden Versionen sind gleichwertig, *wenn Dilations* für 4D-Eingaben oder `{ 1,1 }` für `{ 1,1,1 }` 5D-Eingabefeatures auf festgelegt ist.

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.

## <a name="tensor-constraints"></a>Tensoreinschränkungen
* *InputTensor,* *OutputIndicesTensor* und *OutputTensor* müssen denselben *DimensionCount aufweisen.*
* *InputTensor und* *OutputTensor* müssen denselben *Datentyp haben.*

## <a name="tensor-support"></a>Tensor-Unterstützung
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 und höher
| Tensor | Typ | Unterstützte Dimensionsanzahlen | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 4 bis 5 | FLOAT32, FLOAT16, INT8, UINT8 |
| OutputTensor | Ausgabe | 4 bis 5 | FLOAT32, FLOAT16, INT8, UINT8 |
| OutputIndicesTensor | Optionale Ausgabe | 4 bis 5 | UINT32 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 und höher
| Tensor | Typ | Unterstützte Dimensionsanzahlen | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Eingabe | 4 bis 5 | FLOAT32, FLOAT16 |
| OutputTensor | Ausgabe | 4 bis 5 | FLOAT32, FLOAT16 |
| OutputIndicesTensor | Optionale Ausgabe | 4 bis 5 | UINT32 |


## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Windows 10, Version 2004 (10.0; Build 19041) |
| **Unterstützte Mindestversion (Server)** | Windows Server, Version 2004 (10.0; Build 19041) |
| **Header** | directml.h |