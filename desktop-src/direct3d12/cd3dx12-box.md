---
title: CD3DX12_BOX-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12 \_ Box-Struktur zu ermöglichen.
ms.assetid: 7E1A352C-D664-4538-BA78-91493980559D
keywords:
- CD3DX12_BOX Struktur
topic_type:
- apiref
api_name:
- CD3DX12_BOX
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.topic: reference
ms.localizationpriority: low
ms.date: 05/31/2018
ms.openlocfilehash: c689c9bfe611651248280f7536bd91a9f4d003d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371892"
---
# <a name="cd3dx12_box-structure"></a>CD3DX12 \_ Box-Struktur

Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12 \_ Box**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) -Struktur zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_BOX  : public D3D12_BOX{
   CD3DX12_BOX();
   explicit CD3DX12_BOX(const D3D12_BOX& o);
   explicit CD3DX12_BOX(LONG Left, LONG Right);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Right, LONG Bottom);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Front, LONG Right, LONG Bottom, LONG Back);
   ~CD3DX12_BOX();
   operator const D3D12_BOX&() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ Box ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 Box-Felds \_ .

</dd> <dt>

**explizites CD3DX12 Box-Feld \_ (konstant D3D12 \_ Box& o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12-Felds \_ , das mit dem Inhalt einer anderen [**D3D12 \_ Box**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) -Struktur initialisiert wird.

</dd> <dt>

**explizites CD3DX12 \_ Feld (Long Left, Long right)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 Felds \_ und initialisiert die folgenden Parameter:

Long Left

Long right

</dd> <dt>

**explizites CD3DX12 \_ Feld (Long Left, Long Top, Long right, Long Bottom)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 Felds \_ und initialisiert die folgenden Parameter:

Long Left

Langer Anfang

Long right

Long-Bottom

</dd> <dt>

**explizites CD3DX12 \_ Feld (Long Left, Long Top, Long Front, Long right, Long Bottom, Long Back)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 Felds \_ und initialisiert die folgenden Parameter:

Long Left

Langer Anfang

Lange Vorderseite

Long right

Long-Bottom

Lange wieder

</dd> <dt>

**~ CD3DX12 \_ Box ()**
</dt> <dd>

Zerstört eine Instanz einer CD3DX12 \_ Box.

</dd> <dt>

**Operator Konstanten D3D12 \_ Box& () Konstanten**
</dt> <dd>

Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12- \_ Feld**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





