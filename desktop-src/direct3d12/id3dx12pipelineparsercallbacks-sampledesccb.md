---
title: ID3DX12PipelineParserCallbacks SampleDescCb-Methode (D3DX12.h)
description: Ruft den Rückruf eines Beispielbeschreibungsunterobjekts eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: 32F112D3-97B1-45C2-8744-9F27DC95C249
keywords:
- SampleDescCb-Methode
- SampleDescCb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, SampleDescCb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.SampleDescCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ba360b8f6af83f0d5bd626793dedba4f830d94cd49dc984da807588ea186c33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124028"
---
# <a name="id3dx12pipelineparsercallbackssampledesccb-method"></a>ID3DX12PipelineParserCallbacks::SampleDescCb-Methode

Ruft den Rückruf eines Beispielbeschreibungsunterobjekts eines Objekts auf, das diese Schnittstelle implementiert.

## <a name="syntax"></a>Syntax


```C++
void SampleDescCb(
  [ref] const DXGI_SAMPLE_DESC &SampleDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SampleDesc* \[ Ref\]
</dt> <dd>

Typ: **const [**DXGI SAMPLE \_ \_ DESC**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)**

Details des Beispielbeschreibungsunterobjekts, das aus einem Pipelinezustandsstream analysiert wurde.

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

[**DXGI \_ SAMPLE \_ DESC**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)
</dt> </dl>

 

