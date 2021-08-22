---
title: DXCoreAdapterMemoryBudgetNodeSegmentGroup
description: Beschreibt eine Speichersegmentgruppe für einen Adapter.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: b39557226034e9462e8d51c79aa9b8276659cfe296138df2a3a57f279106f5bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118654"
---
# <a name="dxcoreadaptermemorybudgetnodesegmentgroup-structure"></a>DXCoreAdapterMemoryBudgetNodeSegmentGroup-Struktur

Beschreibt eine Speichersegmentgruppe für einen Adapter.

## <a name="syntax"></a>Syntax

```cpp
struct DXCoreAdapterMemoryBudgetNodeSegmentGroup
{
  uint32_t nodeIndex;
  DXCoreSegmentGroup segmentGroup;
};
```

## <a name="members"></a>Member

### <a name="nodeindex"></a>nodeIndex

Typ: **uint32_t**

Gibt den physischen Adapter des Geräts an, für den die Adapterspeicherinformationen abgefragt werden. Legen Sie für den Einzeladaptervorgang diesen Wert auf 0 (null) fest. Wenn mehrere Adapterknoten verfügbar sind, legen Sie diese auf den Index des Knotens (den physischen Adapter des Geräts) fest, für den Sie Adapterspeicherinformationen abfragen möchten (siehe Systeme mit mehreren [Adaptern).](../../direct3d12/multi-engine.md)

### <a name="segmentgroup"></a>segmentGroup

Typ: **[DXCoreSegmentGroup](./ne-dxcore_interface-dxcoresegmentgroup.md)**

Gibt die Adapterspeichersegment-Gruppierung an, die Sie abfragen möchten.

## <a name="see-also"></a>Weitere Informationen

[DXCore-Referenz](../dxcore-reference.md)

[Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)

[Systeme mit mehreren Adaptern](../../direct3d12/multi-engine.md)