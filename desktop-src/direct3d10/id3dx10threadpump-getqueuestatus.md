---
description: Abrufen der Anzahl von Elementen in jeder der drei Warteschlangen innerhalb der Threadpumpe.
ms.assetid: b5b829a5-5ef7-4ef5-afb4-efe1bb22ae70
title: ID3DX10ThreadPump::GetQueueStatus-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.GetQueueStatus
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9cab3211765f12812e08845165c41868049020573a3cbfb706fad01821a2c3bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118100202"
---
# <a name="id3dx10threadpumpgetqueuestatus-method"></a>ID3DX10ThreadPump::GetQueueStatus-Methode

Abrufen der Anzahl von Elementen in jeder der drei Warteschlangen innerhalb der Threadpumpe.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetQueueStatus(
  [in] UINT *pIoQueue,
  [in] UINT *pProcessQueue,
  [in] UINT *pDeviceQueue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pIoQueue* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Anzahl der Elemente in der E/A-Warteschlange.

</dd> <dt>

*pProcessQueue* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Anzahl der Elemente in der Prozesswarteschlange.

</dd> <dt>

*pDeviceQueue* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Anzahl der Elemente in der Gerätewarteschlange.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 10-Rückgabecodes aufgeführten](d3d10-graphics-reference-returnvalues.md)Werte.

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

 

 
