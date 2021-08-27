---
title: CD3DX12_RANGE-Struktur (D3dx12.h)
description: Eine Hilfsstruktur, um eine einfache Initialisierung einer D3D12 \_ RANGE-Struktur zu ermöglichen.
ms.assetid: 5D5192BF-D14C-487B-A214-F8428E82AF0E
keywords:
- CD3DX12_RANGE-Struktur
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
ms.openlocfilehash: 371df1fb6c1b6ce9984fbed5bb388d7026ddd193d0ab2d434710df3618da7ca8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118808516"
---
# <a name="cd3dx12_range-structure"></a>CD3DX12 \_ RANGE-Struktur

Eine Hilfsstruktur, um eine einfache Initialisierung einer [**D3D12 \_ RANGE-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) zu ermöglichen.

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

**CD3DX12 \_ RANGE()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ RANGE.

</dd> <dt>

**explicit CD3DX12 \_ RANGE(const D3D12 \_ RANGE &o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ RANGE, initialisiert mit dem Inhalt einer anderen [**D3D12 \_ RANGE-Struktur.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)

</dd> <dt>

**CD3DX12 \_ RANGE(SIZE \_ T begin, SIZE T \_ end)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ RANGE und initialisiert die folgenden Parameter:

SIZE \_ T begin

SIZE \_ T end

</dd> <dt>

**operator const D3D12 \_ RANGE&() const**
</dt> <dd>

Definiert den & Pass-by-Reference-Operator für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12 \_ RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





