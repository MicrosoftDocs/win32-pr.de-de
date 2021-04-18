---
title: D3DX12ParsePipelineStream-Funktion (D3dx12. h)
description: Analysiert eine Pipeline Status-Datenstrom Beschreibung und ruft für jede analysierte untergeordnete Instanz einen benutzerdefinierten Rückruf auf.
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
ms.openlocfilehash: b6778c29793f01ff7f1e5fd6424fb6795a29e64c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354986"
---
# <a name="d3dx12parsepipelinestream-function"></a>D3DX12ParsePipelineStream-Funktion

Analysiert eine Pipeline Status-Datenstrom Beschreibung und ruft für jede analysierte untergeordnete Instanz einen benutzerdefinierten Rückruf auf.

## <a name="syntax"></a>Syntax


```C++
HRESULT inline D3DX12ParsePipelineStream(
   const D3D12_PIPELINE_STATE_STREAM_DESC &Desc,
         ID3DX12PipelineParserCallbacks   *pCallbacks
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wird deaktiviert* \[ atur\]
</dt> <dd>

Typ: **Konstanten [**D3D12 \_ Pipeline \_ State \_ Stream \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc)**

Die Beschreibung des Pipeline Zustandsdaten Stroms, die analysiert werden soll.

</dd> <dt>

*pcallbacks* 
</dt> <dd>

Typ: **[ **ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)\***

Eine-Struktur, die die Rückrufe angibt, die für jeden untergeordneten Objekttyp aufgerufen werden sollen, sowie zusätzliche Rückrufe, die im Fall eines Fehler bei der Verarbeitung aufgerufen werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Diese Methode gibt einen HRESULT Success (**S \_ OK** -oder **E \_ invalidArg** -Fehler zurück, wenn ein unbekannter unter Typ gefunden wird, wenn die Datenstrom Beschreibung leer ist, NULL ist oder doppelte unter Objekte (einschließlich abgeleiteter unter Objekte) enthält, oder wenn *pcallbacks* NULL ist. In jedem Fall, dass E \_ invalidArg zurückgegeben wird, wird zuerst ein entsprechender Rückruf aufgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Bibliothek<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Funktionen des Hilfsprogramms für D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





