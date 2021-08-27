---
title: DXCoreAdapterPreference
description: Definiert Konstanten, die DXCore-Adaptereinstellungen angeben, die als Listensortierkriterien verwendet werden sollen.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: a58f2c948751d5217a89e52bc862057ac6a67c85bdf2fabed96c2b5ad68364cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117730"
---
# <a name="dxcoreadapterpreference-enum"></a>DXCoreAdapterPreference-Enum

## <a name="description"></a>Beschreibung

Definiert Konstanten, die DXCore-Adaptereinstellungen angeben, die als Listensortierkriterien verwendet werden sollen. Sie können eine DXCore-Adapterliste sortieren, indem Sie ein Array von **DXCoreAdapterPreference** an [IDXCoreAdapterList::Sort übergeben.](./nf-dxcore_interface-idxcoreadapterlist-sort.md)

## <a name="syntax"></a>Syntax

```cpp
enum class DXCoreAdapterPreference : uint32_t
{
  Hardware = 0,
  MinimumPower = 1,
  HighPerformance = 2
};
```

## <a name="enum-fields"></a>Aufzählfelder

### <a name="hardware"></a>Hardware

Gibt eine Einstellung für Hardwareadapter an (im Gegensatz zu Softwareadaptern).

### <a name="minimumpower"></a>MinimumPower

Gibt eine Einstellung für die minimal betriebene GPU an (z. B. einen integrierten Grafikprozessor oder iGPU).

### <a name="highperformance"></a>HighPerformance

Gibt eine Einstellung für die GPU mit der höchsten Leistung an, z. B. einen externen Grafikprozessor (xGPU), sofern verfügbar, oder einen diskreten Grafikprozessor (Discrete Graphics Processor, dGPU), sofern verfügbar.

## <a name="see-also"></a>Siehe auch

[IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md), [DXCore-Referenz](../dxcore-reference.md), Verwenden von DXCore zum [Auflisten von Adaptern](../dxcore-enum-adapters.md)