---
title: ID3DX12PipelineParserCallbacks ibstripcutvaluecb-Methode (D3DX12. h)
description: Ruft den untergeordneten Rückruf Wert des Index Puffers eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: 702CA90A-FF20-4554-9469-C86428C203BC
keywords:
- Ibstripcutvaluecb-Methode
- Ibstripcutvaluecb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, ibstripcutvaluecb-Methode
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
ms.openlocfilehash: f79fca93e76f43b97ffc8e133594805214fe84cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350704"
---
# <a name="id3dx12pipelineparsercallbacksibstripcutvaluecb-method"></a>ID3DX12PipelineParserCallbacks:: ibstripcutvaluecb-Methode

Ruft den untergeordneten Rückruf Wert des Index Puffers eines Objekts auf, das diese Schnittstelle implementiert.

## <a name="syntax"></a>Syntax


```C++
void IBStripCutValueCb(
   D3D12_INDEX_BUFFER_STRIP_CUT_VALUE IBStripCutValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ibstripcutvalue* 
</dt> <dd>

Type: **[ **D3D12 \_ Index- \_ Puffer \_ Strip- \_ Ausschneide \_ Wert**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)**

Details des von einem Pipeline Status-Stream analysierten Bereichs Ausschneide Werts für den Index Puffer.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt nichts zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX12. h</dt> </dl>  |
| Bibliothek<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Hilfsschnittstellen für Direct3D 12](helper-interfaces-for-d3d12.md)
</dt> <dt>

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[**D3D12 \_ Index-Puffer leisten- \_ \_ \_ Ausschneide \_ Wert**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)
</dt> </dl>

 

 





