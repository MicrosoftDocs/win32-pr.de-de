---
title: CD3DX12_RT_FORMAT_ARRAY-Struktur (D3dx12. h)
description: Eine hilfsstruktur, mit der die einfache Initialisierung einer \_ Array Struktur im D3D12 RT-Format aktiviert werden kann \_ \_ .
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
ms.openlocfilehash: c05b7ae9e51d2d6b2a43f45dc83bda2074f6b734
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106360238"
---
# <a name="cd3dx12_rt_format_array-structure"></a>CD3DX12 \_ RT- \_ Format \_ Array Struktur

Eine hilfsstruktur, mit der die einfache Initialisierung einer Array Struktur im [**D3D12 \_ RT- \_ \_ Format**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) aktiviert werden kann.

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

**CD3DX12 \_ RT- \_ Format \_ Array ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 RT- \_ \_ Format \_ Arrays.

</dd> <dt>

**explizites CD3DX12 \_ RT- \_ Format \_ Array (konstant D3D12 \_ RT- \_ Format \_ Array& o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ RT- \_ Format \_ Arrays, das mit Werten initialisiert wird, die aus einer Array Struktur des [**D3D12 RT- \_ \_ Formats \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) kopiert wurden.

</dd> <dt>

**explizites CD3DX12 \_ RT- \_ Format \_ Array (Konstante DXGI- \_ Format \* pformats, uint-numformats)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ RT- \_ Format \_ Arrays, das mit den in der Parameterliste übergebenen Werten initialisiert wird. Der Inhalt des Arrays, das durch den *pformats* -Parameter angegeben wird, wird in das Member-Array **rtformats** kopiert. Das von *pformats* angegebene Array hat die gleiche Größe wie **rtformats**.

</dd> <dt>

**Operator Konstanten D3D12 \_ RT- \_ Format \_ Array& () Konstanten**
</dt> <dd>

Implizite Konvertierung in eine [**Array Struktur im D3D12 \_ RT- \_ Format \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) . Da das D3D12 \_ RT- \_ Format \_ Array der zugrunde liegende Typ von CD3DX12- \_ tiefen \_ Schablone DESC1 ist \_ , wird das-Objekt einfach als Array Verweis des Konstanten D3D12 \_ RT- \_ Formats \_ an sich selbst zurückgegeben.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**D3D12 \_ RT- \_ Format \_ Array**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





