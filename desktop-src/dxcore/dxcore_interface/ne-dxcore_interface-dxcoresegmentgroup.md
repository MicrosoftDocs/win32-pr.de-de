---
title: DXCoreSegmentGroup
description: Definiert Konstanten, die die Speichersegmentgruppe eines Adapters angeben.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 2474f8084035ddb67f7081ea45cd1d1743c053415a7bbade68ecff3d4527636c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279622"
---
# <a name="dxcoresegmentgroup-enum"></a>DXCoreSegmentGroup-Enum

Definiert Konstanten, die die Speichersegmentgruppe eines Adapters angeben.

## <a name="syntax"></a>Syntax

```cpp
enum class DXCoreSegmentGroup : uint32_t
{
  Local = 0,
  NonLocal = 1
};
```

## <a name="constants"></a>Konstanten

### <a name="local"></a>Lokal

Gibt eine Gruppierung von Segmenten an, die für den Adapter als lokal betrachtet wird und den schnellsten Arbeitsspeicher darstellt, der für die GPU verfügbar ist. Ihre Anwendung sollte die lokale Segmentgruppe als Zielgröße für den Arbeitssatz festlegen.

### <a name="nonlocal"></a>Nichtlokale

Gibt eine Gruppierung von Segmenten an, die für den Adapter als nicht lokal betrachtet werden und möglicherweise eine langsamere Leistung als die lokale Segmentgruppe haben.

## <a name="see-also"></a>Siehe auch

[DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md)