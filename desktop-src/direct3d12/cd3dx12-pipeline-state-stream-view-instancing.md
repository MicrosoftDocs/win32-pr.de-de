---
title: CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING-Struktur (D3dx12.h)
description: Eine Hilfsstruktur, die zum Umschließen einer [CD3DX12_VIEW_INSTANCING_DESC-Struktur](cd3dx12-view-instancing-desc.md) verwendet wird. Ermöglicht Shadern das Rendern in mehreren Ansichten mit einem einzelnen Zeichnen-Aufruf. nützlich für stereo-Vision oder Cubemap-Generierung.
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING-Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/05/2021
ms.openlocfilehash: 6bf5d69232f9cf61e7b650df1f53229eabff4e0a0199ef5ec804e6d592855a2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119261777"
---
# <a name="cd3dx12_pipeline_state_stream_view_instancing-structure"></a>CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING-Struktur

Eine Hilfsstruktur, die zum Umschließen einer [CD3DX12_VIEW_INSTANCING_DESC-Struktur](cd3dx12-view-instancing-desc.md) verwendet wird. Ermöglicht Shadern das Rendern in mehreren Ansichten mit einem einzelnen Zeichnen-Aufruf. nützlich für stereo-Vision oder Cubemap-Generierung.

## <a name="syntax"></a>Syntax

```cpp
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_VIEW_INSTANCING_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_VIEW_INSTANCING, CD3DX12_DEFAULT> CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING;
```

**CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING** ist eine `typedef` Spezialisierung der [CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT](cd3dx12-pipeline-state-stream-subobject.md) Vorlage.

## <a name="members"></a>Member

Weitere Informationen finden Sie [unter CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT](cd3dx12-pipeline-state-stream-subobject.md) und [CD3DX12_VIEW_INSTANCING_DESC](cd3dx12-view-instancing-desc.md).

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Weitere Informationen

* [Hilfsstrukturen für Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT](cd3dx12-pipeline-state-stream-subobject.md)
* [D3D12_PIPELINE_STATE_SUBOBJECT_TYPE](/windows/win32/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
* [D3DX12_VIEW_INSTANCING_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)
