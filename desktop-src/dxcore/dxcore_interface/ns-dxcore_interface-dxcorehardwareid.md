---
title: DXCoreHardwareID
description: Stellt die PnP-Hardware-ID-Teile für einen Adapter dar.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 68cdb130dd6f0c0338e5b94da2f68c58f98bb91d404871e18ac82e817881117c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118627"
---
# <a name="dxcorehardwareid-structure"></a>DXCoreHardwareID-Struktur

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

### <a name="vendorid"></a>Vendorid

Typ: **uint32_t \***

Die PCI-ID des Hardwareanbieters des Adapters.

### <a name="deviceid"></a>deviceId

Typ: **uint32_t \***

Die PCI-ID des Hardwaregeräts des Adapters.

### <a name="subsysid"></a>subSysId

Typ: **uint32_t \***

Die PCI-ID des Hardwaresubsystems des Adapters.

### <a name="revision"></a>revision

Typ: **uint32_t \***

Die PCI-ID der Revisionsnummer des Adapters.

## <a name="see-also"></a>Weitere Informationen

[DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md)