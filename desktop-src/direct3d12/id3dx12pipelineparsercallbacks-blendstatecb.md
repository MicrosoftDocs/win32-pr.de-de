---
title: ID3DX12PipelineParserCallbacks blendstatuecb-Methode (D3DX12. h)
description: Ruft den untergeordneten Blend-Zustands Beschreibungs Rückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: C00C733B-4123-4795-9A93-973F30BE456B
keywords:
- Blendstatuecb-Methode
- Blendstatuecb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks Interface, blendstatus ECB-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.BlendStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 119733fbe82203a6e423fb0ef9b07d3ecff70619
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353382"
---
# <a name="id3dx12pipelineparsercallbacksblendstatecb-method"></a>ID3DX12PipelineParserCallbacks:: blendstatuecb-Methode

Ruft den untergeordneten Blend-Zustands Beschreibungs Rückruf eines Objekts auf, das diese Schnittstelle implementiert.

## <a name="syntax"></a>Syntax


```C++
void BlendStateCb(
  [ref] const D3D12_BLEND_DESC &BlendState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Blendstate* \[ atur\]
</dt> <dd>

Typ: **Konstanten [**D3D12 \_ Blend \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)**

Details der Blend-Statusbeschreibung, die aus einem Pipeline Status-Stream analysiert wurde.

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

[**D3D12 \_ Blend- \_ Entsc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> </dl>

 

 





