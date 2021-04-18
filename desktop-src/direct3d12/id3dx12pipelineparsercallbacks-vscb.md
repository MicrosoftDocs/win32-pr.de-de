---
title: ID3DX12PipelineParserCallbacks vscb-Methode (D3DX12. h)
description: Ruft den Vertex-shadersubobject-Rückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: 65A185B7-C790-4254-A3C5-EBBE9C38CA4E
keywords:
- Vscb-Methode
- Vscb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, vscb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.VSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eef9ab27b2f9fd4b93190e2eea453397de297013
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365324"
---
# <a name="id3dx12pipelineparsercallbacksvscb-method"></a>ID3DX12PipelineParserCallbacks:: vscb-Methode

Ruft den Vertex-shadersubobject-Rückruf eines Objekts auf, das diese Schnittstelle implementiert.

## <a name="syntax"></a>Syntax


```C++
void VSCb(
  [ref] const D3D12_SHADER_BYTECODE &VS
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Vs* \[ atur\]
</dt> <dd>

Typ: **Konstanten [**D3D12 \_ Shader- \_ Bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**

Details des Vertex-Shader-unter Objekts, das aus einem Pipeline Status-Stream analysiert wurde.

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

[**D3D12- \_ Shader- \_ Bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





