---
description: Erstellen Sie ein Thread-Pump.
ms.assetid: a7a016e2-784d-4d7a-8058-88895bf3c4e2
title: D3DX10CreateThreadPump-Funktion (d3dx10. h)
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
ms.openlocfilehash: 8a27f8df1f4eaa8e7f41e863d703063308f9c595
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961723"
---
# <a name="d3dx10createthreadpump-function"></a>D3DX10CreateThreadPump-Funktion

Erstellen Sie ein Thread-Pump.

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

*ciothreads* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Anzahl der zu erstellenden e/a-Threads. Wenn 0 angegeben wird, versucht Direct3D, die optimale Anzahl von Threads basierend auf der Hardwarekonfiguration zu berechnen.

</dd> <dt>

*cprocthreads* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Anzahl der zu erstellenden Prozessthreads. Wenn 0 angegeben wird, versucht Direct3D, die optimale Anzahl von Threads basierend auf der Hardwarekonfiguration zu berechnen.

</dd> <dt>

*ppthreadpump* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\*\***

Die erstellte Thread-Pump. Siehe [**ID3DX10ThreadPump-Schnittstelle**](id3dx10threadpump.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="remarks"></a>Bemerkungen

Ein Thread Pump ist ein sehr Ressourcen intensives Objekt. Pro Anwendung sollte nur ein Thread Pump erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Funktionen](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
