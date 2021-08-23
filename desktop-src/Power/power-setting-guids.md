---
description: GuiDs für Energieeinstellungen identifizieren Energieänderungsereignisse.
ms.assetid: 39D432A7-54F8-4135-B98C-7290F95B054A
title: Energieeinstellungs-GUIDs (WinNT.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b05909509e0c3ed581582ebe90b10e5df4e91a31b7ab050b3fd1ef6679b1a3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887030"
---
# <a name="power-setting-guids"></a>GUIDs für Energieeinstellungen

Die **GUID der Energieeinstellung** identifiziert Energieänderungsereignisse. In diesem Thema werden **guiD-Einstellungen für Benachrichtigungen** aufgeführt, die für Anwendungen am nützlichsten sind. Eine Anwendung sollte sich für jedes Energieänderungsereignis registrieren, das sich auf das Verhalten auswirken kann. Jedes Mal, wenn sich eine Einstellung ändert, wird eine Benachrichtigung gesendet.

Die **GUID-Einstellungen für** Energieeinstellungen werden in WinNT.h definiert.

<dl> <dt>

<span id="GUID_ACDC_POWER_SOURCE"></span><span id="guid_acdc_power_source"></span>**GUID \_ ACDC \_ POWER \_ SOURCE**
</dt> <dd> <dl> <dt>

5D3E9A59-E9D5-4B00-A6BD-FF34FF516548
</dt> <dt>



Die Systemstromquelle wurde geändert. Der **Datenmember** ist ein **DWORD mit** Werten aus der [**SYSTEM POWER \_ \_ CONDITION-Enumeration,**](/windows/desktop/api/WinNT/ne-winnt-system_power_condition) die die aktuelle Stromquelle angibt.

<dl> <dt>

**PoAc** (0): Der Computer wird von einer Netzstromquelle (oder ähnlichem) betrieben, z. B. einem Laptop, der von einem 12-V-Adapter betrieben wird.
</dt> <dt>

**PoDc** (1): Der Computer wird von einer integrierten Akkustromquelle betrieben.
</dt> <dt>

**PoHot** (2): Der Computer wird von einer kurzfristigen Stromquelle wie einem USV-Gerät betrieben.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_BATTERY_PERCENTAGE_REMAINING"></span><span id="guid_battery_percentage_remaining"></span>**VERBLEIBENDER \_ \_ GUID-AKKUPROZENTSATZ \_**
</dt> <dd> <dl> <dt>

A7AD8041-B45A-4CAE-87A3-ABERBB468A9E1
</dt> <dt>



Die verbleibende Akkukapazität wurde geändert. Die Granularität variiert von System zu System, aber die kleinste Granularität beträgt 1 Prozent. Der **Data-Member** ist ein **DWORD-Wert,** der die aktuelle Akkukapazität als Prozentsatz zwischen 0 und 100 angibt.


</dt> </dl> </dd> <dt>

<span id="GUID_CONSOLE_DISPLAY_STATE"></span><span id="guid_console_display_state"></span>**ANZEIGEZUSTAND \_ DER GUID-KONSOLE \_ \_**
</dt> <dd> <dl> <dt>

6FE69556-704A-47A0-8F24-C28D936FDA47
</dt> <dt>



Der Anzeigezustand des aktuellen Monitors hat sich geändert.

**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Benachrichtigung ist ab Windows 8 und Windows Server 2012.

Der **Data-Member** ist ein **DWORD** mit einem der folgenden Werte.

<dl> <dt>

0x0: Die Anzeige ist deaktiviert.
</dt> <dt>

0x1: Die Anzeige ist ein.
</dt> <dt>

0x2: Die Anzeige ist abgeblendet.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_GLOBAL_USER_PRESENCE"></span><span id="guid_global_user_presence"></span>**GLOBALE \_ \_ GUID-BENUTZERERFAHRUNG \_**
</dt> <dd> <dl> <dt>

786E8A1D-B427-4344-9207-09E70BDCBEA9
</dt> <dt>



Der Benutzerstatus, der einer Sitzung zugeordnet ist, wurde geändert. Dies stellt den kombinierten Status der Benutzerpräsenz für alle lokalen und Remotesitzungen im System dar.

Diese Benachrichtigung wird nur an Dienste und andere Programme gesendet, die in Sitzung 0 ausgeführt werden. Benutzermodusanwendungen sollten sich stattdessen für **GUID \_ SESSION USER \_ \_ PRESENCE** registrieren.

**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Benachrichtigung ist ab Windows 8 und Windows Server 2012.

Der **Data-Member** ist ein **DWORD** mit einem der folgenden Werte.

<dl> <dt>

**PowerUserPresent** (0): Der Benutzer ist in jeder lokalen oder Remotesitzung auf dem System vorhanden.
</dt> <dt>

**PowerUserInactive** (2): Der Benutzer ist in einer lokalen oder Remotesitzung auf dem System nicht vorhanden.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_IDLE_BACKGROUND_TASK"></span><span id="guid_idle_background_task"></span>**HINTERGRUNDAUFGABE "GUID \_ IM \_ \_ LEERLAUF"**
</dt> <dd> <dl> <dt>

515C31D8-F734-163D-A0FD-11A08C91E8F1
</dt> <dt>



Das System ist ausgelastet. Dies weist darauf hin, dass das System in naher Zukunft nicht in den Leerlaufzustand über geht und dass die aktuelle Zeit ein guter Zeitpunkt ist, an dem Komponenten Hintergrund- oder Leerlaufaufgaben ausführen können, die andernfalls verhindern würden, dass der Computer in den Leerlaufzustand eintritt.

Es gibt keine Benachrichtigung, wenn das System in den Leerlaufzustand wechseln kann. Die Taskbenachrichtigung im Hintergrund im Leerlauf gibt nicht an, ob ein Benutzer auf dem Computer vorhanden ist. Der **Daten-Member** verfügt über keine Informationen und kann ignoriert werden.


</dt> </dl> </dd> <dt>

<span id="GUID_MONITOR_POWER_ON"></span><span id="guid_monitor_power_on"></span>**\_GUID-MONITOR \_ \_ EIN/EIN**
</dt> <dd> <dl> <dt>

02731015-4510-4526-99E6-E5A17EBD1AEA
</dt> <dt>



Der primäre Systemmonitor wurde ein- oder ausgeschaltet. Diese Benachrichtigung ist nützlich für Komponenten, die Inhalte aktiv auf dem Anzeigegerät rendern, z. B. für die Medienvisualisierung. Diese Anwendungen sollten sich für diese Benachrichtigung registrieren und das Rendern von Grafikinhalten beenden, wenn der Monitor ausgeschaltet ist, um den Energieverbrauch des Systems zu reduzieren. Der **Daten-Member** ist ein **DWORD,** das den aktuellen Monitorstatus angibt.

<dl> <dt>

0x0: Der Monitor ist deaktiviert.
</dt> <dt>

0x1: Der Monitor ist ein.
</dt> </dl>

**Windows 8 und Windows Server 2012:** Neue Anwendungen sollten anstelle **dieser Benachrichtigung \_ GUID CONSOLE \_ DISPLAY \_ STATE** verwenden.

</dl> </dd> <dt>

<span id="GUID_POWER_SAVING_STATUS"></span><span id="guid_power_saving_status"></span>**\_GUID– \_ \_ ENERGIESPARSTATUS**
</dt> <dd> <dl> <dt>

E00958C0-C213-4ACE-AC77-FECCED2EEEA5
</dt> <dt>



Der Akkusparer wurde als Reaktion auf sich ändernde Energiebedingungen aus- oder eingeschaltet. Diese Benachrichtigung ist nützlich für Komponenten, die an der Energieversorgung beteiligt sind. Diese Anwendungen sollten sich für diese Benachrichtigung registrieren und Energie sparen, wenn Stromsparmodus ist.

Der **Data-Member** ist ein **DWORD,das** Stromsparmodus angibt.

<dl> <dt>

0x0: Der Akkusparer ist ausgeschaltet.
</dt> <dt>

0x1: Der Akkusparer ist ein. Sparen Sie nach Möglichkeit Energie.
</dt> </dl>

Allgemeine Informationen zu Stromsparmodus finden Sie unter Stromsparmodus [(in den Richtlinien für Hardwarekomponenten).](/windows-hardware/design/component-guidelines/battery-saver)

</dl> </dd> <dt>

<span id="GUID_POWERSCHEME_PERSONALITY"></span><span id="guid_powerscheme_personality"></span>**\_GUID-FÄHIGKEITENCHEME-PERSÖNLICHKEIT \_**
</dt> <dd> <dl> <dt>

245d8541-3943-4422-b025-13A784F679B7
</dt> <dt>



Die Persönlichkeit des aktiven Energieschemas hat sich geändert. Alle Energieschemas sind einer dieser Persönlichkeiten zuordnen. Der **Daten-Member** ist eine **GUID,** die die neue Persönlichkeit des aktiven Energieschemas angibt.

<dl> <dt>



**GUID \_ \_ \_ MINDESTLEISTUNGSEINSPARUNGEN** (8C5E7FDA-E8BF-4A96-9A85-A6E23A8C635C)

Hohe Leistung: Das Schema ist so konzipiert, dass es eine maximale Leistung auf Kosten von Einsparungen beim Stromverbrauch erzielt.


</dt> <dt>



**GUID \_ MAXIMALE \_ \_ ENERGIEEINSPARUNGEN** (A1841308-3541-4FAB-BC81-F71556F20B4A)

Power Saver: Das Schema ist so konzipiert, dass es maximale Einsparungen beim Stromverbrauch auf Kosten der Systemleistung und Reaktionsfähigkeit ermöglicht.


</dt> <dt>



**GUID \_ TYPISCHE \_ \_ ENERGIEEINSPARUNGEN** (381B4222-F694-41F0-9685-FF5BB260DF2E)

Automatisch: Das Schema ist so konzipiert, dass leistungs- und energieverbrauchsbasierte Einsparungen automatisch ausgeglichen werden.


</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_SESSION_DISPLAY_STATUS"></span><span id="guid_session_display_status"></span>**ANZEIGESTATUS \_ DER GUID-SITZUNG \_ \_**
</dt> <dd> <dl> <dt>

2B84C20E-AD23-4ddf-93DB-05FFBD7EFCA5
</dt> <dt>



Die anzeige, die der Sitzung der Anwendung zugeordnet ist, wurde ein- oder ausgeschaltet.

**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Benachrichtigung ist ab Windows 8 und Windows Server 2012.

Diese Benachrichtigung wird nur an Benutzermodusanwendungen gesendet. Dienste und andere Programme, die in Sitzung 0 ausgeführt werden, erhalten diese Benachrichtigung nicht. Der **Data-Member** ist ein **DWORD** mit einem der folgenden Werte.

<dl> <dt>

0x0: Die Anzeige ist deaktiviert.
</dt> <dt>

0x1: Die Anzeige ist ein.
</dt> <dt>

0x2: Die Anzeige ist abgeblendet.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_SESSION_USER_PRESENCE"></span><span id="guid_session_user_presence"></span>**GUID \_ SESSION \_ USER \_ PRESENCE**
</dt> <dd> <dl> <dt>

3C0F4548-C03F-4c4d-B9F2-237EDE686376
</dt> <dt>



Der der Sitzung der Anwendung zugeordnete Benutzerstatus hat sich geändert.

**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Benachrichtigung ist ab Windows 8 und Windows Server 2012.

Diese Benachrichtigung wird nur an Benutzermodusanwendungen gesendet, die in einer interaktiven Sitzung ausgeführt werden. Dienste und andere Programme, die in Sitzung 0 ausgeführt werden, sollten sich für **GUID \_ GLOBAL USER \_ PRESENCE \_ registrieren.** Der **Data-Member** ist ein **DWORD** mit einem der folgenden Werte.

<dl> <dt>

**PowerUserPresent** (0): Der Benutzer stellt Eingaben für die Sitzung zur Verfügung.
</dt> <dt>

**PowerUserInactive** (2): Das Timeout der Benutzeraktivität ist ohne Interaktion des Benutzers verstrichen.
</dt> </dl>

> [!Note]  
> Alle Anwendungen, die in einer interaktiven Benutzermodussitzung ausgeführt werden, sollten diese Einstellung verwenden. Wenn sich Kernelmodusanwendungen für den Monitorstatus registrieren, sollten sie stattdessen **GUID \_ CONSOLE DISPLAY \_ \_ STATUS** verwenden.

 

</dl> </dd> <dt>

<span id="GUID_SYSTEM_AWAYMODE"></span><span id="guid_system_awaymode"></span>**GUID \_ SYSTEM \_ AWAYMODE**
</dt> <dd> <dl> <dt>

98A7F580-01F7-48AA-9C0F-44352C29E5C0
</dt> <dt>



Das System wird in den oder aus dem Modus entfernt. Der **Data-Member** ist ein **DWORD,** das den aktuellen Status des Weg-Modus angibt.

<dl> <dt>

0x0: Der Computer wird beendet.
</dt> <dt>

0x1: Der Computer geht in den Modus "Weg".
</dt> </dl>

</dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WinNT.h</dt> </dl> |



 

