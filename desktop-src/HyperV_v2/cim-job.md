---
description: Ein logisches Element, das eine Arbeitseinheit darstellt, die ausgeführt werden soll, z. b. ein Skript oder ein Druckauftrag. Ein Auftrag unterscheidet sich von einem Prozess, weil ein Auftrag geplant oder in die Warteschlange eingereiht werden kann, und seine Ausführung ist nicht auf ein einzelnes System beschränkt.
ms.assetid: 35e35c3f-617b-429b-b68f-fa0c0c330e92
title: CIM_Job-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job
- CIM_Job.JobStatus
- CIM_Job.TimeSubmitted
- CIM_Job.ScheduledStartTime
- CIM_Job.StartTime
- CIM_Job.ElapsedTime
- CIM_Job.JobRunTimes
- CIM_Job.RunMonth
- CIM_Job.RunDay
- CIM_Job.RunDayOfWeek
- CIM_Job.RunStartInterval
- CIM_Job.LocalOrUtcTime
- CIM_Job.UntilTime
- CIM_Job.Notify
- CIM_Job.Owner
- CIM_Job.Priority
- CIM_Job.PercentComplete
- CIM_Job.DeleteOnCompletion
- CIM_Job.ErrorCode
- CIM_Job.ErrorDescription
- CIM_Job.RecoveryAction
- CIM_Job.OtherRecoveryAction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6b59a162d36ee677ad00c8cc574282f970bc1d80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960276"
---
# <a name="cim_job-class-hyper-v-management"></a>CIM_Job-Klasse (Hyper-V-Verwaltung)

Ein logisches Element, das eine Arbeitseinheit darstellt, die ausgeführt werden soll, z. b. ein Skript oder ein Druckauftrag. Ein Auftrag unterscheidet sich von einem Prozess, weil ein Auftrag geplant oder in die Warteschlange eingereiht werden kann, und seine Ausführung ist nicht auf ein einzelnes System beschränkt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Job : CIM_LogicalElement
{
  string   JobStatus;
  datetime TimeSubmitted;
  datetime ScheduledStartTime;
  datetime StartTime;
  datetime ElapsedTime;
  uint32   JobRunTimes = 1;
  uint8    RunMonth;
  sint8    RunDay;
  sint8    RunDayOfWeek;
  datetime RunStartInterval;
  uint16   LocalOrUtcTime;
  datetime UntilTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  uint16   PercentComplete;
  boolean  DeleteOnCompletion;
  uint16   ErrorCode;
  string   ErrorDescription;
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
};
```

## <a name="members"></a>Member

Die **CIM- \_ Auftrags** Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **CIM- \_ Auftrags** Klasse verfügt über diese Methoden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Methode</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="cim-job-killjob.md"><strong>Killjob</strong></a></td>
<td style="text-align: left;">Diese Methode ist als veraltet markiert. Verwenden Sie stattdessen die <strong>requestStateChange</strong> -Methode.<br/>
<blockquote>
[!Note]<br />
Veraltete Beschreibung: fährt einen Auftrag herunter.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ Auftrags** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Deleteoncompletion**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**True** , um den Auftrag nach dem Abschluss zu löschen. andernfalls **false**.

> [!Note]  
> Diese Eigenschaft löscht keine Aufträge, die beendet werden, bevor diese Eigenschaft auf " **true**" festgelegt ist.

 

</dd> <dt>

**Verweilzeit**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Dauer, für die der Auftrag ausgeführt wurde.

</dd> <dt>

**ErrorCode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Auftrag**".**ErrorDescription**")
</dt> </dl>

Ein Hersteller spezifischer Fehlercode, der Verarbeitungs Informationen für wiederkehrende Aufträge erfasst. Der Wert muss auf 0 (null) festgelegt werden, wenn der Auftrag ohne Fehler abgeschlossen wurde.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Auftrag**".**ErrorCode**")
</dt> </dl>

Eine frei Form Zeichenfolge, die eine Beschreibung des entsprechenden Fehlercodes in der **errorCode** -Eigenschaft enthält.

</dd> <dt>

**Jobruntimes**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, wie oft der Auftrag ausgeführt werden soll.

</dd> <dt>

**Auftragsstatus**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)".**OperationalStatus**")
</dt> </dl>

Eine frei Form Zeichenfolge, die den Status des Auftrags darstellt.

</dd> <dt>

**Localorutctime**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Uhrzeiten in den Eigenschaften **runstartinterval** und **UntilTime** Ortszeit oder UTC-Zeiten darstellen.

<dt>

<span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>

**Ortszeit** (1)


</dt> <dd></dd> <dt>

<span id="UTC_Time"></span><span id="utc_time"></span><span id="UTC_TIME"></span>

**UTC-Zeit** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Benachrichtigen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Benutzer, der benachrichtigt werden soll, wenn ein Auftrag abgeschlossen oder fehlschlägt.

</dd> <dt>

**Otherherstellyaction**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Auftrag**".**Wiederherstellbares Action**")
</dt> </dl>

Eine Zeichenfolge, die die Wiederherstellungs Aktion beschreibt, wenn die **Wiederherstellungs Action** -Eigenschaft " **other** " ("1") ist.

</dd> <dt>

**Besitzer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ owningjobelements**](cim-owningjobelement.md)")
</dt> </dl>

Der Benutzer, der den Auftrag übermittelt hat, oder der Dienst-oder Methodenname, der den Auftrag angefordert hat.

</dd> <dt>

**PercentComplete**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Prozent"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (101), **Punit** ("Prozent")
</dt> </dl>

Der Prozentsatz des Auftrags, der beendet wurde.

> [!Note]  
> Der Wert "101" ist nicht definiert und wird in der nächsten Haupt Revision der Spezifikation nicht zugelassen.

 

</dd> <dt>

**Priority**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Wichtigkeit des Auftrags. Je niedriger die Zahl, desto höher die Priorität.

</dd> <dt>

**Wiederherstellbarkeits Aktion**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Auftrag**".**Otherherstellyaction**")
</dt> </dl>

Beschreibt die Wiederherstellungs Aktion, die ausgeführt werden soll, wenn ein laufauftrag fehlschlägt.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd>

Es ist unbekannt, welche Wiederherstellungs Aktion durchführen werden soll.

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)


</dt> <dd>

Die Wiederherstellungs Aktion wird in der **otherwiederherstellungsaction** -Eigenschaft angegeben.

</dd> <dt>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Nicht fortsetzen** (2)


</dt> <dd>

Beendet die Ausführung des Auftrags und aktualisiert seinen Status entsprechend.

</dd> <dt>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Fortfahren mit dem nächsten Auftrag** (3)


</dt> <dd>

Fahren Sie mit dem nächsten Auftrag in der Warteschlange fort.

</dd> <dt>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Auftrag erneut ausführen** (4)


</dt> <dd>

Der Auftrag sollte erneut ausgeführt werden.

</dd> <dt>

<span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>

<span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>**Wiederherstellungsauftrag ausführen** (5)


</dt> <dd>

Führen Sie den mit der **wiederherstellungsjob** -Beziehung verknüpften Auftrag aus. Beachten Sie, dass sich der Wiederherstellungsauftrag bereits in der Warteschlange befinden muss, von der er ausgeführt wird.

</dd> </dl>

</dd> <dt>

**Runday**
</dt> <dd> <dl> <dt>

Datentyp: **sint8**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (-31), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (31), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Job**.**Runmonth**","**CIM- \_ Auftrag**.**Rundayof Week**","**CIM- \_ Auftrag**.**Runstartinterval**")
</dt> </dl>

Eine ganze Zahl, die in Verbindung mit der **rundayofweek** -Eigenschaft verwendet wird, um den Tag anzugeben, an dem der Auftrag verarbeitet wird. Wenn **rundayofweek** auf NULL festgelegt ist, gibt **runday** den Tag des Monats an, an dem der Auftrag verarbeitet wird. Wenn **runday** eine negative Ganzzahl ist, gibt Sie einen Tag relativ zum Ende des Monats an, oder wenn **runday** eine positive ganze Zahl ist, gibt Sie einen Tag relativ zum Anfang des Monats an.

</dd> <dt>

**Rundayof-Woche**
</dt> <dd> <dl> <dt>

Datentyp: **sint8**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Auftrag**".**Runmonth**","**CIM- \_ Auftrag**.**Runday**","**CIM- \_ Auftrag**.**Runstartinterval**")
</dt> </dl>

Eine ganze Zahl, die in Verbindung mit der **runday** -Eigenschaft verwendet wird, um den Tag anzugeben, an dem der Auftrag verarbeitet wird. Wenn **rundayofweek** auf NULL festgelegt ist, gibt **runday** den Tag des Monats an, an dem der Auftrag verarbeitet wird.

<dt>

<span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>

**-Samstag** (-7)


</dt> <dd></dd> <dt>

<span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>

**-Freitag** (-6)


</dt> <dd></dd> <dt>

<span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>

**-Donnerstag** (-5)


</dt> <dd></dd> <dt>

<span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>

**-Mittwoch** (-4)


</dt> <dd></dd> <dt>

<span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>

**-Dienstag** (-3)


</dt> <dd></dd> <dt>

<span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>

**-Montag** (-2)


</dt> <dd></dd> <dt>

<span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>

**-Sonntag** (-1)


</dt> <dd></dd> <dt>

<span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>

**Exactdayosmonth** (0)


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**Sonntag** (1)


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**Montag** (2)


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**Dienstag** (3)


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**Mittwoch** (4)


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**Donnerstag** (5)


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**Freitag** (6)


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**Samstag** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**Runmonth**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Auftrag**".**Runday**","**CIM- \_ Auftrag**.**Rundayof Week**","**CIM- \_ Auftrag**.**Runstartinterval**")
</dt> </dl>

Der Monat, an dem der Auftrag verarbeitet wird.

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

**Januar** (0)


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

**Februar** (1)


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

**März** (2)


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

**April** (3)


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

**Mai** (4)


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

**Juni** (5)


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

**Juli** (6)


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

**August** (7)


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

**September** (8)


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

**Oktober** (9)


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

**November** (10)


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

**Dezember** (11)


</dt> <dd></dd> </dl>

</dd> <dt>

**Runstartinterval**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Auftrag**".**Runmonth**","**CIM- \_ Auftrag**.**Runday**","**CIM- \_ Auftrag**.**Rundayof Week**","**CIM- \_ Auftrag**.**Runstartinterval**")
</dt> </dl>

Das Zeitintervall nach Mitternacht, zu dem der Auftrag verarbeitet wird. "00000000020000.000000:000" gibt z. b. an, dass der Auftrag unter oder nach zwei Uhr Ortszeit oder UTC-Zeit (UTC mit der **localorutctime** -Eigenschaft angegeben) ausgeführt wird.

</dd> <dt>

**Scheduledstarttime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM- \_ Auftrag**.**Runmonth**","**CIM- \_ Auftrag**.**Runday**","**CIM- \_ Auftrag**.**Rundayof Week**","**CIM- \_ Auftrag**.**Runstartinterval**")
</dt> </dl>

> [!Note]  
> Diese Eigenschaft ist veraltet. Stattdessen empfiehlt es sich, die Eigenschaften **runmonth**, **runday**, **rundayosweek** und **runstartinterval** zu verwenden.

 

Der Zeitpunkt, zu dem der Start des aktuellen Auftrags geplant ist. Diese Zeit kann durch ein Datum und eine Uhrzeit oder ein Intervall in Relation zum Zeitpunkt, zu dem die Eigenschaft angefordert wird, dargestellt werden. Ein Wert aller Nullen gibt an, dass der Auftrag bereits ausgeführt wird.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Zeitpunkt, zu dem der Auftrag gestartet wurde. Diese Zeit kann durch ein Datum und eine Uhrzeit oder durch ein Intervall dargestellt werden, das relativ zu dem Zeitpunkt ist, zu dem die Eigenschaft angefordert wird.

</dd> <dt>

**Timesub;**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Zeitpunkt, zu dem der Auftrag übermittelt wurde. Ein Wert aller Nullen gibt an, dass das übergeordnete Element kein Datum und keine Uhrzeit melden kann.

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Auftrag**".**Localorutctime**")
</dt> </dl>

Die Zeit, nach der der Auftrag ungültig wird oder angehalten werden soll. Die Zeit kann durch ein Datum und eine Uhrzeit oder durch ein Intervall in Relation zum Zeitpunkt, zu dem diese Eigenschaft angefordert wird, dargestellt werden. Ein Wert aller Neunen gibt an, dass der Auftrag unbegrenzt ausgeführt werden kann.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> </dl>

 

