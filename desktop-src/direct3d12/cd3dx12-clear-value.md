---
title: CD3DX12_CLEAR_VALUE -Struktur (D3dx12.h)
description: Eine Hilfsstruktur, um eine einfache Initialisierung einer D3D12 \_ CLEAR \_ VALUE-Struktur zu ermöglichen.
ms.assetid: C3E2FAF4-79C4-49CA-B7D3-1FED69C8F7A7
keywords:
- CD3DX12_CLEAR_VALUE-Struktur
topic_type:
- apiref
api_name:
- CD3DX12_CLEAR_VALUE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 785ab3c8312949bfc692fcd7c8d1dace28734ce08e5763387a744eb28f2000f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988490"
---
# <a name="cd3dx12_clear_value-structure"></a>CD3DX12 \_ CLEAR \_ VALUE-Struktur

Eine Hilfsstruktur, um eine einfache Initialisierung einer [**D3D12 \_ CLEAR \_ VALUE-Struktur zu**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_CLEAR_VALUE  : public D3D12_CLEAR_VALUE{
   CD3DX12_CLEAR_VALUE();
   explicit CD3DX12_CLEAR_VALUE(const D3D12_CLEAR_VALUE &o);
   CD3DX12_CLEAR_VALUE(DXGI_FORMAT format, const FLOAT color[ 4 ]);
   CD3DX12_CLEAR_VALUE(DXGI_FORMAT format, FLOAT depth, UINT8 stencil);
   operator const D3D12_CLEAR_VALUE&() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ CLEAR \_ VALUE()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ CLEAR \_ VALUE.

</dd> <dt>

**explicit CD3DX12 \_ CLEAR \_ VALUE(const D3D12 \_ CLEAR VALUE &\_ o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 CLEAR VALUE, initialisiert mit dem Inhalt einer anderen \_ \_ [**D3D12 \_ CLEAR \_ VALUE-Struktur.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value)

</dd> <dt>

**CD3DX12 \_ CLEAR \_ VALUE(DXGI \_ FORMAT format, const FLOAT color \[ 4 \] )**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ CLEAR \_ VALUE und initialisiert die folgenden Parameter:

[**DXGI \_ FORMAT-Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

FLOAT-Farbe \[ 4 \]

</dd> <dt>

**CD3DX12 \_ CLEAR \_ VALUE(DXGI \_ FORMAT format, FLOAT depth, UINT8 stencil)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ CLEAR \_ VALUE und initialisiert die folgenden Parameter:

[**DXGI \_ FORMAT-Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

FLOAT-Tiefe

UINT8-Schablone

</dd> <dt>

**operator const D3D12 \_ CLEAR \_ VALUE&() const**
</dt> <dd>

Definiert den & pass-by-reference-Operator für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**D3D12 \_ CLEAR \_ VALUE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

