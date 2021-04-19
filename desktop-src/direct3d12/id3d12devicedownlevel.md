---
title: ID3D12DeviceDownlevel-Schnittstelle
description: Stellt eine Windows-7-spezifische Abfrage für die Speicher Statistik bereit.
keywords:
- ID3D12DeviceDownlevel-Schnittstelle
topic_type:
- apiref
api_name:
- ID3D12DeviceDownlevel
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 401cbd0045211ef51e3ef6b06042262964ae2ec5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373483"
---
# <a name="id3d12devicedownlevel-interface"></a>ID3D12DeviceDownlevel-Schnittstelle

Auf diese Schnittstelle kann über **QueryInterface** von einem [Direct3D 12-Gerät](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) aus zugegriffen werden, wenn [Direct3D 12 unter Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)verwendet wird. Es stellt eine Windows-7-spezifische Abfrage für die Speicher Statistik bereit.

### <a name="methods"></a>Methoden

Die **ID3D12DeviceDownlevel** -Schnittstelle verfügt über diese Methoden.

| Methode | BESCHREIBUNG |
|:-------|:------------|
| [**Queryvideomemoryinfo**](id3d12devicedownlevel-queryvideomemoryinfo.md) | Stellt Arbeitsspeicher Statistiken für Windows 7 bereit. |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------|------------------|
| Header | d3d12downlevel. h |
| DLL    | D3D12.dll (nur Windows 7) |

## <a name="see-also"></a>Siehe auch
* [Direct3D 12 auf Windows 7-Schnittstellen](direct3d-12on7-interfaces.md)
* [Referenz zu Direct3D 12 auf Windows 7 (d3d12downlevel. h)](direct3d-12on7-reference.md)
* [Direct3D 12 unter Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
