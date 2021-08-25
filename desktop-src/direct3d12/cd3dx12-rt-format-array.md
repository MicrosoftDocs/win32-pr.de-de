---
title: CD3DX12_RT_FORMAT_ARRAY-Struktur (D3dx12.h)
description: Eine Hilfsstruktur, um eine einfache Initialisierung einer D3D12 \_ RT \_ FORMAT \_ ARRAY-Struktur zu ermöglichen.
ms.assetid: E890DD33-599F-4B20-BD15-2734867788E5
keywords:
- CD3DX12_RT_FORMAT_ARRAY Struktur
topic_type:
- apiref
api_name:
- CD3DX12_RT_FORMAT_ARRAY
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a9c153b98e84176d2682f028657176902fb68ebc0e8e1e52c69c196842dc2fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988361"
---
# <a name="cd3dx12_rt_format_array-structure"></a>CD3DX12 \_ RT \_ FORMAT \_ ARRAY-Struktur

Eine Hilfsstruktur, um eine einfache Initialisierung einer [**D3D12 \_ RT \_ FORMAT \_ ARRAY-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_RT_FORMAT_ARRAY  : public D3D12_RT_FORMAT_ARRAY{
  CD3DX12_RT_FORMAT_ARRAY CD3DX12_RT_FORMAT_ARRAY();
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const D3D12_RT_FORMAT_ARRAY& o);
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const DXGI_FORMAT* pFormats, UINT NumFormats);
                          operator const D3D12_RT_FORMAT_ARRAY&() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ RT \_ FORMAT \_ ARRAY()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ RT \_ FORMAT \_ ARRAY.

</dd> <dt>

**explicit CD3DX12 \_ RT \_ FORMAT \_ ARRAY(const D3D12 \_ RT FORMAT ARRAY& \_ \_ o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ RT \_ FORMAT \_ ARRAY, initialisiert mit Werten, die aus einer [**D3D12 \_ RT FORMAT \_ \_ ARRAY-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) kopiert wurden.

</dd> <dt>

**explicit CD3DX12 \_ RT \_ FORMAT \_ ARRAY(const DXGI \_ FORMAT \* pFormats, UINT NumFormats)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ RT \_ FORMAT \_ ARRAY, initialisiert mit den in der Parameterliste übergebenen Werten. Der Inhalt des durch den *pFormats-Parameter angegebenen Arrays* wird in das Memberarray **RTFormats** kopiert. Es wird davon ausgegangen, dass das von *pFormats* angegebene Array die gleiche Größe wie **RTFormats hat.**

</dd> <dt>

**operator const D3D12 \_ RT \_ FORMAT ARRAY \_&() const**
</dt> <dd>

Implizite Konvertierung in eine [**D3D12 \_ RT \_ FORMAT \_ ARRAY-Struktur.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) Da D3D12 \_ RT FORMAT ARRAY der zugrunde liegende Typ von \_ \_ CD3DX12 \_ DEPTH \_ STENCIL \_ DESC1 ist, wird das Objekt einfach als const D3D12 \_ RT FORMAT \_ \_ ARRAY-Verweis auf sich selbst zurückgegeben.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**D3D12 \_ RT \_ FORMAT \_ ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





