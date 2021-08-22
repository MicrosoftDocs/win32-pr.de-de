---
title: DirectML-Konstanten
description: Die folgenden Konstanten werden in `DirectML.h` deklariert.
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
ms.openlocfilehash: 5f2d95d0eef67309ef1e5902ed6b968616b38bc081bd259d77418e950e4e028f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989600"
---
# <a name="directml-constants"></a>DirectML-Konstanten

Die folgenden Konstanten werden in `DirectML.h` deklariert.

| Konstante | Wert | BESCHREIBUNG |
|-|-|-|
| DML_TENSOR_DIMENSION_COUNT_MAX | 5 | DirectML-Tensoren unterstützen maximal 5 Dimensionen für DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0. |
| DML_TENSOR_DIMENSION_COUNT_MAX1 | 8 | DirectML-Tensoren unterstützen maximal 8 Dimensionen für DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0. |
| DML_TEMPORARY_BUFFER_ALIGNMENT | 256 | Temporäre und persistente Puffer müssen über eine Basisadresse verfügen, die auf 256 Bytes ausgerichtet ist. |
| DML_PERSISTENT_BUFFER_ALIGNMENT | 256 | Temporäre und persistente Puffer müssen über eine Basisadresse verfügen, die auf 256 Bytes ausgerichtet ist. |
| DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT | 16 | Puffertensoren haben eine Mindestanforderung für die Ausrichtung der Basisadresse von 16 Byte. |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header | DirectML.h |

## <a name="see-also"></a>Siehe auch

* [DirectML-Referenz](direct3d-directml-reference.md)
* [Core-Referenz](direct3d-12-core-reference.md)
* [Referenz für Direct3D 12](direct3d-12-reference.md)
