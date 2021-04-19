---
title: ID3DX12PipelineParserCallbacks nodemaskcb-Methode (D3DX12. h)
description: Ruft den nodemask-untergeordneten Rückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: F5A408B7-A777-4BBC-A2A3-1BC3551E65ED
keywords:
- Nodemaskcb-Methode
- Nodemaskcb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks Interface, nodemaskcb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.NodemaskCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdf1cc03f60259c395ca8c459ddd5a308e3dcd6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353338"
---
# <a name="id3dx12pipelineparsercallbacksnodemaskcb-method"></a>ID3DX12PipelineParserCallbacks:: nodemaskcb-Methode

Ruft den nodemask-untergeordneten Rückruf eines Objekts auf, das diese Schnittstelle implementiert.

## <a name="syntax"></a>Syntax


```C++
void NodemaskCb(
   
        UINT
       Nodemask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Nodemask* 
</dt> <dd>

Typ: **uint**

Details zum nodemask-unter Objekt, das aus einem Pipeline Status-Stream analysiert wurde.

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
</dt> </dl>

 

 





