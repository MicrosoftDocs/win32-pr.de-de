---
title: ID3DX12PipelineParserCallbacks samplemaskcb-Methode (D3DX12. h)
description: Ruft den Sample Mask-Unterordner Rückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: 4D729414-1E04-407B-B32F-ECE1EA9FF414
keywords:
- Samplemaskcb-Methode
- Samplemaskcb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, samplemaskcb-Methode
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
ms.openlocfilehash: 0124b228056089e21c078ffce25ce59eef0e3dee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371880"
---
# <a name="id3dx12pipelineparsercallbackssamplemaskcb-method"></a>ID3DX12PipelineParserCallbacks:: samplemaskcb-Methode

Ruft den Sample Mask-Unterordner Rückruf eines Objekts auf, das diese Schnittstelle implementiert.

## <a name="syntax"></a>Syntax


```C++
void SampleMaskCb(
   
        UINT
           SampleMask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Samplemask* 
</dt> <dd>

Typ: **uint**

Details zum in einem Pipeline Status-Stream analysierten Sample Mask-unter Objekt.

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

 

 





