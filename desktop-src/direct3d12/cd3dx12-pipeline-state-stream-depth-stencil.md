---
title: CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL -Struktur (D3dx12.h)
description: Eine Hilfsstruktur, die verwendet wird, um eine Tiefen-Schablonenbeschreibung als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist. | CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL -Struktur (D3dx12.h)
ms.assetid: 4FB54EA5-FCC6-4B64-A747-27DFE4C1D2DC
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL-Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0b9cc7ba6b37858ae355d9470f321f991e8329f5fbf7aabd23b6f8bcfe7d8fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858180"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil-structure"></a>CD3DX12 \_ PIPELINE STATE STREAM DEPTH \_ \_ \_ \_ STENCIL-Struktur

Eine Hilfsstruktur, die verwendet wird, um eine Tiefen-Schablonenbeschreibung als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL {
                                              CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL;
                                              CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL(CD3DX12_DEPTH_STENCIL_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL operator=(CD3DX12_DEPTH_STENCIL_DESC const& i);
                                              operator CD3DX12_DEPTH_STENCIL_DESC() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ DEPTH \_ STENCIL**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12 \_ PIPELINE \_ STATE STREAM \_ \_ \_ DEPTH-SCHABLOne.

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM DEPTH \_ \_ \_ \_ STENCIL(CD3DX12 \_ DEPTH \_ STENCIL \_ DESC const &i)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 PIPELINE STATE STREAM DEPTH-SCHABLOne, die mit dem Unterobjekttyp D3D12 PIPELINE STATE SUBOBJECT TYPE DEPTH STENCIL initialisiert wurde, und unterobjektdaten, die aus \_ \_ i kopiert \_ \_ \_ wurden, einer [**CD3DX12 \_ DEPTH \_ STENCIL \_ DESC-Struktur.**](cd3dx12-depth-stencil-desc.md) **\_ \_ \_ \_ \_ \_** 

</dd> <dt>

**operator=(CD3DX12 \_ DEPTH \_ STENCIL \_ DESC const& i)**
</dt> <dd>

Kopierzuweisungsoperator.

</dd> <dt>

**Operator CD3DX12 \_ DEPTH \_ STENCIL \_ DESC() const**
</dt> <dd>

Implizite Konvertierung in eine [**CD3DX12 \_ DEPTH \_ STENCIL \_ DESC-Struktur.**](cd3dx12-depth-stencil-desc.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

CD3DX12 PIPELINE STATE STREAM DEPTH STENCIL ist eine Typedef-Spezialisierung der \_ \_ VORLAGE \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) und wie folgt definiert:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL;
          
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[**D3D12 \_ PIPELINE \_ STATE \_ SUBOBJECT \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

