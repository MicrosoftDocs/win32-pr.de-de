---
title: ID3DX12PipelineParserCallbacks SampleMaskCb-Methode (D3DX12.h)
description: Ruft den Beispielmasken-Unterobjektrückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: 4D729414-1E04-407B-B32F-ECE1EA9FF414
keywords:
- SampleMaskCb-Methode
- SampleMaskCb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, SampleMaskCb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.SampleMaskCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64acc7e969f52e78250cde9bc4c693ce3eae06ae3edd08e7f18c65dc0ff6fa8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069590"
---
# <a name="id3dx12pipelineparsercallbackssamplemaskcb-method"></a>ID3DX12PipelineParserCallbacks::SampleMaskCb-Methode

Ruft den Beispielmasken-Unterobjektrückruf eines Objekts auf, das diese Schnittstelle implementiert.

## <a name="syntax"></a>Syntax


```C++
void SampleMaskCb(
   
        UINT
           SampleMask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SampleMask* 
</dt> <dd>

Typ: **UINT**

Details des Beispielmasken-Unterobjekts, das aus einem Pipelinezustandsdatenstrom analysiert wird.

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
</dt> </dl>

 

 





