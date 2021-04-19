---
title: CD3DX12_RESOURCE_DESC-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12 \_ Resource \_ DESC-Struktur zu ermöglichen.
ms.assetid: F18D41BE-8AEF-444E-AC8B-EC57C63BF083
keywords:
- CD3DX12_RESOURCE_DESC Struktur
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
ms.openlocfilehash: 1b341646b2dee7f469235c0b0bc9bb4550e56ff5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351987"
---
# <a name="cd3dx12_resource_desc-structure"></a>CD3DX12 Ressourcen-zu- \_ \_ Struktur-Struktur

Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12 \_ Resource \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) -Struktur zu ermöglichen.

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

**CD3DX12- \_ Ressource \_ ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12- \_ Ressource \_ .

</dd> <dt>

**explizites CD3DX12 Resource Manager- \_ Ressourcen \_ (konstant D3D12 \_ Ressourcen- \_& o)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12- \_ Ressource \_ , die mit dem Inhalt einer anderen [**D3D12 \_ Resource \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) -Debug-Struktur initialisiert wird.

</dd> <dt>

**CD3DX12 \_ Resource \_ DESC (D3D12 \_ Resource \_ Dimension Dimension, UINT64 Alignment, UINT64 Width, uint Height, UInt16 depthorarraysize, UInt16 miplevels, DXGI \_ Format Format, uint samplecount, uint samplequality, D3D12 \_ Texture \_ Layout Layout, D3D12 \_ \_ Ressourcenflags Flags)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 \_ Resource \_ DESC und initialisiert die folgenden Parameter:

[**D3D12 \_ Dimension der Ressourcen \_ Dimension**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)

UINT64-Ausrichtung

UINT64-Breite

Uint-Höhe

UInt16 depthorarraysize

UInt16 miplevels

[**DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Format

Uint-samplecount

Uint samplequality

[**D3D12 \_ Layout des Textur \_ Layouts**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)

[**D3D12 \_ \_Ressourcenflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) -Flags

</dd> <dt>

**statischer Inline Puffer (Konstante D3D12 \_ Ressourcen \_ Zuordnungs \_ Info& resallocinfo, \_ D3D12 \_ Ressourcenflags Flags = D3D12 \_ \_ ressourcenflag \_ None)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ \_ \_ Informationen zur Ressourcenzuweisung**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resallocinfo

Opt [**D3D12 \_ \_Ressourcenflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) Flags = \_ D3D12 \_ ressourcenflag " \_ None"

</dd> <dt>

**statischer Inline Puffer (UINT64 Width, \_ D3D12 \_ Ressourcenflags Flags = D3D12 \_ \_ ressourcenflag \_ None, UINT64 Alignment = 0)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

UINT64-Breite

Opt [**D3D12 \_ \_Ressourcenflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) Flags = \_ D3D12 \_ ressourcenflag " \_ None"

Opt UINT64 Alignment = 0

</dd> <dt>

**static Inline Tex1D (DXGI \_ Format Format, UINT64 Width, UInt16 arraySize = 1, UInt16 miplevels = 0, D3D12 \_ \_ Ressourcenflags Flags = \_ D3D12 \_ ressourcentflag \_ None, D3D12 \_ Texture \_ Layout Layout = D3D12 \_ Texture \_ Layout \_ unknown, UINT64 Alignment = 0)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Format

UINT64-Breite

Opt UInt16 arraySize = 1

Opt UInt16 miplevels = 0

Opt [**D3D12 \_ \_Ressourcenflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) Flags = \_ D3D12 \_ ressourcenflag " \_ None"

Opt [**D3D12 \_ Layout des Textur \_ Layouts**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = D3D12 \_ Textur \_ Layout \_ unbekannt

Opt UINT64 Alignment = 0

</dd> <dt>

**static Inline Tex2D (DXGI \_ Format Format, UINT64 Width, uint Height, UInt16 arraySize = 1, UInt16 miplevels = 0, uint samplecount = 1, uint samplequality = 0, D3D12 \_ \_ Ressourcenflags Flags = D3D12 \_ Resource \_ Flag \_ None, D3D12 \_ Texture \_ Layout Layout = D3D12 \_ Texture \_ Layout \_ unknown, UINT64 Alignment = 0)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Format

UINT64-Breite

Uint-Höhe

Opt UInt16 arraySize = 1

Opt UInt16 miplevels = 0

Opt Uint samplecount = 1

Opt Uint samplequality = 0

Opt [**D3D12 \_ \_Ressourcenflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) Flags = \_ D3D12 \_ ressourcenflag " \_ None"

Opt [**D3D12 \_ Layout des Textur \_ Layouts**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = D3D12 \_ Textur \_ Layout \_ unbekannt

Opt UINT64 Alignment = 0

</dd> <dt>

**static Inline Tex3D (DXGI \_ Format Format, UINT64 Width, uint Height, UInt16 Tiefe, UInt16 miplevels = 0, D3D12 \_ \_ Ressourcenflags Flags = \_ D3D12 \_ ressourcentflag \_ None, D3D12 \_ Texture Layout \_ Layout = D3D12 \_ Texture \_ Layout \_ unknown, UINT64 Alignment = 0)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Format

UINT64-Breite

Uint-Höhe

UInt16 Tiefe

Opt UInt16 miplevels = 0

Opt [**D3D12 \_ \_Ressourcenflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) Flags = \_ D3D12 \_ ressourcenflag " \_ None"

Opt [**D3D12 \_ Layout des Textur \_ Layouts**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = D3D12 \_ Textur \_ Layout \_ unbekannt

Opt UINT64 Alignment = 0

</dd> <dt>

**Inline Tiefe () konstant**
</dt> <dd>

Wenn Dimension = = [**D3D12 \_ Resource \_ Dimension**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D, wird depthorarraysize zurückgegeben. Wenn Dimension! = D3D12 \_ Resource \_ Dimension \_ TEXTURE3D, wird 1 zurückgegeben.

</dd> <dt>

**Inline arraySize () konstant**
</dt> <dd>

Wenn Dimension! = D3D12 \_ Resource \_ Dimension \_ TEXTURE3D, wird depthorarraysize zurückgegeben. Wenn Dimension = = D3D12 \_ Resource \_ Dimension \_ TEXTURE3D, wird 1 zurückgegeben. Weitere Informationen finden Sie unter [**D3D12 \_ Resource \_ Dimension**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D.

</dd> <dt>

**Inline planecount (ID3D12Device \* pdevice) konstant**
</dt> <dd>

Gibt D3D12GetFormatPlaneCount (pdevice, Format) zurück. Siehe [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) und [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device).

</dd> <dt>

**Inline-unter Berichte (ID3D12Device \* pdevice) konstant**
</dt> <dd>

Gibt die Anzahl der unter Ressourcen zurück, die als miplevels \* arraySize () \* planecount (pdevice) berechnet werden.

</dd> <dt>

**Inline-calcsubresource (uint mipslice, uint arrayslice, uint planeslice)**
</dt> <dd>

Berechnet mithilfe von [**D3D12CalcSubresource**](d3d12calcsubresource.md)einen subresource-Index.

</dd> <dt>

**Operator Konstanten D3D12 \_ Ressourcen- \_& () Konstanten**
</dt> <dd>

Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.

</dd> <dt>

**Operator = = (konstant D3D12 \_ Ressourcen- \_& l, konstant D3D12 \_ Ressource \_& r)**
</dt> <dd>

Gibt "true" zurück, wenn alle Elemente der einzelnen-Strukturen identisch sind.

</dd> <dt>

**Operator! = (Konstante D3D12 \_ Ressourcen- \_& l, konstant D3D12 \_ Ressource \_& r)**
</dt> <dd>

Gibt false zurück, wenn alle Member jeder Struktur identisch sind.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12 \_ Ressource \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

