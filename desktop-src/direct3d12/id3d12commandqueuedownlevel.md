---
title: ID3D12CommandQueueDownlevel-Schnittstelle
description: Stellt einen Windows-7-spezifischen, vorhandenen Mechanismus bereit.
keywords:
- ID3D12CommandQueueDownlevel-Schnittstelle
topic_type:
- apiref
api_name:
- ID3D12CommandQueueDownlevel
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 6f2aee6fd1b0f58469162c640d92aeb187bd9641
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370401"
---
# <a name="id3d12commandqueuedownlevel-interface"></a>ID3D12CommandQueueDownlevel-Schnittstelle

Auf diese Schnittstelle kann über **QueryInterface** aus einer [Direct3D 12-Befehls Warteschlange](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) zugegriffen werden, wenn [Direct3D 12 unter Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)verwendet wird. Es stellt einen Windows-7-spezifischen Mechanismus bereit.

### <a name="methods"></a>Methoden

Die **ID3D12CommandQueueDownlevel** -Schnittstelle verfügt über diese Methoden.

| Methode | BESCHREIBUNG |
|:-------|:------------|
| [**Anzahl**](id3d12commandqueuedownlevel-present.md) | Kopiert Inhalt aus einer D3D12 Texture2D-Ressource in ein-Fenster. |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------|------------------|
| Header | d3d12downlevel. h |
| DLL    | D3D12.dll (nur Windows 7) |

## <a name="see-also"></a>Siehe auch
* [Direct3D 12 auf Windows 7-Schnittstellen](direct3d-12on7-interfaces.md)
* [Referenz zu Direct3D 12 auf Windows 7 (d3d12downlevel. h)](direct3d-12on7-reference.md)
* [Direct3D 12 unter Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
