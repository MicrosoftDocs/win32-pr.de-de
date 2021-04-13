---
title: DXCoreAdapterMemoryBudgetNodeSegmentGroup
description: Beschreibt eine Speichersegment Gruppe für einen Adapter.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c583b746b304232fc65c4281f67b0190b2d24c3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390460"
---
# <a name="dxcoreadaptermemorybudgetnodesegmentgroup-structure"></a>Dxcoreadaptermemorybudgetnoentsegmentgroup-Struktur

Beschreibt eine Speichersegment Gruppe für einen Adapter.

## <a name="syntax"></a>Syntax

```cpp
struct DXCoreAdapterMemoryBudgetNodeSegmentGroup
{
  uint32_t nodeIndex;
  DXCoreSegmentGroup segmentGroup;
};
```

## <a name="members"></a>Member

### <a name="nodeindex"></a>nodeindex

Typ: **uint32_t**

Gibt den physischen Adapter des Geräts an, für den die Adapter Speicherinformationen abgefragt werden. Legen Sie für den Einzel Adapter Vorgang den Wert auf 0 (null) fest. Wenn mehrere Adapter Knoten vorhanden sind, legen Sie diese auf den Index des Knotens (den physischen Adapter des Geräts) fest, für den Sie die Informationen zum Adapter Speicher Abfragen möchten (siehe [multiadaptersysteme](../../direct3d12/multi-engine.md)).

### <a name="segmentgroup"></a>segmentgroup

Typ: **[dxcoresegmentgroup](./ne-dxcore_interface-dxcoresegmentgroup.md)**

Gibt die Gruppe der Adapter Speichersegmente an, die Sie Abfragen möchten.

## <a name="see-also"></a>Siehe auch

[DXCore-Referenz](../dxcore-reference.md)

[Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)

[Systeme mit mehreren Adaptern](../../direct3d12/multi-engine.md)