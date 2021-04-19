---
title: ID3DX12PipelineParserCallbacks errorunknownsubobject-Methode (D3DX12. h)
description: Ruft den unbekannten untergeordneten Fehler Rückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: 612D7C44-4DC5-4DEA-B369-09C27123D45E
keywords:
- Errorunknownsubobject-Methode
- Errorunknownsubobject-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks Interface, errorunknownsubobject-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorUnknownSubobject
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e294e3face085c5298f3cc624d7c0ef70dcf865
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355213"
---
# <a name="id3dx12pipelineparsercallbackserrorunknownsubobject-method"></a>ID3DX12PipelineParserCallbacks:: errorunknownsubobject-Methode

Ruft den unbekannten untergeordneten Fehler Rückruf eines Objekts auf, das diese Schnittstelle implementiert.

## <a name="syntax"></a>Syntax


```C++
void ErrorUnknownSubobject(
   
        UINT
           UnknownTypeValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Unknowntypevalue* 
</dt> <dd>

Typ: **uint**

Der unbekannte untergeordnete Typ des versuchten untergeordneten Objekts.

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

 

 





