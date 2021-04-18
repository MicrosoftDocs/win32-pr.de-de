---
title: DXCoreSegmentGroup
description: Definiert Konstanten, die die Speichersegment Gruppierung eines Adapters angeben.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ce94d5f806879ea84f64c88d3a62b074a5c5415b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337441"
---
# <a name="dxcoresegmentgroup-enum"></a>Dxcoresegmentgroup-Enumeration

Definiert Konstanten, die die Speichersegment Gruppierung eines Adapters angeben.

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

Gibt eine Gruppierung von Segmenten an, die für den Adapter als lokal angesehen werden, und stellt den schnellsten verfügbaren Arbeitsspeicher für die GPU dar. Die Anwendung sollte die lokale Segment Gruppe als Zielgröße für das Workingset als Ziel festlegen.

### <a name="nonlocal"></a>Nicht lokalen

Gibt eine Gruppierung von Segmenten an, die für den Adapter als nicht lokal betrachtet werden und möglicherweise eine langsamere Leistung als die lokale Segment Gruppe aufweisen.

## <a name="see-also"></a>Siehe auch

[DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)