---
description: Erstellen Sie eine Threadpumpe.
ms.assetid: a7a016e2-784d-4d7a-8058-88895bf3c4e2
title: D3DX10CreateThreadPump-Funktion (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateThreadPump
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 99b5766625f2a269d1fb36e9e808c206d0e3040419f505622ccfe1e27ca4bcdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118541058"
---
# <a name="d3dx10createthreadpump-function"></a>D3DX10CreateThreadPump-Funktion

Erstellen Sie eine Threadpumpe.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10CreateThreadPump(
  _In_  UINT              cIoThreads,
  _In_  UINT              cProcThreads,
  _Out_ ID3DX10ThreadPump **ppThreadPump
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cIoThreads* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Anzahl der zu erstellenden E/A-Threads. Wenn 0 angegeben ist, versucht Direct3D, die optimale Anzahl von Threads basierend auf der Hardwarekonfiguration zu berechnen.

</dd> <dt>

*cProcThreads* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Anzahl der zu erstellenden Prozessthreads. Wenn 0 angegeben ist, versucht Direct3D, die optimale Anzahl von Threads basierend auf der Hardwarekonfiguration zu berechnen.

</dd> <dt>

*ppThreadPump* \[ out\]
</dt> <dd>

Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\*\***

Die erstellte Threadpumpe. Siehe [**ID3DX10ThreadPump-Schnittstelle.**](id3dx10threadpump.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 10-Rückgabecodes aufgeführten](d3d10-graphics-reference-returnvalues.md)Werte.

## <a name="remarks"></a>Hinweise

Eine Threadpumpe ist ein sehr ressourcenintensives Objekt. Pro Anwendung sollte nur eine Threadpumpe erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Universell Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
