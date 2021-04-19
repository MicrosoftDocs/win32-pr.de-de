---
title: CD3DX12_DESCRIPTOR_RANGE1-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12 \_ Descriptor \_ Bereich1-Struktur zu ermöglichen.
ms.assetid: 9D073158-5907-4D1C-8D75-72B304277DAD
keywords:
- CD3DX12_DESCRIPTOR_RANGE1 Struktur
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
ms.openlocfilehash: 6386d8094d573fba9cd3af44b0148215ee621e2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373490"
---
# <a name="cd3dx12_descriptor_range1-structure"></a>CD3DX12 \_ Descriptor \_ Bereich1-Struktur

Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12 \_ Descriptor \_ Bereich1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) -Struktur zu ermöglichen.

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

**CD3DX12 \_ Descriptor \_ Bereich1 ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12- \_ Deskriptors \_ Bereich1.

</dd> <dt>

**expliziter CD3DX12- \_ Deskriptor \_ Bereich1 (konstant D3D12 \_ Deskriptor \_ Bereich1 &o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ Deskriptors \_ Bereich1, die mit dem Inhalt einer anderen [**D3D12 \_ Descriptor \_ Bereich1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) -Struktur initialisiert wird.

</dd> <dt>

**CD3DX12 \_ Descriptor \_ Bereich1 (D3D12 \_ deskriptorbereichstyp \_ \_ RangeType, uint numdescriptors, uint baseshaderregister, uint registerspace = 0, D3D12 \_ deskriptorbereichsflags \_ \_ = D3D12 \_ deskriptorbereichsflag \_ \_ \_ None, uint offsetindescriptorsfromtablestart = D3D12 \_ \_ deskriptorrange \_ Offset \_ Append)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ Deskriptors \_ Bereich1 und initialisiert die folgenden Parameter:

[**D3D12 \_ \_ \_ Deskriptorbereichstyp**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) "RangeType"

Uint-numdeskriptors

Uint baseshaderregister

Uint registerspace = 0

[**D3D12 \_ Deskriptorbereichsflags \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) -Flags = D3D12 \_ deskriptorbereichsflag " \_ \_ \_ None"

Uint offsetindescriptorsfromtablestart = D3D12 \_ \_ deskriptorrange \_ Offset \_ Anfügen

</dd> <dt>

**Inline-init (D3D12 \_ Descriptor \_ Range \_ Type RangeType, uint numdescriptors, uint baseshaderregister, uint registerspace = 0, D3D12 \_ Descriptor \_ Range \_ Flags Flags = D3D12 \_ Descriptor \_ Range \_ Flag \_ None, uint offsetindescriptorsfromtablestart = D3D12 \_ Descriptor \_ Range \_ Offset \_ Append)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ \_ \_ Deskriptorbereichstyp**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) "RangeType"

Uint-numdeskriptors

Uint baseshaderregister

Uint registerspace = 0

[**D3D12 \_ Deskriptorbereichsflags \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) -Flags = D3D12 \_ deskriptorbereichsflag " \_ \_ \_ None"

Uint offsetindescriptorsfromtablestart = D3D12 \_ \_ deskriptorrange \_ Offset \_ Anfügen

</dd> <dt>

**static Inline init (D3D12 \_ Descriptor \_ Bereich1 &Range, D3D12 \_ Descriptor \_ Range \_ Type RangeType, uint numdescriptors, uint baseshaderregister, uint registerspace = 0, D3D12 \_ Descriptor \_ Range \_ Flags Flags = D3D12 \_ Descriptor \_ Range \_ Flag \_ None, uint offsetindescriptorsfromtablestart = D3D12 \_ Descriptor \_ Range \_ Offset \_ Append)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ Deskriptor \_ Bereich1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) &Bereich

[**D3D12 \_ \_ \_ Deskriptorbereichstyp**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) "RangeType"

Uint-numdeskriptors

Uint baseshaderregister

Uint registerspace = 0

[**D3D12 \_ Deskriptorbereichsflags \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) -Flags = D3D12 \_ deskriptorbereichsflag " \_ \_ \_ None"

Uint offsetindescriptorsfromtablestart = D3D12 \_ \_ deskriptorrange \_ Offset \_ Anfügen

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12- \_ Deskriptor \_ Bereich1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





