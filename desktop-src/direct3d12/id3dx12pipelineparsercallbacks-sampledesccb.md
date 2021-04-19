---
title: ID3DX12PipelineParserCallbacks sampledesccb-Methode (D3DX12. h)
description: Ruft den Beispiel Beschreibungs-Rückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: 32F112D3-97B1-45C2-8744-9F27DC95C249
keywords:
- Sampledesccb-Methode
- Sampledesccb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, sampledesccb-Methode
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
ms.openlocfilehash: 0644837720dd8c81dc1c7577a1d6506ebdf61c24
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361181"
---
# <a name="id3dx12pipelineparsercallbackssampledesccb-method"></a>ID3DX12PipelineParserCallbacks:: sampledesccb-Methode

Ruft den Beispiel Beschreibungs-Rückruf eines Objekts auf, das diese Schnittstelle implementiert.

## <a name="syntax"></a>Syntax


```C++
void SampleDescCb(
  [ref] const DXGI_SAMPLE_DESC &SampleDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Sampledäsc* \[ atur\]
</dt> <dd>

Type: Konstante **[**DXGI \_ Sample \_ DESC**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)**

Details der Beispiel Beschreibung, die aus einem Pipeline Status-Stream analysiert wurde.

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

[**DXGI-Beispiel (Debug) \_ \_**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)
</dt> </dl>

 

