---
UID: NE:directml.DML_DEPTH_SPACE_ORDER
title: DML_DEPTH_SPACE_ORDER
description: Definiert Konstanten, die die Transformation steuern, die in den DirectML-Operatoren DML_OPERATOR_DEPTH_TO_SPACE1 **und** DML_OPERATOR_SPACE_TO_DEPTH1. [](/windows/win32/api/directml/ne-directml-dml_operator_type)
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
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
- DML_DEPTH_SPACE_ORDER
- directml/DML_DEPTH_SPACE_ORDER
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
- DML_DEPTH_SPACE_ORDER
ms.openlocfilehash: 009686adfc054c7b6344f01edafedaf2921693d5
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417217"
---
# <a name="dml_depth_space_order-enumeration-directmlh"></a>DML_DEPTH_SPACE_ORDER -Enumeration (directml.h)

Definiert Konstanten, die die Transformation steuern, die in den DirectML-Operatoren DML_OPERATOR_DEPTH_TO_SPACE1 **und** DML_OPERATOR_SPACE_TO_DEPTH1. [](/windows/win32/api/directml/ne-directml-dml_operator_type) Diese werden innerhalb der [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) [und](./ns-directml-dml_space_to_depth1_operator_desc.md) DML_SPACE_TO_DEPTH1_OPERATOR_DESC verwendet.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax
```cpp
typedef enum DML_DEPTH_SPACE_ORDER {
  DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW,
  DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH
} ;
```

## <a name="constants"></a>Konstanten

| Name | BESCHREIBUNG |
| ---- |:---- |
| DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW | Bewirkt, dass tensors, die in [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) und [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) verwendet werden, mit den folgenden Layouts interpretiert werden, wobei Dimensionen in Klammern zusammen flach werden.<br><br>- **Tiefenversion:**[Batch, (BlockHeight, BlockWidth, Channels), Height, Width]<br>- **Raumversion:**[Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)] |
| DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH | Bewirkt, dass tensors, die in [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) und [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) verwendet werden, mit den folgenden Layouts interpretiert werden, wobei Dimensionen in Klammern zusammen flach werden.<br><br>- **Tiefenversion:**[Batch, (Channels, BlockHeight, BlockWidth), Height, Width]<br>- **Raumversion:**[Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)] |

## <a name="remarks"></a>Hinweise

Beispiele [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) auswirkungen [dieser DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) finden Sie in der Dokumentation zu DML_SPACE_TO_DEPTH1_OPERATOR_DESC Und-Daten.

## <a name="requirements"></a>Requirements (Anforderungen)
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |

## <a name="see-also"></a>Siehe auch

* [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md)
* [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md)

## <a name="availability"></a>Verfügbarkeit
Diese Enumeration wurde in `DML_FEATURE_LEVEL_2_1` eingeführt.