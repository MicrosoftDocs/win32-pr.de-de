---
title: ID3DX12PipelineParserCallbacks primitivetopologytypecb-Methode (D3DX12. h)
description: Ruft den untergeordneten Topologietyp-Rückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: FF9D8D5C-3A6A-40D8-8EA4-3EA305EB4568
keywords:
- Primitivetopologytypecb-Methode
- Primitivetopologytypecb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, primitivetopologytypecb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.PrimitiveTopologyTypeCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01a2d73edd6ac94719905757d75a756c905c832
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357253"
---
# <a name="id3dx12pipelineparsercallbacksprimitivetopologytypecb-method"></a>ID3DX12PipelineParserCallbacks::P rimitivetopologytypecb-Methode

Ruft den untergeordneten Topologietyp-Rückruf eines Objekts auf, das diese Schnittstelle implementiert.

## <a name="syntax"></a>Syntax


```C++
void PrimitiveTopologyTypeCb(
   D3D12_PRIMITIVE_TOPOLOGY_TYPE PrimitiveTopologyType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Primitivetopologytype* 
</dt> <dd>

Type: **[ **D3D12 \_ primitiver \_ \_ Topologietyp**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)**

Details des primitiven topologietyps, der aus einem Pipeline Status-Stream analysiert wurde.

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

[**D3D12 \_ primitiver \_ \_ Topologietyp**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)
</dt> </dl>

 

 





