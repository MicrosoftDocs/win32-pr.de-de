---
title: ID3DX12PipelineParserCallbacks RasterizerStateCb-Methode (D3DX12.h)
description: Ruft den Rückruf des Unterobjekts der Rasterizerzustandsbeschreibung eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: 125FC6EC-B749-4EE2-9D34-14BD12993BDC
keywords:
- RasterizerStateCb-Methode
- RasterizerStateCb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, RasterizerStateCb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RasterizerStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39a179f26d88f25027eb9ffc2b4b3712ac963b65179334fff1bfa4d6103ef76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528620"
---
# <a name="id3dx12pipelineparsercallbacksrasterizerstatecb-method"></a>ID3DX12PipelineParserCallbacks::RasterizerStateCb-Methode

Ruft den Rückruf des Unterobjekts der Rasterizerzustandsbeschreibung eines Objekts auf, das diese Schnittstelle implementiert.

## <a name="syntax"></a>Syntax


```C++
void RasterizerStateCb(
  [ref] const D3D12_RASTERIZER_DESC &RasterizerState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*RasterizerState* \[ Ref\]
</dt> <dd>

Typ: **const [**D3D12 \_ RASTERIZER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)**

Details des Rasterizer-Zustandsbeschreibungs-Unterobjekts, das aus einem Pipelinezustandsstream analysiert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt nichts zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX12.h</dt> </dl>  |
| Bibliothek<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Hilfsschnittstellen für Direct3D 12](helper-interfaces-for-d3d12.md)
</dt> <dt>

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[**D3D12 \_ RASTERIZER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> </dl>

 

 





