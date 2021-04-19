---
title: CD3DX12_DESCRIPTOR_RANGE-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die die einfache Initialisierung einer D3D12- \_ deskriptorbereichstruktur ermöglicht \_ .
ms.assetid: F066ECA5-5E52-4483-B773-B43C5F12809B
keywords:
- CD3DX12_DESCRIPTOR_RANGE Struktur
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
ms.openlocfilehash: b511af1766daaefa7f92d33b71841b3a69c99927
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350664"
---
# <a name="cd3dx12_descriptor_range-structure"></a>CD3DX12- \_ \_ deskriptorbereichstruktur

Eine hilfsstruktur, die die einfache Initialisierung einer [**D3D12- \_ \_ deskriptorbereichstruktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) ermöglicht.

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

**CD3DX12- \_ \_ Deskriptorbereich ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines D3DX12- \_ \_ Deskriptorbereichs.

</dd> <dt>

**expliziter CD3DX12- \_ \_ Deskriptorbereich (konstant D3D12 \_ \_ Deskriptorbereich &o)**
</dt> <dd>

Erstellt eine neue Instanz eines D3DX12- \_ \_ Deskriptorbereichs, der mit dem Inhalt einer anderen [**D3D12- \_ \_ deskriptorbereichstruktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) initialisiert wird.

</dd> <dt>

**CD3DX12 \_ Descriptor \_ Range (D3D12 \_ deskriptorbereichstyp \_ \_ RangeType, uint numdescriptors, uint baseshaderregister, uint registerspace = 0, uint offsetindescriptorsfromtablestart = D3D12 \_ \_ deskriptorrange \_ Offset \_ Append)**
</dt> <dd>

Erstellt eine neue Instanz eines D3DX12- \_ \_ Deskriptorbereichs und initialisiert die folgenden Parameter:

[**D3D12 \_ \_ \_ Deskriptorbereichstyp**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) "RangeType"

Uint-numdeskriptors

Uint baseshaderregister

Uint registerspace = 0

Uint offsetindescriptorsfromtablestart = D3D12 \_ \_ deskriptorrange \_ Offset \_ Anfügen

</dd> <dt>

**Inline-init (D3D12 \_ Descriptor \_ Range \_ Type RangeType, uint numdescriptors, uint baseshaderregister, uint registerspace = 0, uint offsetindescriptorsfromtablestart = D3D12 \_ Descriptor \_ Range \_ Offset \_ Append)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ \_ \_ Deskriptorbereichstyp**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) "RangeType"

Uint-numdeskriptors

Uint baseshaderregister

Uint registerspace = 0

Uint offsetindescriptorsfromtablestart = D3D12 \_ \_ deskriptorrange \_ Offset \_ Anfügen

</dd> <dt>

**static Inline init (D3D12 \_ Descriptor \_ Range &Range, D3D12 \_ Descriptor \_ Range \_ Type RangeType, uint numdescriptors, uint baseshaderregister, uint registerspace = 0, uint offsetindescriptorsfromtablestart = D3D12 \_ \_ deskriptorrange \_ Offset \_ Append)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ \_Deskriptorbereich**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) &Bereich

[**D3D12 \_ \_ \_ Deskriptorbereichstyp**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) "RangeType"

Uint-numdeskriptors

Uint baseshaderregister

Uint registerspace = 0

Uint offsetindescriptorsfromtablestart = D3D12 \_ \_ deskriptorrange \_ Offset \_ Anfügen

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12- \_ \_ Deskriptorbereich**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





