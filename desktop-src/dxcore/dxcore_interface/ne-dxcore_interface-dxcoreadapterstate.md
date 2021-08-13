---
title: DXCoreAdapterState
description: Definiert Konstanten, die Arten von DXCore-Adapterzuständen angeben.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6878aaccb61fd164fcf834561fcf70f13d2609de595687b6ef6301778c87f81e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119367080"
---
# <a name="dxcoreadapterstate-enum"></a>DXCoreAdapterState-Enum

Definiert Konstanten, die Arten von DXCore-Adapterzuständen angeben. Übergeben Sie eine dieser Konstanten an die [IDXCoreAdapter::QueryState-Methode,](./nf-dxcore_interface-idxcoreadapter-querystate.md) um das Adapterzustandselement für eine Zustandsart abzurufen. übergeben Sie eine Konstante an die [IDXCoreAdapter::SetState-Methode,](./nf-dxcore_interface-idxcoreadapter-setstate.md) um die Informationen eines Adapters für ein Zustandselement zu festlegen.

## <a name="syntax"></a>Syntax

```cpp
enum class DXCoreAdapterState : uint32_t
{
  IsDriverUpdateInProgress = 0,
  AdapterMemoryBudget = 1
};
```

## <a name="constants"></a>Konstanten

### <a name="isdriverupdateinprogress"></a>IsDriverUpdateInProgress

Gibt den <em>IsDriverUpdateInProgress-Adapterstatus</em> an, der angibt, dass ein Treiberupdate auf dem Adapter initiiert, aber noch `true` nicht abgeschlossen wurde. Wenn das Treiberupdate bereits abgeschlossen wurde, wurde der Adapter ungültig gemacht, und Ihr [QueryState-Aufruf](./nf-dxcore_interface-idxcoreadapter-querystate.md) gibt ein <b>HRESULT</b> von <b>DXGI_ERROR_DEVICE_REMOVED.</b>

Beim Aufrufen [von QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md)hat das <em>Zustandselement IsDriverUpdateInProgress</em> den Typ uint8_t <b>,</b>der einen booleschen Wert darstellt.

<b>Wichtig</b>. Dieses Zustandselement wird für [SetState nicht unterstützt.](./nf-dxcore_interface-idxcoreadapter-setstate.md)

### <a name="adaptermemorybudget"></a>AdapterMemoryBudget

Gibt den <em>AdapterMemoryBudget-Adapterstatus</em> an, der das Adapterspeicherbudget auf dem Adapter abruft oder angibt.

Beim Aufrufen [von QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md)weist der <em>AdapterMemoryBudget-Adapterstatus</em> den Typ <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> für *inputStateDetails* und <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudget">den Typ DXCoreAdapterMemoryBudget</a> für *outputBuffer auf.*

## <a name="see-also"></a>Weitere Informationen

[IDXCoreAdapter::QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), [IDXCoreAdapter::SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), [DXCore-Referenz](../dxcore-reference.md), Verwenden von DXCore zum [Aufzählen von Adaptern](../dxcore-enum-adapters.md)