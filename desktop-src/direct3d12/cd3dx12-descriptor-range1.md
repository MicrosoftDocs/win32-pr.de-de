---
title: CD3DX12_DESCRIPTOR_RANGE1-Struktur (D3dx12.h)
description: Eine Hilfsstruktur, um die einfache Initialisierung einer D3D12 \_ DESCRIPTOR \_ RANGE1-Struktur zu ermöglichen.
ms.assetid: 9D073158-5907-4D1C-8D75-72B304277DAD
keywords:
- CD3DX12_DESCRIPTOR_RANGE1-Struktur
topic_type:
- apiref
api_name:
- CD3DX12_DESCRIPTOR_RANGE1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 404cb41a019dac404bbe351f78f1d1e65277dd9ad2aecf2cc2d94d06fe242f6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989880"
---
# <a name="cd3dx12_descriptor_range1-structure"></a>CD3DX12 \_ DESCRIPTOR \_ RANGE1-Struktur

Eine Hilfsstruktur, um eine einfache Initialisierung einer [**D3D12 \_ DESCRIPTOR \_ RANGE1-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_DESCRIPTOR_RANGE1  : public D3D12_DESCRIPTOR_RANGE1{
       CD3DX12_DESCRIPTOR_RANGE1();
       explicit CD3DX12_DESCRIPTOR_RANGE1(const D3D12_DESCRIPTOR_RANGE1 &o);
       CD3DX12_DESCRIPTOR_RANGE1(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void inline Init(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void static inline Init(D3D12_DESCRIPTOR_RANGE1 &range, D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ DESCRIPTOR \_ RANGE1()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ DESCRIPTOR \_ RANGE1.

</dd> <dt>

**explicit CD3DX12 \_ DESCRIPTOR \_ RANGE1(const D3D12 \_ DESCRIPTOR \_ RANGE1 &o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ DESCRIPTOR \_ RANGE1, initialisiert mit dem Inhalt einer anderen [**D3D12 \_ DESCRIPTOR \_ RANGE1-Struktur.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)

</dd> <dt>

**CD3DX12 \_ DESCRIPTOR \_ RANGE1(D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12 \_ DESCRIPTOR \_ RANGE \_ FLAGS flags = D3D12 \_ DESCRIPTOR \_ RANGE \_ FLAG \_ NONE, UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE \_ OFFSET \_ APPEND)**
</dt> <dd>

Erstellt eine neue Instanz von CD3DX12 \_ DESCRIPTOR \_ RANGE1 und initialisiert die folgenden Parameter:

[**D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UINT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

[**D3D12 \_ DESCRIPTOR \_ RANGE \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = D3D12 \_ DESCRIPTOR \_ RANGE \_ FLAG \_ NONE

UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE \_ OFFSET \_ APPEND

</dd> <dt>

**inline Init(D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12 \_ DESCRIPTOR \_ RANGE \_ FLAGS flags = D3D12 \_ DESCRIPTOR \_ RANGE FLAG \_ \_ NONE, UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE OFFSET \_ \_ APPEND)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UINT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

[**D3D12 \_ DESCRIPTOR \_ RANGE \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = D3D12 \_ DESCRIPTOR \_ RANGE \_ FLAG \_ NONE

UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE \_ OFFSET \_ APPEND

</dd> <dt>

**static inline Init(D3D12 \_ DESCRIPTOR \_ RANGE1 &range, D3D12 \_ DESCRIPTOR \_ RANGE TYPE \_ rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12 \_ DESCRIPTOR \_ RANGE \_ FLAGS flags = D3D12 \_ DESCRIPTOR \_ RANGE FLAG \_ \_ NONE, UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE OFFSET \_ \_ APPEND)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ DESCRIPTOR \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) &-Bereich

[**D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UINT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

[**D3D12 \_ DESCRIPTOR \_ RANGE \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = D3D12 \_ DESCRIPTOR \_ RANGE \_ FLAG \_ NONE

UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE \_ OFFSET \_ APPEND

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**D3D12 \_ DESCRIPTOR \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





