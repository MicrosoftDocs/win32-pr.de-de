---
description: Die addadvisepacket-Methode fügt der Liste der ausstehenden Anforderungen eine Benachrichtigungs Anforderung hinzu.
ms.assetid: 138d8404-7d28-47cc-91b4-4733a113ac7a
title: Camschedule. addadvisepacket-Methode (dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.AddAdvisePacket
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dd9586b09586c12f1a30f45b512336831372295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368602"
---
# <a name="camscheduleaddadvisepacket-method"></a>Camschedule. addadvisepacket-Methode

Die- `AddAdvisePacket` Methode fügt der Liste der ausstehenden Anforderungen eine anforderungsanforderung hinzu.

## <a name="syntax"></a>Syntax


```C++
DWORD_PTR AddAdvisePacket(
  [ref] const REFERENCE_TIME &time1,
  [ref] const REFERENCE_TIME &time2,
              HANDLE         hNotify,
              BOOL           bPeriodic
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*zeitpunkt1 zeitlich* \[ atur\]
</dt> <dd>

Angeforderte Zeit für die Empfehlung.

</dd> <dt>

*zeitpunkt2?* \[ atur\]
</dt> <dd>

Für regelmäßige Anforderungs Anforderungen die Zeit zwischen Benachrichtigungen. Dieser Parameter wird ignoriert, wenn *bperiodisch* den Wert **false** hat.

</dd> <dt>

*hnotify* 
</dt> <dd>

Handle für eine Semaphor, wenn *bperiodisch* **true** ist, oder Handle für ein Ereignis, wenn *bperiodisch* den Wert **false** hat.

</dd> <dt>

*bperiodisch* 
</dt> <dd>

Boolescher Wert, der angibt, ob eine regelmäßige Benachrichtigung oder eine One-Shot-Benachrichtigung hinzugefügt werden soll. **True** gibt an, dass die Benachrichtigung regelmäßig erfolgt. der *zeitpunkt2?* -Parameter gibt die Zeit zwischen Benachrichtigungen an. Der Wert **false** gibt an, dass die Benachrichtigung nur einmal auftritt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Bezeichner für die Benachrichtigungs Anforderung zurück (das "Cookie"). Wenn die Methode fehlschlägt, ist der Rückgabewert 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dsschedule. h (Include Streams. h)</dt> </dl>                                                                                |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Camschedule-Klasse**](camschedule.md)
</dt> </dl>

 

 




