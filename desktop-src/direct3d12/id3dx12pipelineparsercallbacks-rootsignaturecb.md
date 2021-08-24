---
title: ID3DX12PipelineParserCallbacks RootSignatureCb-Methode (D3DX12.h)
description: Ruft den Rückruf eines Stammsignaturunterobjekts eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: FD467001-41B1-4A73-8E54-12C6B5EEAC3E
keywords:
- RootSignatureCb-Methode
- RootSignatureCb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, RootSignatureCb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RootSignatureCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52b284a1f44ae1f77c80788b1af21cf29ba480881e82feac38bfccdba6e8e8ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792150"
---
# <a name="id3dx12pipelineparsercallbacksrootsignaturecb-method"></a>ID3DX12PipelineParserCallbacks::RootSignatureCb-Methode

Ruft den Rückruf eines Stammsignaturunterobjekts eines Objekts auf, das diese Schnittstelle implementiert.

## <a name="syntax"></a>Syntax


```C++
void RootSignatureCb(
   ID3D12RootSignature *RootSignature
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*RootSignature* 
</dt> <dd>

Typ: **[ **ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)\***

Details des Stammsignatur-Unterobjekts, das aus einem Pipelinezustandsstream analysiert wird.

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

[**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)
</dt> </dl>

 

