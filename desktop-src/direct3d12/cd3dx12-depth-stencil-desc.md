---
title: CD3DX12_DEPTH_STENCIL_DESC-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12- \_ tiefen \_ Schablone- \_ DESC-Struktur zu ermöglichen.
ms.assetid: D3DB04C3-4564-45A4-830A-E63B8D308B33
keywords:
- CD3DX12_DEPTH_STENCIL_DESC Struktur
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
ms.openlocfilehash: 2f36a071251a12c4d27d06586775c01759b88d38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367350"
---
# <a name="cd3dx12_depth_stencil_desc-structure"></a>CD3DX12 \_ Tiefe Schablone-Struktur-Debug- \_ \_ Struktur

Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12- \_ tiefen \_ Schablone- \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) -Struktur zu ermöglichen.

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

**CD3DX12 \_ tiefen \_ Schablone \_ ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer D3DX12- \_ tiefen \_ Schablone \_ .

</dd> <dt>

**explizites CD3DX12 \_ tiefen \_ Schablone \_ (konstant D3D12 \_ tiefen Schablone- \_ \_& o)**
</dt> <dd>

Erstellt eine neue Instanz einer D3DX12- \_ tiefen \_ Schablone \_ , die mit dem Inhalt einer anderen [**D3D12- \_ tiefen \_ Schablone \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) -Erstellungs Struktur initialisiert wird.

</dd> <dt>

**explizites CD3DX12 \_ tiefen \_ Schablone \_ (CD3DX12 \_ Standard)**
</dt> <dd>

Erstellt eine neue Instanz einer D3DX12- \_ tiefen \_ Schablone \_ DESC, die mit Standardparametern initialisiert wird.

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

**explizites CD3DX12 \_ tiefen \_ Schablone \_ DESC (bool depthenable, D3D12 \_ Tiefe \_ Write \_ Mask depthschreitemask, D3D12 \_ COMPARISON \_ Func depthfunc, bool stencilenable, Uint8 stencilread Mask, Uint8 stencilbeschreib temask, D3D12 \_ Stencil \_ op frontstencilfailop, D3D12 \_ Stencil \_ op frontstencildepthfailop, D3D12 \_ Stencil \_ op frontstencilpassop, D3D12 \_ COMPARISON \_ Func frontstencilfunc, D3D12 \_ Stencil \_ op backstencilfailop, D3D12 \_ Stencil op \_ backstencildepthfailop, D3D12 \_ Stencil \_ op backstencilpassop, D3D12 \_ Comparison \_ Func backstencilfunc)**
</dt> <dd>

Erstellt eine neue Instanz einer D3DX12- \_ tiefen \_ Schablone- \_ DESC und initialisiert die folgenden Parameter:

Bool depthenable

[**D3D12 \_ "Tiefe \_ Schreib \_ Maske**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) " depthschreitemask

[**D3D12 \_ Vergleichs- \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) -depthfunc

Boolescher Wert

Uint8 stencillesmaske

Uint8 stencilschreitefrage

[**D3D12 \_ Schablone \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontstencilfailop

[**D3D12 \_ Schablone \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontstencildepthfailop

[**D3D12 \_ Schablone \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontstencilpassop

[**D3D12 \_ Vergleichs- \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) frontstencilfunc

[**D3D12 \_ Stencil \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backstencilfailop

[**D3D12 \_ Schablone \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backstencildepthfailop

[**D3D12 \_ Schablone \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backstencilpassop

[**D3D12 \_ Vergleichs- \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) -backstencilfunc

</dd> <dt>

**~ CD3DX12 \_ tiefen \_ Schablone \_ ()**
</dt> <dd>

Zerstört eine Instanz einer CD3DX12- \_ tiefen \_ Schablone \_ .

</dd> <dt>

**Operator Konstanten D3D12 \_ tiefen \_ Schablone \_& () Konstanten**
</dt> <dd>

Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12 \_ tiefen \_ Schablone-Schablone \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





