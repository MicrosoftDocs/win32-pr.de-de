---
title: CD3DX12_BLEND_DESC-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12 \_ Blend- \_ DESC-Struktur zu ermöglichen.
ms.assetid: D37BB62E-904B-4953-9119-21F3B37570C0
keywords:
- CD3DX12_BLEND_DESC Struktur
topic_type:
- apiref
api_name:
- CD3DX12_BLEND_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb88ce003f74251c3ce34a2ca47ae2fb55f892d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363961"
---
# <a name="cd3dx12_blend_desc-structure"></a>CD3DX12 \_ Blend- \_ Entsc-Struktur

Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12 \_ Blend- \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) -Struktur zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_BLEND_DESC  : public D3D12_BLEND_DESC{
   CD3DX12_BLEND_DESC();
   explicit CD3DX12_BLEND_DESC(const D3D12_BLEND_DESC& o);
   explicit CD3DX12_BLEND_DESC(CD3DX12_DEFAULT);
   ~CD3DX12_BLEND_DESC();
   operator const D3D12_BLEND_DESC&() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ Blend-Debug \_ ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 Blend- \_ \_ Absc.

</dd> <dt>

**explizites CD3DX12 \_ Blend- \_ decod (konstant D3D12 \_ Blend- \_& o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ Blend- \_ Inhalts, das mit dem Inhalt einer anderen [**D3D12 \_ \_ Blend**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) -Debug-Struktur initialisiert wird.

</dd> <dt>

**explizites CD3DX12 Blend-Debug \_ \_ (CD3DX12- \_ Standard)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ Blend- \_ DESC, das mit Standardparametern initialisiert wird.



| State                                   | Standardwert                    |
|-----------------------------------------|----------------------------------|
| Alpha atocoverageenable                   | **FALSE**                        |
| Independentblendenable                  | **FALSE**                        |
| RenderTarget \[ 0 \] . Blendbar           | **FALSE**                        |
| RenderTarget \[ 0 \] . Logicopenable         | **FALSE**                        |
| RenderTarget \[ 0 \] . Srcblend              | D3D12 \_ Blend \_ 1                |
| RenderTarget \[ 0 \] . Destblend             | D3D12 \_ Blend \_ null               |
| RenderTarget \[ 0 \] . Blendop               | D3D12 \_ Blend- \_ op- \_ Add            |
| RenderTarget \[ 0 \] . Srcblendalpha         | D3D12 \_ Blend \_ 1                |
| RenderTarget \[ 0 \] . Destblendalpha        | D3D12 \_ Blend \_ null               |
| RenderTarget \[ 0 \] . Blendopalpha          | D3D12 \_ Blend- \_ op- \_ Add            |
| RenderTarget \[ 0 \] . Logicop               | D3D12 \_ Logic \_ op \_ NoOp           |
| RenderTarget \[ 0 \] . Rendertargetschreitemask | D3D12 \_ Color \_ Write \_ \_ all aktivieren |



 

</dd> <dt>

**~ CD3DX12 \_ Blend-Debug \_ ()**
</dt> <dd>

Zerstört eine Instanz eines CD3DX12 \_ Blend- \_ Entsc.

</dd> <dt>

**Operator Konstanten D3D12 \_ Blend- \_& () Konstanten**
</dt> <dd>

Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12 \_ Blend- \_ Entsc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





