---
description: Aktiviert ein Microsoft DirectDraw-kernelmodusobjekt nach einem Modusschalter erneut.
ms.assetid: 26451881-cebf-4db1-aeed-365f0dae6704
title: Ntgdiddreenabledirectdrawobject-Funktion (ntgdi. h)
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
ms.openlocfilehash: afd736317ecdf802cb418e81063b622db43f0651
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127284"
---
# <a name="ntgdiddreenabledirectdrawobject-function"></a>Ntgdiddreenabledirectdrawobject-Funktion

\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden. Verwenden Sie stattdessen DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]

Aktiviert ein Microsoft DirectDraw-kernelmodusobjekt nach einem Modusschalter erneut.

## <a name="syntax"></a>Syntax


```C++
BOOL APIENTRY NtGdiDdReenableDirectDrawObject(
  _In_    HANDLE hDirectDrawLocal,
  _Inout_ BOOL   *pubNewMode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdirectdrawlocal* \[ in\]
</dt> <dd>

Das DirectDraw-Objekt, das erneut aktiviert werden muss.

</dd> <dt>

*pubnewmode* \[ in, out\]
</dt> <dd>

Ein Zeiger auf einen booleschen Wert, der mit einem Wert aufgefüllt wird, der angibt, ob sich der Anzeigemodus geändert hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei erfolgreicher Ausführung (das Gerät kann erneut aktiviert werden) gibt diese Funktion " **true**" zurück. Andernfalls (z. b. wurde der Anzeigetreiber geändert), wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Nachdem das Objekt erneut aktiviert wurde, können die Funktionen für das Gerät über einen [**ntgdiddquerydirectdrawobject**](-dxgkernel-ntgdiddquerydirectdrawobject.md)-Befehl erneut abgefragt werden.

Anwendungen wird empfohlen, die DirectDraw-oder [Direct3D](../direct3d10/d3d10-graphics-reference.md) -APIs zu verwenden, die diesen Prozess unabhängig vom Betriebssystem automatisieren und abstrahieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Unterstützung der untergeordneten Grafik Ebene](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**Ddreenabledirectdrawobject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreenabledirectdrawobject)
</dt> </dl>

 

 
