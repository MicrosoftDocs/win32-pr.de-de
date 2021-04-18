---
UID: NS:directml.DML_MAX_POOLING2_OPERATOR_DESC
title: DML_MAX_POOLING2_OPERATOR_DESC
description: Berechnet den maximalen Wert für die Elemente innerhalb des gleitenden Fensters über den Eingabe Mandanten und gibt optional die Indizes der ausgewählten Maximalwerte zurück.
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
ms.openlocfilehash: 7d2dc9d28e8afcaa5cc6277e26f1f663f3f6688f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106365218"
---
# <a name="dml_max_pooling2_operator_desc-structure-directmlh"></a>DML_MAX_POOLING2_OPERATOR_DESC-Struktur (directml. h)
Berechnet den maximalen Wert für die Elemente innerhalb des gleitenden Fensters über den Eingabe Mandanten und gibt optional die Indizes der ausgewählten Maximalwerte zurück.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

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

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Eingabe-tensorflow der *Größen* `{ BatchCount, ChannelCount, Height, Width }` , wenn *inputtensor. DimensionCount* den Wert 4 hat, und, `{ BatchCount, ChannelCount, Depth, Height, Weight } ` Wenn *inputtensor. DimensionCount* 5 ist.


`OutputTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Ausgabe Mandanten, in den die Ergebnisse geschrieben werden sollen. Die Größen des Ausgabe Mandanten können wie folgt berechnet werden.

```cpp
OutputTensor->Sizes[0] = InputTensor->Sizes[0];
OutputTensor->Sizes[1] = InputTensor->Sizes[1];

for (UINT i = 0; i < DimensionCount; ++i) {
  UINT PaddedSize = InputTensor->Sizes[i + 2] + StartPadding[i] + EndPadding[i];
  OutputTensor->Sizes[i + 2] = (PaddedSize - WindowSizes[i]) / Strides[i] + 1;
}
```


`OutputIndicesTensor`

Type: \_ maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein optionaler ausgabetensor von Indizes für den Eingabe-tensorflow- *inputtensor* der maximalen Werte, die in *outputtensor* erstellt und gespeichert werden. Diese Indexwerte sind NULL basiert und behandeln den Eingabe Mandanten als zusammenhängendes eindimensionales Array. Wenn mehrere Elemente innerhalb des gleitenden Fensters denselben Wert aufweisen, werden die nachfolgenden Gleichheits Werte ignoriert, und der Index zeigt auf den ersten gefundenen Wert. Sowohl der *outputtensor* als auch der *outputindicestensor* haben die gleichen tensorflow-Größen.


`DimensionCount`

Typ: [ **uint**](/windows/desktop/winprog/windows-data-types)

Die Anzahl räumlicher Dimensionen des Input tensorflow *inputtensor*, der auch der Anzahl der Dimensionen des gleitenden Fensters *WindowSize* entspricht. Dieser Wert bestimmt auch die Größe der Felder " *fort* schreiten", " *startpadding*" und " *endpadding* ". Er sollte auf 2 festgelegt werden, wenn *inputtensor* auf 4D festgelegt ist, und 3, wenn es sich um einen 5D-Tensor handelt.


`Strides`

Type: \_ Field \_ size \_ (DimensionCount) <b>Konstanten [uint](/windows/desktop/winprog/windows-data-types) * </b>

Die Schritte für die Abmessungen des gleitenden Fensters von Größen `{ Height, Width }` , wenn *DimensionCount* auf 2 festgelegt ist, oder, wenn der Wert `{ Depth, Height, Width }` auf 3 festgelegt ist.


`WindowSize`

Type: \_ Field \_ size \_ (DimensionCount) <b>Konstanten [uint](/windows/desktop/winprog/windows-data-types) * </b>

Die Abmessungen des gleitenden Fensters in `{ Height, Width }` , wenn *DimensionCount* auf 2 festgelegt ist, oder, `{ Depth, Height, Width }` Wenn es auf 3 festgelegt ist.


`StartPadding`

Type: \_ Field \_ size \_ (DimensionCount) <b>Konstanten [uint](/windows/desktop/winprog/windows-data-types) * </b>

Die Anzahl der Auffüll Elemente, die auf den Anfang jeder räumlichen Dimension des Eingabe-Tensors *inputtensor* angewendet werden sollen. Die Werte sind in `{ Height, Width }` , wenn *DimensionCount* auf 2 festgelegt ist, oder `{ Depth, Height, Width }` Wenn auf 3 festgelegt.


`EndPadding`

Type: \_ Field \_ size \_ (DimensionCount) <b>Konstanten [uint](/windows/desktop/winprog/windows-data-types) * </b>

Die Anzahl der Auffüll Elemente, die auf das Ende jeder räumlichen Dimension des Eingabe-Tensors *inputtensor* angewendet werden sollen. Die Werte sind in `{ Height, Width }` , wenn *DimensionCount* auf 2 festgelegt ist, oder `{ Depth, Height, Width }` Wenn auf 3 festgelegt.


`Dilations`

Type: \_ Field \_ size \_ (DimensionCount) <b>Konstanten [uint](/windows/desktop/winprog/windows-data-types) * </b>

Die Werte für jede räumliche Dimension des Eingabe Mandanten *, von dem* ein Element im gleitenden Fenster für alle Elemente dieses Werts ausgewählt wird. Die Werte sind in `{ Height, Width }` , wenn *DimensionCount* auf 2 festgelegt ist, oder `{ Depth, Height, Width }` Wenn auf 3 festgelegt.


## <a name="remarks"></a>Bemerkungen
**DML_MAX_POOLING2_OPERATOR_DESC** ersetzt die frühere Version [DML_MAX_POOLING_OPERATOR1_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) mit einer zusätzlichen Konstanten Array *Erweiterung*. Die beiden Versionen sind gleichwertig  `{ 1,1 }` , wenn für eine 4D-Eingabe oder `{ 1,1,1 }` für 5D-Eingabe Features festgelegt ist.

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
* ' *Inputtensor*', ' *outputindicestensor*' und ' *outputtensor* ' müssen dieselbe *DimensionCount* aufweisen.
* *Inputtensor* und *outputtensor* müssen denselben *Datentyp* aufweisen.

## <a name="tensor-support"></a>Tensor-Unterstützung
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 und höher
| Tensorflow | Typ | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| Inputtensor | Eingabe | 4 bis 5 | Float32, FLOAT16, int8, Uint8 |
| Outputtensor | Ausgabe | 4 bis 5 | Float32, FLOAT16, int8, Uint8 |
| Outputindicestensor | Optionale Ausgabe | 4 bis 5 | UINT32 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 und höher
| Tensorflow | Typ | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | -------------------------- | -------------------- |
| Inputtensor | Eingabe | 4 bis 5 | Float32, FLOAT16 |
| Outputtensor | Ausgabe | 4 bis 5 | Float32, FLOAT16 |
| Outputindicestensor | Optionale Ausgabe | 4 bis 5 | UINT32 |


## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Windows 10, Version 2004 (10,0; Build 19041) |
| **Unterstützte Mindestversion (Server)** | Windows Server, Version 2004 (10,0; Build 19041) |
| **Header** | directml. h |