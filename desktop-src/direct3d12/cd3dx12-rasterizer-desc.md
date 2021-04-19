---
title: CD3DX12_RASTERIZER_DESC-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12 \_ Rasterizer- \_ DESC-Struktur zu ermöglichen.
ms.assetid: 28AA8256-1CAF-484F-B219-0F0461BA947C
keywords:
- CD3DX12_RASTERIZER_DESC Struktur
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
ms.openlocfilehash: 078b9e92d25cb5309b4cd97d35586192a37eed90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364347"
---
# <a name="cd3dx12_rasterizer_desc-structure"></a>CD3DX12 \_ Rasterizer- \_ Struktur

Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12 \_ Rasterizer- \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) -Struktur zu ermöglichen.

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

**CD3DX12 \_ Rasterizer \_ deaktiviert ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ Rasterizer-Moduls \_ .

</dd> <dt>

**explizites CD3DX12 \_ Rasterizer-Element \_ (konstant D3D12 \_ Rasterizer- \_& o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ Rasterizer-Moduls \_ , das mit dem Inhalt einer anderen [**D3D12 \_ Rasterizer \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) -Erstellungs Struktur initialisiert wurde.

</dd> <dt>

**explizites CD3DX12 \_ Rasterizer-Element \_ (CD3DX12- \_ Standard)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ Rasterizer- \_ DESC, initialisiert mit Standardparametern.

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

**explizites CD3DX12 \_ Rasterizer \_ DESC (D3D12 \_ Fill \_ Mode FillMode, D3D12 \_ cull \_ Mode CullMode, bool frontcounteruhrzeiger Sinn, int depthbias, float depthbiasclamp, float slopescaleddepthbias, bool depthclipenable, bool multisampleenable, bool antialiasedlineenable, uint forcedsamplecount, D3D12 \_ konservative \_ rasterisierungsmodus \_ conservativeraster)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ Rasterizer- \_ DESC und initialisiert die folgenden Parameter:

[**D3D12 \_ Füllmodus für Füll \_ Modus**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode)

[**D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode) CullMode im cull-Modus

Bool frontcounteruhrzeiger Sinn

INT depthbias

FLOAT depthbiasclamp

FLOAT slopescaleddepthbias

Boolescher Wert

Bool multisampleenable

Bool antialiasedlineenable

Uint forcedsamplecount

[**D3D12 \_ Konservativer \_ rasterisierungsmodus \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) conservativeraster

</dd> <dt>

**~ CD3DX12 \_ Rasterizer- \_ Decoder ()**
</dt> <dd>

Zerstört eine Instanz eines CD3DX12 \_ Rasterizer-Moduls \_ .

</dd> <dt>

**Operator Konstanten D3D12 \_ Rasterizer- \_& () Konstanten**
</dt> <dd>

Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12 \_ Rasterizer- \_ Abteilung**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





