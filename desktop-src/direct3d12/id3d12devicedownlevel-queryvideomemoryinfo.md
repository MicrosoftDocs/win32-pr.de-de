---
title: ID3D12DeviceDownlevel::QueryVideoMemoryInfo-Methode
description: Kopiert Inhalte aus einer Direct3D 12 Texture2D-Ressource in ein Fenster. | ID3D12DeviceDownlevel::QueryVideoMemoryInfo-Methode
keywords:
- QueryVideoMemoryInfo-Methode
- QueryVideoMemoryInfo-Methode, ID3D12DeviceDownlevel-Schnittstelle
- ID3D12DeviceDownlevel-Schnittstelle, QueryVideoMemoryInfo-Methode
topic_type:
- apiref
api_name:
- ID3D12DeviceDownlevel.QueryVideoMemoryInfo
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 526d25e8331fc949eb470c0813a083774afddc94312ed6751aaab9672e557d3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124108"
---
# <a name="id3d12devicedownlevelqueryvideomemoryinfo-method"></a>ID3D12DeviceDownlevel::QueryVideoMemoryInfo-Methode

Stellt Speicherstatistiken für Windows 7 bereit. Diese Methode entspricht [IDXGIAdapter3::QueryVideoMemoryInfo](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo), die in Windows 7 nicht verfügbar ist.

## <a name="syntax"></a>Syntax

```cpp
HRESULT QueryVideoMemoryInfo( 
    UINT NodeIndex,
    DXGI_MEMORY_SEGMENT_GROUP MemorySegmentGroup,
    DXGI_QUERY_VIDEO_MEMORY_INFO *pVideoMemoryInfo
);
```

## <a name="parameters"></a>Parameter

`NodeIndex`

Typ: **UINT**

Gibt den physischen Adapter des Geräts an, für den die Videospeicherinformationen abgefragt werden. Legen Sie diese Einstellung für einen Einzel-GPU-Vorgang auf 0 (null) fest. Wenn mehrere GPU-Knoten vorhanden sind, legen Sie diese auf den Index des Knotens (physischer Adapter des Geräts) fest, für den die Videospeicherinformationen abgefragt werden. Weitere Informationen finden Sie unter [Systeme mit mehreren Adaptern.](multi-engine.md)

`MemorySegmentGroup`

Typ: **[DXGI_MEMORY_SEGMENT_GROUP](/windows/win32/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)**

Gibt einen **DXGI_MEMORY_SEGMENT_GROUP** an, der die Gruppe als lokal oder nicht lokal identifiziert.

`pVideoMemoryInfo`

Typ: **[DXGI_QUERY_VIDEO_MEMORY_INFO](/windows/win32/api/dxgi1_4/ns-dxgi1_4-dxgi_query_video_memory_info)\***

Füllt eine **DXGI_QUERY_VIDEO_MEMORY_INFO-Struktur** mit den aktuellen Werten auf.

## <a name="return-value"></a>Rückgabewert

Gibt **S_OK** bei Erfolg oder andernfalls ein fehlerhaftes HRESULT zurück.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------|------------------|
| Header | d3d12downlevel.h und dxgi1_4.h |
| DLL    | D3D12.dll (nur Windows 7) |

## <a name="see-also"></a>Weitere Informationen
* [ID3D12DeviceDownlevel](id3d12devicedownlevel.md)
* [Direct3D 12 auf Windows 7-Schnittstellen](direct3d-12on7-interfaces.md)
* [Direct3D 12 auf Windows 7-Referenz (d3d12downlevel.h)](direct3d-12on7-reference.md)
* [Direct3D 12 unter Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
