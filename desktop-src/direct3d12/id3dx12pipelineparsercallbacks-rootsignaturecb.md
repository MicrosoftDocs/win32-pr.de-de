---
title: ID3DX12PipelineParserCallbacks rootsignaturecb-Methode (D3DX12. h)
description: Ruft den untergeordneten Signatur-untergeordneten Rückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: FD467001-41B1-4A73-8E54-12C6B5EEAC3E
keywords:
- Rootsignaturecb-Methode
- Rootsignaturecb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, rootsignaturecb-Methode
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
ms.openlocfilehash: 78160ff1e61432a0711876934215ff15afb918de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373482"
---
# <a name="id3dx12pipelineparsercallbacksrootsignaturecb-method"></a>ID3DX12PipelineParserCallbacks:: rootsignaturecb-Methode

Ruft den untergeordneten Signatur-untergeordneten Rückruf eines Objekts auf, das diese Schnittstelle implementiert.

## <a name="syntax"></a>Syntax


```C++
void RootSignatureCb(
   ID3D12RootSignature *RootSignature
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Rootsignature* 
</dt> <dd>

Typ: **[ **ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)\***

Details des Stamm Signatur Objekts, das aus einem Pipeline Status-Stream analysiert wurde.

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

[**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)
</dt> </dl>

 

