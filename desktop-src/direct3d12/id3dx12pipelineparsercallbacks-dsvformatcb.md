---
title: ID3DX12PipelineParserCallbacks DepthStencilStateCb-Methode (D3DX12.h) (DSV)
description: Ruft den Rückruf des Unterobjektrückrufs für das Format des Tiefenschablonenwerts eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: BDD3AB24-34C6-41C8-984D-78A45867BF24
keywords:
- DepthStencilStateCb-Methode
- DepthStencilStateCb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, DepthStencilStateCb-Methode
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
ms.openlocfilehash: d72a7501c57af515a9c9e26a435aaae02ae3ebd4cdb260f37800fda1be3d720e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096418"
---
# <a name="id3dx12pipelineparsercallbacks-depthstencilstatecb-method-d3dx12h-for-depth-stencil-value"></a>ID3DX12PipelineParserCallbacks DepthStencilStateCb-Methode (D3DX12.h) für den Tiefenschablonenwert

Ruft den Rückruf des Unterobjektrückrufs für das Format des Tiefenschablonenwerts eines Objekts auf, das diese Schnittstelle implementiert.

## <a name="syntax"></a>Syntax


```C++
void DepthStencilStateCb(
   DXGI_FORMAT DepthStencilState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DepthStencilState* 
</dt> <dd>

Typ: **[ **DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Details des Unterobjekts für das Format des Tiefenschablonenwerts, das aus einem Pipelinezustandsdatenstrom analysiert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt nichts zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX12.h</dt> </dl>  |
| Bibliothek<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Hilfsschnittstellen für Direct3D 12](helper-interfaces-for-d3d12.md)
</dt> <dt>

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[**\_DXGI-FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> </dl>

 

