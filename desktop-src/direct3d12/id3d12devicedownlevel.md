---
title: ID3D12DeviceDownlevel-Schnittstelle
description: Stellt eine Windows-7-spezifische Abfrage zur Speicherstatistik zur Verfügung.
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
ms.openlocfilehash: 8cd9b39e865377734fca3d0791b89219d611f57f456a85a8f9b12e345aba9e99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124078"
---
# <a name="id3d12devicedownlevel-interface"></a>ID3D12DeviceDownlevel-Schnittstelle

Auf diese Schnittstelle kann über **QueryInterface** von einem [Direct3D 12-Gerät](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) aus zugegriffen werden, wenn [Direct3D 12](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)auf Windows 7 verwendet wird. Sie stellt eine Windows-7-spezifische Abfrage zur Speicherstatistik zur Verfügung.

### <a name="methods"></a>Methoden

Die **ID3D12DeviceDownlevel-Schnittstelle** verfügt über diese Methoden.

| Methode | Beschreibung |
|:-------|:------------|
| [**QueryVideoMemoryInfo**](id3d12devicedownlevel-queryvideomemoryinfo.md) | Stellt Speicherstatistiken für Windows 7 zur Verfügung. |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------|------------------|
| Header | d3d12downlevel.h |
| DLL    | D3D12.dll (nur Windows 7) |

## <a name="see-also"></a>Weitere Informationen
* [Direct3D 12 auf Windows 7-Schnittstellen](direct3d-12on7-interfaces.md)
* [Referenz zu Direct3D 12 Windows 7 (d3d12downlevel.h)](direct3d-12on7-reference.md)
* [Direct3D 12 unter Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
