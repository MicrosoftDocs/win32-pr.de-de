---
title: ID3DX12PipelineParserCallbacks RTVFormatsCb-Methode (D3DX12.h)
description: Ruft den Arrayunterobjektrückruf des Renderzielformats eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: 0D5F0BC4-D9E2-4B16-99B5-509454AF8C02
keywords:
- RTVFormatsCb-Methode
- RTVFormatsCb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, RTVFormatsCb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RTVFormatsCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d826bd2c2f3c5f1c0783a4be2cba132e4874f5a54776c227590dd87f5365d347
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045438"
---
# <a name="id3dx12pipelineparsercallbacksrtvformatscb-method"></a>ID3DX12PipelineParserCallbacks::RTVFormatsCb-Methode

Ruft den Arrayunterobjektrückruf des Renderzielformats eines Objekts auf, das diese Schnittstelle implementiert.

## <a name="syntax"></a>Syntax


```C++
void RTVFormatsCb(
  [ref] const D3D12_RT_FORMAT_ARRAY &RTVFormats
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*RTVFormats* \[ Ref\]
</dt> <dd>

Typ: **const [**D3D12 \_ RT FORMAT \_ \_ ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)**

Details des Arrayunterobjekts im Renderzielformat, das aus einem Pipelinezustandsstream analysiert wird.

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

[**D3D12 \_ RT \_ FORMAT \_ ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





