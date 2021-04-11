---
description: Übermittelt einen Auftrag an ein Betriebssystem zur Ausführung zu einem bestimmten Zeitpunkt und zum angegebenen Zeitpunkt in der Zukunft.
ms.assetid: 9d582fbb-24cb-401d-8b77-af7671a24e6d
ms.tgt_platform: multiple
title: Create-Methode der Win32_ScheduledJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9f1acae94ea29d2d57b2952c0b0adc267ad3066c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342349"
---
# <a name="create-method-of-the-win32_scheduledjob-class"></a>Create-Methode der Win32 \_ ScheduledJob-Klasse

Die **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) -Methode sendet einen Auftrag an ein Betriebssystem zur Ausführung zu einem bestimmten Zeitpunkt und Datum in der Zukunft. Diese Methode erfordert, dass der Zeit Plan Dienst auf dem Computer gestartet wird, an den der Auftrag übermittelt wird.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 Create(
  [in]           string   Command,
  [in]           datetime StartTime,
  [in, optional] boolean  RunRepeatedly,
  [in, optional] uint32   DaysOfWeek,
  [in, optional] uint32   DaysOfMonth,
  [in, optional] boolean  InteractWithDesktop,
  [out]          uint32   JobId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Befehl* \[ in\]
</dt> <dd>

Der Name des Befehls, des Batch Programms oder der Binärdatei und Befehlszeilenparameter, die vom Zeit Plan Dienst zum Aufrufen des Auftrags verwendet werden.

Beispiel: "Debug/q/f".

</dd> <dt>

*StartTime* \[ in\]
</dt> <dd>

Koordinierte Weltzeit (UTC) zum Ausführen eines Auftrags. Das Formular muss wie folgt lauten: "YYYYMMDDHHMMSS. Mmmmmm (+-) OOO ", wobei" YYYYMMDD "durch" "ersetzt werden muss \* \* \* \* \* \* \* \* . Beispiel: " \* \* \* \* \* \* \* \* 143000.000000-420" gibt 14,30 (2:30 Uhr) an. PST mit Sommerzeit.

Der Abschnitt "(+-) OOO" des StartTime-Eigenschafts Werts ist die aktuelle Abweichung für die lokale Zeit Übersetzung. Die Verschiebung ist der Unterschied zwischen der UTC-Zeit und der Ortszeit. Multiplizieren Sie die Anzahl der Stunden, die Ihre Zeitzone vor oder hinter der Ortszeit (GMT) um 60 liegen soll, um die Verschiebung für Ihre Zeitzone zu berechnen (verwenden Sie eine positive Zahl für die Anzahl von Stunden, wenn Ihre Zeitzone vor GMT liegt, und eine negative Zahl, wenn sich Ihre Zeitzone hinter GMT befindet). Fügen Sie der Berechnung eine zusätzliche 60 hinzu, wenn die Zeitzone die Sommerzeit verwendet. Die Pacific Standard Time-Zone beträgt z. b. acht Stunden hinter GMT. Daher entspricht der Bias dem Wert-420 (-8 \* 60 + 60), wenn die Sommerzeit verwendet wird, und-480 (-8 \* 60), wenn die Sommerzeit nicht in Gebrauch ist. Sie können auch den Wert der Bias ermitteln, indem Sie die Eigenschaft "Bias" der [**Win32- \_ Zeit Zonen**](win32-timezone.md) Klasse Abfragen.

</dd> <dt>

*Runwiederholtes* \[ Ausführen in, optional\]
</dt> <dd>

**True** gibt an, dass ein geplanter Auftrag an bestimmten Tagen wiederholt ausgeführt wird. Der Standardwert ist **False**.

</dd> <dt>

*DaysOfWeek* \[ in, optional\]
</dt> <dd>

Tage der Woche, an denen die Ausführung eines Auftrags geplant ist. wird nur verwendet, wenn der Parameter *runwiederholter* den Wert **true** hat. Um einen Auftrag für mehr als einen Tag der Woche zu planen, verknüpfen Sie die entsprechenden Werte in einem logischen OR-Operator. Wenn Sie z. b. einen Auftrag für Dienstag und freitags planen möchten, ist der Wert von *DaysOfWeek* 2 oder 16.

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


</dt> <dd></dd> </dl> </dd> <dt>

*DaysOfMonth* \[ in, optional\]
</dt> <dd>

Tage des Monats, an denen die Ausführung eines Auftrags geplant ist. wird nur verwendet, wenn der Parameter *runwiederholter* den Wert **true** hat.

<dt>

<span id="1"></span>

<span id="1"></span>**1** (1)


</dt> <dd>

Tag 1 eines Monats

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2** (2)


</dt> <dd>

Tag 2 eines Monats

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3** (4)


</dt> <dd>

Tag 3 eines Monats

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4** (8)


</dt> <dd>

Tag 4 eines Monats

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5** (16)


</dt> <dd>

Tag 5 eines Monats

</dd> <dt>

<span id="6"></span>

<span id="6"></span>**6** (32)


</dt> <dd>

Tag 6 eines Monats

</dd> <dt>

<span id="7"></span>

<span id="7"></span>**7** (64)


</dt> <dd>

Tag 7 eines Monats

</dd> <dt>

<span id="8"></span>

<span id="8"></span>**8** (128)


</dt> <dd>

Tag 8 eines Monats

</dd> <dt>

<span id="9"></span>

<span id="9"></span>**9** (256)


</dt> <dd>

Tag 9 eines Monats

</dd> <dt>

<span id="10"></span>

<span id="10"></span>**10** (512)


</dt> <dd>

Tag 10 eines Monats

</dd> <dt>

<span id="11"></span>

<span id="11"></span>**11** (1024)


</dt> <dd>

Tag 11 eines Monats

</dd> <dt>

<span id="12"></span>

<span id="12"></span>**12** (2048)


</dt> <dd>

Tag 12 eines Monats

</dd> <dt>

<span id="13"></span>

<span id="13"></span>**13** (4096)


</dt> <dd>

Tag 13 eines Monats

</dd> <dt>

<span id="14"></span>

<span id="14"></span>**14** (8192)


</dt> <dd>

Tag 14 eines Monats

</dd> <dt>

<span id="15"></span>

<span id="15"></span>**15** (16384)


</dt> <dd>

Tag 15 eines Monats

</dd> <dt>

<span id="16"></span>

<span id="16"></span>**16** (32768)


</dt> <dd>

Tag 16 eines Monats

</dd> <dt>

<span id="17"></span>

<span id="17"></span>**17** (65536)


</dt> <dd>

Tag 17 eines Monats

</dd> <dt>

<span id="18"></span>

<span id="18"></span>**18** (131072)


</dt> <dd>

Tag 18 eines Monats

</dd> <dt>

<span id="19"></span>

<span id="19"></span>**19** (262144)


</dt> <dd>

Tag 19 eines Monats

</dd> <dt>

<span id="20"></span>

<span id="20"></span>**20** (524288)


</dt> <dd>

Tag 20 eines Monats

</dd> <dt>

<span id="21"></span>

<span id="21"></span>**21** (1048576)


</dt> <dd>

Tag 21 eines Monats

</dd> <dt>

<span id="22"></span>

<span id="22"></span>**22** (2097152)


</dt> <dd>

Tag 22 eines Monats

</dd> <dt>

<span id="23"></span>

<span id="23"></span>**23** (4194304)


</dt> <dd>

Tag 23 eines Monats

</dd> <dt>

<span id="24"></span>

<span id="24"></span>**24** (8388608)


</dt> <dd>

Tag 24 eines Monats

</dd> <dt>

<span id="25"></span>

<span id="25"></span>**25** (16777216)


</dt> <dd>

Tag 25 eines Monats

</dd> <dt>

<span id="26"></span>

<span id="26"></span>**26** (33554432)


</dt> <dd>

Tag 26 eines Monats

</dd> <dt>

<span id="27"></span>

<span id="27"></span>**27** (67108864)


</dt> <dd>

Tag 27 eines Monats

</dd> <dt>

<span id="28"></span>

<span id="28"></span>**28** (134217728)


</dt> <dd>

Tag 28 eines Monats

</dd> <dt>

<span id="29"></span>

<span id="29"></span>**29** (268435456)


</dt> <dd>

Tag 29 eines Monats

</dd> <dt>

<span id="30"></span>

<span id="30"></span>**30** (536870912)


</dt> <dd>

Tag 30 eines Monats

</dd> <dt>

<span id="31"></span>

<span id="31"></span>**31** (1073741824)


</dt> <dd>

Tag 31 eines Monats

</dd> </dl> </dd> <dt>

*InteractWithDesktop* \[ in, optional\]
</dt> <dd>

Wenn der Wert **true** ist, sollte der angegebene Auftrag interaktiv sein, was bedeutet, dass ein Benutzer während der Ausführung des Auftrags Eingaben an einen geplanten Auftrag übergeben kann. Der Standardwert ist **False**.

</dd> <dt>

*JobID* \[ vorgenommen\]
</dt> <dd>

Bezeichnernummer eines Auftrags. Dieser Parameter ist ein Handle für einen Auftrag, der auf einem Computer geplant wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei erfolgreicher Ausführung den Wert 0 (null) und eine andere Zahl zurück, um einen Fehler anzugeben. Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Erfolgreicher Abschluss**
</dt> <dd>

0

Die Anforderung wird akzeptiert.

</dd> <dt>

**Nicht unterstützt**
</dt> <dd>

1

Die Anforderung wird nicht unterstützt.

</dd> <dt>

**Zugriff verweigert**
</dt> <dd>

2

Der Benutzer verfügt nicht über die erforderlichen Zugriffsrechte.

</dd> <dt>

**Unbekannter Fehler.**
</dt> <dd>

8

Interaktiver Prozess.

</dd> <dt>

**Der Pfad wurde nicht gefunden**
</dt> <dd>

9

Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.

</dd> <dt>

**Ungültiger Parameter**
</dt> <dd>

21

An den Dienst wurden ungültige Parameter übermittelt.

</dd> <dt>

**Dienst wurde nicht gestartet.**
</dt> <dd>

22

Das Konto, unter dem dieser Dienst ausgeführt wird, ist ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.

</dd> <dt>

**Andere**
</dt> <dd>

23 4294967295

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn der geplante Auftrag ein interaktives Programm (z. b. Notepad) startet, muss die **interactwithdeskto** -Eigenschaft auf **true** festgelegt werden, oder der Programm Bildschirm ist nicht sichtbar. Der Prozess wird weiterhin im **Task-Manager** angezeigt, auch wenn er nicht auf dem Bildschirm angezeigt wird.

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

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ ScheduledJob**](win32-scheduledjob.md)
</dt> </dl>

 

