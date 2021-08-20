---
description: Fügen Sie der Threadpump ein Arbeitselement hinzu.
ms.assetid: f07789dc-a3d5-4bad-9768-527e701271b8
title: ID3DX10ThreadPump::AddWorkItem-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.AddWorkItem
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 43602019018a9751453eb93f4ffb9b1c29eada6caf120a6721522982c3355dfc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609320"
---
# <a name="id3dx10threadpumpaddworkitem-method"></a>ID3DX10ThreadPump::AddWorkItem-Methode

Fügen Sie der Threadpump ein Arbeitselement hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddWorkItem(
  [in]  ID3DX10DataLoader    *pDataLoader,
  [in]  ID3DX10DataProcessor *pDataProcessor,
  [in]  HRESULT              *pHResult,
  [out] void                 **ppDeviceObject
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDataLoader* \[ In\]
</dt> <dd>

Typ: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\***

Das Lader, das vom Threadpump verwendet wird, wenn für ein Arbeitselement Daten geladen werden müssen.

</dd> <dt>

*pDataProcessor* \[ In\]
</dt> <dd>

Typ: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\***

Der Prozessor, den die Threadpump verwendet, wenn für ein Arbeitselement Daten verarbeitet werden müssen.

</dd> <dt>

*pHResult* \[ In\]
</dt> <dd>

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Ein Zeiger auf den Rückgabewert. Kann NULL **sein.**

</dd> <dt>

*ppDeviceObject* \[ out\]
</dt> <dd>

Typ: **\* \* void**

Das Gerät, das das -Objekt verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Unter [Direct3D 10-Rückgabecodes aufgeführten Werte.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10ThreadPump](id3dx10threadpump.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




