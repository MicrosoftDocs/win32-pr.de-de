---
title: ID3DX12PipelineParserCallbacks errorduplitoresubobject-Methode (D3DX12. h)
description: Ruft den doppelten untergeordneten Fehler Rückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: 625C72C4-7BFB-4DAD-8D39-EDDBC7189499
keywords:
- Errorduplitoresubobject-Methode
- Errorduplitoresubobject-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks Interface, errorduplitoresubobject-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorDuplicateSubobject
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b00dae4675ff05a43e566a8ead815ea24f6c16
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361226"
---
# <a name="id3dx12pipelineparsercallbackserrorduplicatesubobject-method"></a>ID3DX12PipelineParserCallbacks:: errorduplitoresubobject-Methode

Ruft den doppelten untergeordneten Fehler Rückruf eines Objekts auf, das diese Schnittstelle implementiert.

## <a name="syntax"></a>Syntax


```C++
void ErrorDuplicateSubobject(
   D3D12_PIPELINE_STATE_SUBOBJECT_TYPE DuplicateType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Duplialisietype* 
</dt> <dd>

Type: **[ **D3D12 \_ Pipeline \_ State \_ SubObject \_ Type**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)**

Der Typ des untergeordneten Objekts, das dupliziert wurde.

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

[**D3D12 \_ Pipeline \_ Status-unter Objekt- \_ \_ Typ**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

