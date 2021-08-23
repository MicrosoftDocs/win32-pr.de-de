---
title: CD3DX12_RECT-Struktur (D3dx12.h)
description: Eine Hilfsstruktur, um eine einfache Initialisierung einer D3D12 \_ RECT-Struktur zu ermöglichen.
ms.assetid: FBF01294-1448-4D9A-BA6B-27D5D59C2958
keywords:
- CD3DX12_RECT-Struktur
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
ms.openlocfilehash: bff9df3a4c7df2f30e9614b16d5f8b89ea1b6f0279a1566b206cabef7260fb28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729340"
---
# <a name="cd3dx12_rect-structure"></a>CD3DX12 \_ RECT-Struktur

Eine Hilfsstruktur, um eine einfache Initialisierung einer [**D3D12 \_ RECT-Struktur**](d3d12-rect.md) zu ermöglichen.

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

**CD3DX12 \_ RECT()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ RECT.

</dd> <dt>

**explicit CD3DX12 \_ RECT(const D3D12 \_ RECT& o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ RECT, initialisiert mit dem Inhalt einer anderen [**D3D12 \_ RECT-Struktur.**](d3d12-rect.md)

</dd> <dt>

**Explicit CD3DX12 \_ RECT(LONG Left, LONG Top, LONG Right, LONG Bottom)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ RECT und initialisiert die folgenden Parameter:

LONG Left

LONG Top

LONG Right

LONG Bottom

</dd> <dt>

**~CD3DX12 \_ RECT()**
</dt> <dd>

Zerstört eine Instanz eines CD3DX12 \_ RECT.

</dd> <dt>

**operator const D3D12 \_ RECT&() const**
</dt> <dd>

Definiert den & Pass-by-Reference-Operator für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12 \_ RECT**](d3d12-rect.md)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





