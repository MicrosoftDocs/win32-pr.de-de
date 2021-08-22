---
title: ID3DX12PipelineParserCallbacks IBStripCutValueCb-Methode (D3DX12.h)
description: Ruft den Indexpuffer-Strip-Cut-Wert-Unterobjektrückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: 702CA90A-FF20-4554-9469-C86428C203BC
keywords:
- IBStripCutValueCb-Methode
- IBStripCutValueCb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, IBStripCutValueCb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.IBStripCutValueCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbdbbe2d66ae38a3bcd04ee84e6db15841d8f74a3b0d311552a51a892445b38f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124068"
---
# <a name="id3dx12pipelineparsercallbacksibstripcutvaluecb-method"></a>ID3DX12PipelineParserCallbacks::IBStripCutValueCb-Methode

Ruft den Indexpuffer-Strip-Cut-Wert-Unterobjektrückruf eines Objekts auf, das diese Schnittstelle implementiert.

## <a name="syntax"></a>Syntax


```C++
void IBStripCutValueCb(
   D3D12_INDEX_BUFFER_STRIP_CUT_VALUE IBStripCutValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IBStripCutValue* 
</dt> <dd>

Typ: **[ **D3D12 \_ INDEX BUFFER STRIP CUT \_ \_ \_ \_ VALUE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)**

Details des index buffer strip-cut value-Unterobjekts, das aus einem Pipelinezustandsdatenstrom analysiert wird.

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

[**D3D12 \_ INDEX \_ BUFFER \_ STRIP \_ CUT \_ VALUE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)
</dt> </dl>

 

 





