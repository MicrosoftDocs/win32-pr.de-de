---
title: CD3DX12_ROOT_DESCRIPTOR_TABLE1-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12-Stamm \_ \_ Deskriptor Table1-Struktur zu ermöglichen \_ .
ms.assetid: 82AC1948-92AA-4A4D-B443-717E9BF3046D
keywords:
- CD3DX12_ROOT_DESCRIPTOR_TABLE1 Struktur
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR_TABLE1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e3538e5e1e199fdb6f8c7473af4996ccd7b7f1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354410"
---
# <a name="cd3dx12_root_descriptor_table1-structure"></a>CD3DX12 \_ root \_ Descriptor \_ Table1-Struktur

Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12-Stamm \_ \_ Deskriptor \_ Table1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) -Struktur zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_ROOT_DESCRIPTOR_TABLE1  : public D3D12_ROOT_DESCRIPTOR_TABLE1{
       CD3DX12_ROOT_DESCRIPTOR_TABLE1();
       explicit CD3DX12_ROOT_DESCRIPTOR_TABLE1(const D3D12_ROOT_DESCRIPTOR_TABLE1 &o);
       CD3DX12_ROOT_DESCRIPTOR_TABLE1(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
  void inline Init(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
  void static inline Init(D3D12_ROOT_DESCRIPTOR_TABLE1 &rootDescriptorTable, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ root \_ Descriptor \_ Table1 ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12-Stamm \_ \_ Deskriptors \_ Table1.

</dd> <dt>

**expliziter CD3DX12-Stamm \_ \_ Deskriptor \_ Table1 (konstant D3D12 Stamm \_ \_ Deskriptor \_ Table1 &o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ root \_ Descriptor \_ Table1, initialisiert mit dem Inhalt einer anderen [**D3D12 \_ root \_ Descriptor \_ Table1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) -Struktur.

</dd> <dt>

**CD3DX12 \_ root \_ Descriptor \_ Table1 (uint numdescriptorranges, Konstanten D3D12 \_ Descriptor \_ Bereich1 \* \_ pdescriptorranges)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ root \_ Descriptor \_ Table1 und initialisiert die folgenden Parameter:

Uint numdescriptor Ranges

Konstanten [**D3D12 \_ Deskriptor \_ Bereich1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pdescriptorranges

</dd> <dt>

**Inline-init (uint numdescriptorranges, Konstanten D3D12 \_ Deskriptor \_ Bereich1 \* \_ pdescriptorranges)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

Uint numdescriptor Ranges

Konstanten [**D3D12 \_ Deskriptor \_ Bereich1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pdescriptorranges

</dd> <dt>

**static Inline init (D3D12 \_ root \_ Descriptor \_ Table1 &rootdescriptortable, uint numdescriptorranges, Konstanten D3D12 \_ Descriptor \_ Bereich1 \* \_ pdescriptorranges)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ Stamm \_ Deskriptor \_ Table1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) &rootdescriptortable

Uint numdescriptor Ranges

Konstanten [**D3D12 \_ Deskriptor \_ Bereich1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pdescriptorranges

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12-Stamm \_ \_ Deskriptor \_ Table1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





