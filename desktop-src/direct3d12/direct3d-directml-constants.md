---
title: DirectML-Konstanten
description: Die folgenden Konstanten werden in deklariert `DirectML.h` .
keywords:
- Konstanten
topic_type:
- apiref
api_name:
- DirectML constants
api_location:
- DirectML.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 11/04/2020
ms.openlocfilehash: d6c3791812f3ac1191f1959150bd5ac7059c54fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371882"
---
# <a name="directml-constants"></a>DirectML-Konstanten

Die folgenden Konstanten werden in deklariert `DirectML.h` .

| Konstante | Wert | BESCHREIBUNG |
|-|-|-|
| DML_TENSOR_DIMENSION_COUNT_MAX | 5 | Directml-Tensoren unterstützen für DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0 maximal 5 Dimensionen. |
| DML_TENSOR_DIMENSION_COUNT_MAX1 | 8 | Directml-Tensoren unterstützen für DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0 maximal 8 Dimensionen. |
| DML_TEMPORARY_BUFFER_ALIGNMENT | 256 | Temporäre und permanente Puffer müssen eine Basisadresse aufweisen, die auf 256 Bytes ausgerichtet ist. |
| DML_PERSISTENT_BUFFER_ALIGNMENT | 256 | Temporäre und permanente Puffer müssen eine Basisadresse aufweisen, die auf 256 Bytes ausgerichtet ist. |
| DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT | 16 | Puffer-Tensoren haben eine minimale Basisadressen-Ausrichtungs Anforderung von 16 Bytes. |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header | D3D12. h |

## <a name="see-also"></a>Siehe auch

* [DirectML-Referenz](direct3d-directml-reference.md)
* [Core-Referenz](direct3d-12-core-reference.md)
* [Referenz für Direct3D 12](direct3d-12-reference.md)
