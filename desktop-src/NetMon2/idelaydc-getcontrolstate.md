---
description: 'IDelaydC::GetControlState-Methode: Die GetControlState-Methode ruft den Zustand der Erfassung ab, der angibt, ob die Erfassung ausgeführt oder angehalten wird.'
ms.assetid: 21b7faaa-591f-4e15-b4e9-453ea690ab4a
title: IDelaydC::GetControlState-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 825112ec9a33ef176d5a69765837214249e33102
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110768"
---
# <a name="idelaydcgetcontrolstate-method"></a>IDelaydC::GetControlState-Methode

Die **GetControlState-Methode** ruft den Zustand der [*Erfassung*](c.md)ab, der angibt, ob die Erfassung ausgeführt oder angehalten wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IsRunnning* \[ out\]
</dt> <dd>

Indikator, dass die aktuelle Erfassung ausgeführt wird, einschließlich, wenn die Erfassung angehalten wird.

</dd> <dt>

*IsPaused* \[ out\]
</dt> <dd>

Indikator, dass die aktuelle Erfassung angehalten wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                          | Beschreibung                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl> | Das NPP ist nicht mit dem Netzwerk verbunden. Rufen Sie [IDelaydC::Connect](idelaydc-connect.md) auf, um die NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**NMERR \_ NICHT \_ VERZÖGERT**</dt> </dl>   | Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [IDelaydC::Connect-Methode.](idelaydc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode kann jedes Mal aufgerufen werden, wenn das NPP mit dem Netzwerk verbunden ist, indem die [IDelaydC-Schnittstelle](idelaydc.md) verwendet wird. Sie können diese Methode verwenden, um herauszufinden, ob eine Erfassung ausgeführt wird, ob die Erfassung angehalten wurde oder ob die Erfassung beendet wurde, das NPP jedoch nicht getrennt ist.

Die Methoden zum Starten, Anhalten und Beenden der Erfassung sind unten in der Liste Siehe auch aufgeführt.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC::Connect](idelaydc-connect.md)
</dt> <dt>

[IDelaydC::P ause](idelaydc-pause.md)
</dt> <dt>

[IDelaydC::Start](idelaydc-start.md)
</dt> <dt>

[IDelaydC::Stop](idelaydc-stop.md)
</dt> </dl>

 

 




