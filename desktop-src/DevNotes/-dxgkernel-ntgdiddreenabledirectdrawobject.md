---
description: Aktiviert ein Microsoft DirectDraw-Geräteobjekt im Kernelmodus nach einem Moduswechsel erneut.
ms.assetid: 26451881-cebf-4db1-aeed-365f0dae6704
title: NtGdiDdReenableDirectDrawObject-Funktion (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdReenableDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 808e2e74492b9a3e828e09389e04f0e1e4b09fef9a63fdd7a22d81521b3df30d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045570"
---
# <a name="ntgdiddreenabledirectdrawobject-function"></a>NtGdiDdReenableDirectDrawObject-Funktion

\[Diese Funktion kann bei jeder Betriebssystemrevision geändert werden. Verwenden Sie stattdessen DirectDraw und Microsoft Direct3DAPIs. Diese APIs isolieren Anwendungen vor solchen Betriebssystemänderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeigetreibern.\]

Aktiviert ein Microsoft DirectDraw-Geräteobjekt im Kernelmodus nach einem Moduswechsel erneut.

## <a name="syntax"></a>Syntax


```C++
BOOL APIENTRY NtGdiDdReenableDirectDrawObject(
  _In_    HANDLE hDirectDrawLocal,
  _Inout_ BOOL   *pubNewMode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDirectDrawLocal* \[ In\]
</dt> <dd>

DirectDraw-Objekt, das erneut aktiviert werden muss.

</dd> <dt>

*pubNewMode* \[ in, out\]
</dt> <dd>

Zeiger auf eine BOOL, die mit einem Wert gefüllt wird, der darstellt, ob sich der Anzeigemodus geändert hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Fehler erfolgreich ist (das Gerät kann erneut aktiviert werden), gibt diese Funktion **TRUE zurück.** Andernfalls (z. B. wurde der Anzeigetreiber geändert), wird **FALSE zurückgegeben.**

## <a name="remarks"></a>Hinweise

Nachdem das Objekt erneut aktiviert wurde, können die Funktionen für das Gerät über einen Aufruf von [**NtGdiDdQueryDirectDrawObject erneut abgefragt werden.**](-dxgkernel-ntgdiddquerydirectdrawobject.md)

Anwendungen wird empfohlen, die DirectDraw- oder [Direct3D-APIs](../direct3d10/d3d10-graphics-reference.md) der Version 8 zu verwenden, die diesen Prozess unabhängig vom Betriebssystem automatisieren und abstrahieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Clientunterstützung auf niedriger Grafikebene](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**DdReenableDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreenabledirectdrawobject)
</dt> </dl>

 

 
