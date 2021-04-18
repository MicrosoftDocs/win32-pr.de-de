---
title: CD3DX12_ROOT_DESCRIPTOR_TABLE-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die die einfache Initialisierung einer D3D12 \_ - \_ stammdeskriptortabellenstruktur ermöglicht \_ .
ms.assetid: 154B4C50-4E94-471C-A44E-F120A84F007C
keywords:
- CD3DX12_ROOT_DESCRIPTOR_TABLE Struktur
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR_TABLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f675624526a959e6cf92172383b12590c36fc408
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354350"
---
# <a name="cd3dx12_root_descriptor_table-structure"></a>CD3DX12 \_ - \_ stammdeskriptortabellenstruktur \_

Eine hilfsstruktur, die die einfache Initialisierung einer [**D3D12 \_ - \_ stammdeskriptortabellenstruktur \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) ermöglicht.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_ROOT_DESCRIPTOR_TABLE  : public D3D12_ROOT_DESCRIPTOR_TABLE{
       CD3DX12_ROOT_DESCRIPTOR_TABLE();
       explicit CD3DX12_ROOT_DESCRIPTOR_TABLE(const D3D12_ROOT_DESCRIPTOR_TABLE &o);
       CD3DX12_ROOT_DESCRIPTOR_TABLE(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
  void inline Init(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
  void static inline Init(D3D12_ROOT_DESCRIPTOR_TABLE &rootDescriptorTable, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ - \_ stammdeskriptortabelle \_ ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12- \_ \_ stammdeskriptortabelle \_ .

</dd> <dt>

**explizite CD3DX12 \_ - \_ stammdeskriptortabelle \_ (konstant D3D12 \_ \_ stammdeskriptortabelle \_ &o)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12- \_ \_ \_ stammdeskriptortabelle, die mit dem Inhalt einer anderen [**D3D12- \_ \_ stammdeskriptortabellenstruktur \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) initialisiert wird.

</dd> <dt>

**CD3DX12 \_ root \_ Descriptor \_ Table (uint numdescriptorranges, Konstanten D3D12 \_ Descriptor \_ Range \* \_ pdescriptorranges)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12- \_ \_ \_ stammdeskriptortabelle und initialisiert die folgenden Parameter:

Uint numdescriptor Ranges

[**D3D12 \_ \_Deskriptorbereich**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) " \* \_ pdescriptorranges"

</dd> <dt>

**Inline-init (uint numdescriptorranges, Konstanten D3D12 \_ \_ Deskriptorbereich \* \_ pdescriptorranges)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

Uint numdescriptor Ranges

[**D3D12 \_ \_Deskriptorbereich**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) " \* \_ pdescriptorranges"

</dd> <dt>

**static Inline init (D3D12 \_ root \_ Descriptor- \_ Tabelle &rootdescriptortable, uint numdescriptorranges, Konstanten D3D12 \_ \_ deskriptorrange \* \_ pdescriptorranges)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ \_ \_ Stammdeskriptortabelle**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) &rootdescriptortable

Uint numdescriptor Ranges

[**D3D12 \_ \_Deskriptorbereich**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) " \* \_ pdescriptorranges"

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12 \_ - \_ stammdeskriptortabelle \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





