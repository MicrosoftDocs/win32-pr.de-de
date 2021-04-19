---
title: CD3DX12_RANGE-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die die einfache Initialisierung einer D3D12- \_ Bereichs Struktur ermöglicht.
ms.assetid: 5D5192BF-D14C-487B-A214-F8428E82AF0E
keywords:
- CD3DX12_RANGE Struktur
topic_type:
- apiref
api_name:
- CD3DX12_RANGE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b6b92cd24a981d48252f5ad457f7ac0320e2d7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367490"
---
# <a name="cd3dx12_range-structure"></a>CD3DX12 \_ Range-Struktur

Eine hilfsstruktur, die die einfache Initialisierung einer [**D3D12- \_ Bereichs**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) Struktur ermöglicht.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_RANGE  : public D3D12_RANGE{
   CD3DX12_RANGE();
   explicit CD3DX12_RANGE(const D3D12_RANGE &o);
   CD3DX12_RANGE(SIZE_T begin, SIZE_T end);
   operator const D3D12_RANGE&() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ Range ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ Bereichs.

</dd> <dt>

**expliziter CD3DX12 \_ Bereich (konstant D3D12 \_ Bereich &o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ Bereichs, der mit dem Inhalt einer anderen D3D12- [**\_ Bereichs**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) Struktur initialisiert wird.

</dd> <dt>

**CD3DX12 \_ Range (size \_ t Begin, size \_ t End)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ Bereichs und initialisiert die folgenden Parameter:

\_Anfangs Größe

Ende der Größe \_

</dd> <dt>

**Operator konstant D3D12 \_ Bereichs& () Konstanten**
</dt> <dd>

Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12 \_ Bereich**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





