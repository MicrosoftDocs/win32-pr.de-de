---
description: Ein logisches Element, das eine auszuführende Arbeitseinheit darstellt, z. B. ein Skript oder einen Druckauftrag. Ein Auftrag ist von einem Prozess getrennt, da ein Auftrag geplant oder in die Warteschlange eingereiht werden kann und seine Ausführung nicht auf ein einzelnes System beschränkt ist.
ms.assetid: 35e35c3f-617b-429b-b68f-fa0c0c330e92
title: CIM_Job -Klasse (Hyper-V-Verwaltung)
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
ms.openlocfilehash: 8eb8f63ec9d2cdd881a2ba0946f83a40fb8be866
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474586"
---
# <a name="cim_job-class-hyper-v-management"></a>CIM_Job -Klasse (Hyper-V-Verwaltung)

Ein logisches Element, das eine auszuführende Arbeitseinheit darstellt, z. B. ein Skript oder einen Druckauftrag. Ein Auftrag ist von einem Prozess getrennt, da ein Auftrag geplant oder in die Warteschlange eingereiht werden kann und seine Ausführung nicht auf ein einzelnes System beschränkt ist.

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

Die **CIM \_ Job-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **CIM \_ Job-Klasse** verfügt über diese Methoden.




| Methode | BESCHREIBUNG | 
|--------|-------------|
| <a href="cim-job-killjob.md"><strong>KillJob</strong></a> | Diese Methode ist als veraltet markiert. Verwenden Sie stattdessen die <strong>RequestStateChange-Methode.</strong><br /><blockquote>[!Note]<br />Veraltete Beschreibung: Beendet einen Auftrag.</blockquote><br /> | 




 

### <a name="properties"></a>Eigenschaften

Die **\_ CIM-Auftragsklasse** verfügt über diese Eigenschaften.

<dl> <dt>

**DeleteOnCompletion**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**True,** um den Auftrag nach Abschluss zu löschen; andernfalls **FALSE.**

> [!Note]  
> Diese Eigenschaft löscht keine Abgeschlossenaufträge, bevor diese Eigenschaft auf **True festgelegt ist.**

 

</dd> <dt>

**ElapsedTime**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Dauer, für die der Auftrag ausgeführt wurde.

</dd> <dt>

**ErrorCode**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ CIM-Auftrag**.**ErrorDescription**")
</dt> </dl>

Ein herstellerspezifischer Fehlercode, der Verarbeitungsinformationen für wiederkehrende Aufträge erfasst. Der Wert muss auf 0 (null) festgelegt werden, wenn der Auftrag ohne Fehler abgeschlossen wurde.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ CIM-Auftrag**.**ErrorCode**")
</dt> </dl>

Eine Freiformzeichenfolge, die eine Beschreibung des entsprechenden Fehlercodes in der **ErrorCode-Eigenschaft** enthält.

</dd> <dt>

**JobRunTimes**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
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

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**")
</dt> </dl>

Eine Freiformzeichenfolge, die den Status des Auftrags darstellt.

</dd> <dt>

**LocalOrUtcTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Zeiten in den **Eigenschaften RunStartInterval** und **UntilTime** lokale Oder UTC-Zeiten darstellen.

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

Der Benutzer, der benachrichtigt werden soll, wenn ein Auftrag abgeschlossen wird oder fehlschlägt.

</dd> <dt>

**OtherRecoveryAction**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ CIM-Auftrag**.**RecoveryAction**")
</dt> </dl>

Eine Zeichenfolge, die die Wiederherstellungsaktion beschreibt, wenn die **RecoveryAction-Eigenschaft** **Other** ("1") ist.

</dd> <dt>

**Besitzer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) [**("CIM \_ OwningJobElement**](cim-owningjobelement.md).")
</dt> </dl>

Der Benutzer, der den Auftrag übermittelt hat, oder der Dienst- oder Methodenname, der den Auftrag angefordert hat.

</dd> <dt>

**PercentComplete**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Percent"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (101), **PUnit** ("percent")
</dt> </dl>

Der Prozentsatz des abgeschlossenen Auftrags.

> [!Note]  
> Der Wert "101" ist nicht definiert und ist in der nächsten hauptrevision der Spezifikation nicht zulässig.

 

</dd> <dt>

**Priority**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Wichtigkeit des Auftrags. Je niedriger die Zahl, desto höher die Priorität.

</dd> <dt>

**RecoveryAction**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ CIM-Auftrag**.**OtherRecoveryAction**")
</dt> </dl>

Beschreibt die Wiederherstellungsaktion, die ausgeführt werden soll, wenn ein Ausführungsauftrag fehlschlägt.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd>

Welche Wiederherstellungsaktion sie ergreifen soll, ist unbekannt.

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)


</dt> <dd>

Die Wiederherstellungsaktion wird in der **OtherRecoveryAction-Eigenschaft** angegeben.

</dd> <dt>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Nicht fortfahren** (2)


</dt> <dd>

Beenden Sie die Ausführung des Auftrags, und aktualisieren Sie den Status entsprechend.

</dd> <dt>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Weiter mit nächstem Auftrag** (3)


</dt> <dd>

Fahren Sie mit dem nächsten Auftrag in der Warteschlange fort.

</dd> <dt>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Auftrag erneut ausführen** (4)


</dt> <dd>

Der Auftrag sollte erneut ausgeführt werden.

</dd> <dt>

<span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>

<span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>**Ausführen des Wiederherstellungsauftrags** (5)


</dt> <dd>

Führen Sie den auftrag aus, der mithilfe der **RecoveryJob-Beziehung zugeordnet** ist. Beachten Sie, dass sich der Wiederherstellungsauftrag bereits in der Warteschlange befinden muss, aus der er ausgeführt wird.

</dd> </dl>

</dd> <dt>

**RunDay**
</dt> <dd> <dl> <dt>

Datentyp: **sint8**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (-31), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (31), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ CIM-Auftrag**.**RunMonth**", "**CIM \_ Job**.**RunDayOfWeek**", "**\_ CIM-Auftrag**.**RunStartInterval**")
</dt> </dl>

Eine ganze Zahl, die in Verbindung mit der **RunDayOfWeek-Eigenschaft verwendet** wird, um den Tag anzugeben, an dem der Auftrag verarbeitet wird. Oder wenn **RunDayOfWeek** auf 0 (null) festgelegt ist, gibt **RunDay** den Tag des Monats an, an dem der Auftrag verarbeitet wird. Wenn **RunDay** eine negative ganze Zahl ist, wird ein Tag relativ zum Monatsende angegeben, oder wenn **RunDay** eine positive ganze Zahl ist, wird ein Tag relativ zum Monatsanfang angegeben.

</dd> <dt>

**RunDayOfWeek**
</dt> <dd> <dl> <dt>

Datentyp: **sint8**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ CIM-Auftrag**.**RunMonth**", "**CIM \_ Job**.**RunDay**", "**CIM \_ Job**.**RunStartInterval**")
</dt> </dl>

Eine ganze Zahl, die in Verbindung mit der **RunDay-Eigenschaft** verwendet wird, um den Tag anzugeben, an dem der Auftrag verarbeitet wird. Oder wenn **RunDayOfWeek** auf 0 (null) festgelegt ist, gibt **RunDay** den Tag des Monats an, an dem der Auftrag verarbeitet wird.

<dt>

<span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>

**-Saturday** (-7)


</dt> <dd></dd> <dt>

<span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>

**-Friday** (-6)


</dt> <dd></dd> <dt>

<span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>

**-Thursday** (-5)


</dt> <dd></dd> <dt>

<span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>

**-Wednesday** (-4)


</dt> <dd></dd> <dt>

<span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>

**-Tuesday** (-3)


</dt> <dd></dd> <dt>

<span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>

**-Monday** (-2)


</dt> <dd></dd> <dt>

<span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>

**-Sunday** (-1)


</dt> <dd></dd> <dt>

<span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>

**ExactDayOfMonth** (0)


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

**RunMonth**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ CIM-Auftrag**.**RunDay**", "**CIM \_ Job**.**RunDayOfWeek**", "**\_ CIM-Auftrag**.**RunStartInterval**")
</dt> </dl>

Der Monat, in dem der Auftrag verarbeitet wird.

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

**RunStartInterval**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ CIM-Auftrag**.**RunMonth**", "**CIM \_ Job**.**RunDay**", "**CIM \_ Job**.**RunDayOfWeek**", "**\_ CIM-Auftrag**.**RunStartInterval**")
</dt> </dl>

Das Zeitintervall nach Mitternacht, in dem der Auftrag verarbeitet wird. "0000000000200000.000000:000" gibt beispielsweise an, dass der Auftrag am oder nach zwei Uhr Ortszeit oder UTC-Zeit ausgeführt wird (UTC wird mit der **LocalOrUtcTime-Eigenschaft** angegeben).

</dd> <dt>

**ScheduledStartTime**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**Veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**\_ CIM-Auftrag**.**RunMonth**", "**CIM \_ Job**.**RunDay**", "**CIM \_ Job**.**RunDayOfWeek**", "**\_ CIM-Auftrag**.**RunStartInterval**")
</dt> </dl>

> [!Note]  
> Diese Eigenschaft ist veraltet. Stattdessen wird empfohlen, die Eigenschaften **RunMonth,** **RunDay,** **RunDayOfWeek** und **RunStartInterval zu** verwenden.

 

Die Zeit, zu der der aktuelle Auftrag gestartet werden soll. Diese Zeit kann durch ein Datum und eine Uhrzeit oder ein Intervall relativ zur Uhrzeit dargestellt werden, zu der die Eigenschaft angefordert wird. Der Wert aller Nullen gibt an, dass der Auftrag bereits ausgeführt wird.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Uhrzeit, zu der der Auftrag gestartet wurde. Diese Uhrzeit kann durch ein Datum und eine Uhrzeit oder durch ein Intervall relativ zur Uhrzeit dargestellt werden, zu der die Eigenschaft angefordert wird.

</dd> <dt>

**TimeSubmitted**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Zeit, zu der der Auftrag übermittelt wurde. Ein Wert aller Nullen gibt an, dass das übergeordnete Element kein Datum und keine Uhrzeit melden kann.

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ CIM-Auftrag**.**LocalOrUtcTime**")
</dt> </dl>

Die Zeit, nach der der Auftrag ungültig wird oder beendet werden soll. Die Uhrzeit kann durch ein Datum und eine Uhrzeit oder durch ein Intervall relativ zur Uhrzeit dargestellt werden, zu der diese Eigenschaft angefordert wird. Der Wert "alle Neunen" gibt an, dass der Auftrag unbegrenzt ausgeführt werden kann.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> </dl>

 

