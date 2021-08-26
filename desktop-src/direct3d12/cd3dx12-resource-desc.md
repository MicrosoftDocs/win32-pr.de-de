---
title: CD3DX12_RESOURCE_DESC -Struktur (D3dx12.h)
description: Eine Hilfsstruktur, um eine einfache Initialisierung einer D3D12 \_ RESOURCE \_ DESC-Struktur zu ermöglichen.
ms.assetid: F18D41BE-8AEF-444E-AC8B-EC57C63BF083
keywords:
- CD3DX12_RESOURCE_DESC-Struktur
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c9d92953abdb0cf77a7a55f7b64341b857a111baaef0d84d4d44855b02efb2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028300"
---
# <a name="cd3dx12_resource_desc-structure"></a>CD3DX12 \_ RESOURCE \_ DESC-Struktur

Eine Hilfsstruktur, um eine einfache Initialisierung einer [**D3D12 \_ RESOURCE \_ DESC-Struktur zu**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_RESOURCE_DESC  : public D3D12_RESOURCE_DESC{
                        CD3DX12_RESOURCE_DESC();
                        explicit CD3DX12_RESOURCE_DESC(const D3D12_RESOURCE_DESC& o);
                        CD3DX12_RESOURCE_DESC(D3D12_RESOURCE_DIMENSION dimension, UINT64 alignment, UINT64 width, UINT height, UINT16 depthOrArraySize, UINT16 mipLevels, DXGI_FORMAT format, UINT sampleCount, UINT sampleQuality, D3D12_TEXTURE_LAYOUT layout, D3D12_RESOURCE_FLAGS flags);
  CD3DX12_RESOURCE_DESC static inline Buffer(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE);
  CD3DX12_RESOURCE_DESC static inline Buffer(UINT64 width, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex1D(DXGI_FORMAT format, UINT64 width, UINT16 arraySize = 1, UINT16 mipLevels = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex2D(DXGI_FORMAT format, UINT64 width, UINT height, UINT16 arraySize = 1, UINT16 mipLevels = 0, UINT sampleCount = 1, UINT sampleQuality = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex3D(DXGI_FORMAT format, UINT64 width, UINT height, UINT16 depth, UINT16 mipLevels = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  UINT16                inline Depth() const;
  UINT16                inline ArraySize() const;
  UINT8                 inline PlaneCount(ID3D12Device* pDevice) const;
  UINT                  inline Subresources(ID3D12Device* pDevice) const;
  UINT                  inline CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice);
                        operator const D3D12_RESOURCE_DESC&() const;
                        operator == (const D3D12_RESOURCE_DESC& l, const D3D12_RESOURCE_DESC& r);
                        operator !=  (const D3D12_RESOURCE_DESC& l, const D3D12_RESOURCE_DESC& r);
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ RESOURCE \_ DESC()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ RESOURCE \_ DESC.

</dd> <dt>

**explizites CD3DX12 \_ RESOURCE \_ DESC(const D3D12 \_ RESOURCE \_ DESC& o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 RESOURCE DESC, initialisiert mit dem Inhalt einer anderen \_ \_ [**D3D12 \_ RESOURCE \_ DESC-Struktur.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)

</dd> <dt>

**CD3DX12 \_ RESOURCE \_ DESC(D3D12 \_ RESOURCE DIMENSION \_ dimension, UINT64 alignment, UINT64 width, UINT height, UINT16 depthOrArraySize, UINT16 mipLevels, DXGI \_ FORMAT format, UINT sampleCount, UINT sampleQuality, D3D12 \_ TEXTURE LAYOUT \_ layout, D3D12 \_ RESOURCE \_ FLAGS flags)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ RESOURCE \_ DESC und initialisiert die folgenden Parameter:

[**D3D12 \_ RESOURCE \_ DIMENSION-Dimension**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)

UINT64-Ausrichtung

UINT64-Breite

UINT-Höhe

UINT16 depthOrArraySize

UINT16 mipLevels

[**DXGI \_ FORMAT-Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

UINT sampleCount

UINT sampleQuality

[**D3D12 \_ \_TEXTURLAYOUT-Layout**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)

[**D3D12 \_ RESOURCE \_ FLAGS-Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags)

</dd> <dt>

**static inline Buffer(const D3D12 \_ RESOURCE ALLOCATION INFO& \_ \_ resAllocInfo, D3D12 \_ RESOURCE \_ FLAGS flags = D3D12 \_ RESOURCE FLAG \_ \_ NONE)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ RESOURCE \_ ALLOCATION \_ INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

(opt) [**D3D12 \_ RESOURCE \_ FLAGS-Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = D3D12 \_ RESOURCE FLAG \_ \_ NONE

</dd> <dt>

**static inline Buffer(UINT64 width, D3D12 \_ RESOURCE \_ FLAGS flags = D3D12 \_ RESOURCE FLAG \_ \_ NONE, UINT64 alignment = 0)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

UINT64-Breite

(opt) [**D3D12 \_ RESOURCE \_ FLAGS-Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = D3D12 \_ RESOURCE FLAG \_ \_ NONE

(opt) UINT64-Ausrichtung = 0

</dd> <dt>

**static inline Tex1D(DXGI \_ FORMAT format, UINT64 width, UINT16 arraySize = 1, UINT16 mipLevels = 0, D3D12 \_ RESOURCE \_ FLAGS flags = D3D12 \_ RESOURCE FLAG \_ \_ NONE, D3D12 \_ TEXTURE LAYOUT layout = \_ D3D12 \_ TEXTURE LAYOUT \_ \_ UNKNOWN, UINT64 alignment = 0)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**DXGI \_ FORMAT-Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

UINT64-Breite

(opt) UINT16 arraySize = 1

(opt) UINT16 mipLevels = 0

(opt) [**D3D12 \_ RESOURCE \_ FLAGS-Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = D3D12 \_ RESOURCE FLAG \_ \_ NONE

(opt) [**D3D12 \_ \_TEXTURLAYOUTlayout**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = D3D12 \_ \_ TEXTURLAYOUT \_ UNBEKANNT

(opt) UINT64-Ausrichtung = 0

</dd> <dt>

**static inline Tex2D(DXGI \_ FORMAT format, UINT64 Width, UINT height, UINT16 arraySize = 1, UINT16 mipLevels = 0, UINT sampleCount = 1, UINT sampleQuality = 0, D3D12 \_ RESOURCE \_ FLAGS flags = D3D12 \_ RESOURCE FLAG \_ \_ NONE, D3D12 \_ TEXTURE LAYOUT layout = \_ D3D12 \_ TEXTURE LAYOUT \_ \_ UNKNOWN, UINT64 alignment = 0)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**DXGI \_ FORMAT-Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

UINT64-Breite

UINT-Höhe

(opt) UINT16 arraySize = 1

(opt) UINT16 mipLevels = 0

(opt) UINT sampleCount = 1

(opt) UINT sampleQuality = 0

(opt) [**D3D12 \_ RESOURCE \_ FLAGS-Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = D3D12 \_ RESOURCE FLAG \_ \_ NONE

(opt) [**D3D12 \_ \_TEXTURLAYOUTlayout**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = D3D12 \_ \_ TEXTURLAYOUT \_ UNBEKANNT

(opt) UINT64-Ausrichtung = 0

</dd> <dt>

**static inline Tex3D(DXGI \_ FORMAT format, UINT64 width, UINT height, UINT16 depth, UINT16 mipLevels = 0, D3D12 \_ RESOURCE \_ FLAGS flags = D3D12 \_ RESOURCE FLAG \_ \_ NONE, D3D12 \_ TEXTURE LAYOUT layout = \_ D3D12 \_ TEXTURE LAYOUT \_ \_ UNKNOWN, UINT64 alignment = 0)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**DXGI \_ FORMAT-Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

UINT64-Breite

UINT-Höhe

UINT16-Tiefe

(opt) UINT16 mipLevels = 0

(opt) [**D3D12 \_ RESOURCE \_ FLAGS-Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = D3D12 \_ RESOURCE FLAG \_ \_ NONE

(opt) [**D3D12 \_ \_TEXTURLAYOUTlayout**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = D3D12 \_ \_ TEXTURLAYOUT \_ UNBEKANNT

(opt) UINT64-Ausrichtung = 0

</dd> <dt>

**inline Depth() const**
</dt> <dd>

Wenn Dimension == [**D3D12 \_ RESOURCE \_ DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D ist, gibt DepthOrArraySize zurück. Wenn Dimension != D3D12 \_ RESOURCE \_ DIMENSION \_ TEXTURE3D, gibt 1 zurück.

</dd> <dt>

**inline ArraySize() const**
</dt> <dd>

Wenn Dimension != D3D12 \_ RESOURCE \_ DIMENSION \_ TEXTURE3D, gibt DepthOrArraySize zurück. Wenn Dimension == D3D12 \_ RESOURCE \_ DIMENSION \_ TEXTURE3D ist, wird 1 zurückgegeben. Siehe [**D3D12 \_ RESOURCE \_ DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D.

</dd> <dt>

**inline PlaneCount(ID3D12Device \* pDevice) const**
</dt> <dd>

Gibt D3D12GetFormatPlaneCount(pDevice, Format) zurück. Siehe [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) und [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device).

</dd> <dt>

**inline Subresources(ID3D12Device \* pDevice) const**
</dt> <dd>

Gibt die Anzahl der Unterressourcen zurück, berechnet als MipLevels \* ArraySize() \* PlaneCount(pDevice).

</dd> <dt>

**inline CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice)**
</dt> <dd>

Berechnet einen Unterressourcenindex mithilfe von [**D3D12CalcSubresource.**](d3d12calcsubresource.md)

</dd> <dt>

**operator const D3D12 \_ RESOURCE \_ DESC&() const**
</dt> <dd>

Definiert den & pass-by-reference-Operator für den übergeordneten Strukturtyp.

</dd> <dt>

**operator == (const D3D12 \_ RESOURCE \_ DESC& l, const D3D12 \_ RESOURCE \_ DESC& r)**
</dt> <dd>

Gibt TRUE zurück, wenn alle Member jeder Struktur identisch sind.

</dd> <dt>

**operator != (const D3D12 \_ RESOURCE \_ DESC& l, const D3D12 \_ RESOURCE \_ DESC& r)**
</dt> <dd>

Gibt FALSE zurück, wenn alle Member jeder Struktur identisch sind.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12 \_ RESOURCE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

