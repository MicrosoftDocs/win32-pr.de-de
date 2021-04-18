---
title: CD3DX12_DEPTH_STENCIL_DESC1-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12- \_ tiefen \_ Schablone \_ DESC1-Struktur zu ermöglichen.
ms.assetid: 8EB008F9-212D-486E-9C62-D7BA9D3C6807
keywords:
- CD3DX12_DEPTH_STENCIL_DESC1 Struktur
topic_type:
- apiref
api_name:
- CD3DX12_DEPTH_STENCIL_DESC1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976c05ec4f3ca85ccfcebb6a13dbe408ba05c64e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354990"
---
# <a name="cd3dx12_depth_stencil_desc1-structure"></a>CD3DX12 \_ Tiefe \_ Schablone \_ DESC1 Struktur

Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12- \_ tiefen \_ Schablone \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) -Struktur zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_DEPTH_STENCIL_DESC1  : public D3D12_DEPTH_STENCIL_DESC1{
  CD3DX12_DEPTH_STENCIL_DESC1 CD3DX12_DEPTH_STENCIL_DESC1();
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(const D3D12_DEPTH_STENCIL_DESC1& o);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(const D3D12_DEPTH_STENCIL_DESC& o);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(CD3DX12_DEFAULT);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(BOOL depthEnable, D3D12_DEPTH_WRITE_MASK depthWriteMask, D3D12_COMPARISON_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12_STENCIL_OP frontStencilFailOp, D3D12_STENCIL_OP frontStencilDepthFailOp, D3D12_STENCIL_OP frontStencilPassOp, D3D12_COMPARISON_FUNC frontStencilFunc, D3D12_STENCIL_OP backStencilFailOp, D3D12_STENCIL_OP backStencilDepthFailOp, D3D12_STENCIL_OP backStencilPassOp, D3D12_COMPARISON_FUNC backStencilFunc, BOOL depthBoundsTestEnable);
                              ~CD3DX12_DEPTH_STENCIL_DESC1();
                              operator const D3D12_DEPTH_STENCIL_DESC1&() const;
                              operator const D3D12_DEPTH_STENCIL_DESC() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ Tiefe \_ Schablone \_ DESC1 ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12- \_ tiefen \_ Schablone \_ DESC1.

</dd> <dt>

**explizite CD3DX12 \_ Tiefe \_ Schablone \_ DESC1 (konstant D3D12 \_ Tiefe \_ Schablone \_ DESC1& o)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12- \_ tiefen \_ Schablone \_ DESC1, die mit Werten initialisiert wird, die aus einer [**D3D12- \_ tiefen \_ Schablone \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) -Struktur kopiert wurden.

</dd> <dt>

**explizite CD3DX12 \_ Tiefe \_ Schablone \_ DESC1 (konstant D3D12 \_ tiefen \_ Schablone \_& o)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12- \_ tiefen \_ Schablone \_ DESC1, die mit Werten initialisiert wird, die aus einer [**D3D12- \_ tiefen Schablone- \_ \_ decoderstruktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) kopiert werden.

und der zusätzliche **depthboundstestenable** -Member ist auf **false** festgelegt.

</dd> <dt>

**explizite CD3DX12 \_ Tiefe \_ Schablone \_ DESC1 (CD3DX12- \_ Standard)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12- \_ tiefen \_ Schablone \_ DESC1, die mit dem von D3DX12 vorgeschriebenen Standardzustand initialisiert wird:

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
    DepthBoundsTestEnable = FALSE;
          
```

</dd> <dt>

**explizite CD3DX12 \_ Tiefe \_ Schablone \_ DESC1 (bool depthenable, D3D12- \_ Tiefe \_ Schreib \_ Maske depthschreitemask, D3D12 \_ COMPARISON \_ Func depthfunc, bool stencilenable, Uint8 stencilread Mask, Uint8 stencilschreitemask, D3D12 \_ Stencil \_ op frontstencilfailop, D3D12 \_ Stencil \_ op frontstencildepthfailop, D3D12 \_ Stencil \_ op frontstencilpassop, D3D12 \_ Comparison \_ Func frontstencilfunc, D3D12 \_ Stencil \_ op backstencilfailop, D3D12 \_ Stencil \_ op backstencildepthfailop, D3D12 \_ Stencil \_ op backstencilpassop, D3D12 \_ COMPARISON \_ Func backstencilfunc, bool depthboundstestenable)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12- \_ tiefen \_ Schablone \_ DESC1, die mit den in der Parameterliste übergebenen Werten initialisiert wird.

</dd> <dt>

**~ CD3DX12 \_ Tiefe \_ Schablone \_ DESC1 ()**
</dt> <dd>

Zerstört eine Instanz einer D3DX12- \_ tiefen \_ Schablone \_ DESC1.

</dd> <dt>

**Operator Konstanten D3D12 \_ tiefen \_ Schablone \_ DESC1& () Konstanten**
</dt> <dd>

Implizite Konvertierung in eine D3D12 \_ Tiefe \_ Schablone \_ DESC1-Struktur. Da D3D12 \_ Tiefe \_ Schablone \_ DESC1 der zugrunde liegende Typ von CD3DX12 \_ Tiefe \_ Schablone DESC1 ist \_ , wird das Objekt einfach als eine Konstante D3D12-tiefen Schablone zurückgegeben \_ \_ \_ DESC1 Verweis auf sich selbst.

</dd> <dt>

**Operator Konstanten D3D12 \_ tiefen \_ Schablone \_ () Konstanten**
</dt> <dd>

Implizite Konvertierung in den Wert einer D3D12- \_ tiefen \_ Schablone- \_ Struktur. Da \_ die D3D12 \_ -tiefen Schablone \_ DESC nicht der zugrunde liegende Typ der \_ CD3DX12 \_ -tiefen Schablone \_ DESC1 ist, wird eine neue D3D12 \_ \_ -tiefen Schablone \_ -DESC-Instanz erstellt und als Wert zurückgegeben. Beachten Sie, dass die D3D12- \_ tiefen \_ Schablone \_ DESC nicht den **depthboundstestenable** -Member enthält, sodass dieser Wert bei der Konvertierung verloren geht.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**D3D12 \_ Tiefe \_ Schablone \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)
</dt> <dt>

[**D3D12 \_ tiefen \_ Schablone-Schablone \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> </dl>

 

 





