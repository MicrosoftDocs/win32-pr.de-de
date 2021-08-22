---
title: CD3DX12_DESCRIPTOR_RANGE-Struktur (D3dx12.h)
description: Eine Hilfsstruktur, um eine einfache Initialisierung einer D3D12 \_ DESCRIPTOR \_ RANGE-Struktur zu ermöglichen.
ms.assetid: F066ECA5-5E52-4483-B773-B43C5F12809B
keywords:
- CD3DX12_DESCRIPTOR_RANGE-Struktur
topic_type:
- apiref
api_name:
- CD3DX12_DESCRIPTOR_RANGE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 641afe973c89d66257a8fc7b46defe2e77d8a8667094448ef58ab4beb2839b8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989940"
---
# <a name="cd3dx12_descriptor_range-structure"></a>CD3DX12 \_ DESCRIPTOR \_ RANGE-Struktur

Eine Hilfsstruktur, um eine einfache Initialisierung einer [**D3D12 \_ DESCRIPTOR \_ RANGE-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_DESCRIPTOR_RANGE  : public D3D12_DESCRIPTOR_RANGE{
       CD3DX12_DESCRIPTOR_RANGE();
       explicit CD3DX12_DESCRIPTOR_RANGE(const D3D12_DESCRIPTOR_RANGE &o);
       CD3DX12_DESCRIPTOR_RANGE(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void inline Init(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void static inline Init(D3D12_DESCRIPTOR_RANGE &range, D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ DESCRIPTOR \_ RANGE()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines D3DX12 \_ DESCRIPTOR \_ RANGE.

</dd> <dt>

**explicit CD3DX12 \_ DESCRIPTOR \_ RANGE(const D3D12 \_ DESCRIPTOR \_ RANGE &o)**
</dt> <dd>

Erstellt eine neue Instanz eines D3DX12 \_ DESCRIPTOR \_ RANGE, initialisiert mit dem Inhalt einer anderen [**D3D12 \_ DESCRIPTOR \_ RANGE-Struktur.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)

</dd> <dt>

**CD3DX12 \_ DESCRIPTOR \_ RANGE(D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE \_ OFFSET \_ APPEND)**
</dt> <dd>

Erstellt eine neue Instanz eines D3DX12 \_ DESCRIPTOR \_ RANGE und initialisiert die folgenden Parameter:

[**D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UINT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE \_ OFFSET \_ APPEND

</dd> <dt>

**inline Init(D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE OFFSET \_ \_ APPEND)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UINT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE \_ OFFSET \_ APPEND

</dd> <dt>

**static inline Init(D3D12 \_ DESCRIPTOR \_ RANGE &range, D3D12 \_ DESCRIPTOR \_ RANGE TYPE \_ rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE OFFSET \_ \_ APPEND)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ \_DESKRIPTORBEREICH**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) &Bereich

[**D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UINT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE \_ OFFSET \_ APPEND

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_D3D12-DESKRIPTORBEREICH \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





