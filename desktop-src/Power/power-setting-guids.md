---
description: Mit Energie Einstellungs-GUIDs werden Energie Änderungs Ereignisse identifiziert.
ms.assetid: 39D432A7-54F8-4135-B98C-7290F95B054A
title: Energie Einstellungs-GUIDs (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67dfd619d93f4318dbcfe2b44b5f8ba24460bd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354778"
---
# <a name="power-setting-guids"></a>Energie Einstellungs-GUIDs

Mit der Energie Einstellungs- **GUID** s werden Strom Änderungs Ereignisse identifiziert. In diesem Thema werden die Energie Einstellungs- **GUID** s für Benachrichtigungen aufgelistet, die für-Anwendungen am nützlichsten sind. Eine Anwendung sollte für jedes Strom Änderungs Ereignis registriert werden, das sich auf das Verhalten auswirken könnte. Die Benachrichtigung wird jedes Mal gesendet, wenn eine Einstellung geändert wird.

Die Energie Einstellungs- **GUID** s sind in "Winnt. h" definiert.

<dl> <dt>

<span id="GUID_ACDC_POWER_SOURCE"></span><span id="guid_acdc_power_source"></span>**GUID- \_ ACDC- \_ Strom \_ Quelle**
</dt> <dd> <dl> <dt>

5d3e9a59-e9d5-4b00-a6bd-ff34ff516548
</dt> <dt>



Die Stromquelle des Systems hat sich geändert. Der **Datenmember** ist ein **DWORD** mit Werten aus der [**\_ systemstrombedingungs \_**](/windows/desktop/api/WinNT/ne-winnt-system_power_condition) -Enumeration, die die aktuelle Stromquelle angibt.

<dl> <dt>

**POAC** (0): der Computer wird durch eine Stromversorgung der Stromversorgung (oder ähnliches, z. b. durch einen 12-v-Auto Mobil Adapter) betrieben.
</dt> <dt>

**PODC** (1): der Computer wird durch eine Stromquelle für den Akku Betrieb betrieben.
</dt> <dt>

**Pohot** (2): der Computer wird durch eine kurzfristige Stromquelle, z. b. ein UPS-Gerät, betrieben.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_BATTERY_PERCENTAGE_REMAINING"></span><span id="guid_battery_percentage_remaining"></span>**\_ \_ verbleibender GUID-Akku Anteil \_**
</dt> <dd> <dl> <dt>

A7AD8041-B45A-4CAE-87A3-EECBB468A9E1
</dt> <dt>



Die verbleibende Akkukapazität hat sich geändert. Die Granularität variiert von System zu System, die feinste Granularität ist jedoch 1 Prozent. Der **Datenmember** ist ein **DWORD** , das die aktuelle Akkukapazität angibt, die als Prozentsatz zwischen 0 und 100 verbleiben.


</dt> </dl> </dd> <dt>

<span id="GUID_CONSOLE_DISPLAY_STATE"></span><span id="guid_console_display_state"></span>**\_ \_ Anzeige \_ Status der GUID-Konsole**
</dt> <dd> <dl> <dt>

6fe69556-704A-47a0-8F 24-c28d936fida47
</dt> <dt>



Der Anzeige Zustand des aktuellen Monitors hat sich geändert.

**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Benachrichtigung ist ab Windows 8 und Windows Server 2012 verfügbar.

Der **Datenmember** ist ein **DWORD** mit einem der folgenden Werte.

<dl> <dt>

0x0-die Anzeige ist deaktiviert.
</dt> <dt>

0x1-die Anzeige ist on.
</dt> <dt>

0x2-die Anzeige ist abgedimmt.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_GLOBAL_USER_PRESENCE"></span><span id="guid_global_user_presence"></span>**globale GUID- \_ \_ Benutzer \_ Präsenz**
</dt> <dd> <dl> <dt>

786e8a1d-B427-4344-9207-09e70bdcbea9
</dt> <dt>



Der Benutzer Status, der einer Sitzung zugeordnet ist, wurde geändert. Dies stellt den kombinierten Status der Benutzer Präsenz in allen lokalen und Remote Sitzungen des Systems dar.

Dieser Benachrichtigung werden nur Dienste und andere Programme, die in Sitzung 0 ausgeführt werden, gesendet. Benutzermodusanwendungen sollten sich stattdessen für die **\_ \_ Benutzer \_ Präsenz der GUID-Sitzung** registrieren.

**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Benachrichtigung ist ab Windows 8 und Windows Server 2012 verfügbar.

Der **Datenmember** ist ein **DWORD** mit einem der folgenden Werte.

<dl> <dt>

**Poweruserpresent** (0): der Benutzer ist in einer lokalen oder Remote Sitzung auf dem System vorhanden.
</dt> <dt>

**Poweruserinaktiv** (2): der Benutzer ist in keiner lokalen oder Remote Sitzung auf dem System vorhanden.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_IDLE_BACKGROUND_TASK"></span><span id="guid_idle_background_task"></span>**GUID \_ - \_ Hintergrund \_ Aufgabe im Leerlauf**
</dt> <dd> <dl> <dt>

515c31d8-f 734-163D-a0ld-11a08c91e8f 1
</dt> <dt>



Das System ist ausgelastet. Dies weist darauf hin, dass das System in naher Zukunft nicht in den Leerlauf wechselt und dass die aktuelle Zeit für Komponenten zum Ausführen von Hintergrund-oder Leerlauf Aufgaben geeignet ist, die andernfalls verhindern, dass der Computer in den Leerlauf wechselt.

Es gibt keine Benachrichtigung, wenn sich das System in den Leerlauf versetzen kann. Die Benachrichtigung im Hintergrund des Hintergrund Tasks gibt nicht an, ob ein Benutzer auf dem Computer vorhanden ist. Der **Datenmember** weist keine Informationen auf und kann ignoriert werden.


</dt> </dl> </dd> <dt>

<span id="GUID_MONITOR_POWER_ON"></span><span id="guid_monitor_power_on"></span>**\_ \_ Einschalten des GUID-Monitors \_**
</dt> <dd> <dl> <dt>

02731015-4510-4526-99e6-e5a17ebd1aea
</dt> <dt>



Der primäre System Monitor wurde eingeschaltet oder ausgeschaltet. Diese Benachrichtigung ist nützlich für Komponenten, die Inhalte aktiv auf dem Anzeigegerät darstellen, wie z. b. Medien Visualisierung. Diese Anwendungen sollten sich für diese Benachrichtigung registrieren und das Rendering von Grafikinhalten beenden, wenn der Monitor deaktiviert ist, um den Energieverbrauch des Systems zu reduzieren. Der **Datenmember** ist ein **DWORD** , das den aktuellen Monitor Zustand angibt.

<dl> <dt>

0x0-der Monitor ist deaktiviert.
</dt> <dt>

0x1-der Monitor ist on.
</dt> </dl>

**Windows 8 und Windows Server 2012:** In neuen Anwendungen sollte der **\_ \_ Anzeige \_ Zustand der GUID-Konsole** anstelle dieser Benachrichtigung verwendet werden.

</dl> </dd> <dt>

<span id="GUID_POWER_SAVING_STATUS"></span><span id="guid_power_saving_status"></span>**GUID- \_ Energie \_ Spar \_ Status**
</dt> <dd> <dl> <dt>

E00958C0-C213-4ACE-AC77-FECCED2EEEA5
</dt> <dt>



Der Akku Schoner wurde als Reaktion auf veränderliche Energiebedingungen ausgeschaltet oder eingeschaltet. Diese Benachrichtigung ist nützlich für Komponenten, die an der Energieeinsparung beteiligt sind. Diese Anwendungen sollten sich für diese Benachrichtigung registrieren und die Stromversorgung einsparen, wenn der Akku Schoner eingeschaltet ist.

Der **Datenmember** ist ein **DWORD** , das den Akku Zustand angibt.

<dl> <dt>

0x0-Akku Schoner ist deaktiviert.
</dt> <dt>

0x1-Akku Schoner ist eingeschaltet. Sparen Sie nach Möglichkeit Energie.
</dt> </dl>

Allgemeine Informationen zum Akku Schoner finden Sie unter [Batterie Schoner (in den Richtlinien für die Hardwarekomponente)](/windows-hardware/design/component-guidelines/battery-saver).

</dl> </dd> <dt>

<span id="GUID_POWERSCHEME_PERSONALITY"></span><span id="guid_powerscheme_personality"></span>**GUID- \_ powerscheme- \_ Persönlichkeit**
</dt> <dd> <dl> <dt>

245d8541-3943-4422-B025-13a784f 679b7
</dt> <dt>



Die aktive Energie Schema-Persönlichkeit hat sich geändert. Alle Energie Schemas werden einer dieser Persönlichkeiten zugeordnet. Der **Datenmember** ist eine **GUID** , die die neue aktive Energie Schema-Persönlichkeit angibt.

<dl> <dt>



**GUID \_ Minimale \_ Energie \_ Einsparung** (8c5e7f da-e8bf -4a96-9a85-a6e23a8c635c)

Hohe Leistung: das Schema ist darauf ausgelegt, eine maximale Leistung auf Kosten der Stromverbrauchs Einsparungen zu erzielen.


</dt> <dt>



**GUID \_ Maximale \_ Energie \_ Einsparung** (A1841308-3541-4FAB-BC81-F71556F20B4A)

Energiesparmodus: das Schema ist so konzipiert, dass es auf Kosten der Systemleistung und Reaktionsfähigkeit einen maximalen Stromverbrauch ermöglicht.


</dt> <dt>



**GUID \_ Typische \_ Strom \_ Einsparung** (381b4222-f694-41f0-9685-ff5bb260df2e)

Automatisch: das Schema ist so konzipiert, dass die Leistung und der Energieverbrauch automatisch ausgeglichen werden.


</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_SESSION_DISPLAY_STATUS"></span><span id="guid_session_display_status"></span>**\_ \_ Anzeige \_ Status der GUID-Sitzung**
</dt> <dd> <dl> <dt>

2b84 c20e-AD23-4ddf-93dB-05ffbd7efca5
</dt> <dt>



Die Anzeige, die der Sitzung der Anwendung zugeordnet ist, wurde eingeschaltet oder deaktiviert.

**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Benachrichtigung ist ab Windows 8 und Windows Server 2012 verfügbar.

Diese Benachrichtigung wird nur an Benutzermodusanwendungen gesendet. Dienste und andere Programme, die in Sitzung 0 ausgeführt werden, erhalten diese Benachrichtigung nicht. Der **Datenmember** ist ein **DWORD** mit einem der folgenden Werte.

<dl> <dt>

0x0-die Anzeige ist deaktiviert.
</dt> <dt>

0x1-die Anzeige ist on.
</dt> <dt>

0x2-die Anzeige ist abgedimmt.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_SESSION_USER_PRESENCE"></span><span id="guid_session_user_presence"></span>**\_ \_ Benutzer \_ Präsenz in GUID-Sitzung**
</dt> <dd> <dl> <dt>

3c0f 4548-c03f -4c4d-b9f 2-237ede686376
</dt> <dt>



Der Benutzer Status, der der Sitzung der Anwendung zugeordnet ist, wurde geändert.

**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Benachrichtigung ist ab Windows 8 und Windows Server 2012 verfügbar.

Diese Benachrichtigung wird nur an Benutzermodusanwendungen gesendet, die in einer interaktiven Sitzung ausgeführt werden. Dienste und andere Programme, die in Sitzung 0 ausgeführt werden, sollten sich für die **globale GUID- \_ \_ Benutzer \_ Präsenz** registrieren. Der **Datenmember** ist ein **DWORD** mit einem der folgenden Werte.

<dl> <dt>

**Poweruserpresent** (0): der Benutzer stellt Eingaben für die Sitzung bereit.
</dt> <dt>

**Poweruserinaktiv** (2): das Timeout der Benutzeraktivität ist ohne Interaktion mit dem Benutzer abgelaufen.
</dt> </dl>

> [!Note]  
> Diese Einstellung sollte von allen Anwendungen verwendet werden, die in einer interaktiven benutzermodussitzung ausgeführt werden. Wenn kernelmodusanwendungen den Monitor Status registrieren, sollten Sie stattdessen den **\_ \_ Anzeige \_ Status der GUID-Konsole** verwenden.

 

</dl> </dd> <dt>

<span id="GUID_SYSTEM_AWAYMODE"></span><span id="guid_system_awaymode"></span>**GUID- \_ System- \_ awaymode**
</dt> <dd> <dl> <dt>

98a7f 580-017-48aa-9c0f -44352c29e5c0
</dt> <dt>



Das System wechselt in den Modus und verlässt den Modus. Der **Datenmember** ist ein **DWORD** , das den aktuellen Status des entfernten Modus angibt.

<dl> <dt>

0x0-der Computer verlässt den Modus.
</dt> <dt>

0x1-der Computer wechselt in den Modus "entfernt".
</dt> </dl>

</dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WinNT. h</dt> </dl> |



 

