---
title: Schtasks.exe
description: Ermöglicht einem Administrator das Erstellen, Löschen, Abfragen, Ändern, Ausführen und Beenden geplanter Aufgaben auf einem lokalen oder Remotecomputer.
ms.assetid: 3cf973de-14c4-4ca9-86a7-7f97181bd9e0
keywords:
- Schtasks.exe Taskplaner
topic_type:
- apiref
api_name:
- Schtasks.exe
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 0da33bf63d999ddad42f58dfa15a1c36571a664855ac20e48ef43bfd7aecd55b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139383"
---
# <a name="schtasksexe"></a>Schtasks.exe

Ermöglicht einem Administrator das Erstellen, Löschen, Abfragen, Ändern, Ausführen und Beenden geplanter Aufgaben auf einem lokalen oder Remotecomputer. Beim Ausführen von Schtasks.exe ohne Argumente werden der Status und die nächste Laufzeit für jeden registrierten Task angezeigt. 

Weitere Informationen zu Taskplaner finden Sie in dieser Einführung: [Taskplaner für Entwickler.](task-scheduler-start-page.md)

## <a name="creating-a-task"></a>Erstellen einer Aufgabe

Die folgende Syntax wird verwendet, um eine Aufgabe auf dem lokalen Oder Remotecomputer zu erstellen.

``` syntax
schtasks /Create 
[/S system [/U username [/P [password]]]]
[/RU username [/RP [password]] /SC schedule [/MO modifier] [/D day]
[/M months] [/I idletime] /TN taskname /TR taskrun [/ST starttime]
[/RI interval] [ {/ET endtime | /DU duration} [/K] 
[/XML xmlfile] [/V1]] [/SD startdate] [/ED enddate] [/IT] [/Z] [/F]
```

### <a name="parameters"></a>Parameter

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S-System** 
</dt> <dd>

Ein -Wert, der den Remotecomputer angibt, mit dem eine Verbindung hergestellt werden soll. Wenn dieser Wert nicht angegeben wird, wird der Systemparameter standardmäßig auf dem lokalen Computer verwendet.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U-Benutzername** 
</dt> <dd>

Ein -Wert, der den Benutzerkontext angibt, unter dem Schtasks.exe ausgeführt werden soll.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span> **\[ /P-Kennwort \]**
</dt> <dd>

Ein -Wert, der das Kennwort für einen bestimmten Benutzerkontext angibt. Wenn diese Angabe nicht erfolgt, fordert Schtasks.exe den Benutzer zur Eingabe auf.

</dd> <dt>

<span id="_RU_username"></span><span id="_ru_username"></span><span id="_RU_USERNAME"></span>**/RU-Benutzername** 
</dt> <dd>

Ein -Wert, der den Benutzerkontext angibt, unter dem der Task ausgeführt wird. Gültige Werte für das Systemkonto sind "", "NT AUTHORITY \\ SYSTEM" oder "SYSTEM". Für Taskplaner 2.0-Tasks sind "NT AUTHORITY \\ LOCALSERVICE" und "NT AUTHORITY \\ NETWORKSERVICE" ebenfalls gültige Werte.

</dd> <dt>

<span id="_RP__password_"></span><span id="_rp__password_"></span><span id="_RP__PASSWORD_"></span> **\[ /RP-Kennwort \]**
</dt> <dd>

Ein -Wert, der das Kennwort für den mit dem /RU-Parameter angegebenen Benutzer angibt. Um zur Eingabe des Kennworts aufzufordern, muss der Wert entweder " \* " oder kein Wert sein. Dieses Kennwort wird für das Systemkonto ignoriert. Dieser Parameter muss entweder mit /RU oder dem /XML-Switch kombiniert werden.

</dd> <dt>

<span id="_SC_schedule"></span><span id="_sc_schedule"></span><span id="_SC_SCHEDULE"></span>**/SC-Zeitplan** 
</dt> <dd>

Ein -Wert, der die Zeitplanhäufigkeit angibt. Gültige Werte sind: MINUTE, HOURLY, DAILY, WEEKLY, MONTHLY, ONCE, ONLOGON, ONIDLE und ONEVENT.

</dd> <dt>

<span id="_MO_modifier"></span><span id="_mo_modifier"></span><span id="_MO_MODIFIER"></span> **/MO-Modifizierer**
</dt> <dd>

Ein -Wert, der den Zeitplantyp verfeinern soll, um eine feineren Steuerung der Zeitplanwiederholung zu ermöglichen. Gültige Werte sind:

-   MINUTE: 1 bis 1439 Minuten.
-   STÜNDLICH: 1 bis 23 Stunden.
-   TÄGLICH: 1 bis 365 Tage.
-   WÖCHENTLICH: Wochen 1 bis 52.
-   ONCE: Keine Modifizierer.
-   ONSTART: Keine Modifizierer.
-   ONLOGON: Keine Modifizierer.
-   ONIDLE: Keine Modifizierer.
-   MONATLICH: 1 – 12 oder FIRST, SECOND, THIRD, FOURTH, LAST und LASTDAY.
-   ONEVENT: XPath-Ereignisabfragezeichenfolge.

</dd> <dt>

<span id="_D_days"></span><span id="_d_days"></span><span id="_D_DAYS"></span>**/D** **Tage**
</dt> <dd>

Ein -Wert, der den Wochentag zum Ausführen der Aufgabe angibt. Gültige Werte sind: MON, TUE, WED, DO, FR, SAT, SUN und für die monatlichen Zeitpläne 1 bis 31 (Tage des Monats). Das Platzhalterzeichen ( \* ) gibt alle Tage an.

</dd> <dt>

<span id="_M_months"></span><span id="_m_months"></span><span id="_M_MONTHS"></span>**/M** **Monate**
</dt> <dd>

Ein -Wert, der Monate des Jahres angibt. Der Standardwert ist der erste Tag des Monats. Gültige Werte sind: JAN, FEB, MAR, APR, MAY, JUN, JUL, AUG, SEP, OCT, NOV und DEC. Das Platzhalterzeichen ( \* ) gibt alle Monate an.

</dd> <dt>

<span id="_I_idletime"></span><span id="_i_idletime"></span><span id="_I_IDLETIME"></span>**/I** **idletime**
</dt> <dd>

Ein -Wert, der die Leerlaufzeit angibt, die gewartet werden soll, bevor ein geplanter ONIDLE-Task ausgeführt wird. Der gültige Bereich beträgt 1 bis 999 Minuten.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**
</dt> <dd>

Ein -Wert, der einen Namen angibt, der den geplanten Task eindeutig identifiziert.

</dd> <dt>

<span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **taskrun**
</dt> <dd>

Ein -Wert, der den Pfad und den Dateinamen der Aufgabe angibt, die zum geplanten Zeitpunkt ausgeführt werden soll. Beispiel: C: \\ Windows \\ System32 \\calc.exe.

</dd> <dt>

<span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/ST** **starttime**
</dt> <dd>

Ein -Wert, der die Startzeit zum Ausführen der Aufgabe angibt. Das Zeitformat ist HH:mm (24-Stunden-Zeit). Beispielsweise gibt 14:30 14:30 Uhr an. Der Standardwert ist die aktuelle Uhrzeit ist /ST ist nicht angegeben. Diese Option ist mit dem /SC ONCE-Argument erforderlich.

</dd> <dt>

<span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span> **/RI-Intervall**
</dt> <dd>

Ein -Wert, der das Wiederholungsintervall in Minuten angibt. Dies gilt nicht für die folgenden Zeitplantypen: MINUTE, HOURLY, ONSTART, ONLOGON, ONIDLE und ONEVENT. Der gültige Bereich beträgt 1 bis 599940 Minuten. Wenn entweder die Parameter /ET oder /DU angegeben sind, beträgt der Standardwert 10 Minuten.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/ET** **endtime**
</dt> <dd>

Ein -Wert, der die Endzeit zum Ausführen des Tasks angibt. Das Zeitformat ist HH:mm (24-Stunden-Zeit). Beispielsweise gibt 14:50 14:50 Uhr an. Dies gilt nicht für die folgenden Zeitplantypen: ONSTART, ONLOGON, ONIDLE und ONEVENT.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/DU** **duration**
</dt> <dd>

Ein -Wert, der die Dauer für die Ausführung des Tasks angibt. Das Zeitformat ist HH:mm (24-Stunden-Zeit). Beispielsweise gibt 14:50 14:50 Uhr an. Dies gilt nicht für /ET und für die folgenden Zeitplantypen: ONSTART, ONLOGON, ONIDLE und ONEVENT. Bei /V1-Tasks (Taskplaner 1.0-Tasks) beträgt die Standarddauer eine Stunde, wenn /RI angegeben ist.

**Windows XP:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_K_"></span><span id="_k_"></span>**/K** 
</dt> <dd>

Ein -Wert, der die Aufgabe zur Endzeit oder Dauer beendet. Dies gilt nicht für die folgenden Zeitplantypen: ONSTART, ONLOGON, ONIDLE und ONEVENT. Entweder /ET oder /DU muss angegeben werden.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **startdate**
</dt> <dd>

Ein -Wert, der das erste Datum angibt, an dem die Aufgabe ausgeführt werden soll. Das Format ist mm/dd/yyyy. Dieser Wert ist standardmäßig auf das aktuelle Datum eingestellt. Dies gilt nicht für die folgenden Zeitplantypen: ONCE, ONSTART, ONLOGON, ONIDLE und ONEVENT.

</dd> <dt>

<span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/ED** **enddate**
</dt> <dd>

Ein -Wert, der das letzte Datum angibt, an dem der Task ausgeführt wird. Das Format ist mm/dd/yyyy. Dies gilt nicht für die folgenden Zeitplantypen: ONCE, ONSTART, ONLOGON, ONIDLE und ONEVENT.

</dd> <dt>

<span id="_EC_ChannelName"></span><span id="_ec_channelname"></span><span id="_EC_CHANNELNAME"></span>**/EC** **ChannelName**
</dt> <dd>

Ein -Wert, der den Ereigniskanal für ONEVENT-Trigger angibt.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_IT_"></span><span id="_it_"></span>**/IT** 
</dt> <dd>

Ein -Wert, mit dem der Task nur interaktiv ausgeführt werden kann, wenn der /RU-Benutzer derzeit zum Zeitpunkt der Ausführung des Tasks angemeldet ist. Die Aufgabe wird nur ausgeführt, wenn der Benutzer angemeldet ist.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_NP_"></span><span id="_np_"></span>**/NP** 
</dt> <dd>

Ein -Wert, der angibt, dass kein Kennwort gespeichert wird. Die Aufgabe wird nicht interaktiv als der angegebene Benutzer ausgeführt. Es sind nur lokale Ressourcen verfügbar.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_Z_"></span><span id="_z_"></span>**/Z** 
</dt> <dd>

Ein -Wert, der die Aufgabe markiert, die nach der letzten Ausführung gelöscht werden soll.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_XML_xmlfile"></span><span id="_xml_xmlfile"></span><span id="_XML_XMLFILE"></span>**/XML xmlfile** 
</dt> <dd>

Ein -Wert, der eine Aufgabe aus einer XML-Datei erstellt. Dieser Parameter kann mit den Schaltern /RU und /RP oder mit dem Schalter /RP allein kombiniert werden, wenn die Aufgaben-XML bereits den Prinzipal enthält.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_V1_"></span><span id="_v1_"></span>**/V1** 
</dt> <dd>

Ein -Wert, der eine Aufgabe erstellt, die für Windows 2000-, Windows Server 2003- und Windows XP-Plattformen sichtbar ist.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_F_"></span><span id="_f_"></span>**F** 
</dt> <dd>

Ein -Wert, der die Aufgabe erzwingen und Warnungen unterdrückt, wenn der angegebene Task bereits vorhanden ist.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span>**/RL-Ebene** 
</dt> <dd>

Ein -Wert, der die Ausführungsebene für den Task festlegt. Gültige Werte sind LIMITED und HIGHEST. Der Standardwert ist LIMITED.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/DELAY** **delaytime**
</dt> <dd>

Ein -Wert, der die Wartezeit angibt, mit der der Task nach dem Auslösen des Triggers verzögert wird. Das Zeitformat ist mmmm:ss. Diese Option ist nur für die Zeitplantypen ONSTART, ONLOGON und ONEVENT gültig.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="___"></span>**/?** 
</dt> <dd>

Ein -Wert, der die Hilfemeldung für Schtasks.exe anzeigt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Verwenden Sie beim Erstellen einer Aufgabe auf einem Remotecomputer, der unter dem Betriebssystem Windows XP, Windows Server 2003 oder Windows 2000 ausgeführt wird, den Schalter /V1.

Sie können keine nicht interaktive Remote-Taskplaner 1.0-Aufgabe erstellen (erstellen Sie eine Aufgabe, indem Sie nicht den /IT-Switch und den /V1-Switch verwenden), wenn auf dem Remotecomputer die Firewallausnahme Datei- und Druckerfreigabe aktiviert und die Firewallausnahme für die Verwaltung geplanter Remoteaufgaben deaktiviert ist.

## <a name="deleting-a-task"></a>Löschen einer Aufgabe

Die folgende Syntax wird verwendet, um einen oder mehrere geplante Aufgaben zu löschen.

``` syntax
schtasks /Delete 
[/S system [/U username [/P [password]]]]
[/TN taskname] [/F]
```

### <a name="parameters"></a>Parameter

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S-System** 
</dt> <dd>

Ein -Wert, der den Remotecomputer angibt, mit dem eine Verbindung hergestellt werden soll. Wenn dieser Wert nicht angegeben wird, wird der Systemparameter standardmäßig auf dem lokalen Computer verwendet.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U-Benutzername** 
</dt> <dd>

Ein -Wert, der den Benutzerkontext angibt, unter dem Schtasks.exe ausgeführt werden soll.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span> **\[ /P-Kennwort \]**
</dt> <dd>

Ein -Wert, der das Kennwort für den angegebenen Benutzerkontext angibt. Wenn diese Angabe nicht erfolgt, fordert Schtasks.exe den Benutzer zur Eingabe auf.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**
</dt> <dd>

Ein -Wert, der den Namen des zu löschenden geplanten Tasks angibt. Das Platzhalterzeichen ( \* ) kann verwendet werden, um alle Aufgaben zu löschen.

</dd> <dt>

<span id="_F_"></span><span id="_f_"></span>**F** 
</dt> <dd>

Ein -Wert, der das Löschen der Aufgabe erzwingen und Warnungen unterdrückt, wenn der angegebene Task ausgeführt wird.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Ein -Wert, der Hilfe für Schtasks.exe anzeigt.

</dd> </dl>

## <a name="running-a-task"></a>Ausführen einer Aufgabe

Die folgende Syntax wird verwendet, um sofort eine geplante Aufgabe auszuführen.

``` syntax
schtasks /Run 
[/S system [/U username [/P [password]]]]
/TN taskname
```

### <a name="parameters"></a>Parameter

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S-System** 
</dt> <dd>

Ein -Wert, der den Remotecomputer angibt, mit dem eine Verbindung hergestellt werden soll. Wenn dieser Wert nicht angegeben wird, wird der Systemparameter standardmäßig auf dem lokalen Computer verwendet.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U-Benutzername** 
</dt> <dd>

Ein -Wert, der den Benutzerkontext angibt, unter dem Schtasks.exe ausgeführt werden soll.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span> **\[ /P-Kennwort \]**
</dt> <dd>

Ein -Wert, der das Kennwort für den angegebenen Benutzerkontext angibt. Wenn diese Angabe nicht erfolgt, fordert Schtasks.exe den Benutzer zur Eingabe auf.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**
</dt> <dd>

Ein -Wert, der den Namen der auszuführenden geplanten Aufgabe angibt.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Ein -Wert, der Hilfe für Schtasks.exe anzeigt.

</dd> </dl>

## <a name="ending-a-running-task"></a>Beenden eines ausgeführten Tasks

Die folgende Syntax wird verwendet, um eine ausgeführte geplante Aufgabe zu beenden.

> [!Note]  
> Um die Ausführung eines Remotetasks zu beenden, stellen Sie sicher, dass auf dem Remotecomputer die Firewallausnahmen Datei- und Druckerfreigabe und Verwaltung geplanter Remoteaufgaben aktiviert sind.

 

``` syntax
schtasks /End 
[/S system [/U username [/P [password]]]]
/TN taskname
```

### <a name="parameters"></a>Parameter

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S-System** 
</dt> <dd>

Ein -Wert, der den Remotecomputer angibt, mit dem eine Verbindung hergestellt werden soll. Wenn dieser Wert nicht angegeben wird, wird der Systemparameter standardmäßig auf dem lokalen Computer verwendet.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U-Benutzername** 
</dt> <dd>

Ein -Wert, der den Benutzerkontext angibt, unter dem Schtasks.exe ausgeführt werden soll.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span> **\[ /P-Kennwort \]**
</dt> <dd>

Ein -Wert, der das Kennwort für den angegebenen Benutzerkontext angibt. Wenn diese Angabe nicht erfolgt, fordert Schtasks.exe den Benutzer zur Eingabe auf.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**
</dt> <dd>

Ein -Wert, der den Namen des zu beendenden geplanten Tasks angibt.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Ein -Wert, der Hilfe für Schtasks.exe anzeigt.

</dd> </dl>

## <a name="querying-for-task-information"></a>Abfragen von Aufgabeninformationen

Die folgende Syntax wird verwendet, um die geplanten Aufgaben vom lokalen Computer oder Remotecomputer anzuzeigen.

``` syntax
schtasks /Query 
[/S system [/U username [/P [password]]]]
[/FO format | /XML] [/NH] [/V] [/TN taskname] [/?]
```

### <a name="parameters"></a>Parameter

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S-System** 
</dt> <dd>

Ein -Wert, der den Remotecomputer angibt, mit dem eine Verbindung hergestellt werden soll. Wenn dieser Wert nicht angegeben wird, wird der Systemparameter standardmäßig auf dem lokalen Computer verwendet.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U-Benutzername** 
</dt> <dd>

Ein -Wert, der den Benutzerkontext angibt, unter dem Schtasks.exe ausgeführt werden soll.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span> **\[ /P-Kennwort \]**
</dt> <dd>

Ein -Wert, der das Kennwort für den angegebenen Benutzerkontext angibt. Wenn diese Angabe nicht erfolgt, fordert Schtasks.exe den Benutzer zur Eingabe auf.

</dd> <dt>

<span id="_FO_format"></span><span id="_fo_format"></span><span id="_FO_FORMAT"></span>**/FO-Format** 
</dt> <dd>

Ein -Wert, der das Ausgabeformat angibt. Gültige Werte sind TABLE, LIST und CSV.

</dd> <dt>

<span id="_NH_"></span><span id="_nh_"></span>**/NH** 
</dt> <dd>

Ein -Wert, der angibt, dass der Spaltenheader nicht in der Ausgabe angezeigt werden soll. Dies gilt nur für TABLE- und CSV-Formate.

</dd> <dt>

<span id="_V_"></span><span id="_v_"></span>**/V** 
</dt> <dd>

Ein -Wert, der eine ausführliche Taskausgabe anzeigt.

> [!Note]  
> Wenn eine Aufgabe nur einmal ausgeführt werden soll, lautet die angezeigte Zeitplaninformation "Zeitplanungsdaten sind in diesem Format nicht verfügbar".

 

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**
</dt> <dd>

Ein -Wert, der den Aufgabennamen angibt, für den die Informationen abgerufen werden sollen. Wenn kein Aufgabenname angegeben wird, werden Informationen für alle Aufgaben angezeigt.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_XML_"></span><span id="_xml_"></span>**/XML** 
</dt> <dd>

Ein -Wert, der verwendet wird, um die Taskdefinitionen im XML-Format anzuzeigen.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Ein -Wert, der zum Anzeigen der Hilfe für Schtasks.exe verwendet wird.

</dd> </dl>

## <a name="changing-a-task"></a>Ändern einer Aufgabe

Die folgende Syntax wird verwendet, um die Ausführung des Programms zu ändern oder das Benutzerkonto und Kennwort zu ändern, das von einer geplanten Aufgabe verwendet wird.

``` syntax
schtasks /Change 
[/S system [/U username [/P [password]]]] /TN taskname
{ [/RU runasuser] [/RP runaspassword] [/TR taskrun] [/ST starttime] 
[/RI interval] [ {/ET endtime | /DU duration} [/K] ]
[/SD startdate] [/ED enddate] [/ENABLE | /DISABLE] [/IT] [/Z] }
```

### <a name="parameters"></a>Parameter

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S-System** 
</dt> <dd>

Ein -Wert, der den Remotecomputer angibt, mit dem eine Verbindung hergestellt werden soll. Wenn dieser Wert nicht angegeben wird, wird der Systemparameter standardmäßig auf dem lokalen Computer verwendet.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U-Benutzername** 
</dt> <dd>

Ein -Wert, der den Benutzerkontext angibt, unter dem Schtasks.exe ausgeführt werden soll.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span> **\[ /P-Kennwort \]**
</dt> <dd>

Ein -Wert, der das Kennwort für den angegebenen Benutzerkontext angibt. Wenn diese Angabe nicht erfolgt, fordert Schtasks.exe den Benutzer zur Eingabe auf.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**
</dt> <dd>

Ein -Wert, der angibt, welcher geplante Task geändert werden soll.

</dd> <dt>

<span id="_RU_runasuser"></span><span id="_ru_runasuser"></span><span id="_RU_RUNASUSER"></span>**/RU** **runasuser**
</dt> <dd>

Ein -Wert, der den Benutzernamen (Benutzerkontext) ändert, unter dem die geplante Aufgabe ausgeführt wird. Gültige Werte für das Systemkonto sind "", "NT AUTHORITY \\ SYSTEM" oder "SYSTEM". Für Taskplaner 2.0-Tasks sind "NT AUTHORITY \\ LOCALSERVICE" und "NT AUTHORITY \\ NETWORKSERVICE" ebenfalls gültige Werte.

</dd> <dt>

<span id="_RP_runaspassword"></span><span id="_rp_runaspassword"></span><span id="_RP_RUNASPASSWORD"></span>**/RP** **runaspassword**
</dt> <dd>

Ein -Wert, der ein neues Kennwort für den vorhandenen Benutzerkontext oder das Kennwort für ein neues Benutzerkonto angibt. Dieses Kennwort wird für das Systemkonto ignoriert.

</dd> <dt>

<span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **taskrun**
</dt> <dd>

Ein -Wert, der ein neues Programm angibt, das die Aufgabe ausführen wird.

</dd> <dt>

<span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/ST** **starttime**
</dt> <dd>

Ein -Wert, der die Startzeit zum Ausführen der Aufgabe angibt. Das Zeitformat ist HH:mm (24-Stunden-Zeit). Beispielsweise gibt 14:30 14:30 Uhr an.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span> **/RI-Intervall**
</dt> <dd>

Ein -Wert, der das Wiederholungsintervall in Minuten angibt. Der gültige Bereich beträgt 1 bis 599940 Minuten.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/ET** **endtime**
</dt> <dd>

Ein -Wert, der die Endzeit für die Aufgabe angibt. Das Zeitformat ist HH:mm (24-Stunden-Zeit). Beispielsweise gibt 14:50 14:50 Uhr an.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/DU** **duration**
</dt> <dd>

Ein -Wert, der die Dauer für die Ausführung des Tasks angibt. Das Zeitformat ist HH:mm (24-Stunden-Zeit). Beispielsweise gibt 14:50 14:50 Uhr an. Dies gilt nicht für den /ET-Parameter.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_K_"></span><span id="_k_"></span>**/K** 
</dt> <dd>

Ein -Wert, der die Aufgabe zur Endzeit oder Dauer beendet.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **startdate**
</dt> <dd>

Ein -Wert, der das erste Datum angibt, an dem die Aufgabe ausgeführt werden soll. Das Format ist mm/dd/yyyy.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/ED** **enddate**
</dt> <dd>

Ein -Wert, der das letzte Datum angibt, an dem der Task ausgeführt wird. Das Format ist mm/dd/yyyy.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_IT_"></span><span id="_it_"></span>**/IT** 
</dt> <dd>

Ein -Wert, mit dem der Task nur interaktiv ausgeführt werden kann, wenn der /RU-Benutzer derzeit zum Zeitpunkt der Ausführung des Tasks angemeldet ist. Die Aufgabe wird nur ausgeführt, wenn der Benutzer angemeldet ist.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span>**/RL-Ebene** 
</dt> <dd>

Ein -Wert, der die Ausführungsebene für den Task festlegt. Gültige Werte sind LIMITED und HIGHEST.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_ENABLE_"></span><span id="_enable_"></span>**/ENABLE** 
</dt> <dd>

Ein -Wert, der die geplante Aufgabe aktiviert. Eine aktivierte Aufgabe kann ausgeführt werden, und eine deaktivierte Aufgabe kann nicht ausgeführt werden.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_DISABLE_"></span><span id="_disable_"></span>**/DISABLE** 
</dt> <dd>

Ein -Wert, der die Ausführung des geplanten Tasks deaktiviert.

> [!Note]  
> Wenn ein Remotetask Taskplaner 1.0 durch Schtasks.exe deaktiviert wird und auf dem Remotecomputer die Firewallausnahme datei- und druckerfreigabe aktiviert und die Firewallausnahme für die Verwaltung geplanter Remoteaufgaben deaktiviert ist, wird der Task nicht deaktiviert, wenn er aus einer Taskplaner 2.0-API gelesen wird.

 

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_Z_"></span><span id="_z_"></span>**/Z** 
</dt> <dd>

Ein -Wert, der die Aufgabe markiert, die nach der letzten Ausführung gelöscht werden soll.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/DELAY** **delaytime**
</dt> <dd>

Ein -Wert, der die Wartezeit zum Verzögern der Ausführung des Tasks nach dem Auslösen des Triggers angibt. Das Zeitformat ist mmmm:ss. Diese Option ist nur für Aufgaben mit den Zeitplantypen ONSTART, ONLOGON und ONEVENT gültig.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="___"></span>**/?** 
</dt> <dd>

Ein -Wert, der die Hilfemeldung für Schtasks.exe anzeigt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



 

 





