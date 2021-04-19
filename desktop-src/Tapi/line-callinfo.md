---
description: Die TAPI-zeilige \_ CallInfo-Meldung wird gesendet, wenn sich die Aufruf Informationen über den angegebenen Aufruf geändert haben. Die Anwendung kann linegetcallinfo aufrufen, um die aktuellen Aufruf Informationen zu bestimmen.
ms.assetid: eb882409-6842-434e-9f93-61cf0c11d1d0
title: LINE_CALLINFO Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6005ab5383816ead440f5a1a7d580bfaccb5c1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356482"
---
# <a name="line_callinfo-message"></a>Zeile \_ CallInfo-Meldung

Die TAPI- **zeilige \_ CallInfo** -Meldung wird gesendet, wenn sich die Aufruf Informationen über den angegebenen Aufruf geändert haben. Die Anwendung kann [**linegetcallinfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) aufrufen, um die aktuellen Aufruf Informationen zu bestimmen.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdevice* 
</dt> <dd>

Ein Handle für den-Befehl.

</dd> <dt>

*dwcallbackinstance* 
</dt> <dd>

Die beim Öffnen der Zeile des Aufrufs angegebene Rückruf Instanz.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Das aufrufinformationselement, das geändert wurde. Kann eine oder mehrere der [**linecallinfostate- \_ Konstanten**](linecallinfostate--constants.md)sein.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

An Anwendungen, die bereits über ein Handle für den Aufruf verfügen, wird eine **Zeile " \_ CallInfo** " mit dem Hinweis " *nuwnersincr*", " *numuwnersdecr*" und/oder " *nummonitorschge* " gesendet. Dies kann das Ergebnis einer anderen Anwendung sein, die den Besitz ändert oder eine Überwachung für einen Aufruf mit [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen), [**lineclose**](/windows/desktop/api/Tapi/nf-tapi-lineclose), [**LineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown), [**linesetcallprivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege), [**linegetnewcalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)und [**linegetconfig frelatedcalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)durchführt.

Diese **Zeilen- \_ CallInfo** -Meldungen werden nicht gesendet, wenn eine Benachrichtigung über einen neuen Aufruf in [**einer \_ zeilencallstate**](line-callstate.md) -Nachricht bereitgestellt wird, da die Aufruf Informationen bereits die richtige Anzahl von Besitzern und Monitoren zum Zeitpunkt der Übermittlung der Zeilen Aufruf \_ Zustands Meldungen widerspiegeln. **Zeile \_ CallInfo** -Meldungen werden auch dann unterdrückt, wenn TAPI von TAPI zum Überwachen des nicht unbekannten Mechanismus linecallstate angeboten wird \_ .

> [!Note]  
> Die Anwendung, die eine Änderung in der Anzahl von Besitzern oder Monitoren bewirkt (z. b. durch Aufrufen von [**linedezugecall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) oder [**linesetcallprivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)), empfängt nicht selbst eine Meldung, die angibt, dass die Änderung abgeschlossen wurde.

 

Für einen Aufruf werden keine **Zeilen- \_ CallInfo** -Meldungen gesendet, nachdem der Aufruf in den *Leerlauf* Zustand wechselt. Insbesondere werden Änderungen an der Anzahl von Besitzern und Monitoren nicht gemeldet, wenn Anwendungen ihre Handles für den Leerlauf aufzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**lineclose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[**linedezugewiesene eCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall)
</dt> <dt>

[**linegetcallinfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[**lineget-frelatedcalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)
</dt> <dt>

[**linegetnewcalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)
</dt> <dt>

[**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**linesetcallprivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)
</dt> <dt>

[**LineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> </dl>

 

 




