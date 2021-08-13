---
title: ID3DX12PipelineParserCallbacks BlendStateCb-Methode (D3DX12.h)
description: Ruft den Rückruf des Unterobjekts für die Beschreibung des Blendzustands eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: C00C733B-4123-4795-9A93-973F30BE456B
keywords:
- BlendStateCb-Methode
- BlendStateCb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, BlendStateCb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.BlendStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65a9d84e3648a54668211b8b9e590c653111c93553115aba43b5353f9549bfc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528978"
---
# <a name="id3dx12pipelineparsercallbacksblendstatecb-method"></a>ID3DX12PipelineParserCallbacks::BlendStateCb-Methode

Ruft den Rückruf des Unterobjekts für die Beschreibung des Blendzustands eines Objekts auf, das diese Schnittstelle implementiert.

## <a name="syntax"></a>Syntax


```C++
void BlendStateCb(
  [ref] const D3D12_BLEND_DESC &BlendState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*BlendState* \[ Ref\]
</dt> <dd>

Typ: **const [**D3D12 \_ BLEND \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)**

Details des Ausblendzustandsbeschreibungs-Unterobjekts, das aus einem Pipelinezustandsstream analysiert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt nichts zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX12.h</dt> </dl>  |
| Bibliothek<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Hilfsschnittstellen für Direct3D 12](helper-interfaces-for-d3d12.md)
</dt> <dt>

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[**D3D12 \_ BLEND \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> </dl>

 

 





