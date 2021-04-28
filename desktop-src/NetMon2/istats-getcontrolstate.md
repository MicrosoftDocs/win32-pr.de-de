---
description: 'IStats::GetControlState-Methode: Die GetControlState-Methode ruft den Zustand der Erfassung ab, der angibt, ob die Erfassung ausgeführt oder angehalten wird.'
ms.assetid: 0faf2300-d9ff-4fe0-9d50-18beafd1daea
title: IStats::GetControlState-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 25532293335756a872ef5104d5eef66027fe2ae4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098468"
---
# <a name="istatsgetcontrolstate-method"></a>IStats::GetControlState-Methode

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



| Rückgabecode                                                                                            | Beschreibung                                                                                                                       |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl>   | Das NPP ist nicht mit dem Netzwerk verbunden. Rufen Sie [IStats::Connect](istats-connect.md) auf, um die NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**NMERR \_ NOT \_ STATS \_ ONLY**</dt> </dl> | Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [IStats::Connect-Methode.](istats-connect.md)<br/>                     |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode kann jedes Mal aufgerufen werden, wenn das NPP mit dem Netzwerk verbunden ist. Sie können diese Methode verwenden, um herauszufinden, ob eine Erfassung ausgeführt wird, ob die Erfassung angehalten wurde oder ob die Erfassung beendet wurde, das NPP jedoch nicht getrennt ist.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats::Connect](istats-connect.md)
</dt> <dt>

[IStats::P ause](istats-pause.md)
</dt> <dt>

[IStatsC::Start](istats-start.md)
</dt> <dt>

[IStatsC::Stop](istats-stop.md)
</dt> </dl>

 

 




