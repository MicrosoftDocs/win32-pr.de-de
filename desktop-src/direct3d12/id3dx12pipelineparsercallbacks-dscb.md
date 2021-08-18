---
title: ID3DX12PipelineParserCallbacks DSCb-Methode (D3DX12.h)
description: Ruft den Domänen-Shader-Unterobjektrückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: F4877211-4122-4418-9323-3F68B0BB3363
keywords:
- DSCb-Methode
- DSCb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, DSCb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63c4cee98bf617fb02cb5c543050f51c56a733d56964e2139e5b7357c7a88034
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528988"
---
# <a name="id3dx12pipelineparsercallbacksdscb-method"></a>ID3DX12PipelineParserCallbacks::D SCb-Methode

Ruft den Domänen-Shader-Unterobjektrückruf eines Objekts auf, das diese Schnittstelle implementiert.

## <a name="syntax"></a>Syntax


```C++
void DSCb(
  [ref] const D3D12_SHADER_BYTECODE &DS
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DS* \[ Ref\]
</dt> <dd>

Typ: **const [**D3D12 \_ SHADER \_ BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**

Details des Domänen-Shader-Unterobjekts, das aus einem Pipelinezustandsstream analysiert wird.

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

[**\_D3D12-SHADER-BYTECODE \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





