---
title: D3DX12ParsePipelineStream-Funktion (D3dx12.h)
description: Analysiert eine Pipelinezustandsstreambeschreibung und ruft einen benutzerdefinierten Rückruf für jede analysierte Unterobjektinstanz auf.
ms.assetid: BE4E8CC4-1E1F-4FE8-B109-05FAF93EB620
keywords:
- D3DX12ParsePipelineStream-Funktion
topic_type:
- apiref
api_name:
- D3DX12ParsePipelineStream
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbdd472d118a5ec9d49c5f105ee6b8e8ef2e3ea540f6f1954bad17273e9e030f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608560"
---
# <a name="d3dx12parsepipelinestream-function"></a>D3DX12ParsePipelineStream-Funktion

Analysiert eine Pipelinezustandsstreambeschreibung und ruft einen benutzerdefinierten Rückruf für jede analysierte Unterobjektinstanz auf.

## <a name="syntax"></a>Syntax


```C++
HRESULT inline D3DX12ParsePipelineStream(
   const D3D12_PIPELINE_STATE_STREAM_DESC &Desc,
         ID3DX12PipelineParserCallbacks   *pCallbacks
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Desc* \[ Ref\]
</dt> <dd>

Typ: **const [**D3D12 \_ PIPELINE STATE STREAM \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc)**

Die zu analysierende Beschreibung des Pipelinezustandsstreams.

</dd> <dt>

*pCallbacks* 
</dt> <dd>

Typ: **[ **ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)\***

Eine -Struktur, die die Rückrufe angibt, die für jeden Unterobjekttyp und zusätzliche Rückrufe für den Fall eines Analysefehlers aufruft werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Diese Methode gibt einen HRESULT-Erfolg zurück (**S \_ OK-** oder **E \_ INVALIDARG-Fehler,** wenn ein unbekannter Unterobjekttyp gefunden wird, wenn die Streambeschreibung leer ist, NULL ist oder doppelte Unterobjekte (einschließlich abgeleiteter Unterobjekte) enthält, oder , wenn *pCallbacks* NULL ist. In jedem Fall, in dem E \_ INVALIDARG zurückgegeben wird, wird zuerst ein entsprechender Rückruf aufgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx12.h</dt> </dl>  |
| Bibliothek<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Funktionen des Hilfsprogramms für D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





