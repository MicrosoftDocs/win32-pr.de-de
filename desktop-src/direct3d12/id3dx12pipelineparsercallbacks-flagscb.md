---
title: ID3DX12PipelineParserCallbacks flagscb-Methode (D3DX12. h)
description: Ruft den untergeordneten Flags-Rückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: 81DD8CF3-87BA-4380-BECD-70A80580048A
keywords:
- Flagscb-Methode
- Flagscb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, flagscb-Methode
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
ms.openlocfilehash: f30ac5a0ca3a749144e263a1d993166b8e13ddac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363991"
---
# <a name="id3dx12pipelineparsercallbacksflagscb-method"></a>ID3DX12PipelineParserCallbacks:: flagscb-Methode

Ruft den untergeordneten Flags-Rückruf eines Objekts auf, das diese Schnittstelle implementiert.

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

Type: **[ **D3D12 \_ Pipeline \_ State \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)**

Details der Flags, die aus einem Pipeline Status-Stream analysiert wurden.

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

[**D3D12 \_ Pipeline \_ - \_ Statusflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)
</dt> </dl>

 

 





