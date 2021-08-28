---
title: CD3DX12_RESOURCE_DESC1 -Struktur (D3dx12.h)
description: Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3DX12_RESOURCE_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instancing_desc) ermöglicht.
keywords:
- CD3DX12_RESOURCE_DESC1-Struktur
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_DESC1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2021
ms.openlocfilehash: 87fe62c475e1d961258671355c4c9be133bf0a41
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813236"
---
# <a name="cd3dx12_resource_desc1-structure"></a>CD3DX12_RESOURCE_DESC1-Struktur

Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3DX12_RESOURCE_DESC1**](/windows/win32/api/d3d12/D3DX12_RESOURCE_DESC1/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1) ermöglicht.

## <a name="syntax"></a>Syntax

```cpp
struct CD3DX12_RESOURCE_DESC1 : public D3D12_RESOURCE_DESC1
{
    CD3DX12_RESOURCE_DESC1();
    explicit CD3DX12_RESOURCE_DESC1(const D3D12_RESOURCE_DESC1& o) noexcept;
    CD3DX12_RESOURCE_DESC1(
        D3D12_RESOURCE_DIMENSION dimension,
        UINT64 alignment,
        UINT64 width,
        UINT height,
        UINT16 depthOrArraySize,
        UINT16 mipLevels,
        DXGI_FORMAT format,
        UINT sampleCount,
        UINT sampleQuality,
        D3D12_TEXTURE_LAYOUT layout,
        D3D12_RESOURCE_FLAGS flags,
        UINT samplerFeedbackMipRegionWidth = 0,
        UINT samplerFeedbackMipRegionHeight = 0,
        UINT samplerFeedbackMipRegionDepth = 0) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Buffer(
        const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Buffer(
        UINT64 width,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE,
        UINT64 alignment = 0) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Tex1D(
        DXGI_FORMAT format,
        UINT64 width,
        UINT16 arraySize = 1,
        UINT16 mipLevels = 0,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE,
        D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN,
        UINT64 alignment = 0) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Tex2D(
        DXGI_FORMAT format,
        UINT64 width,
        UINT height,
        UINT16 arraySize = 1,
        UINT16 mipLevels = 0,
        UINT sampleCount = 1,
        UINT sampleQuality = 0,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE,
        D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN,
        UINT64 alignment = 0,
        UINT samplerFeedbackMipRegionWidth = 0,
        UINT samplerFeedbackMipRegionHeight = 0,
        UINT samplerFeedbackMipRegionDepth = 0) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Tex3D(
        DXGI_FORMAT format,
        UINT64 width,
        UINT height,
        UINT16 depth,
        UINT16 mipLevels = 0,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE,
        D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN,
        UINT64 alignment = 0) noexcept;
    inline UINT16 Depth() const noexcept;
    inline UINT16 ArraySize() const noexcept;
    inline UINT8 PlaneCount(_In_ ID3D12Device* pDevice) const noexcept;
    inline UINT Subresources(_In_ ID3D12Device* pDevice) const noexcept;
    inline UINT CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice) noexcept;
};
inline bool operator==(const D3D12_RESOURCE_DESC1& l, const D3D12_RESOURCE_DESC1& r) noexcept;
inline bool operator!=(const D3D12_RESOURCE_DESC1& l, const D3D12_RESOURCE_DESC1& r) noexcept;
```

## <a name="members"></a>Member

`CD3DX12_RESOURCE_DESC1`

Standardkonstruktor Erstellt eine neue, nicht initialisierte Instanz eines **CD3DX12_RESOURCE_DESC1.**

`CD3DX12_RESOURCE_DESC1(const D3D12_RESOURCE_DESC1&)`

Konstruktor, der eine neue Instanz eines **-CD3DX12_RESOURCE_DESC1** mit dem Inhalt einer -Struktur [**D3DX12_RESOURCE_DESC1**](/windows/win32/api/d3d12/D3DX12_RESOURCE_DESC1/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1) initialisiert wird.

`CD3DX12_RESOURCE_DESC1(D3D12_RESOURCE_DIMENSION, UINT64, UINT64, UINT, UINT16, UINT16, DXGI_FORMAT, UINT, UINT, D3D12_TEXTURE_LAYOUT, D3D12_RESOURCE_FLAGS, UINT = 0, UINT = 0, UINT = 0)`

Konstruktor, der eine neue Instanz eines **-CD3DX12_RESOURCE_DESC1** mit den übergebenen Parametern initialisiert wird.

`Buffer(const D3D12_RESOURCE_ALLOCATION_INFO&, D3D12_RESOURCE_FLAGS = D3D12_RESOURCE_FLAG_NONE)`

Eine statische Funktion, die eine neue  Instanz eines -Werts erstellt und zurückgibt CD3DX12_RESOURCE_DESC1 mit diesen Werten initialisiert wird.

|Datenelement|Wert|
|-|-|
|Dimension|D3D12_RESOURCE_DIMENSION_BUFFER|
|Ausrichtung|*resAllocInfo*. Ausrichtung|
|Width|*resAllocInfo*. SizeInBytes|
|Height|1|
|DepthOrArraySize|1|
|MipLevels|1|
|Format|DXGI_FORMAT_UNKNOWN|
|SampleDesc.Count|1|
|SampleDesc.Quality|0|
|Layout|D3D12_TEXTURE_LAYOUT_ROW_MAJOR|
|Flags|*flags*|
|SamplerFeedbackMipRegion.Width|0|
|SamplerFeedbackMipRegion.Height|0|
|SamplerFeedbackMipRegion.Depth|0|

`Buffer(UINT64, D3D12_RESOURCE_FLAGS = D3D12_RESOURCE_FLAG_NONE, UINT64 = 0)`

Eine statische Funktion, die eine neue  Instanz eines -Werts erstellt und zurückgibt CD3DX12_RESOURCE_DESC1 mit diesen Werten initialisiert wird.

|Datenelement|Wert|
|-|-|
|Dimension|D3D12_RESOURCE_DIMENSION_BUFFER|
|Ausrichtung|*Ausrichtung*|
|Width|*width*|
|Height|1|
|DepthOrArraySize|1|
|MipLevels|1|
|Format|DXGI_FORMAT_UNKNOWN|
|SampleDesc.Count|1|
|SampleDesc.Quality|0|
|Layout|D3D12_TEXTURE_LAYOUT_ROW_MAJOR|
|Flags|*flags*|
|SamplerFeedbackMipRegion.Width|0|
|SamplerFeedbackMipRegion.Height|0|
|SamplerFeedbackMipRegion.Depth|0|

`Tex1D(DXGI_FORMAT, UINT64, UINT16 = 1, UINT16 = 0, D3D12_RESOURCE_FLAGS D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 = 0)`

Eine statische Funktion, die eine neue  Instanz eines -Werts erstellt und zurückgibt CD3DX12_RESOURCE_DESC1 mit diesen Werten initialisiert wird.

|Datenelement|Wert|
|-|-|
|Dimension|D3D12_RESOURCE_DIMENSION_TEXTURE1D|
|Ausrichtung|*Ausrichtung*|
|Width|*width*|
|Height|1|
|DepthOrArraySize|*arraySize*|
|MipLevels|*mipLevels*|
|Format|*format*|
|SampleDesc.Count|1|
|SampleDesc.Quality|0|
|Layout|*Layout*|
|Flags|*flags*|
|SamplerFeedbackMipRegion.Width|0|
|SamplerFeedbackMipRegion.Height|0|
|SamplerFeedbackMipRegion.Depth|0|

`Tex2D(DXGI_FORMAT, UINT64, UINT, UINT16 = 1, UINT16 = 0, UINT = 1, UINT = 0, D3D12_RESOURCE_FLAGS = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 = 0, UINT = 0, UINT = 0, UINT = 0)`

Eine statische Funktion, die eine neue Instanz eines **CD3DX12_RESOURCE_DESC1** mit diesen Werten initialisiert erstellt und zurückgibt.

|Datenelement|Wert|
|-|-|
|Dimension|D3D12_RESOURCE_DIMENSION_TEXTURE2D|
|Ausrichtung|*Ausrichtung*|
|Width|*width*|
|Height|*height*|
|DepthOrArraySize|*arraySize*|
|MipLevels|*mipLevels*|
|Format|*format*|
|SampleDesc.Count|*sampleCount*|
|SampleDesc.Quality|*sampleQuality*|
|Layout|*Layout*|
|Flags|*flags*|
|SamplerFeedbackMipRegion.Width|*samplerFeedbackMipRegionWidth*|
|SamplerFeedbackMipRegion.Height|*samplerFeedbackMipRegionHeight*|
|SamplerFeedbackMipRegion.Depth|*samplerFeedbackMipRegionDepth*|

`Tex3D(DXGI_FORMAT, UINT64, UINT, UINT16, UINT16 = 0, D3D12_RESOURCE_FLAGS = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 = 0)`

Eine statische Funktion, die eine neue Instanz eines **CD3DX12_RESOURCE_DESC1** mit diesen Werten initialisiert erstellt und zurückgibt.

|Datenelement|Wert|
|-|-|
|Dimension|D3D12_RESOURCE_DIMENSION_TEXTURE3D|
|Ausrichtung|*Ausrichtung*|
|Width|*width*|
|Height|*height*|
|DepthOrArraySize|*Tiefe*|
|MipLevels|*mipLevels*|
|Format|*format*|
|SampleDesc.Count|1|
|SampleDesc.Quality|0|
|Layout|*Layout*|
|Flags|*flags*|
|SamplerFeedbackMipRegion.Width|0|
|SamplerFeedbackMipRegion.Height|0|
|SamplerFeedbackMipRegion.Depth|0|

`Depth`

Gibt einen **UINT16-Wert** zurück, der die Tiefe der Ressource enthält.

`ArraySize`

Gibt einen **UINT16-Wert** zurück, der die Arraygröße der Ressource enthält.

`PlaneCount(ID3D12Device*)`

Gibt einen **UINT8-Wert** zurück, der die Ebenenanzahl für das Format der Ressource enthält.

`Subresources(ID3D12Device*)`

Gibt einen **UINT** zurück, der die Anzahl der Unterressourcen in der Ressource enthält.

`CalcSubresource(UINT, UINT, UINT)`

Füllt einen **UINT** mit einem Unterressourcenindex für die Ressource basierend auf den übergebenen Parametern auf und gibt ihn zurück.

`operator==(const D3D12_RESOURCE_DESC1&, const D3D12_RESOURCE_DESC1&)`

Eine freie Funktion, die `true` zurückgibt, wenn die beiden Parameter memberweise gleich sind, andernfalls `false` .

`operator!=(const D3D12_RESOURCE_DESC1&, const D3D12_RESOURCE_DESC1&)`

Eine freie Funktion, die `true` zurückgibt, wenn die beiden Parameter memberweise ungleich sind, andernfalls `false` .

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Siehe auch

* [D3DX12_RESOURCE_DESC1](/windows/win32/api/d3d12/D3DX12_RESOURCE_DESC1/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1)
* [Hilfsstrukturen für Direct3D 12](helper-structures-for-d3d12.md)
