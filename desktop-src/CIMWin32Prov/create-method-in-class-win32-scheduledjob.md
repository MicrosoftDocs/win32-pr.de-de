---
description: Übermittelt einen Auftrag zur Ausführung zu einem bestimmten Zeitpunkt und einem bestimmten Datum in der Zukunft an ein Betriebssystem.
ms.assetid: 9d582fbb-24cb-401d-8b77-af7671a24e6d
ms.tgt_platform: multiple
title: Create-Methode der Win32_ScheduledJob Klasse
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
ms.openlocfilehash: a7788c894646b3ebb07fc9d3d98aeeda54b9172b5dde01e7eb65975bb2d95d61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547410"
---
# <a name="create-method-of-the-win32_scheduledjob-class"></a>Create-Methode der Win32 \_ ScheduledJob-Klasse

Die **Methode** [WMI-Klasse erstellen](/windows/desktop/WmiSdk/retrieving-a-class) übermittelt einen Auftrag zur Ausführung zu einem bestimmten Zeitpunkt und einem bestimmten Datum in der Zukunft an ein Betriebssystem. Diese Methode erfordert, dass der Zeitplandienst auf dem Computer gestartet wird, an den der Auftrag übermittelt wird.

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

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

*Befehl* \[ In\]
</dt> <dd>

Der Name des Befehls, des Batchprogramms oder der Binärdatei sowie der Befehlszeilenparameter, die der Zeitplandienst zum Aufrufen des Auftrags verwendet.

Beispiel: "defrag /q /f".

</dd> <dt>

*StartTime* \[ In\]
</dt> <dd>

koordinierte Weltzeit (UTC) zum Ausführen eines Auftrags. Das Formular muss sein: "YYYYMMDDHHMMSS. MMMMMM(+-)OOO", wobei "YYYYMMDD" durch " " ersetzt werden \* \* \* \* \* \* \* \* muss. Beispiel: \* \* \* \* \* \* \* \* "143000.000000-420" gibt 14,30 (14:30 Uhr) an. PST mit tatsächlicher Sommerzeit.

Der Abschnitt "(+-)OOO" des StartTime-Eigenschaftswerts ist die aktuelle Abweichung für die Lokale Zeitübersetzung. Die Abweichung ist der Unterschied zwischen der UTC-Zeit und der Ortszeit. Multiplizieren Sie zum Berechnen der Abweichung für Ihre Zeitzone die Anzahl der Stunden, die Ihre Zeitzone voraus oder hinter Greenwich Mean Time (GMT) liegt, mit 60 (verwenden Sie eine positive Zahl für die Anzahl der Stunden, wenn Ihre Zeitzone vor GMT liegt, und eine negative Zahl, wenn sich Ihre Zeitzone hinter GMT befindet). Fügen Sie ihrer Berechnung weitere 60 hinzu, wenn in Ihrer Zeitzone die Sommerzeit verwendet wird. Die Pacific Standard Time Zone liegt beispielsweise acht Stunden hinter GMT, daher entspricht die Abweichung -420 (-8 60 + 60), wenn Sommerzeit verwendet wird, und \* -480 (-8 60), wenn die Sommerzeit nicht \* verwendet wird. Sie können den Wert der Verzerrung auch ermitteln, indem Sie die Bias-Eigenschaft der [**Win32 \_ TimeZone-Klasse**](win32-timezone.md) abfragen.

</dd> <dt>

*RunRepeatedly* \[ in, optional\]
</dt> <dd>

True **gibt an,** dass ein geplanter Auftrag wiederholt an bestimmten Tagen ausgeführt wird. Der Standardwert ist **False**.

</dd> <dt>

*DaysOfWeek* \[ in, optional\]
</dt> <dd>

Wochentage, an denen die Ausführung eines Auftrags geplant ist; wird nur verwendet, wenn *der RunRepeatedly-Parameter* true **ist.** Um einen Auftrag für mehr als einen Tag der Woche zu planen, verbinden Sie die entsprechenden Werte in einem logischen OR. Um beispielsweise einen Auftrag für Dienstag und Freitag zu planen, ist der Wert von *DaysOfWeek* 2 ODER 16.

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

Tage des Monats, an denen die Ausführung eines Auftrags geplant ist; wird nur verwendet, wenn *der RunRepeatedly-Parameter* true **ist.**

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

True **gibt an,** dass der angegebene Auftrag interaktiv sein sollte, was bedeutet, dass ein Benutzer während der Ausführung des Auftrags Eingaben für einen geplanten Auftrag geben kann. Der Standardwert ist **False**.

</dd> <dt>

*JobId* \[ out\]
</dt> <dd>

Bezeichnernummer eines Auftrags. Dieser Parameter ist ein Handle für einen Auftrag, der auf einem Computer geplant wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolgreicher einen Wert von 0 (null) und eine andere Zahl zurück, um einen Fehler anzugeben. Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).

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

Der Benutzer hat nicht den erforderlichen Zugriff.

</dd> <dt>

**Unbekannter Fehler**
</dt> <dd>

8

Interaktiver Prozess.

</dd> <dt>

**Der Pfad wurde nicht gefunden**
</dt> <dd>

9

Der Verzeichnispfad zur ausführbaren Dienstdatei wurde nicht gefunden.

</dd> <dt>

**Ungültiger Parameter**
</dt> <dd>

21

Ungültige Parameter wurden an den Dienst übergeben.

</dd> <dt>

**Der Dienst wurde nicht gestartet.**
</dt> <dd>

22

Das Konto, unter dem dieser Dienst ausgeführt wird, ist ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Diensts.

</dd> <dt>

**Andere**
</dt> <dd>

23 4294967295

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn ihr geplanter Auftrag ein interaktives Programm wie Editor startet, muss die **InteractWithDeskto-Eigenschaft** auf **True** festgelegt werden, oder der Bildschirm des Programms ist nicht sichtbar. Der Prozess wird weiterhin in **der** Task-Manager auch wenn er nicht auf dem Bildschirm angezeigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ ScheduledJob**](win32-scheduledjob.md)
</dt> </dl>

 

