---
title: DXCoreAdapterPreference
description: Definiert Konstanten, die DXCore-Adapter Einstellungen angeben, die als Listen Sortierkriterien verwendet werden sollen.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 4301bdc1fe0ece8d9594ec3287e2ea8ddcce8f0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390745"
---
# <a name="dxcoreadapterpreference-enum"></a>Dxcoreadapterpreference-Aufzählung

## <a name="description"></a>BESCHREIBUNG

Definiert Konstanten, die DXCore-Adapter Einstellungen angeben, die als Listen Sortierkriterien verwendet werden sollen. Sie können eine DXCore-Adapter Liste sortieren, indem Sie ein Array von **dxcoreadapterpreference** an [idxcoreadapterlist:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md)übergeben.

## <a name="syntax"></a>Syntax

```cpp
enum class DXCoreAdapterPreference : uint32_t
{
  Hardware = 0,
  MinimumPower = 1,
  HighPerformance = 2
};
```

## <a name="enum-fields"></a>Aufzählungs Felder

### <a name="hardware"></a>Hardware

Gibt eine bevorzugte Einstellung für Hardware Adapter an (im Gegensatz zu Software Adaptern).

### <a name="minimumpower"></a>Minimumpower

Gibt eine bevorzugte GPU (z. b. einen integrierten Grafikprozessor oder igpu) an.

### <a name="highperformance"></a>HighPerformance

Gibt die bevorzugte GPU an, z. b. einen externen Grafikprozessor (xgpu), falls verfügbar, oder einen diskreten Grafikprozessor (dGPU), falls verfügbar.

## <a name="see-also"></a>Siehe auch

[Idxcoreadapterlist:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)