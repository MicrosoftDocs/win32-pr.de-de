---
title: CD3DX12_BOX -Struktur (D3dx12.h)
description: Eine Hilfsstruktur, um eine einfache Initialisierung einer D3D12 \_ BOX-Struktur zu ermöglichen.
ms.assetid: 7E1A352C-D664-4538-BA78-91493980559D
keywords:
- CD3DX12_BOX-Struktur
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
ms.openlocfilehash: f2aa358d8b2d772d45c6387221dd9e660a9630fbf90535ada7dcceefc3257879
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851410"
---
# <a name="cd3dx12_box-structure"></a>CD3DX12 \_ BOX-Struktur

Eine Hilfsstruktur, um eine einfache Initialisierung einer [**D3D12 \_ BOX-Struktur zu**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) ermöglichen.

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

**CD3DX12 \_ BOX()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12 \_ BOX.

</dd> <dt>

**explicit CD3DX12 \_ BOX(const D3D12 \_ BOX& o)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 BOX, die mit dem Inhalt einer anderen \_ [**D3D12 \_ BOX-Struktur initialisiert**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) wird.

</dd> <dt>

**explicit CD3DX12 \_ BOX(LONG Left, LONG Right)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 \_ BOX und initialisiert die folgenden Parameter:

LONG Left

LONG Right

</dd> <dt>

**explicit CD3DX12 \_ BOX(LONG Left, LONG Top, LONG Right, LONG Bottom)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 \_ BOX und initialisiert die folgenden Parameter:

LONG Left

LONG Top

LONG Right

LONG Bottom

</dd> <dt>

**explicit CD3DX12 \_ BOX(LONG Left, LONG Top, LONG Front, LONG Right, LONG Bottom, LONG Back)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 \_ BOX und initialisiert die folgenden Parameter:

LONG Left

LONG Top

LONG Front

LONG Right

LONG Bottom

LONG Back

</dd> <dt>

**~CD3DX12 \_ BOX()**
</dt> <dd>

Zerstört eine Instanz einer CD3DX12 \_ BOX.

</dd> <dt>

**operator const D3D12 \_ BOX&() const**
</dt> <dd>

Definiert den & pass-by-reference-Operator für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**D3D12 \_ BOX**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





