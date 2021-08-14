---
title: ID3DX12PipelineParserCallbacks FlagsCb-Methode (D3DX12.h)
description: Ruft den Flags-Unterobjektrückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: 81DD8CF3-87BA-4380-BECD-70A80580048A
keywords:
- FlagsCb-Methode
- FlagsCb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, FlagsCb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.FlagsCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d14e8b507ae04a5f35b2786ca4ba7ab6ec19bb449492aa2c40f32510cd3ecb57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528782"
---
# <a name="id3dx12pipelineparsercallbacksflagscb-method"></a>ID3DX12PipelineParserCallbacks::FlagsCb-Methode

Ruft den Flags-Unterobjektrückruf eines Objekts auf, das diese Schnittstelle implementiert.

## <a name="syntax"></a>Syntax


```C++
void FlagsCb(
   D3D12_PIPELINE_STATE_FLAGS Flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* 
</dt> <dd>

Typ: **[ **D3D12 \_ PIPELINE \_ STATE \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)**

Details des Flags-Unterobjekts, das aus einem Pipelinezustandsstream analysiert wird.

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

[**D3D12 \_ PIPELINE \_ STATE \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)
</dt> </dl>

 

 





