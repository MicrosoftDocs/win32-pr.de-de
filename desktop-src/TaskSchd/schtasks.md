---
title: Schtasks.exe
description: Ermöglicht es einem Administrator, geplante Aufgaben auf einem lokalen Computer oder einem Remote Computer zu erstellen, zu löschen, abzufragen, zu ändern, auszuführen und zu beenden.
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
ms.openlocfilehash: 1c9ba2c13053a8c550128f5d66623b5eed3a9dec
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314633"
---
# <a name="schtasksexe"></a>Schtasks.exe

Ermöglicht es einem Administrator, geplante Aufgaben auf einem lokalen Computer oder einem Remote Computer zu erstellen, zu löschen, abzufragen, zu ändern, auszuführen und zu beenden. Wenn Sie Schtasks.exe ohne Argumente ausführen, werden der Status und die nächste Laufzeit für jede registrierte Aufgabe angezeigt. 

Weitere Informationen zu Taskplaner finden Sie in der folgenden Einführung: [Taskplaner für Entwickler](task-scheduler-start-page.md).

## <a name="creating-a-task"></a>Erstellen einer Aufgabe

Die folgende Syntax wird verwendet, um eine Aufgabe auf dem lokalen Computer oder dem Remote Computer zu erstellen.

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

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** - **System**
</dt> <dd>

Ein-Wert, der den Remote Computer für die Verbindung angibt. Wenn kein Wert angegeben wird, wird der Systemparameter standardmäßig auf dem lokalen Computer verwendet.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **Benutzername**
</dt> <dd>

Ein-Wert, der den Benutzer Kontext angibt, unter dem Schtasks.exe ausgeführt werden soll.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ Kennwort \]**
</dt> <dd>

Ein-Wert, der das Kennwort für einen angegebenen Benutzer Kontext angibt. Wenn die Angabe ausgelassen wird, fordert Schtasks.exe den Benutzer zur Eingabe auf.

</dd> <dt>

<span id="_RU_username"></span><span id="_ru_username"></span><span id="_RU_USERNAME"></span>**/Ru** **Benutzername**
</dt> <dd>

Ein-Wert, der den Benutzer Kontext angibt, unter dem die Aufgabe ausgeführt wird. Gültige Werte für das Systemkonto sind "", "NT Authority \\ System" oder "System". Bei Taskplaner 2,0-Tasks sind auch "NT Authority \\ LocalService" und "NT Authority \\ Network Service" gültige Werte.

</dd> <dt>

<span id="_RP__password_"></span><span id="_rp__password_"></span><span id="_RP__PASSWORD_"></span>**/RP aus** **\[ Kennwort \]**
</dt> <dd>

Ein-Wert, der das Kennwort für den mit dem/ru-Parameter angegebenen Benutzer angibt. Um zur Eingabe des Kennworts aufzufordern, muss der Wert entweder " \* " oder kein Wert sein. Dieses Kennwort wird für das Systemkonto ignoriert. Dieser Parameter muss entweder mit/ru oder mit dem/XML-Schalter kombiniert werden.

</dd> <dt>

<span id="_SC_schedule"></span><span id="_sc_schedule"></span><span id="_SC_SCHEDULE"></span>**/SC** 
</dt> <dd>

Ein-Wert, der die Zeit Plan Häufigkeit angibt. Gültige Werte sind: Minute, stündlich, täglich, wöchentlich, monatlich, einmal, onlogon, OnIdle und OnEvent.

</dd> <dt>

<span id="_MO_modifier"></span><span id="_mo_modifier"></span><span id="_MO_MODIFIER"></span>**/Monat** - **Modifizierer**
</dt> <dd>

Ein Wert, der den Zeit Plantyp verfeinert, um eine präzisere Steuerung der Zeit Plan Wiederholung zu ermöglichen. Gültige Werte sind:

-   Minute: 1-1439 Minuten.
-   Stündlich: 1-23 Stunden.
-   Täglich: 1-365 Tage.
-   Wöchentlich: 1-52.
-   Once: keine Modifizierer.
-   OnStart: keine Modifizierer.
-   Onlogon: keine Modifizierer.
-   OnIdle: keine Modifizierer.
-   Monatlich: 1-12 oder erster, zweiter, Dritter, Vierter, letzter und Nachname.
-   OnEvent: XPath-Ereignis Abfrage Zeichenfolge.

</dd> <dt>

<span id="_D_days"></span><span id="_d_days"></span><span id="_D_DAYS"></span>**/D** **Tage**
</dt> <dd>

Ein-Wert, der den Wochentag angibt, an dem die Aufgabe ausgeführt werden soll. Gültige Werte sind Mon, di, Wed, Do, Fri, Sat, Sun und für monatliche Zeitpläne 1-31 (Tage des Monats) Das Platzhalter Zeichen ( \* ) gibt alle Tage an.

</dd> <dt>

<span id="_M_months"></span><span id="_m_months"></span><span id="_M_MONTHS"></span>**/M** **Monate**
</dt> <dd>

Ein-Wert, der Monate des Jahres angibt. Der Standardwert ist der erste Tag des Monats. Gültige Werte sind: Jan, Feb, Mar, Apr, May, Jun, Jul, Aug, Sep, Oct, Nov und Dec. Das Platzhalter Zeichen ( \* ) gibt alle Monate an.

</dd> <dt>

<span id="_I_idletime"></span><span id="_i_idletime"></span><span id="_I_IDLETIME"></span>**/I** **IdleTime**
</dt> <dd>

Ein-Wert, der den Zeitraum angibt, der vor dem Ausführen einer geplanten OnIdle-Aufgabe gewartet werden soll. Der gültige Bereich ist 1-999 Minuten.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **Taskname**
</dt> <dd>

Ein-Wert, der einen Namen angibt, der die geplante Aufgabe eindeutig identifiziert.

</dd> <dt>

<span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **taskrun**
</dt> <dd>

Ein-Wert, der den Pfad und den Dateinamen der Aufgabe angibt, die zum geplanten Zeitpunkt ausgeführt werden soll. Beispiel: C: \\ Windows \\ system32 \\calc.exe.

</dd> <dt>

<span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/St** **StartTime**
</dt> <dd>

Ein-Wert, der die Startzeit zum Ausführen der Aufgabe angibt. Das Zeitformat ist hh: mm (24-Stunden-Zeit). 14:30 gibt beispielsweise 2:30Uhr an. Der Standardwert ist die aktuelle Uhrzeit, an der/St nicht angegeben ist. Diese Option ist für das/SC Once-Argument erforderlich.

</dd> <dt>

<span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** - **Intervall**
</dt> <dd>

Ein-Wert, der das Wiederholungsintervall in Minuten angibt. Dies gilt nicht für die folgenden Zeit Plan Typen: Minute, stündlich, OnStart, onlogon, OnIdle und OnEvent. Der gültige Bereich ist 1-599940 Minuten. Wenn entweder der/et-Parameter oder der/du-Parameter angegeben wird, beträgt der Standardwert 10 Minuten.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/Et** **EndTime**
</dt> <dd>

Ein-Wert, der die Endzeit angibt, zu der die Aufgabe ausgeführt werden soll. Das Zeitformat ist hh: mm (24-Stunden-Zeit). 14:50 gibt beispielsweise 2:50uhr an. Dies gilt nicht für die folgenden Zeit Plan Typen: OnStart, onlogon, OnIdle und OnEvent.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/Du** - **Dauer**
</dt> <dd>

Ein-Wert, der die Dauer angibt, mit der der Task ausgeführt wird. Das Zeitformat ist hh: mm (24-Stunden-Zeit). 14:50 gibt beispielsweise 2:50uhr an. Dies gilt nicht für/et und für die folgenden Zeit Plan Typen: OnStart, onlogon, OnIdle und OnEvent. Bei/v1-Aufgaben (Taskplaner 1,0-Tasks), wenn/RI angegeben wird, ist der Standardwert für die Dauer 1 Stunde.

**Windows XP:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_K_"></span><span id="_k_"></span>**/K** 
</dt> <dd>

Ein-Wert, der die Aufgabe zum Endzeit-oder Dauer Zeitpunkt beendet. Dies gilt nicht für die folgenden Zeit Plan Typen: OnStart, onlogon, OnIdle und OnEvent. Es muss entweder/et oder/du angegeben werden.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **StartDate**
</dt> <dd>

Ein-Wert, der das erste Datum angibt, an dem die Aufgabe ausgeführt werden soll. Das Format ist "mm/dd/yyyy". Dieser Wert wird standardmäßig auf das aktuelle Datum eingestellt. Dies gilt nicht für die folgenden Zeit Plan Typen: Once, OnStart, onlogon, OnIdle und OnEvent.

</dd> <dt>

<span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/Ed** **EndDate**
</dt> <dd>

Ein-Wert, der das letzte Datum angibt, an dem die Aufgabe ausgeführt wird. Das Format ist "mm/dd/yyyy". Dies gilt nicht für die folgenden Zeit Plan Typen: Once, OnStart, onlogon, OnIdle und OnEvent.

</dd> <dt>

<span id="_EC_ChannelName"></span><span id="_ec_channelname"></span><span id="_EC_CHANNELNAME"></span>**/EC** **ChannelName**
</dt> <dd>

Ein-Wert, der den Ereignis Kanal für OnEvent-Trigger angibt.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_IT_"></span><span id="_it_"></span>**/IT** 
</dt> <dd>

Ein Wert, mit dem die Aufgabe interaktiv ausgeführt werden kann, wenn der/ru-Benutzer zurzeit beim Ausführen der Aufgabe angemeldet ist. Der Task wird nur ausgeführt, wenn der Benutzer angemeldet ist.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_NP_"></span><span id="_np_"></span>**/NP** 
</dt> <dd>

Ein Wert, der angibt, dass kein Kennwort gespeichert wird. Der Task wird nicht interaktiv als der angegebene Benutzer ausgeführt. Es sind nur lokale Ressourcen verfügbar.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_Z_"></span><span id="_z_"></span>**"/Z** 
</dt> <dd>

Ein-Wert, der die Aufgabe kennzeichnet, die nach der letzten Ausführung gelöscht werden soll.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_XML_xmlfile"></span><span id="_xml_xmlfile"></span><span id="_XML_XMLFILE"></span>**/XML** **xmlfile**
</dt> <dd>

Ein-Wert, der eine Aufgabe aus einer XML-Datei erstellt. Dieser Parameter kann mit/ru-und/RP aus-Switches oder mit dem/RP aus-Switch allein kombiniert werden, wenn die Task-XML bereits den Prinzipal enthält.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_V1_"></span><span id="_v1_"></span>**/V1** 
</dt> <dd>

Ein Wert, der eine Aufgabe erstellt, die für die Plattformen Windows 2000, Windows Server 2003 und Windows XP sichtbar ist.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_F_"></span><span id="_f_"></span>**/F** 
</dt> <dd>

Ein Wert, der die Aufgabe erzwungen erstellt und Warnungen unterdrückt, wenn die angegebene Aufgabe bereits vorhanden ist.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span>**/RL** - **Ebene**
</dt> <dd>

Ein-Wert, der die Ausführungs Ebene für die Aufgabe festlegt. Gültige Werte sind Limited und höchste. Der Standardwert ist "Limited".

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/Delay** **Delta Time**
</dt> <dd>

Ein-Wert, der die Wartezeit angibt, nach der der Task nach dem Auslösen des Auslösers verzögert wird. Das Zeitformat ist mmmm: SS. Diese Option ist nur für die Zeit Plan Typen OnStart, onlogon und OnEvent gültig.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="___"></span>**/?** 
</dt> <dd>

Ein-Wert, der die Hilfe Meldung für Schtasks.exe anzeigt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie beim Erstellen einer Aufgabe auf einem Remote Computer, auf dem das Betriebssystem Windows XP, Windows Server 2003 oder Windows 2000 ausgeführt wird, den/v1-Schalter.

Sie können keine nicht interaktive Remote Taskplaner 1,0-Aufgabe erstellen (erstellen Sie einen Task, indem Sie den Schalter/IT nicht verwenden, und verwenden Sie den Schalter/v1), wenn auf dem Remote Computer die Firewallausnahme für Datei-und Druckerfreigabe aktiviert ist und die Firewallausnahme für die Remote Verwaltung geplanter Tasks deaktiviert ist.

## <a name="deleting-a-task"></a>Löschen einer Aufgabe

Die folgende Syntax wird verwendet, um eine oder mehrere geplante Tasks zu löschen.

``` syntax
schtasks /Delete 
[/S system [/U username [/P [password]]]]
[/TN taskname] [/F]
```

### <a name="parameters"></a>Parameter

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** - **System**
</dt> <dd>

Ein-Wert, der den Remote Computer für die Verbindung angibt. Wenn kein Wert angegeben wird, wird der Systemparameter standardmäßig auf dem lokalen Computer verwendet.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **Benutzername**
</dt> <dd>

Ein-Wert, der den Benutzer Kontext angibt, unter dem Schtasks.exe ausgeführt werden soll.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ Kennwort \]**
</dt> <dd>

Ein-Wert, der das Kennwort für den angegebenen Benutzer Kontext angibt. Wenn die Angabe ausgelassen wird, fordert Schtasks.exe den Benutzer zur Eingabe auf.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **Taskname**
</dt> <dd>

Ein-Wert, der den Namen der zu löschenden geplanten Aufgabe angibt. Das Platzhalter Zeichen ( \* ) kann verwendet werden, um alle Aufgaben zu löschen.

</dd> <dt>

<span id="_F_"></span><span id="_f_"></span>**/F** 
</dt> <dd>

Ein Wert, der die Aufgabe erzwungen und Warnungen unterdrückt, wenn die angegebene Aufgabe ausgeführt wird.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Ein-Wert, der die Hilfe für Schtasks.exe anzeigt.

</dd> </dl>

## <a name="running-a-task"></a>Ausführen einer Aufgabe

Die folgende Syntax wird verwendet, um eine geplante Aufgabe sofort auszuführen.

``` syntax
schtasks /Run 
[/S system [/U username [/P [password]]]]
/TN taskname
```

### <a name="parameters"></a>Parameter

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** - **System**
</dt> <dd>

Ein-Wert, der den Remote Computer für die Verbindung angibt. Wenn kein Wert angegeben wird, wird der Systemparameter standardmäßig auf dem lokalen Computer verwendet.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **Benutzername**
</dt> <dd>

Ein-Wert, der den Benutzer Kontext angibt, unter dem Schtasks.exe ausgeführt werden soll.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ Kennwort \]**
</dt> <dd>

Ein-Wert, der das Kennwort für den angegebenen Benutzer Kontext angibt. Wenn die Angabe ausgelassen wird, fordert Schtasks.exe den Benutzer zur Eingabe auf.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **Taskname**
</dt> <dd>

Ein-Wert, der den Namen des geplanten Tasks angibt, der ausgeführt werden soll.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Ein-Wert, der die Hilfe für Schtasks.exe anzeigt.

</dd> </dl>

## <a name="ending-a-running-task"></a>Beenden einer laufenden Aufgabe

Die folgende Syntax wird verwendet, um eine laufende geplante Aufgabe zu verhindern.

> [!Note]  
> Um das Ausführen einer Remote Aufgabe zu verhindern, stellen Sie sicher, dass der Remote Computer über die Datei-und Druckerfreigabe und die Verwaltung von Firewallausnahmen für Remote geplante Tasks verfügt.

 

``` syntax
schtasks /End 
[/S system [/U username [/P [password]]]]
/TN taskname
```

### <a name="parameters"></a>Parameter

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** - **System**
</dt> <dd>

Ein-Wert, der den Remote Computer für die Verbindung angibt. Wenn kein Wert angegeben wird, wird der Systemparameter standardmäßig auf dem lokalen Computer verwendet.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **Benutzername**
</dt> <dd>

Ein-Wert, der den Benutzer Kontext angibt, unter dem Schtasks.exe ausgeführt werden soll.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ Kennwort \]**
</dt> <dd>

Ein-Wert, der das Kennwort für den angegebenen Benutzer Kontext angibt. Wenn die Angabe ausgelassen wird, fordert Schtasks.exe den Benutzer zur Eingabe auf.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **Taskname**
</dt> <dd>

Ein-Wert, der den Namen der geplanten Aufgabe angibt, die beendet werden soll.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Ein-Wert, der die Hilfe für Schtasks.exe anzeigt.

</dd> </dl>

## <a name="querying-for-task-information"></a>Abfragen von Task Informationen

Die folgende Syntax wird verwendet, um die geplanten Tasks auf dem lokalen Computer oder dem Remote Computer anzuzeigen.

``` syntax
schtasks /Query 
[/S system [/U username [/P [password]]]]
[/FO format | /XML] [/NH] [/V] [/TN taskname] [/?]
```

### <a name="parameters"></a>Parameter

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** - **System**
</dt> <dd>

Ein-Wert, der den Remote Computer für die Verbindung angibt. Wenn kein Wert angegeben wird, wird der Systemparameter standardmäßig auf dem lokalen Computer verwendet.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **Benutzername**
</dt> <dd>

Ein-Wert, der den Benutzer Kontext angibt, unter dem Schtasks.exe ausgeführt werden soll.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ Kennwort \]**
</dt> <dd>

Ein-Wert, der das Kennwort für den angegebenen Benutzer Kontext angibt. Wenn die Angabe ausgelassen wird, fordert Schtasks.exe den Benutzer zur Eingabe auf.

</dd> <dt>

<span id="_FO_format"></span><span id="_fo_format"></span><span id="_FO_FORMAT"></span>**/FO** - **Format**
</dt> <dd>

Ein-Wert, der das Ausgabeformat angibt. Gültige Werte sind "Table", "List" und "CSV".

</dd> <dt>

<span id="_NH_"></span><span id="_nh_"></span>**/NH** 
</dt> <dd>

Ein-Wert, der angibt, dass der Spaltenheader nicht in der Ausgabe angezeigt werden soll. Dies gilt nur für Tabellen-und CSV-Formate.

</dd> <dt>

<span id="_V_"></span><span id="_v_"></span>**/V** 
</dt> <dd>

Ein-Wert, der ausführliche Task Ausgaben anzeigt.

> [!Note]  
> Wenn für eine Aufgabe nur ein einziges Mal ausgeführt werden soll, sind die angezeigten Zeit Plan Informationen "Zeit Plan Daten sind in diesem Format nicht verfügbar".

 

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **Taskname**
</dt> <dd>

Ein-Wert, der den Aufgaben Namen angibt, für den die Informationen abgerufen werden sollen. Wenn kein Aufgaben Name angegeben ist, werden Informationen zu allen Aufgaben angezeigt.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_XML_"></span><span id="_xml_"></span>**/XML** 
</dt> <dd>

Ein-Wert, der verwendet wird, um die Aufgaben Definitionen im XML-Format anzuzeigen.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Ein-Wert, der verwendet wird, um die Hilfe für Schtasks.exe anzuzeigen.

</dd> </dl>

## <a name="changing-a-task"></a>Ändern einer Aufgabe

Die folgende Syntax wird verwendet, um die Ausführung des Programms zu ändern oder um das von einer geplanten Aufgabe verwendete Benutzerkonto und Kennwort zu ändern.

``` syntax
schtasks /Change 
[/S system [/U username [/P [password]]]] /TN taskname
{ [/RU runasuser] [/RP runaspassword] [/TR taskrun] [/ST starttime] 
[/RI interval] [ {/ET endtime | /DU duration} [/K] ]
[/SD startdate] [/ED enddate] [/ENABLE | /DISABLE] [/IT] [/Z] }
```

### <a name="parameters"></a>Parameter

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** - **System**
</dt> <dd>

Ein-Wert, der den Remote Computer für die Verbindung angibt. Wenn kein Wert angegeben wird, wird der Systemparameter standardmäßig auf dem lokalen Computer verwendet.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **Benutzername**
</dt> <dd>

Ein-Wert, der den Benutzer Kontext angibt, unter dem Schtasks.exe ausgeführt werden soll.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ Kennwort \]**
</dt> <dd>

Ein-Wert, der das Kennwort für den angegebenen Benutzer Kontext angibt. Wenn die Angabe ausgelassen wird, fordert Schtasks.exe den Benutzer zur Eingabe auf.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **Taskname**
</dt> <dd>

Ein-Wert, der angibt, welche geplante Aufgabe geändert werden soll.

</dd> <dt>

<span id="_RU_runasuser"></span><span id="_ru_runasuser"></span><span id="_RU_RUNASUSER"></span>**/Ru** **RunAsUser**
</dt> <dd>

Ein-Wert, der den Benutzernamen (Benutzer Kontext) ändert, unter dem die geplante Aufgabe ausgeführt wird. Gültige Werte für das Systemkonto sind "", "NT Authority \\ System" oder "System". Bei Taskplaner 2,0-Tasks sind auch "NT Authority \\ LocalService" und "NT Authority \\ Network Service" gültige Werte.

</dd> <dt>

<span id="_RP_runaspassword"></span><span id="_rp_runaspassword"></span><span id="_RP_RUNASPASSWORD"></span>**/RP aus** **runaspassword**
</dt> <dd>

Ein-Wert, der ein neues Kennwort für den vorhandenen Benutzer Kontext oder das Kennwort für ein neues Benutzerkonto angibt. Dieses Kennwort wird für das Systemkonto ignoriert.

</dd> <dt>

<span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **taskrun**
</dt> <dd>

Ein-Wert, der ein neues Programm angibt, das vom Task ausgeführt wird.

</dd> <dt>

<span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/St** **StartTime**
</dt> <dd>

Ein-Wert, der die Startzeit zum Ausführen der Aufgabe angibt. Das Zeitformat ist hh: mm (24-Stunden-Zeit). 14:30 gibt beispielsweise 2:30Uhr an.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** - **Intervall**
</dt> <dd>

Ein-Wert, der das Wiederholungsintervall in Minuten angibt. Der gültige Bereich ist 1-599940 Minuten.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/Et** **EndTime**
</dt> <dd>

Ein-Wert, der die Endzeit der Aufgabe angibt. Das Zeitformat ist hh: mm (24-Stunden-Zeit). 14:50 gibt beispielsweise 2:50uhr an.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/Du** - **Dauer**
</dt> <dd>

Ein-Wert, der die Dauer angibt, mit der der Task ausgeführt wird. Das Zeitformat ist hh: mm (24-Stunden-Zeit). 14:50 gibt beispielsweise 2:50uhr an. Dies gilt nicht für den/et-Parameter.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_K_"></span><span id="_k_"></span>**/K** 
</dt> <dd>

Ein-Wert, der die Aufgabe zum Endzeit-oder Dauer Zeitpunkt beendet.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **StartDate**
</dt> <dd>

Ein-Wert, der das erste Datum angibt, an dem die Aufgabe ausgeführt werden soll. Das Format ist "mm/dd/yyyy".

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/Ed** **EndDate**
</dt> <dd>

Ein-Wert, der das letzte Datum angibt, an dem die Aufgabe ausgeführt wird. Das Format ist "mm/dd/yyyy".

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_IT_"></span><span id="_it_"></span>**/IT** 
</dt> <dd>

Ein Wert, mit dem die Aufgabe interaktiv ausgeführt werden kann, wenn der/ru-Benutzer zurzeit beim Ausführen der Aufgabe angemeldet ist. Der Task wird nur ausgeführt, wenn der Benutzer angemeldet ist.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span>**/RL** - **Ebene**
</dt> <dd>

Ein-Wert, der die Ausführungs Ebene für die Aufgabe festlegt. Gültige Werte sind Limited und höchste.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_ENABLE_"></span><span id="_enable_"></span>**/ENABLE** 
</dt> <dd>

Ein-Wert, der die geplante Aufgabe ermöglicht. Eine aktivierte Aufgabe kann ausgeführt werden, und eine deaktivierte Aufgabe kann nicht ausgeführt werden.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_DISABLE_"></span><span id="_disable_"></span>**/Disable** 
</dt> <dd>

Ein-Wert, der die Ausführung der geplanten Aufgabe deaktiviert.

> [!Note]  
> Wenn eine Remote Taskplaner 1,0-Aufgabe durch Schtasks.exe deaktiviert wird und auf dem Remote Computer die Firewallausnahme für Datei-und Druckerfreigabe aktiviert ist und die Firewallausnahme für die Remote Verwaltung geplanter Tasks deaktiviert ist, wird die Aufgabe beim Lesen aus einer Taskplaner 2,0-API nicht deaktiviert.

 

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_Z_"></span><span id="_z_"></span>**"/Z** 
</dt> <dd>

Ein-Wert, der die Aufgabe kennzeichnet, die nach der letzten Ausführung gelöscht werden soll.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/Delay** **Delta Time**
</dt> <dd>

Ein-Wert, der die Wartezeit angibt, nach der die Ausführung der Aufgabe nach dem Auslösen des Auslösers verzögert wird. Das Zeitformat ist mmmm: SS. Diese Option ist nur für Tasks mit den Zeit Plan Typen OnStart, onlogon und OnEvent gültig.

**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.

</dd> <dt>

<span id="___"></span>**/?** 
</dt> <dd>

Ein-Wert, der die Hilfe Meldung für Schtasks.exe anzeigt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



 

 





