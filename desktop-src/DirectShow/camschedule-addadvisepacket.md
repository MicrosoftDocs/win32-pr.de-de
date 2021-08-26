---
description: Die AddAdvisePacket-Methode fügt der Liste der ausstehenden Anforderungen eine Empfehlungsanforderung hinzu.
ms.assetid: 138d8404-7d28-47cc-91b4-4733a113ac7a
title: CABSchedule.AddAdvisePacket-Methode (Dsschedule.h)
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
ms.openlocfilehash: 9a7509e4696214279e99ff15f21f2634dce7921796ae2ca112ae563ab170a2d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084530"
---
# <a name="camscheduleaddadvisepacket-method"></a>CABSchedule.AddAdvisePacket-Methode

Die `AddAdvisePacket` -Methode fügt der Liste der ausstehenden Anforderungen eine Empfehlungsanforderung hinzu.

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

*time1* \[ Ref\]
</dt> <dd>

Angeforderte Zeit für die Empfehlung.

</dd> <dt>

*time2* \[ Ref\]
</dt> <dd>

Bei regelmäßigen Beratungsanforderungen die Zeit zwischen Benachrichtigungen. Dieser Parameter wird ignoriert, wenn *bPeriodic* **false** ist.

</dd> <dt>

*hNotify* 
</dt> <dd>

Handle für ein Semaphor, wenn *bPeriodic* **TRUE** ist, oder Handle für ein Ereignis, wenn *bPeriodic* **FALSE** ist.

</dd> <dt>

*bPeriodic* 
</dt> <dd>

Boolescher Wert, der angibt, ob eine regelmäßige Benachrichtigung oder eine einmalige Benachrichtigung hinzugefügt werden soll. True gibt an, dass die Benachrichtigung periodisch erfolgt. Der *parameter time2* gibt die Zeit zwischen Benachrichtigungen an. False gibt an, dass die Benachrichtigung nur einmal erfolgt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Bezeichner für die Empfehlungsanforderung (das "Cookie") zurück. Wenn die Methode fehlschlägt, ist der Rückgabewert 0 (null).

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dsschedule.h (include Streams.h)</dt> </dl>                                                                                |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WEBCAMSchedule-Klasse**](camschedule.md)
</dt> </dl>

 

 




