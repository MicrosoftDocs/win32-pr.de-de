---
title: CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 -Struktur (D3dx12.h)
description: Eine Hilfsstruktur, die verwendet wird, um eine Tiefen-Schablonenbeschreibung als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist. | CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 -Struktur (D3dx12.h)
ms.assetid: 7D3554D9-610D-43B5-94F0-68167E966A86
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1-Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f04064a7ab4a7ca100e48da2446501d4415b693ce6abdf213f121952cc8f198
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632528"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil1-structure"></a>CD3DX12 \_ PIPELINE STATE STREAM DEPTH \_ \_ \_ \_ STENCIL1-Struktur

Eine Hilfsstruktur, die verwendet wird, um eine Tiefen-Schablonenbeschreibung als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 {
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1(CD3DX12_DEPTH_STENCIL_DESC1 const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 operator=(CD3DX12_DEPTH_STENCIL_DESC1 const& i);
                                               operator CD3DX12_DEPTH_STENCIL_DESC1() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ DEPTH \_ STENCIL1**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12 \_ PIPELINE STATE STREAM DEPTH \_ \_ \_ \_ STENCIL1.

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM DEPTH \_ \_ \_ \_ STENCIL1(CD3DX12 \_ DEPTH \_ STENCIL \_ DESC1 const &i)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 PIPELINE STATE STREAM DEPTH STENCIL1, initialisiert mit dem Unterobjekttyp \_ \_ D3D12 PIPELINE STATE SUBOBJECT TYPE DEPTH STENCIL1 und unterobjektdaten, die aus \_ i \_ kopiert \_ wurden, einer [**CD3DX12 \_ DEPTH \_ STENCIL \_ DESC1-Struktur.**](cd3dx12-depth-stencil-desc1.md) **\_ \_ \_ \_ \_ \_** 

</dd> <dt>

**operator=(CD3DX12 \_ DEPTH \_ STENCIL \_ DESC1 const& i)**
</dt> <dd>

Kopierzuweisungsoperator.

</dd> <dt>

**Operator CD3DX12 \_ DEPTH \_ STENCIL \_ DESC1() const**
</dt> <dd>

Implizite Konvertierung in eine [**CD3DX12 \_ DEPTH \_ STENCIL \_ DESC1-Struktur.**](cd3dx12-depth-stencil-desc1.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

CD3DX12 PIPELINE STATE STREAM DEPTH STENCIL1 ist eine Typedef-Spezialisierung der \_ \_ VORLAGE \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) und wird wie folgt definiert:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC1, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL1, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
          
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[**D3D12 \_ PIPELINE \_ STATE \_ SUBOBJECT \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

