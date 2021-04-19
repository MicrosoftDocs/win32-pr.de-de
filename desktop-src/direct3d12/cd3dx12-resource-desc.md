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
# <a name="cd3dx12_resource_desc-structure"></a><span data-ttu-id="a45ea-104">CD3DX12 Ressourcen-zu- \_ \_ Struktur-Struktur</span><span class="sxs-lookup"><span data-stu-id="a45ea-104">CD3DX12\_RESOURCE\_DESC structure</span></span>

<span data-ttu-id="a45ea-105">Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12 \_ Resource \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) -Struktur zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="a45ea-105">A helper structure to enable easy initialization of a [**D3D12\_RESOURCE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a45ea-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a45ea-106">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="a45ea-107">Member</span><span class="sxs-lookup"><span data-stu-id="a45ea-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a45ea-108">**CD3DX12- \_ Ressource \_ ()**</span><span class="sxs-lookup"><span data-stu-id="a45ea-108">**CD3DX12\_RESOURCE\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="a45ea-109">Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12- \_ Ressource \_ .</span><span class="sxs-lookup"><span data-stu-id="a45ea-109">Creates a new, uninitialized, instance of a CD3DX12\_RESOURCE\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="a45ea-110">**explizites CD3DX12 Resource Manager- \_ Ressourcen \_ (konstant D3D12 \_ Ressourcen- \_& o)**</span><span class="sxs-lookup"><span data-stu-id="a45ea-110">**explicit CD3DX12\_RESOURCE\_DESC(const D3D12\_RESOURCE\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="a45ea-111">Erstellt eine neue Instanz einer CD3DX12- \_ Ressource \_ , die mit dem Inhalt einer anderen [**D3D12 \_ Resource \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) -Debug-Struktur initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="a45ea-111">Creates a new instance of a CD3DX12\_RESOURCE\_DESC, initialized with the contents of another [**D3D12\_RESOURCE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a45ea-112">**CD3DX12 \_ Resource \_ DESC (D3D12 \_ Resource \_ Dimension Dimension, UINT64 Alignment, UINT64 Width, uint Height, UInt16 depthorarraysize, UInt16 miplevels, DXGI \_ Format Format, uint samplecount, uint samplequality, D3D12 \_ Texture \_ Layout Layout, D3D12 \_ \_ Ressourcenflags Flags)**</span><span class="sxs-lookup"><span data-stu-id="a45ea-112">**CD3DX12\_RESOURCE\_DESC(D3D12\_RESOURCE\_DIMENSION dimension, UINT64 alignment, UINT64 width, UINT height, UINT16 depthOrArraySize, UINT16 mipLevels, DXGI\_FORMAT format, UINT sampleCount, UINT sampleQuality, D3D12\_TEXTURE\_LAYOUT layout, D3D12\_RESOURCE\_FLAGS flags)**</span></span>
</dt> <dd>

<span data-ttu-id="a45ea-113">Erstellt eine neue Instanz einer CD3DX12 \_ Resource \_ DESC und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="a45ea-113">Creates a new instance of a CD3DX12\_RESOURCE\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="a45ea-114">[**D3D12 \_ Dimension der Ressourcen \_ Dimension**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)</span><span class="sxs-lookup"><span data-stu-id="a45ea-114">[**D3D12\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) dimension</span></span>

<span data-ttu-id="a45ea-115">UINT64-Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="a45ea-115">UINT64 alignment</span></span>

<span data-ttu-id="a45ea-116">UINT64-Breite</span><span class="sxs-lookup"><span data-stu-id="a45ea-116">UINT64 width</span></span>

<span data-ttu-id="a45ea-117">Uint-Höhe</span><span class="sxs-lookup"><span data-stu-id="a45ea-117">UINT height</span></span>

<span data-ttu-id="a45ea-118">UInt16 depthorarraysize</span><span class="sxs-lookup"><span data-stu-id="a45ea-118">UINT16 depthOrArraySize</span></span>

<span data-ttu-id="a45ea-119">UInt16 miplevels</span><span class="sxs-lookup"><span data-stu-id="a45ea-119">UINT16 mipLevels</span></span>

<span data-ttu-id="a45ea-120">[**DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Format</span><span class="sxs-lookup"><span data-stu-id="a45ea-120">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="a45ea-121">Uint-samplecount</span><span class="sxs-lookup"><span data-stu-id="a45ea-121">UINT sampleCount</span></span>

<span data-ttu-id="a45ea-122">Uint samplequality</span><span class="sxs-lookup"><span data-stu-id="a45ea-122">UINT sampleQuality</span></span>

<span data-ttu-id="a45ea-123">[**D3D12 \_ Layout des Textur \_ Layouts**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)</span><span class="sxs-lookup"><span data-stu-id="a45ea-123">[**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) layout</span></span>

<span data-ttu-id="a45ea-124">[**D3D12 \_ \_Ressourcenflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) -Flags</span><span class="sxs-lookup"><span data-stu-id="a45ea-124">[**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags</span></span>

</dd> <dt>

<span data-ttu-id="a45ea-125">**statischer Inline Puffer (Konstante D3D12 \_ Ressourcen \_ Zuordnungs \_ Info& resallocinfo, \_ D3D12 \_ Ressourcenflags Flags = D3D12 \_ \_ ressourcenflag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="a45ea-125">**static inline Buffer(const D3D12\_RESOURCE\_ALLOCATION\_INFO& resAllocInfo, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="a45ea-126">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="a45ea-126">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="a45ea-127">[**D3D12 \_ \_ \_ Informationen zur Ressourcenzuweisung**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resallocinfo</span><span class="sxs-lookup"><span data-stu-id="a45ea-127">[**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span></span>

<span data-ttu-id="a45ea-128">Opt [**D3D12 \_ \_Ressourcenflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) Flags = \_ D3D12 \_ ressourcenflag " \_ None"</span><span class="sxs-lookup"><span data-stu-id="a45ea-128">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="a45ea-129">**statischer Inline Puffer (UINT64 Width, \_ D3D12 \_ Ressourcenflags Flags = D3D12 \_ \_ ressourcenflag \_ None, UINT64 Alignment = 0)**</span><span class="sxs-lookup"><span data-stu-id="a45ea-129">**static inline Buffer(UINT64 width, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE, UINT64 alignment = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="a45ea-130">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="a45ea-130">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="a45ea-131">UINT64-Breite</span><span class="sxs-lookup"><span data-stu-id="a45ea-131">UINT64 width</span></span>

<span data-ttu-id="a45ea-132">Opt [**D3D12 \_ \_Ressourcenflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) Flags = \_ D3D12 \_ ressourcenflag " \_ None"</span><span class="sxs-lookup"><span data-stu-id="a45ea-132">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

<span data-ttu-id="a45ea-133">Opt UINT64 Alignment = 0</span><span class="sxs-lookup"><span data-stu-id="a45ea-133">(opt) UINT64 alignment = 0</span></span>

</dd> <dt>

<span data-ttu-id="a45ea-134">**static Inline Tex1D (DXGI \_ Format Format, UINT64 Width, UInt16 arraySize = 1, UInt16 miplevels = 0, D3D12 \_ \_ Ressourcenflags Flags = \_ D3D12 \_ ressourcentflag \_ None, D3D12 \_ Texture \_ Layout Layout = D3D12 \_ Texture \_ Layout \_ unknown, UINT64 Alignment = 0)**</span><span class="sxs-lookup"><span data-stu-id="a45ea-134">**static inline Tex1D(DXGI\_FORMAT format, UINT64 width, UINT16 arraySize = 1, UINT16 mipLevels = 0, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE, D3D12\_TEXTURE\_LAYOUT layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN, UINT64 alignment = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="a45ea-135">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="a45ea-135">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="a45ea-136">[**DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Format</span><span class="sxs-lookup"><span data-stu-id="a45ea-136">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="a45ea-137">UINT64-Breite</span><span class="sxs-lookup"><span data-stu-id="a45ea-137">UINT64 width</span></span>

<span data-ttu-id="a45ea-138">Opt UInt16 arraySize = 1</span><span class="sxs-lookup"><span data-stu-id="a45ea-138">(opt) UINT16 arraySize = 1</span></span>

<span data-ttu-id="a45ea-139">Opt UInt16 miplevels = 0</span><span class="sxs-lookup"><span data-stu-id="a45ea-139">(opt) UINT16 mipLevels = 0</span></span>

<span data-ttu-id="a45ea-140">Opt [**D3D12 \_ \_Ressourcenflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) Flags = \_ D3D12 \_ ressourcenflag " \_ None"</span><span class="sxs-lookup"><span data-stu-id="a45ea-140">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

<span data-ttu-id="a45ea-141">Opt [**D3D12 \_ Layout des Textur \_ Layouts**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = D3D12 \_ Textur \_ Layout \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="a45ea-141">(opt) [**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN</span></span>

<span data-ttu-id="a45ea-142">Opt UINT64 Alignment = 0</span><span class="sxs-lookup"><span data-stu-id="a45ea-142">(opt) UINT64 alignment = 0</span></span>

</dd> <dt>

<span data-ttu-id="a45ea-143">**static Inline Tex2D (DXGI \_ Format Format, UINT64 Width, uint Height, UInt16 arraySize = 1, UInt16 miplevels = 0, uint samplecount = 1, uint samplequality = 0, D3D12 \_ \_ Ressourcenflags Flags = D3D12 \_ Resource \_ Flag \_ None, D3D12 \_ Texture \_ Layout Layout = D3D12 \_ Texture \_ Layout \_ unknown, UINT64 Alignment = 0)**</span><span class="sxs-lookup"><span data-stu-id="a45ea-143">**static inline Tex2D(DXGI\_FORMAT format, UINT64 width, UINT height, UINT16 arraySize = 1, UINT16 mipLevels = 0, UINT sampleCount = 1, UINT sampleQuality = 0, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE, D3D12\_TEXTURE\_LAYOUT layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN, UINT64 alignment = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="a45ea-144">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="a45ea-144">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="a45ea-145">[**DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Format</span><span class="sxs-lookup"><span data-stu-id="a45ea-145">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="a45ea-146">UINT64-Breite</span><span class="sxs-lookup"><span data-stu-id="a45ea-146">UINT64 width</span></span>

<span data-ttu-id="a45ea-147">Uint-Höhe</span><span class="sxs-lookup"><span data-stu-id="a45ea-147">UINT height</span></span>

<span data-ttu-id="a45ea-148">Opt UInt16 arraySize = 1</span><span class="sxs-lookup"><span data-stu-id="a45ea-148">(opt) UINT16 arraySize = 1</span></span>

<span data-ttu-id="a45ea-149">Opt UInt16 miplevels = 0</span><span class="sxs-lookup"><span data-stu-id="a45ea-149">(opt) UINT16 mipLevels = 0</span></span>

<span data-ttu-id="a45ea-150">Opt Uint samplecount = 1</span><span class="sxs-lookup"><span data-stu-id="a45ea-150">(opt) UINT sampleCount = 1</span></span>

<span data-ttu-id="a45ea-151">Opt Uint samplequality = 0</span><span class="sxs-lookup"><span data-stu-id="a45ea-151">(opt) UINT sampleQuality = 0</span></span>

<span data-ttu-id="a45ea-152">Opt [**D3D12 \_ \_Ressourcenflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) Flags = \_ D3D12 \_ ressourcenflag " \_ None"</span><span class="sxs-lookup"><span data-stu-id="a45ea-152">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

<span data-ttu-id="a45ea-153">Opt [**D3D12 \_ Layout des Textur \_ Layouts**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = D3D12 \_ Textur \_ Layout \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="a45ea-153">(opt) [**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN</span></span>

<span data-ttu-id="a45ea-154">Opt UINT64 Alignment = 0</span><span class="sxs-lookup"><span data-stu-id="a45ea-154">(opt) UINT64 alignment = 0</span></span>

</dd> <dt>

<span data-ttu-id="a45ea-155">**static Inline Tex3D (DXGI \_ Format Format, UINT64 Width, uint Height, UInt16 Tiefe, UInt16 miplevels = 0, D3D12 \_ \_ Ressourcenflags Flags = \_ D3D12 \_ ressourcentflag \_ None, D3D12 \_ Texture Layout \_ Layout = D3D12 \_ Texture \_ Layout \_ unknown, UINT64 Alignment = 0)**</span><span class="sxs-lookup"><span data-stu-id="a45ea-155">**static inline Tex3D(DXGI\_FORMAT format, UINT64 width, UINT height, UINT16 depth, UINT16 mipLevels = 0, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE, D3D12\_TEXTURE\_LAYOUT layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN, UINT64 alignment = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="a45ea-156">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="a45ea-156">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="a45ea-157">[**DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Format</span><span class="sxs-lookup"><span data-stu-id="a45ea-157">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="a45ea-158">UINT64-Breite</span><span class="sxs-lookup"><span data-stu-id="a45ea-158">UINT64 width</span></span>

<span data-ttu-id="a45ea-159">Uint-Höhe</span><span class="sxs-lookup"><span data-stu-id="a45ea-159">UINT height</span></span>

<span data-ttu-id="a45ea-160">UInt16 Tiefe</span><span class="sxs-lookup"><span data-stu-id="a45ea-160">UINT16 depth</span></span>

<span data-ttu-id="a45ea-161">Opt UInt16 miplevels = 0</span><span class="sxs-lookup"><span data-stu-id="a45ea-161">(opt) UINT16 mipLevels = 0</span></span>

<span data-ttu-id="a45ea-162">Opt [**D3D12 \_ \_Ressourcenflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) Flags = \_ D3D12 \_ ressourcenflag " \_ None"</span><span class="sxs-lookup"><span data-stu-id="a45ea-162">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

<span data-ttu-id="a45ea-163">Opt [**D3D12 \_ Layout des Textur \_ Layouts**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = D3D12 \_ Textur \_ Layout \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="a45ea-163">(opt) [**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN</span></span>

<span data-ttu-id="a45ea-164">Opt UINT64 Alignment = 0</span><span class="sxs-lookup"><span data-stu-id="a45ea-164">(opt) UINT64 alignment = 0</span></span>

</dd> <dt>

<span data-ttu-id="a45ea-165">**Inline Tiefe () konstant**</span><span class="sxs-lookup"><span data-stu-id="a45ea-165">**inline Depth() const**</span></span>
</dt> <dd>

<span data-ttu-id="a45ea-166">Wenn Dimension = = [**D3D12 \_ Resource \_ Dimension**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D, wird depthorarraysize zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a45ea-166">If Dimension == [**D3D12\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)\_TEXTURE3D, returns DepthOrArraySize.</span></span> <span data-ttu-id="a45ea-167">Wenn Dimension! = D3D12 \_ Resource \_ Dimension \_ TEXTURE3D, wird 1 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a45ea-167">If Dimension != D3D12\_RESOURCE\_DIMENSION\_TEXTURE3D, returns 1.</span></span>

</dd> <dt>

<span data-ttu-id="a45ea-168">**Inline arraySize () konstant**</span><span class="sxs-lookup"><span data-stu-id="a45ea-168">**inline ArraySize() const**</span></span>
</dt> <dd>

<span data-ttu-id="a45ea-169">Wenn Dimension! = D3D12 \_ Resource \_ Dimension \_ TEXTURE3D, wird depthorarraysize zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a45ea-169">If Dimension != D3D12\_RESOURCE\_DIMENSION\_TEXTURE3D, returns DepthOrArraySize.</span></span> <span data-ttu-id="a45ea-170">Wenn Dimension = = D3D12 \_ Resource \_ Dimension \_ TEXTURE3D, wird 1 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a45ea-170">If Dimension == D3D12\_RESOURCE\_DIMENSION\_TEXTURE3D, returns 1.</span></span> <span data-ttu-id="a45ea-171">Weitere Informationen finden Sie unter [**D3D12 \_ Resource \_ Dimension**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D.</span><span class="sxs-lookup"><span data-stu-id="a45ea-171">See [**D3D12\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)\_TEXTURE3D.</span></span>

</dd> <dt>

<span data-ttu-id="a45ea-172">**Inline planecount (ID3D12Device \* pdevice) konstant**</span><span class="sxs-lookup"><span data-stu-id="a45ea-172">**inline PlaneCount(ID3D12Device\* pDevice) const**</span></span>
</dt> <dd>

<span data-ttu-id="a45ea-173">Gibt D3D12GetFormatPlaneCount (pdevice, Format) zurück.</span><span class="sxs-lookup"><span data-stu-id="a45ea-173">Returns D3D12GetFormatPlaneCount(pDevice, Format).</span></span> <span data-ttu-id="a45ea-174">Siehe [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) und [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device).</span><span class="sxs-lookup"><span data-stu-id="a45ea-174">See [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) and [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device).</span></span>

</dd> <dt>

<span data-ttu-id="a45ea-175">**Inline-unter Berichte (ID3D12Device \* pdevice) konstant**</span><span class="sxs-lookup"><span data-stu-id="a45ea-175">**inline Subresources(ID3D12Device\* pDevice) const**</span></span>
</dt> <dd>

<span data-ttu-id="a45ea-176">Gibt die Anzahl der unter Ressourcen zurück, die als miplevels \* arraySize () \* planecount (pdevice) berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="a45ea-176">Returns the number of subresources, calculated as MipLevels \* ArraySize() \* PlaneCount(pDevice).</span></span>

</dd> <dt>

<span data-ttu-id="a45ea-177">**Inline-calcsubresource (uint mipslice, uint arrayslice, uint planeslice)**</span><span class="sxs-lookup"><span data-stu-id="a45ea-177">**inline CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice)**</span></span>
</dt> <dd>

<span data-ttu-id="a45ea-178">Berechnet mithilfe von [**D3D12CalcSubresource**](d3d12calcsubresource.md)einen subresource-Index.</span><span class="sxs-lookup"><span data-stu-id="a45ea-178">Calculates a subresource index, by using [**D3D12CalcSubresource**](d3d12calcsubresource.md).</span></span>

</dd> <dt>

<span data-ttu-id="a45ea-179">**Operator Konstanten D3D12 \_ Ressourcen- \_& () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="a45ea-179">**operator const D3D12\_RESOURCE\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="a45ea-180">Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.</span><span class="sxs-lookup"><span data-stu-id="a45ea-180">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> <dt>

<span data-ttu-id="a45ea-181">**Operator = = (konstant D3D12 \_ Ressourcen- \_& l, konstant D3D12 \_ Ressource \_& r)**</span><span class="sxs-lookup"><span data-stu-id="a45ea-181">**operator == (const D3D12\_RESOURCE\_DESC& l, const D3D12\_RESOURCE\_DESC& r)**</span></span>
</dt> <dd>

<span data-ttu-id="a45ea-182">Gibt "true" zurück, wenn alle Elemente der einzelnen-Strukturen identisch sind.</span><span class="sxs-lookup"><span data-stu-id="a45ea-182">Returns true if all members of each structure are identical.</span></span>

</dd> <dt>

<span data-ttu-id="a45ea-183">**Operator! = (Konstante D3D12 \_ Ressourcen- \_& l, konstant D3D12 \_ Ressource \_& r)**</span><span class="sxs-lookup"><span data-stu-id="a45ea-183">**operator != (const D3D12\_RESOURCE\_DESC& l, const D3D12\_RESOURCE\_DESC& r)**</span></span>
</dt> <dd>

<span data-ttu-id="a45ea-184">Gibt false zurück, wenn alle Member jeder Struktur identisch sind.</span><span class="sxs-lookup"><span data-stu-id="a45ea-184">Returns false if all members of each structure are identical.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a45ea-185">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a45ea-185">Requirements</span></span>



| <span data-ttu-id="a45ea-186">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a45ea-186">Requirement</span></span> | <span data-ttu-id="a45ea-187">Wert</span><span class="sxs-lookup"><span data-stu-id="a45ea-187">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a45ea-188">Header</span><span class="sxs-lookup"><span data-stu-id="a45ea-188">Header</span></span><br/> | <dl> <span data-ttu-id="a45ea-189"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="a45ea-189"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a45ea-190">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a45ea-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a45ea-191">**D3D12 \_ Ressource \_**</span><span class="sxs-lookup"><span data-stu-id="a45ea-191">**D3D12\_RESOURCE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)
</dt> <dt>

[<span data-ttu-id="a45ea-192">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="a45ea-192">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

