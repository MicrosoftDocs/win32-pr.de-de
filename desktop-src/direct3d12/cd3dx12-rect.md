---
title: CD3DX12_RECT-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12 \_ Rect-Struktur zu ermöglichen.
ms.assetid: FBF01294-1448-4D9A-BA6B-27D5D59C2958
keywords:
- CD3DX12_RECT Struktur
topic_type:
- apiref
api_name:
- CD3DX12_RECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6d8c133f14b531433ceb2239377ea85ba212af
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351929"
---
# <a name="cd3dx12_rect-structure"></a>CD3DX12 \_ Rect-Struktur

Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12 \_ Rect**](d3d12-rect.md) -Struktur zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_RECT  : public D3D12_RECT{
   CD3DX12_RECT();
   explicit CD3DX12_RECT(const D3D12_RECT& o);
   explicit CD3DX12_RECT(LONG Left, LONG Top, LONG Right, LONG Bottom);
   ~CD3DX12_RECT();
   operator const D3D12_RECT&() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ Rect ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ Rect.

</dd> <dt>

**explizites CD3DX12 \_ Rect (konstant D3D12 \_ Rect& o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ Rect, das mit dem Inhalt einer anderen [**D3D12 \_ Rect**](d3d12-rect.md) -Struktur initialisiert wird.

</dd> <dt>

**explizites CD3DX12 \_ Rect (Long Left, Long Top, Long right, Long Bottom)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ Rect und initialisiert die folgenden Parameter:

Long Left

Langer Anfang

Long right

Long-Bottom

</dd> <dt>

**~ CD3DX12 \_ Rect ()**
</dt> <dd>

Zerstört eine Instanz eines CD3DX12 \_ Rect.

</dd> <dt>

**Operator Konstanten D3D12 \_ Rect& () Konstanten**
</dt> <dd>

Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12 \_ Rect**](d3d12-rect.md)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





