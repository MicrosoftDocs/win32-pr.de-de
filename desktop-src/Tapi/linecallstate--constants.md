---
description: Die linecallstate \_ -bitflagkonstanten beschreiben die aufrufzustände, in denen ein-Befehl erfolgen kann.
ms.assetid: 18d881ee-cf98-4dec-a561-333c2518935d
title: LINECALLSTATE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d50301dfeca49513a919fba90cc960c7ccb572d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373798"
---
# <a name="linecallstate_-constants"></a>Linecallstate- \_ Konstanten

Die **linecallstate \_** -bitflagkonstanten beschreiben die aufrufzustände, in denen ein-Befehl erfolgen kann.

<dl> <dt>

<span id="LINECALLSTATE_ACCEPTED"></span><span id="linecallstate_accepted"></span>**linecallstate \_ akzeptiert**
</dt> <dd> <dl> <dt>



Der-Rückruf befand sich im Angebots Zustand und wurde akzeptiert. Dies weist auf andere (Überwachungs-) Anwendungen hin, die von der aktuellen Besitzer Anwendung für die Beantwortung des Aufrufes verantwortlich sind. In ISDN wird der Status "akzeptiert" eingegeben, wenn die aufgerufenen Parteien eine Nachricht an den Switch senden, um anzugeben, dass Sie den Aufruf der aufgerufenen Person bereitstellen soll. Dies hat den Nebeneffekt, dass die Benutzer an beiden Enden des Aufrufens (Klingeln) angezeigt werden. Ein eingehender-Rückruf kann immer sofort beantwortet werden, ohne dass er zuerst separat akzeptiert wird.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span>**linecallstate \_ ausgelastet**
</dt> <dd> <dl> <dt>



Der-Befehl empfängt einen ausgelasteten Ton. Ein ausgelasteter Ton gibt an, dass der-Befehl nicht abgeschlossen werden kann, entweder eine Leitung (trunk) oder die Station der Remote Partei wird verwendet. Weitere Informationen finden Sie unter [**linebusymode- \_ Konstanten**](linebusymode--constants.md).


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_CONFERENCED"></span><span id="linecallstate_conferenced"></span>**linecallstate-über \_ Tragung**
</dt> <dd> <dl> <dt>



Der-Rückruf ist ein Member eines Konferenz Aufrufes und befindet sich logisch im verbundenen Zustand.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span>**linecallstate \_ verbunden**
</dt> <dd> <dl> <dt>



Der-Rückruf wurde erstellt, und die Verbindung wird hergestellt. Informationen können über den Aufruf zwischen der Ursprungsadresse und der Zieladresse übertragen werden.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_DIALING"></span><span id="linecallstate_dialing"></span>**linecallstate- \_ Wähl**
</dt> <dd> <dl> <dt>



Der Absender ist für den-Befehl wählbare Ziffern. Die einwählbare Ziffern werden vom-Schalter gesammelt. Beachten Sie, dass weder [**linegeneratedigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) noch [**TSPI \_ linegeneratedigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits) die Linie in den Einwähl Status setzen.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span>**linecallstate \_ Dialtone**
</dt> <dd> <dl> <dt>



Der-Befehl empfängt einen Wählton vom Switch, was bedeutet, dass der Switch bereit ist, eine einwählbare Zahl zu erhalten. Weitere Informationen finden Sie unter [**linedialtonemode- \_ Konstanten**](linedialtonemode--constants.md) für Bezeichner von speziellen Wähltönen, wie z. b. einen ruckeln-Ton der normalen Sprachnachrichten.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span>**linecallstate \_ getrennt**
</dt> <dd> <dl> <dt>



Der Remote Beteiligte hat die Verbindung mit dem-Befehl getrennt.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_IDLE"></span><span id="linecallstate_idle"></span>**linecallstate im \_ Leerlauf**
</dt> <dd> <dl> <dt>



Der-Befehl ist vorhanden, aber es wurde keine Verbindung hergestellt. Im-Befehl ist keine Aktivität vorhanden, was bedeutet, dass zurzeit kein-Rückruf aktiv ist. Ein-Rückruf kann nie aus dem Leerlaufzustand übergehen.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span>**linecallstate- \_ Angebot**
</dt> <dd> <dl> <dt>



Der-Befehl wird der Station angeboten und signalisiert den Eingang eines neuen Aufrufes. Der Angebots Status ist nicht identisch mit der Ursache für das Klingeln eines Telefons oder Computers. In einigen Umgebungen wird der Benutzer aufgrund eines Aufrufes Ansichts Zustands nicht so lange Klingeln, bis der Schalter die Zeile an den Ring anweist. Ein Beispiel für die Verwendung ist, wenn ein eingehender-Befehl in mehreren Stations Sätzen, aber nur in den primären Adress Ringen angezeigt wird. Die Anweisung zum Klingeln wirkt sich nicht auf Aufrufe aus.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_ONHOLD"></span><span id="linecallstate_onhold"></span>**linecallstate \_ OnHold**
</dt> <dd> <dl> <dt>



Der-Befehl wird vom-Schalter angehalten. Dadurch wird die physische Zeile freigegeben, wodurch ein weiterer aufrufsbefehl verwendet werden kann.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_ONHOLDPENDCONF"></span><span id="linecallstate_onholdpendconf"></span>**linecallstate \_ onholdpdconf**
</dt> <dd> <dl> <dt>



Der-Befehl wird zurzeit angehalten, während er einer Konferenz hinzugefügt wird.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_ONHOLDPENDTRANSFER"></span><span id="linecallstate_onholdpendtransfer"></span>**linecallstate \_ onholdpdtransfer**
</dt> <dd> <dl> <dt>



Der-Aufrufer wartet aktuell auf die Übertragung an eine andere Zahl.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_PROCEEDING"></span><span id="linecallstate_proceeding"></span>**linecallstate wird \_ fortgesetzt**
</dt> <dd> <dl> <dt>



Die Wahl ist abgeschlossen, und der Anruf wird durch den Switch oder das Telefon Netzwerk fortgesetzt. Dies tritt auf, nachdem die Unterscheidung vollständig ist und bevor der Anruf die gewählte Partei erreicht, wie von "Ringback", "ausgelastet" oder "Antwort" angegeben.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_RINGBACK"></span><span id="linecallstate_ringback"></span>**linecallstate- \_ Ringback**
</dt> <dd> <dl> <dt>



Die aufzurufende Station ist erreicht, und der Schalter des Ziels erzeugt einen Klingel Ton an den Absender zurück. Ein *Rollback* bedeutet, dass die Zieladresse mit dem-Befehl benachrichtigt wird.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span>**linecallstate \_ specialinfo**
</dt> <dd> <dl> <dt>



Der-Befehl empfängt ein spezielles Informations Signal, das einer Vorabversion vorangestellt ist, die angibt, warum ein-Vorgang nicht abgeschlossen werden kann. Siehe [**linespecialinfo- \_ Konstanten**](linespecialinfo--constants.md).


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_UNKNOWN"></span><span id="linecallstate_unknown"></span>**linecallstate \_ unbekannt**
</dt> <dd> <dl> <dt>



Der-Befehl ist vorhanden, aber sein Status ist zurzeit unbekannt. Dies kann das Ergebnis einer schlechten Rückruf Status Erkennung durch den Dienstanbieter sein. Eine Aufruf Zustands Meldung, bei der der Aufruf Status auf Unknown festgelegt ist, kann auch generiert werden, um die TAPI-dll über einen neuen Aufruf zu informieren, wenn der tatsächliche Aufruf Zustand des Aufrufes nicht genau bekannt ist.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die höherwertigen 8 Bits können einen gerätespezifischen unter Zustand eines beliebigen vordefinierten Zustands definieren, vorausgesetzt, dass eine der oben definierten linecallstate \_ Bits ebenfalls festgelegt ist. Die 24 Bits mit niedriger Ordnung sind für vordefinierte Zustände reserviert.

Die **linecallstate- \_ Konstanten** werden als Parameter von der [**Zeile \_ CallState**](line-callstate.md) -Nachricht verwendet, die an die Anwendung gesendet wird. Die Nachricht enthält den neuen Aufrufstatus, in den der-Befehl umgestellt hat. Diese Konstanten werden auch als Member in der [**linecallstatus**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) -Struktur verwendet, die von der [**linegetcallstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) -Funktion zurückgegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_liniencallstate**](line-callstate.md)
</dt> <dt>

[**Linecallstatus**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[**linegeneratedigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)
</dt> <dt>

[**linegetcallstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)
</dt> </dl>

 

