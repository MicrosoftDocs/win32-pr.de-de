---
title: CD3DX12_RASTERIZER_DESC-Struktur (D3dx12.h)
description: Eine Hilfsstruktur, um eine einfache Initialisierung einer D3D12 \_ RASTERIZER \_ DESC-Struktur zu ermöglichen.
ms.assetid: 28AA8256-1CAF-484F-B219-0F0461BA947C
keywords:
- CD3DX12_RASTERIZER_DESC-Struktur
topic_type:
- apiref
api_name:
- CD3DX12_RASTERIZER_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa95dde87aea8e3c61d0d1fb6de6845f33717f6a46db4df7996a23afd7590b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729430"
---
# <a name="cd3dx12_rasterizer_desc-structure"></a>CD3DX12 \_ RASTERIZER \_ DESC-Struktur

Eine Hilfsstruktur, um eine einfache Initialisierung einer [**D3D12 \_ RASTERIZER \_ DESC-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_RASTERIZER_DESC  : public D3D12_RASTERIZER_DESC{
   CD3DX12_RASTERIZER_DESC();
   explicit CD3DX12_RASTERIZER_DESC(const D3D12_RASTERIZER_DESC& o);
   explicit CD3DX12_RASTERIZER_DESC(CD3DX12_DEFAULT);
   explicit CD3DX12_RASTERIZER_DESC(D3D12_FILL_MODE fillMode, D3D12_CULL_MODE cullMode, BOOL frontCounterClockwise, INT depthBias, FLOAT depthBiasClamp, FLOAT slopeScaledDepthBias, BOOL depthClipEnable, BOOL multisampleEnable, BOOL antialiasedLineEnable, UINT forcedSampleCount, D3D12_CONSERVATIVE_RASTERIZATION_MODE conservativeRaster);
   ~CD3DX12_RASTERIZER_DESC();
   operator const D3D12_RASTERIZER_DESC&() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ RASTERIZER \_ DESC()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ RASTERIZER \_ DESC.

</dd> <dt>

**explicit CD3DX12 \_ RASTERIZER \_ DESC(const D3D12 \_ RASTERIZER \_ DESC& o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ RASTERIZER \_ DESC, initialisiert mit dem Inhalt einer anderen [**D3D12 \_ RASTERIZER \_ DESC-Struktur.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)

</dd> <dt>

**Explicit CD3DX12 \_ RASTERIZER \_ DESC (CD3DX12 \_ DEFAULT)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ RASTERIZER \_ DESC, initialisiert mit Standardparametern.

``` syntax
        FillMode = D3D12_FILL_MODE_SOLID;  
        CullMode = D3D12_CULL_MODE_BACK;  
        FrontCounterClockwise = FALSE;  
        DepthBias = D3D12_DEFAULT_DEPTH_BIAS;  
        DepthBiasClamp = D3D12_DEFAULT_DEPTH_BIAS_CLAMP;  
        SlopeScaledDepthBias = D3D12_DEFAULT_SLOPE_SCALED_DEPTH_BIAS;  
        DepthClipEnable = TRUE;  
        MultisampleEnable = FALSE;  
        AntialiasedLineEnable = FALSE;  
        ForcedSampleCount = 0;  
        ConservativeRaster = D3D12_CONSERVATIVE_RASTERIZATION_MODE_OFF;  
```

</dd> <dt>

**explicit CD3DX12 \_ RASTERIZER \_ DESC(D3D12 \_ FILL MODE \_ fillMode, D3D12 \_ CULL MODE \_ cullMode, BOOL frontCounterClockwise, INT depthBias, FLOAT depthBiasClamp, FLOAT slopeScaledDepthBias, BOOL depthClipEnable, BOOL multisampleEnable, BOOL antialiasedLineEnable, UINT forcedSampleCount, D3D12 \_ CONSERVATIVE \_ RASTERIZATION MODE \_ conservativeRaster)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ RASTERIZER \_ DESC und initialisiert die folgenden Parameter:

[**D3D12 \_ FILL \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode) fillMode

[**D3D12 \_ CULL \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode) cullMode

BOOL frontCounterClockwise

INT depthBias

FLOAT depthBiasClamp

FLOAT slopeScaledDepthBias

BOOL depthClipEnable

BOOL multisampleEnable

BOOL antialiasedLineEnable

UINT forcedSampleCount

[**D3D12 \_ CONSERVATIVE \_ RASTERIZATION \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) conservativeRaster

</dd> <dt>

**~CD3DX12 \_ RASTERIZER \_ DESC()**
</dt> <dd>

Zerstört eine Instanz eines CD3DX12 \_ RASTERIZER \_ DESC.

</dd> <dt>

**operator const D3D12 \_ RASTERIZER \_ DESC&() const**
</dt> <dd>

Definiert den & Pass-by-Reference-Operator für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**D3D12 \_ RASTERIZER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





