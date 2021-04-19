---
title: 'ID3D12DeviceDownlevel:: queryvideomemoryinfo-Methode'
description: 'Kopiert Inhalt aus einer Direct3D 12 Texture2D-Ressource in ein-Fenster. | ID3D12DeviceDownlevel:: queryvideomemoryinfo-Methode'
keywords:
- Queryvideomemoryinfo-Methode
- Queryvideomemoryinfo-Methode, ID3D12DeviceDownlevel-Schnittstelle
- ID3D12DeviceDownlevel Interface, queryvideomemoryinfo-Methode
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
ms.openlocfilehash: 32b93fcbbe44aaae0916e6d8f3f403eb960e26eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355214"
---
# <a name="id3d12devicedownlevelqueryvideomemoryinfo-method"></a>ID3D12DeviceDownlevel:: queryvideomemoryinfo-Methode

Stellt Arbeitsspeicher Statistiken für Windows 7 bereit. Diese Methode entspricht [IDXGIAdapter3:: queryvideomemoryinfo](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo), die unter Windows 7 nicht verfügbar ist.

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

Typ: **uint**

Gibt den physischen Adapter des Geräts an, für den die Informationen zum Videospeicher abgefragt werden. Legen Sie für einen Single-GPU-Vorgang NULL fest. Wenn mehrere GPU-Knoten vorhanden sind, legen Sie diese auf den Index des Knotens (den physischen Adapter des Geräts) fest, für den die Informationen zum Videospeicher abgefragt werden. Weitere Informationen finden Sie unter [multiadaptersysteme](multi-engine.md).

`MemorySegmentGroup`

Typ: **[DXGI_MEMORY_SEGMENT_GROUP](/windows/win32/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)**

Gibt eine **DXGI_MEMORY_SEGMENT_GROUP** an, die die Gruppe als lokal oder nicht lokal identifiziert.

`pVideoMemoryInfo`

Typ: **[DXGI_QUERY_VIDEO_MEMORY_INFO](/windows/win32/api/dxgi1_4/ns-dxgi1_4-dxgi_query_video_memory_info)\***

Füllt eine **DXGI_QUERY_VIDEO_MEMORY_INFO** Struktur mit den aktuellen Werten aus.

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg **S_OK** oder andernfalls ein fehlerhaftes HRESULT zurück.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------|------------------|
| Header | d3d12downlevel. h und dxgi1_4. h |
| DLL    | D3D12.dll (nur Windows 7) |

## <a name="see-also"></a>Siehe auch
* [ID3D12DeviceDownlevel](id3d12devicedownlevel.md)
* [Direct3D 12 auf Windows 7-Schnittstellen](direct3d-12on7-interfaces.md)
* [Referenz zu Direct3D 12 auf Windows 7 (d3d12downlevel. h)](direct3d-12on7-reference.md)
* [Direct3D 12 unter Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
