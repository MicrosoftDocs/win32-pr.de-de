---
title: ID3DX12PipelineParserCallbacks cscb-Methode (D3DX12. h)
description: Ruft den Compute-Shader-untergeordneten Rückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: DE1ABA3D-D372-4D7F-9DB6-4E3360EAFAC2
keywords:
- Cscb-Methode
- Cscb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, cscb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.CSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27dcf175d153211e06864cb73139b03f868d15db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361227"
---
# <a name="id3dx12pipelineparsercallbackscscb-method"></a>ID3DX12PipelineParserCallbacks:: cscb-Methode

Ruft den Compute-Shader-untergeordneten Rückruf eines Objekts auf, das diese Schnittstelle implementiert.

## <a name="syntax"></a>Syntax


```C++
void CSCb(
  [ref] const D3D12_SHADER_BYTECODE &CS
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*CS* \[ atur\]
</dt> <dd>

Typ: **Konstanten [**D3D12 \_ Shader- \_ Bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**

Details des von einem Pipeline Status-Stream analysierten Compute-Shader-untergeordneten Objekts.

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

 

 





