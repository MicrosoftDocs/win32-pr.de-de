---
title: DXCoreHardwareID
description: Stellt die PnP-Hardware-ID-Teile für einen Adapter dar.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6882d9aa16bf72fb33f9a254a6434becb37f9cb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101771"
---
# <a name="dxcorehardwareid-structure"></a>Dxcorehardwareid-Struktur

Stellt die PnP-Hardware-ID-Teile für einen Adapter dar.

## <a name="syntax"></a>Syntax

```cpp
struct DXCoreHardwareID
{
  uint32_t vendorID;
  uint32_t deviceID;
  uint32_t subSysID;
  uint32_t revision;
};
```

## <a name="members"></a>Member

### <a name="vendorid"></a>vendorId

Typ: **uint32_t \***

Die PCI-ID des Hardwareherstellers des Adapters.

### <a name="deviceid"></a>deviceId

Typ: **uint32_t \***

Die PCI-ID des Hardware Geräts des Adapters.

### <a name="subsysid"></a>subsysid

Typ: **uint32_t \***

Die PCI-ID des Hardware Subsystems des Adapters.

### <a name="revision"></a>revision

Typ: **uint32_t \***

Die PCI-ID der Revisionsnummer des Adapters.

## <a name="see-also"></a>Siehe auch

[DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)