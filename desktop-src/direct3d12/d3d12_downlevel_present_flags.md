---
title: D3D12_DOWNLEVEL_PRESENT_FLAGS-Enumeration
description: Flags, die an die ID3D12CommandQueueDownlevel::P Resent-Methode weitergegeben werden.
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
topic_type:
- APIRef
api_name:
- D3D12_DOWNLEVEL_PRESENT_FLAGS
api_type:
- HeaderDef
ms.openlocfilehash: 1ce1536945748bae09fc7a0981c14c076fc6394e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363959"
---
# <a name="d3d12_downlevel_present_flags-enumeration"></a>D3D12 \_ Downlevel \_ Present- \_ Flags-Enumeration

An die [**ID3D12CommandQueueDownlevel::P Resent**](id3d12commandqueuedownlevel-present.md) -Funktion übergebenen Flags, um das Verhalten zu ändern.

## <a name="syntax"></a>Syntax

```cpp
enum D3D12_DOWNLEVEL_PRESENT_FLAGS
{
    D3D12_DOWNLEVEL_PRESENT_FLAG_NONE = 0,
    D3D12_DOWNLEVEL_PRESENT_FLAG_WAIT_FOR_VBLANK = 1
};
```

## <a name="constants"></a>Konstanten

**D3D12 \_ Downlevel \_ Present- \_ Flag " \_ None"**

Es sind keine Optionen ausgewählt.

**D3D12 \_ Downlevel \_ Present- \_ Flag \_ warten \_ auf \_ vblank**

Der **aktuelle** Vorgang wird erst ausgeführt, wenn eine VSYNC seit dem letzten Mal ausgeführt wurde .

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------|------------------|
| Header | d3d12downlevel. h |
| DLL    | D3D12.dll (nur Windows 7) |

## <a name="see-also"></a>Siehe auch
* [ID3D12CommandQueueDownlevel](id3d12commandqueuedownlevel.md)
* [Direct3D 12 auf Windows 7-Enumerationen](direct3d-12on7-enumerations.md)
* [Referenz zu Direct3D 12 auf Windows 7 (d3d12downlevel. h)](direct3d-12on7-reference.md)
* [Direct3D 12 unter Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
