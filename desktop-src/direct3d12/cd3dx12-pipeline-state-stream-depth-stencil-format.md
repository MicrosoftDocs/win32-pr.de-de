---
title: CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um das Format der tiefen Schablone als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.
ms.assetid: 512DB46E-D8F0-482B-9174-C786FB91AFD2
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dc7ae2703ac80ac155c04d42624a081723288bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363960"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil_format-structure"></a>Struktur des CD3DX12-Daten \_ \_ Strom- \_ \_ tiefen \_ Schablonen \_ Formats

Eine hilfsstruktur, die verwendet wird, um das Format der tiefen Schablone als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT {
                                                     CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT;
                                                     CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT(DXGI_FORMAT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT operator=(DXGI_FORMAT const& i);
                                                     operator DXGI_FORMAT() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ Daten \_ \_ Strom- \_ tiefen \_ Schablone- \_ Format des Pipeline Zustands**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz des \_ tiefen Schablone-Formats eines CD3DX12 Pipeline \_ Zustandsdaten \_ Stroms \_ \_ \_ .

</dd> <dt>

**CD3DX12-Daten \_ \_ Strom- \_ \_ tiefen Schablone- \_ \_ Format (DXGI-Format, Konstante \_ &i)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ Pipeline \_ \_ \_ \_ -tiefen Schablone \_ -Formats, das mit einem untergeordneten Typ des untergeordneten Typs **D3D12 \_ Pipeline \_ State \_ unter Objekt \_ Type \_ tiefen \_ Schablone \_ Format** und aus *i* kopierten untergeordneten Daten, einer [**DXGI- \_ formatenumeration**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , initialisiert wird.

</dd> <dt>

**Operator = (DXGI- \_ Format Konstanten& i)**
</dt> <dd>

Kopier Zuweisungs Operator.

</dd> <dt>

**Operator DXGI \_ Format () konstant**
</dt> <dd>

Implizite Konvertierung in eine [**DXGI- \_ formatenumeration**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) .

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

CD3DX12 \_ \_ \_ \_ \_ das tiefen Schablone \_ -Format des Pipeline Zustands Stroms ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und ist wie folgt definiert:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<DXGI_FORMAT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL_FORMAT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT;
          
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**CD3DX12 \_ Pipeline State-Datenstrom-unter \_ \_ \_ Objekt**](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[**D3D12 \_ Pipeline \_ Status-unter Objekt- \_ \_ Typ**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

