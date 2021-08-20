---
title: CD3DX12_DEPTH_STENCIL_DESC -Struktur (D3dx12.h)
description: Eine Hilfsstruktur, um eine einfache Initialisierung einer D3D12 \_ DEPTH \_ STENCIL \_ DESC-Struktur zu ermöglichen.
ms.assetid: D3DB04C3-4564-45A4-830A-E63B8D308B33
keywords:
- CD3DX12_DEPTH_STENCIL_DESC-Struktur
topic_type:
- apiref
api_name:
- CD3DX12_DEPTH_STENCIL_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fdbd7184ad6fc432beb5ba8e9585c2e9a93486acc604f875ff3a70f72e8ec04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531106"
---
# <a name="cd3dx12_depth_stencil_desc-structure"></a>CD3DX12 \_ DEPTH \_ STENCIL \_ DESC-Struktur

Eine Hilfsstruktur, um eine einfache Initialisierung einer [**D3D12 \_ DEPTH \_ STENCIL \_ DESC-Struktur zu**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_DEPTH_STENCIL_DESC  : public D3D12_DEPTH_STENCIL_DESC{
   CD3DX12_DEPTH_STENCIL_DESC();
   explicit CD3DX12_DEPTH_STENCIL_DESC(const D3D12_DEPTH_STENCIL_DESC& o);
   explicit CD3DX12_DEPTH_STENCIL_DESC(CD3DX12_DEFAULT);
   explicit CD3DX12_DEPTH_STENCIL_DESC(BOOL depthEnable, D3D12_DEPTH_WRITE_MASK depthWriteMask, D3D12_COMPARISON_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12_STENCIL_OP frontStencilFailOp, D3D12_STENCIL_OP frontStencilDepthFailOp, D3D12_STENCIL_OP frontStencilPassOp, D3D12_COMPARISON_FUNC frontStencilFunc, D3D12_STENCIL_OP backStencilFailOp, D3D12_STENCIL_OP backStencilDepthFailOp, D3D12_STENCIL_OP backStencilPassOp, D3D12_COMPARISON_FUNC backStencilFunc);
   ~CD3DX12_DEPTH_STENCIL_DESC();
   operator const D3D12_DEPTH_STENCIL_DESC&() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ DEPTH \_ STENCIL \_ DESC()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer D3DX12 \_ DEPTH \_ STENCIL \_ DESC.

</dd> <dt>

**explicit CD3DX12 \_ DEPTH \_ STENCIL \_ DESC(const D3D12 \_ DEPTH \_ STENCIL \_ DESC& o)**
</dt> <dd>

Erstellt eine neue Instanz einer D3DX12 DEPTH-SCHABLONE DESC, die mit dem Inhalt einer anderen \_ \_ \_ [**D3D12 \_ DEPTH \_ STENCIL \_ DESC-Struktur initialisiert**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) wird.

</dd> <dt>

**explizite CD3DX12 \_ DEPTH \_ STENCIL \_ DESC(CD3DX12 \_ DEFAULT)**
</dt> <dd>

Erstellt eine neue Instanz einer D3DX12 \_ DEPTH \_ STENCIL \_ DESC, initialisiert mit Standardparametern.

``` syntax
        DepthEnable = TRUE;  
        DepthWriteMask = D3D12_DEPTH_WRITE_MASK_ALL;  
        DepthFunc = D3D12_COMPARISON_FUNC_LESS;  
        StencilEnable = FALSE;  
        StencilReadMask = D3D12_DEFAULT_STENCIL_READ_MASK;  
        StencilWriteMask = D3D12_DEFAULT_STENCIL_WRITE_MASK;  
        const D3D12_DEPTH_STENCILOP_DESC defaultStencilOp =  
        { D3D12_STENCIL_OP_KEEP, D3D12_STENCIL_OP_KEEP, D3D12_STENCIL_OP_KEEP, D3D12_COMPARISON_FUNC_ALWAYS };  
        FrontFace = defaultStencilOp;  
        BackFace = defaultStencilOp;  
```

</dd> <dt>

**explicit CD3DX12 \_ DEPTH \_ STENCIL \_ DESC(BOOL depthEnable, D3D12 \_ DEPTH WRITE MASK \_ \_ depthWriteMask, D3D12 \_ COMPARISON \_ FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12 \_ STENCIL \_ OP frontStencilFailOp, D3D12 \_ STENCIL \_ OP frontStencilDepthFailOp, \_ D3D12 STENCIL \_ OP frontStencilPassOp, D3D12 \_ COMPARISON \_ FUNC frontStencilFunc, D3D12 \_ STENCIL \_ OP backStencilFailOp, D3D12 \_ STENCIL \_ OP backStencilDepthFailOp, D3D12 \_ STENCIL \_ OP backStencilPassOp, D3D12 \_ COMPARISON \_ FUNC backStencilFunc)**
</dt> <dd>

Erstellt eine neue Instanz einer D3DX12 \_ DEPTH \_ STENCIL \_ DESC und initialisiert die folgenden Parameter:

BOOL depthEnable

[**D3D12 \_ DEPTH \_ WRITE \_ MASK**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) depthWriteMask

[**D3D12 \_ VERGLEICH \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) depthFunc

BOOL stencilEnable

UINT8 stencilReadMask

UINT8 stencilWriteMask

[**D3D12 \_ STENCIL \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilFailOp

[**D3D12 \_ STENCIL \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilDepthFailOp

[**D3D12 \_ STENCIL \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilPassOp

[**D3D12 \_ VERGLEICH \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) frontStencilFunc

[**D3D12 \_ STENCIL \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilFailOp

[**D3D12 \_ STENCIL \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilDepthFailOp

[**D3D12 \_ STENCIL \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilPassOp

[**D3D12 \_ VERGLEICH \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) backStencilFunc

</dd> <dt>

**~CD3DX12 \_ DEPTH \_ STENCIL \_ DESC()**
</dt> <dd>

Zerstört eine Instanz einer CD3DX12 \_ DEPTH \_ STENCIL \_ DESC.

</dd> <dt>

**operator const D3D12 \_ DEPTH \_ STENCIL \_ DESC&() const**
</dt> <dd>

Definiert den & pass-by-reference-Operator für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**D3D12 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





