---
title: CD3DX12_PIPELINE_STATE_STREAM_CS-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die zum Beschreiben eines Compute-Shaders als einzelnes Objekt verwendet wird, das für eine Datenstrom Beschreibung geeignet ist.
ms.assetid: B76B0CB4-FC76-4C5B-84FC-DCFF907BE2F8
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_CS Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_CS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5796e0f96ad4e2a87d2a45519321c363078a34b1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373489"
---
# <a name="cd3dx12_pipeline_state_stream_cs-structure"></a>CD3DX12 \_ Pipeline \_ State \_ Stream \_ CS-Struktur

Eine hilfsstruktur, die zum Beschreiben eines Compute-Shaders als einzelnes Objekt verwendet wird, das für eine Datenstrom Beschreibung geeignet ist.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_CS {
                                   CD3DX12_PIPELINE_STATE_STREAM_CS;
                                   CD3DX12_PIPELINE_STATE_STREAM_CS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_CS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12- \_ Pipeline- \_ Stream- \_ \_ Datenstrom**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12- \_ Pipeline- \_ State-Stream- \_ \_ cs.

</dd> <dt>

**CD3DX12 \_ Pipeline \_ State \_ Stream \_ cs (D3D12 \_ Shader \_ Bytecode Konstanten &i)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ -Pipeline \_ -State- \_ Stream \_ -cs, initialisiert mit einem untergeordneten Typ von **D3D12 Pipeline State-untergeordneten \_ \_ Typ- \_ \_ \_ CS** und unter aus *i* kopierten Daten, einer [**D3D12 \_ Shader- \_ Bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) -Struktur.

</dd> <dt>

**Operator = (D3D12 \_ Shader \_ Bytecode Konstanten& i)**
</dt> <dd>

Kopier Zuweisungs Operator.

</dd> <dt>

**Operator D3D12 \_ Shader \_ Bytecode () Konstanten**
</dt> <dd>

Implizite Konvertierung in eine [**D3D12 \_ Shader- \_ Bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) -Struktur.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

CD3DX12 \_ Pipeline \_ State \_ Stream \_ CS ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und wird wie folgt definiert:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_CS>
    CD3DX12_PIPELINE_STATE_STREAM_CS;
          
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

 

