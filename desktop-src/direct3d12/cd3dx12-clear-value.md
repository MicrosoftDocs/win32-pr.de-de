---
title: CD3DX12_CLEAR_VALUE-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12-Clear-Value-Struktur zu ermöglichen \_ \_ .
ms.assetid: C3E2FAF4-79C4-49CA-B7D3-1FED69C8F7A7
keywords:
- CD3DX12_CLEAR_VALUE Struktur
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
ms.openlocfilehash: 6b9dc7afc62c6e9a3e229e6f5bdc4287bf4b85a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366442"
---
# <a name="cd3dx12_clear_value-structure"></a>CD3DX12 \_ Clear \_ value-Struktur

Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12- \_ Clear- \_ value**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) -Struktur zu ermöglichen.

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

**CD3DX12 \_ Clear \_ value ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 Clear- \_ \_ Werts.

</dd> <dt>

**expliziter CD3DX12 \_ Clear \_ value (konstant D3D12 \_ Clear \_ value &o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ Clear- \_ Werts, initialisiert mit dem Inhalt einer anderen [**D3D12 \_ Clear \_ value**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) -Struktur.

</dd> <dt>

**CD3DX12 \_ Clear \_ value (DXGI \_ Format Format, Konstante float Color \[ 4 \] )**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ Clear- \_ Werts und initialisiert die folgenden Parameter:

[**DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Format

FLOAT-Farbe \[ 4 \]

</dd> <dt>

**CD3DX12 \_ Clear \_ value (DXGI- \_ Format Format, float-Tiefe, Uint8-Schablone)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ Clear- \_ Werts und initialisiert die folgenden Parameter:

[**DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Format

Gleit Komma Tiefe

Uint8-Schablone

</dd> <dt>

**Operator Konstanten D3D12 \_ Clear \_ value& () Konstanten**
</dt> <dd>

Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12 \_ - \_ Wert löschen**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

