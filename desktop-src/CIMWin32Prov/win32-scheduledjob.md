---
description: Stellt einen Auftrag dar, der mit dem AT-Befehl erstellt wurde.
ms.assetid: 2fa69e3f-9a6c-4aa9-8a6c-ea28eb4342ca
ms.tgt_platform: multiple
title: Win32_ScheduledJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob
- Win32_ScheduledJob.Caption
- Win32_ScheduledJob.Description
- Win32_ScheduledJob.InstallDate
- Win32_ScheduledJob.Name
- Win32_ScheduledJob.Status
- Win32_ScheduledJob.ElapsedTime
- Win32_ScheduledJob.Notify
- Win32_ScheduledJob.Owner
- Win32_ScheduledJob.Priority
- Win32_ScheduledJob.TimeSubmitted
- Win32_ScheduledJob.UntilTime
- Win32_ScheduledJob.Command
- Win32_ScheduledJob.DaysOfMonth
- Win32_ScheduledJob.DaysOfWeek
- Win32_ScheduledJob.InteractWithDesktop
- Win32_ScheduledJob.JobId
- Win32_ScheduledJob.JobStatus
- Win32_ScheduledJob.RunRepeatedly
- Win32_ScheduledJob.StartTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50162221e7ca18e07e3599deca2dba67b18ba708
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041361"
---
# <a name="win32_scheduledjob-class"></a>Win32 \_ ScheduledJob-Klasse

Die **Win32 \_ ScheduledJob**- [WMI-Klasse](../wmisdk/retrieving-a-class.md)   stellt einen Auftrag dar, der mit dem **at** -Befehl erstellt wurde.

> [!Note]  
> Die **Win32 \_ ScheduledJob** -Klasse stellt keinen Auftrag dar, der mit dem Assistenten für geplante Aufgaben in der Systemsteuerung erstellt wurde. Sie können eine von WMI erstellte Aufgabe nicht in der Benutzeroberfläche für geplante Aufgaben ändern. Weitere Informationen finden Sie im Abschnitt "Hinweise".

 

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4E0-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("Delete"), AMENDMENT]
class Win32_ScheduledJob : CIM_Job
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime ElapsedTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  datetime TimeSubmitted;
  datetime UntilTime;
  string   Command;
  uint32   DaysOfMonth;
  uint32   DaysOfWeek;
  boolean  InteractWithDesktop;
  uint32   JobId;
  string   JobStatus;
  boolean  RunRepeatedly;
  datetime StartTime;
};
```

## <a name="members"></a>Member

Die **Win32 \_ ScheduledJob** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ ScheduledJob** -Klasse verfügt über diese Methoden.



| Methode                                                      | BESCHREIBUNG                                                                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**Stelle**](create-method-in-class-win32-scheduledjob.md) | Klassenmethode, die einen Auftrag an das Betriebssystem übermittelt, um die Ausführung zu einem bestimmten Zeitpunkt (Datum und Uhrzeit) auszuführen.<br/> |
| [**Lösch**](delete-method-in-class-win32-scheduledjob.md) | Klassenmethode, die einen geplanten Auftrag löscht.<br/>                                                                 |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ ScheduledJob** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Eine kurze Textbeschreibung des-Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Befehl**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**at \_ Info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **Command**")
</dt> </dl>

Der Name des Befehls, des Batch Programms oder der Binärdatei (und Befehlszeilenargumente), den der Zeit Plan Dienst zum Aufrufen des Auftrags verwendet.

Beispiel **: "Debug** - **/q/f**"

</dd> <dt>

**DaysOfMonth**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**at \_**](/windows/win32/api/lmat/ns-lmat-at_info) \| **infodaymonth**")
</dt> </dl>

Tage des Monats, an denen die Ausführung des Auftrags geplant ist. Wenn ein Auftrag für die Ausführung an mehreren Tagen des Monats geplant ist, können diese Werte in einem logischen OR-Vorgang verknüpft werden. Wenn ein Auftrag beispielsweise am 1. und 16. eines jeden Monats ausgeführt werden soll, ist der Wert der **daysOfMonth** -Eigenschaft 1 oder 32768.

<dt>

<span id="1"></span>

<span id="1"></span>**1** (1)


</dt> <dd>

1.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2** (2)


</dt> <dd>

2.

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3** (4)


</dt> <dd>

dritte

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4** (8)


</dt> <dd>

4.

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5** (16)


</dt> <dd>

5.

</dd> <dt>

<span id="6"></span>

<span id="6"></span>**6** (32)


</dt> <dd>

6.

</dd> <dt>

<span id="7"></span>

<span id="7"></span>**7** (64)


</dt> <dd>

7.

</dd> <dt>

<span id="8"></span>

<span id="8"></span>**8** (128)


</dt> <dd>

8.

</dd> <dt>

<span id="9"></span>

<span id="9"></span>**9** (256)


</dt> <dd>

9.

</dd> <dt>

<span id="10"></span>

<span id="10"></span>**10** (512)


</dt> <dd>

10.

</dd> <dt>

<span id="11"></span>

<span id="11"></span>**11** (1024)


</dt> <dd>

11th

</dd> <dt>

<span id="12"></span>

<span id="12"></span>**12** (2048)


</dt> <dd>

12th

</dd> <dt>

<span id="13"></span>

<span id="13"></span>**13** (4096)


</dt> <dd>

13th

</dd> <dt>

<span id="14"></span>

<span id="14"></span>**14** (8192)


</dt> <dd>

14.

</dd> <dt>

<span id="15"></span>

<span id="15"></span>**15** (16384)


</dt> <dd>

15.

</dd> <dt>

<span id="16"></span>

<span id="16"></span>**16** (32768)


</dt> <dd>

16.

</dd> <dt>

<span id="17"></span>

<span id="17"></span>**17** (65536)


</dt> <dd>

17.

</dd> <dt>

<span id="18"></span>

<span id="18"></span>**18** (131072)


</dt> <dd>

18.

</dd> <dt>

<span id="19"></span>

<span id="19"></span>**19** (262144)


</dt> <dd>

19.

</dd> <dt>

<span id="20"></span>

<span id="20"></span>**20** (524288)


</dt> <dd>

20.

</dd> <dt>

<span id="21"></span>

<span id="21"></span>**21** (1048576)


</dt> <dd>

21st

</dd> <dt>

<span id="22"></span>

<span id="22"></span>**22** (2097152)


</dt> <dd>

22nd

</dd> <dt>

<span id="23"></span>

<span id="23"></span>**23** (4194304)


</dt> <dd>

23rd

</dd> <dt>

<span id="24"></span>

<span id="24"></span>**24** (8388608)


</dt> <dd>

24.

</dd> <dt>

<span id="25"></span>

<span id="25"></span>**25** (16777216)


</dt> <dd>

25.

</dd> <dt>

<span id="26"></span>

<span id="26"></span>**26** (33554432)


</dt> <dd>

26.

</dd> <dt>

<span id="27"></span>

<span id="27"></span>**27** (67108864)


</dt> <dd>

27.

</dd> <dt>

<span id="28"></span>

<span id="28"></span>**28** (134217728)


</dt> <dd>

28.

</dd> <dt>

<span id="29"></span>

<span id="29"></span>**29** (268435456)


</dt> <dd>

29.

</dd> <dt>

<span id="30"></span>

<span id="30"></span>**30** (536870912)


</dt> <dd>

30.

</dd> <dt>

<span id="31"></span>

<span id="31"></span>**31** (1073741824)


</dt> <dd>

31.

</dd> </dl>

</dd> <dt>

**DaysOfWeek**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**in \_ Info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **DaysOfWeek**")
</dt> </dl>

Tage der Woche, an denen die Ausführung eines Auftrags geplant ist. Wenn ein Auftrag für die Ausführung an mehreren Wochentagen geplant ist, können die Werte in einem logischen OR verknüpft werden. Wenn beispielsweise geplant ist, dass ein Auftrag montags, mittwochs und freitags ausgeführt wird, beträgt der Wert der **DaysOfWeek** -Eigenschaft 1 oder 4 oder 16.

<dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**Montag** (1)


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**Dienstag** (2)


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**Mittwoch** (4)


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**Donnerstag** (8)


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**Freitag** (16)


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**Samstag** (32)


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**Sonntag** (64)


</dt> <dd></dd> </dl>

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Eine Textbeschreibung des-Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Verweilzeit**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeitspanne, für die der Auftrag ausgeführt wurde.

Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](cim-job.md)geerbt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")
</dt> </dl>

Gibt an, wann das Objekt installiert wurde. Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**InteractWithDesktop**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**in \_ Info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **Flags** \| **Job \_ noninteractive**")
</dt> </dl>

Der angegebene Auftrag ist interaktiv. Dies bedeutet, dass ein Benutzer während der Ausführung eine Eingabe an einen geplanten Auftrag übergeben kann.

</dd> <dt>

**JobId**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**in \_ enum**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **JobID**")
</dt> </dl>

Identifizieren der Auftragsnummer. Sie wird von Methoden als Handle für einen Auftrag verwendet, der auf diesem Computer geplant wird.

</dd> <dt>

**Auftragsstatus**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("Jobstatus"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**at \_ enum**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **Flags** \| **Job \_ exec \_ Error**")
</dt> </dl>

Ausführungs Status bei der letzten Ausführung des Auftrags.

<dt>

<span id="Success"></span><span id="success"></span><span id="SUCCESS"></span>

**Erfolg** ("Erfolg")


</dt> <dd></dd> <dt>

<span id="Failure"></span><span id="failure"></span><span id="FAILURE"></span>

**Fehler** ("Fehler")


</dt> <dd></dd> </dl>

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Die Bezeichnung, nach der das-Objekt bekannt ist. Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Benachrichtigen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Benutzer wird nach Abschluss oder Fehler des Auftrags benachrichtigt.

Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](cim-job.md)geerbt.

</dd> <dt>

**Besitzer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Benutzer, der den Auftrag übermittelt hat.

Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](cim-job.md)geerbt.

</dd> <dt>

**Priority**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wichtigkeit der Ausführung eines Auftrags.

Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](cim-job.md)geerbt.

</dd> <dt>

**Runwiederholtes ausführen**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures on \| [**\_ Info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **Flags** \| **Job in \_ \_ regelmäßigen Abständen ausführen**")
</dt> </dl>

Der geplante Auftrag wird an den Tagen, an denen der Auftrag geplant ist, wiederholt ausgeführt. Wenn der Wert **false** ist, wird der Auftrag einmal ausgeführt.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("StartTime"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**in \_ enum**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **jobtime**")
</dt> </dl>

Die UTC-Zeit zum Ausführen des Auftrags in der Form "YYYYMMDDHHMMSS. Mmmmmm (+-) OOO ", wobei" YYYYMMDD "durch" "ersetzt werden muss \* \* \* \* \* \* \* \* . Der Austausch ist erforderlich, da der Planungsdienst nur das einmalige Ausführen von Aufträgen oder das Ausführen an einem Tag des Monats oder der Woche zulässt. Ein Auftrag kann nicht an einem bestimmten Datum ausgeführt werden.

Der Abschnitt "(+-) OOO" des **StartTime** -Eigenschafts Werts ist die aktuelle Abweichung für die lokale Zeit Übersetzung. Die Verschiebung ist der Unterschied zwischen UTC-Zeit und Ortszeit. Multiplizieren Sie die Anzahl der Stunden, die Ihre Zeitzone vor oder hinter der Ortszeit (GMT) um 60 liegen soll, um die Verschiebung für Ihre Zeitzone zu berechnen (verwenden Sie eine positive Zahl für die Anzahl von Stunden, wenn Ihre Zeitzone vor GMT liegt, und eine negative Zahl, wenn sich Ihre Zeitzone hinter GMT befindet). Fügen Sie der Berechnung eine zusätzliche 60 hinzu, wenn die Zeitzone die Sommerzeit verwendet. Die Pacific Standard Time-Zone beträgt z. b. acht Stunden hinter GMT. Daher entspricht der Bias dem Wert-420 (-8 \* 60 + 60), wenn die Sommerzeit verwendet wird, und-480 (-8 \* 60), wenn die Sommerzeit nicht in Gebrauch ist. Sie können auch den Wert der Bias ermitteln, indem Sie die Eigenschaft "Bias" der [**Win32- \_ Zeit Zonen**](win32-timezone.md) Klasse Abfragen.

Beispiel: " \* \* \* \* \* \* \* \* 123000.000000-420" gibt 14,30 (2:30 Uhr) an. PST mit Sommerzeit.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Eine Zeichenfolge, die den aktuellen Status des Objekts angibt. Der Betriebsstatus und der nicht betriebliche Status können definiert werden. Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten. "Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).

Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten. "Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird. Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

Folgende Werte sind gültig:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Fehler** ("Fehler")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

Herunter **gestuft ("** heruntergestuft")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** ("unbekannt")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred-** Fehler ("pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

Wird **gestartet** ("wird gestartet")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

Wird **beendet ("wird angehalten** ")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Dienst** ("Dienst")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Betont** ("gestresst")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Nicht wiederherstellen** ("nicht wiederherstellen")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Kein Kontakt** ("kein Kontakt")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Verlorene** Kommunikations ("verlorene Kommunikations-")


</dt> <dd></dd> </dl>

</dd> <dt>

**Timesub;**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeitpunkt, zu dem der Auftrag übermittelt wurde.

Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](cim-job.md)geerbt.

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Zeitpunkt, zu dem der Auftrag ungültig ist oder angehalten werden soll.

Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](cim-job.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Jeder Auftrag, der für den Zeit Plan Dienst geplant ist, wird permanent gespeichert (der Planer kann einen Auftrag nach einem Neustart starten) und wird zum angegebenen Zeitpunkt und Tag der Woche oder des Monats ausgeführt. Wenn der Computer nicht aktiv ist oder der geplante Dienst nicht zum angegebenen Zeitpunkt ausgeführt wird, wird der angegebene Auftrag vom Zeit Plan Dienst am nächsten Tag zum angegebenen Zeitpunkt ausgeführt.

Aufträge werden gemäß der koordinierten Weltzeit (UTC) mit dem Versatz Offset von Greenwich Mean Time (GMT) geplant. Dies bedeutet, dass ein Auftrag mit einer beliebigen Zeitzone angegeben werden kann. Die **Win32 \_ ScheduledJob** -Klasse gibt bei der Enumeration eines Objekts die Ortszeit mit dem UTC-Offset zurück und konvertiert die lokale Zeit beim Erstellen neuer Aufträge. Beispiel: ein Auftrag, der zum Ausführen auf einem Computer in Boston um 10:30 Uhr angegeben wird. Die Ortszeit der PST-Zeit wird für die lokale Ausführung um 1:30 Uhr geplant. Dienstag EST.

> [!Note]  
> Ein Client muss berücksichtigen, ob die Sommerzeit auf dem lokalen Computer in Betrieb ist, und wenn dies der Fall ist, subtrahieren Sie einen Bias von 60 Minuten vom UTC-Offset.

 

Die **Win32 \_ ScheduledJob** -Klasse wird vom [**CIM- \_ Auftrag**](cim-job.md)abgeleitet. Sie müssen Mitglied der Gruppe "Administratoren" sein, um einen geplanten Auftrag mit dieser Klasse erstellen zu können.

Die **Win32 \_ ScheduledJob** -Klasse verwendet intern das at-Protokoll, das ab Windows 8 und Windows Server 2012 als veraltet markiert ist. Im ersten Schritt ist das at-Protokollstandard mäßig deaktiviert. Wenn das Protokoll deaktiviert ist, kann beispielsweise der Aufruf der [**Create**](create-method-in-class-win32-scheduledjob.md) -Methode für ein **Win32 \_ ScheduledJob** -Objekt mit dem Fehler 0x8 fehlschlagen. Sie können das at-Protokoll wieder aktivieren, indem Sie den folgenden Registrierungs Eintrag hinzufügen:

``` syntax
Key: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Schedule\Configuration 
Name: EnableAt 
Type: REG_DWORD
Value: 1
```

Möglicherweise müssen Sie den Computer neu starten, damit die Einstellung wirksam wird.

Da **Win32 \_ ScheduledJob** auf der Win32-API [**netschedulejobgetinfo**](/windows/win32/api/lmat/nf-lmat-netschedulejobgetinfo) basiert, können Sie diese Klasse nicht zusammen mit der Taskplaner verwenden. Wenn Sie Taskplaner verwenden möchten, verwenden Sie die Taskplaner-API. Weitere Informationen finden Sie in der [Taskplaner-Referenz](../taskschd/task-scheduler-reference.md).

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird Notepad.exe für die interaktive tägliche Durchführung von 1:25 Uhr auf der lokalen Computerzeit geplant.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set objNewJob = objWMIService.Get("Win32_ScheduledJob")
errJobCreated = objNewJob.Create("Notepad.exe", "********012500.000000-420", True , 4, , True, JobId) 
If errJobCreated <> 0 Then
Wscript.Echo "Error on task creation"
Else
Wscript.Echo "Task created"
End If
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Auftrag**](cim-job.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> <dt>

[WMI-Tasks: geplante Aufgaben](../wmisdk/wmi-tasks--scheduled-tasks.md)
</dt> </dl>

 

 
