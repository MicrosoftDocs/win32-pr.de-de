---
title: ID3DX12PipelineParserCallbacks depthstencilstatuecb-Methode (D3DX12. h)
description: Ruft den Unterbrechungs Status der tiefen Schablone eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: 6E77A3B7-20D8-4D31-9D31-515CF4618157
keywords:
- Depthstencilstatuecb-Methode
- Depthstencilstatus ECB-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks Interface, depthstencilstatuecb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DepthStencilStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 913dbddef0c509174d3600798a6e1380d6098808
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355782"
---
# <a name="id3dx12pipelineparsercallbacks-depthstencilstatecb-method-d3dx12h"></a>ID3DX12PipelineParserCallbacks depthstencilstatuecb-Methode (D3DX12. h)

Ruft den Unterbrechungs Status der tiefen Schablone eines Objekts auf, das diese Schnittstelle implementiert.

## <a name="syntax"></a>Syntax


```C++
void DepthStencilStateCb(
  [ref] const D3D12_DEPTH_STENCIL_DESC &DepthStencilState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Depthstencilstate* \[ atur\]
</dt> <dd>

Typ: **Konstanten [**D3D12 \_ Tiefe \_ Schablone \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)**

Details des von einem Pipeline Status-Stream analysierten tiefen Schablone-Zustands untergeordneten Objekts.

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

[**D3D12 \_ tiefen \_ Schablone-Schablone \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> </dl>

 

 





