---
title: ID3DX12PipelineParserCallbacks InputLayoutCb-Methode (D3DX12.h)
description: Ruft den Eingabelayout-Unterobjektrückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: A21AB7A1-6E51-42CB-BA98-C0BD08D43009
keywords:
- InputLayoutCb-Methode
- InputLayoutCb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, InputLayoutCb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.InputLayoutCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0f7012686c85b38e94f8f3d2400cf406d614fc83ff0ba25e746ac0433b2e167
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528772"
---
# <a name="id3dx12pipelineparsercallbacksinputlayoutcb-method"></a>ID3DX12PipelineParserCallbacks::InputLayoutCb-Methode

Ruft den Eingabelayout-Unterobjektrückruf eines Objekts auf, das diese Schnittstelle implementiert.

## <a name="syntax"></a>Syntax


```C++
void InputLayoutCb(
  [ref] const D3D12_INPUT_LAYOUT_DESC &InputLayout
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*InputLayout* \[ Ref\]
</dt> <dd>

Typ: **const [**D3D12 \_ INPUT LAYOUT \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)**

Details des Eingabelayout-Unterobjekts, das aus einem Pipelinezustandsdatenstrom analysiert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt nichts zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX12.h</dt> </dl>  |
| Bibliothek<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Hilfsschnittstellen für Direct3D 12](helper-interfaces-for-d3d12.md)
</dt> <dt>

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[**\_D3D12-EINGABELAYOUT-DESC \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)
</dt> </dl>

 

 





