---
title: CD3DX12_ROOT_DESCRIPTOR1-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12 \_ root \_ DESCRIPTOR1-Struktur zu ermöglichen.
ms.assetid: 664822BF-5C27-4541-953F-219894547A6C
keywords:
- CD3DX12_ROOT_DESCRIPTOR1 Struktur
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66cb64509c82c11180ca3e1d2937dff5d077897d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361244"
---
# <a name="cd3dx12_root_descriptor1-structure"></a>CD3DX12 \_ root \_ DESCRIPTOR1-Struktur

Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12 \_ root \_ DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) -Struktur zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_ROOT_DESCRIPTOR1  : public D3D12_ROOT_DESCRIPTOR1{
       CD3DX12_ROOT_DESCRIPTOR1();
       explicit CD3DX12_ROOT_DESCRIPTOR1(const D3D12_ROOT_DESCRIPTOR1 &o);
       CD3DX12_ROOT_DESCRIPTOR1(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
  void inline Init(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
  void static inline Init(D3D12_ROOT_DESCRIPTOR1 &table, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ root \_ DESCRIPTOR1 ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ root \_ DESCRIPTOR1.

</dd> <dt>

**explizites CD3DX12 \_ root \_ DESCRIPTOR1 (Konstanten D3D12 \_ root \_ DESCRIPTOR1 &o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ root \_ DESCRIPTOR1, das mit dem Inhalt einer anderen [**D3D12 \_ root \_ DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) -Struktur initialisiert wird.

</dd> <dt>

**CD3DX12 \_ root \_ DESCRIPTOR1 (uint shaderregister, uint registerspace = 0, D3D12 \_ root \_ Descriptor \_ Flags Flags = D3D12 \_ root \_ Descriptor \_ Flag \_ None)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ root \_ DESCRIPTOR1 und initialisiert die folgenden Parameter:

Uint-shaderregister

Uint registerspace = 0

[**D3D12 \_ Flags für \_ \_ stammdeskriptorflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ root \_ Descriptor \_ Flag \_ None

</dd> <dt>

**Inline-init (uint shaderregister, uint registerspace = 0, D3D12 \_ root \_ Descriptor \_ Flags Flags = D3D12 \_ root \_ Descriptor \_ Flag \_ None)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

Uint-shaderregister

Uint registerspace = 0

[**D3D12 \_ Flags für \_ \_ stammdeskriptorflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ root \_ Descriptor \_ Flag \_ None

</dd> <dt>

**static Inline init (D3D12 \_ root \_ DESCRIPTOR1 &Table, uint shaderregister, uint registerspace = 0, D3D12 \_ root \_ Descriptor \_ Flags Flags = D3D12 \_ root \_ Descriptor \_ Flag \_ None)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ Stamm \_ DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) &Tabelle

Uint-shaderregister

Uint registerspace = 0

[**D3D12 \_ Flags für \_ \_ stammdeskriptorflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ root \_ Descriptor \_ Flag \_ None

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12 \_ root \_ DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





