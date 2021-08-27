---
description: Die Ursachencodes für das Herunterfahren werden von den Funktionen ExitWindowsEx und InitiateSystemShutdownEx im dwReason-Parameter verwendet. Vom System werden maximal MAX \_ NUM \_ REASONS-Ursachencodes verarbeitet. MAX \_ NUM REASONS ist in \_ reason.h definiert.
ms.assetid: db1ecee0-40eb-4761-b5d8-9cc3c1c98cdf
title: Ursachencodes für das Herunterfahren des Systems (Reason.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef40cf53afd3abaf261e15f2caba735dea7963ee5b5f19cebc78c63a373962fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073200"
---
# <a name="system-shutdown-reason-codes"></a>Ursachencodes für das Herunterfahren des Systems

Die Ursachencodes für das Herunterfahren werden von den Funktionen [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) und [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) im *dwReason-Parameter* verwendet.

Vom System werden maximal MAX \_ NUM \_ REASONS-Ursachencodes verarbeitet. MAX \_ NUM REASONS ist in \_ reason.h definiert.

Im Folgenden sind die wichtigsten Ursachenflags zu suchen. Sie geben den allgemeinen Problemtyp an.



| Konstante/Wert                                                                                                                                                                                                                                                                                 | BESCHREIBUNG                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SHTDN_REASON_MAJOR_APPLICATION"></span><span id="shtdn_reason_major_application"></span><dl> <dt>**SHTDN \_ REASON \_ MAJOR \_ APPLICATION**</dt> <dt>0x00040000</dt> </dl>             | Anwendungsproblem.<br/>                                                                                                                                      |
| <span id="SHTDN_REASON_MAJOR_HARDWARE"></span><span id="shtdn_reason_major_hardware"></span><dl> <dt>**SHTDN \_ REASON \_ MAJOR \_ HARDWARE**</dt> <dt>0x00010000</dt> </dl>                      | Hardwareproblem.<br/>                                                                                                                                         |
| <span id="SHTDN_REASON_MAJOR_LEGACY_API"></span><span id="shtdn_reason_major_legacy_api"></span><dl> <dt>**SHTDN \_ GRUND: \_ WICHTIGE \_ \_ LEGACY-API-0x00070000**</dt> <dt></dt> </dl>               | Die [**InitiateSystemShutdown-Funktion**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna) wurde anstelle von [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa)verwendet.<br/> |
| <span id="SHTDN_REASON_MAJOR_OPERATINGSYSTEM"></span><span id="shtdn_reason_major_operatingsystem"></span><dl> <dt>**SHTDN \_ GRUND: \_ \_ HAUPTBETRIEBSSYSTEM-0x00020000**</dt> <dt></dt> </dl> | Betriebssystemproblem.<br/>                                                                                                                                 |
| <span id="SHTDN_REASON_MAJOR_OTHER"></span><span id="shtdn_reason_major_other"></span><dl> <dt>**SHTDN \_ REASON \_ MAJOR \_ OTHER**</dt> <dt>0x00000000</dt> </dl>                               | Anderes Problem.<br/>                                                                                                                                            |
| <span id="SHTDN_REASON_MAJOR_POWER"></span><span id="shtdn_reason_major_power"></span><dl> <dt>**SHTDN \_ REASON \_ MAJOR \_ POWER**</dt> <dt>0x00060000</dt> </dl>                               | Stromausfall.<br/>                                                                                                                                          |
| <span id="SHTDN_REASON_MAJOR_SOFTWARE"></span><span id="shtdn_reason_major_software"></span><dl> <dt>**SHTDN \_ REASON \_ MAJOR \_ SOFTWARE**</dt> <dt>0x00030000</dt> </dl>                      | Softwareproblem.<br/>                                                                                                                                         |
| <span id="SHTDN_REASON_MAJOR_SYSTEM"></span><span id="shtdn_reason_major_system"></span><dl> <dt>**SHTDN \_ REASON \_ MAJOR \_ SYSTEM**</dt> <dt>0x00050000</dt> </dl>                            | Systemfehler.<br/>                                                                                                                                         |



Im Folgenden sind die untergeordneten Ursachenflags. Sie ändern das angegebene Hauptgrundflag. Sie können einen beliebigen geringfügigen Grund in Verbindung mit einem beliebigen Hauptgrund verwenden, aber einige Kombinationen sind nicht sinnvoll.



| Konstante/Wert                                                                                                                                                                                                                                                                                                    | BESCHREIBUNG                               |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------|
| <span id="SHTDN_REASON_MINOR_BLUESCREEN"></span><span id="shtdn_reason_minor_bluescreen"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ BLUESCREEN**</dt> <dt>0x0000000F</dt> </dl>                                   | Bluescreen-Absturzereignis.<br/>       |
| <span id="SHTDN_REASON_MINOR_CORDUNPLUGGED"></span><span id="shtdn_reason_minor_cordunplugged"></span><dl> <dt>**SHTDN \_ GRUND \_ FÜR KLEINERE \_ CORDUNPLUGGED-0x0000000b**</dt> <dt></dt> </dl>                          | Unplugged.<br/>                     |
| <span id="SHTDN_REASON_MINOR_DISK"></span><span id="shtdn_reason_minor_disk"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ DISK**</dt> <dt>0x00000007</dt> </dl>                                                     | auswählen.<br/>                          |
| <span id="SHTDN_REASON_MINOR_ENVIRONMENT"></span><span id="shtdn_reason_minor_environment"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ ENVIRONMENT**</dt> <dt>0x0000000c</dt> </dl>                                | Umgebung.<br/>                   |
| <span id="SHTDN_REASON_MINOR_HARDWARE_DRIVER"></span><span id="shtdn_reason_minor_hardware_driver"></span><dl> <dt>**SHTDN \_ GRUND \_ FÜR KLEINERE \_ \_ HARDWARETREIBER-0x0000000d**</dt> <dt></dt> </dl>                   | Treiber.<br/>                        |
| <span id="SHTDN_REASON_MINOR_HOTFIX"></span><span id="shtdn_reason_minor_hotfix"></span><dl> <dt>**SHTDN \_ GRUND \_ FÜR KLEINERE \_ HOTFIX-0x00000011**</dt> <dt></dt> </dl>                                               | Hotfix.<br/>                       |
| <span id="SHTDN_REASON_MINOR_HOTFIX_UNINSTALL"></span><span id="shtdn_reason_minor_hotfix_uninstall"></span><dl> <dt>**SHTDN \_ GRUND \_ FÜR KLEINERE \_ \_ HOTFIXDEINSTALLATIONS-0x00000017**</dt> <dt></dt> </dl>                | Hot Fix-Deinstallation.<br/>        |
| <span id="SHTDN_REASON_MINOR_HUNG"></span><span id="shtdn_reason_minor_hung"></span><dl> <dt>**SHTDN \_ GRUND \_ FÜR \_ GERINGFÜGIGE HUNG-0x00000005**</dt> <dt></dt> </dl>                                                     | Reagiert.<br/>                  |
| <span id="SHTDN_REASON_MINOR_INSTALLATION"></span><span id="shtdn_reason_minor_installation"></span><dl> <dt>**SHTDN \_ GRUND \_ FÜR KLEINERE \_ INSTALLATION**</dt> <dt>0X00000002</dt> </dl>                             | Die Installation.<br/>                  |
| <span id="SHTDN_REASON_MINOR_MAINTENANCE"></span><span id="shtdn_reason_minor_maintenance"></span><dl> <dt>**SHTDN \_ GRUND \_ FÜR GERINGFÜGIGE \_ WARTUNG**</dt> <dt>0x00000001</dt> </dl>                                | Wartung.<br/>                   |
| <span id="SHTDN_REASON_MINOR_MMC"></span><span id="shtdn_reason_minor_mmc"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ MMC**</dt> <dt>0x00000019</dt> </dl>                                                        | MMC-Problem.<br/>                     |
| <span id="SHTDN_REASON_MINOR_NETWORK_CONNECTIVITY"></span><span id="shtdn_reason_minor_network_connectivity"></span><dl> <dt>**SHTDN \_ GRUND \_ FÜR KLEINERE \_ \_ NETZWERKKONNEKTIVITÄT**</dt> <dt>0X00000014</dt> </dl>    | Netzwerkkonnektivität<br/>          |
| <span id="SHTDN_REASON_MINOR_NETWORKCARD"></span><span id="shtdn_reason_minor_networkcard"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ NETWORKCARD**</dt> <dt>0x00000009</dt> </dl>                                | Netzwerkkarte.<br/>                  |
| <span id="SHTDN_REASON_MINOR_OTHER"></span><span id="shtdn_reason_minor_other"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ OTHER**</dt> <dt>0x00000000</dt> </dl>                                                  | Anderes Problem.<br/>                   |
| <span id="SHTDN_REASON_MINOR_OTHERDRIVER"></span><span id="shtdn_reason_minor_otherdriver"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ OTHERDRIVER**</dt> <dt>0x0000000e</dt> </dl>                                | Anderes Treiberereignis.<br/>            |
| <span id="SHTDN_REASON_MINOR_POWER_SUPPLY"></span><span id="shtdn_reason_minor_power_supply"></span><dl> <dt>**SHTDN \_ GRUND \_ FÜR KLEINERE \_ \_ STROMVERSORGUNGs-0x0000000a**</dt> <dt></dt> </dl>                            | Stromversorgung.<br/>                  |
| <span id="SHTDN_REASON_MINOR_PROCESSOR"></span><span id="shtdn_reason_minor_processor"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ PROCESSOR**</dt> <dt>0x00000008</dt> </dl>                                      | Prozessor<br/>                     |
| <span id="SHTDN_REASON_MINOR_RECONFIG"></span><span id="shtdn_reason_minor_reconfig"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ RECONFIG**</dt> <dt>0x00000004</dt> </dl>                                         | Konfigurieren.<br/>                   |
| <span id="SHTDN_REASON_MINOR_SECURITY"></span><span id="shtdn_reason_minor_security"></span><dl> <dt>**SHTDN \_ GRUND \_ FÜR GERINGFÜGIGE \_ 0X00000013**</dt> <dt></dt> </dl>                                         | Sicherheitsproblem.<br/>                |
| <span id="SHTDN_REASON_MINOR_SECURITYFIX"></span><span id="shtdn_reason_minor_securityfix"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ SECURITYFIX**</dt> <dt>0x00000012</dt> </dl>                                | Sicherheitspatch.<br/>                |
| <span id="SHTDN_REASON_MINOR_SECURITYFIX_UNINSTALL"></span><span id="shtdn_reason_minor_securityfix_uninstall"></span><dl> <dt>**SHTDN \_ GRUND: \_ KLEINERE \_ \_ SICHERHEITSFIX-DEINSTALLATIONS-0X00000018**</dt> <dt></dt> </dl> | Deinstallation von Sicherheitspatches.<br/> |
| <span id="SHTDN_REASON_MINOR_SERVICEPACK"></span><span id="shtdn_reason_minor_servicepack"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ SERVICEPACK**</dt> <dt>0x00000010</dt> </dl>                                | Service Pack:<br/>                  |
| <span id="SHTDN_REASON_MINOR_SERVICEPACK_UNINSTALL"></span><span id="shtdn_reason_minor_servicepack_uninstall"></span><dl> <dt>**SHTDN \_ GRUND \_ FÜR KLEINERE \_ \_ SERVICEPACK-DEINSTALLATIONS-0x00000016**</dt> <dt></dt> </dl> | Service Pack-Deinstallation.<br/>   |
| <span id="SHTDN_REASON_MINOR_TERMSRV"></span><span id="shtdn_reason_minor_termsrv"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ TERMSRV**</dt> <dt>0x00000020</dt> </dl>                                            | Terminaldienste.<br/>             |
| <span id="SHTDN_REASON_MINOR_UNSTABLE"></span><span id="shtdn_reason_minor_unstable"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ UNSTABLE**</dt> <dt>0x00000006</dt> </dl>                                         | Instabil.<br/>                      |
| <span id="SHTDN_REASON_MINOR_UPGRADE"></span><span id="shtdn_reason_minor_upgrade"></span><dl> <dt>**SHTDN \_ GRUND \_ FÜR KLEINERE \_ UPGRADE-0x00000003**</dt> <dt></dt> </dl>                                            | Upgrade:<br/>                       |
| <span id="SHTDN_REASON_MINOR_WMI"></span><span id="shtdn_reason_minor_wmi"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ WMI**</dt> <dt>0x00000015</dt> </dl>                                                        | WMI-Problem.<br/>                     |



Die folgenden optionalen Flags stellen zusätzliche Informationen zum Ereignis bereit.



| Konstante/Wert                                                                                                                                                                                                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SHTDN_REASON_FLAG_USER_DEFINED"></span><span id="shtdn_reason_flag_user_defined"></span><dl> <dt>**SHTDN \_ REASON \_ FLAG \_ USER \_ DEFINED**</dt> <dt>0x40000000</dt> </dl> | Der Ursachencode wird vom Benutzer definiert. Weitere Informationen finden Sie unter Definieren eines benutzerdefinierten Ursachencodes. <br/> Wenn dieses Flag nicht vorhanden ist, wird der Grundcode vom System definiert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SHTDN_REASON_FLAG_PLANNED"></span><span id="shtdn_reason_flag_planned"></span><dl> <dt>**SHTDN \_ REASON \_ FLAG \_ PLANNED**</dt> <dt>0x80000000</dt> </dl>                 | Das Herunterfahren war geplant. Das System generiert eine SSD-Datei (System State Data). Diese Datei enthält Systemstatusinformationen wie Prozesse, Threads, Speicherauslastung und Konfiguration. <br/> Wenn dieses Flag nicht vorhanden ist, wurde das Herunterfahren ungeplant. Benachrichtigungs- und Berichterstellungsoptionen werden durch eine Reihe von Richtlinien gesteuert. Nach der Anmeldung zeigt das System beispielsweise ein Dialogfeld an, in dem das ungeplante Herunterfahren angezeigt wird, wenn die Richtlinie aktiviert wurde. Eine SSD-Datei wird nur erstellt, wenn die SSD-Richtlinie auf dem System aktiviert ist. Der Administrator kann [Windows-Fehlerberichterstattung,](../wer/windows-error-reporting.md) um die SSD-Daten an einen zentralen Ort oder an Microsoft zu senden.<br/> |



## <a name="remarks"></a>Hinweise

Die folgenden Kombinationen werden vom System erkannt. Die Tabelle gibt die Zeichenfolge an, die in der Shutdown Event Tracker angezeigt wird, und enthält eine ausführlichere Beschreibung. Die Standardzeichenfolge ist "Aus diesem Grund wurde kein Titel gefunden."



| Kombination                                                                                                | BESCHREIBUNG                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SHTDN \_ REASON \_ MAJOR \_ APPLICATION \| SHTDN \_ REASON \_ MINOR \_ HUNG                                            | "Anwendung: Nicht reagierend" Ein ungeplanter Neustart oder Herunterfahren zur Problembehandlung einer nicht reagierenden Anwendung.<br/>                                                                                                                             |
| SHTDN \_ REASON \_ MAJOR \_ APPLICATION \| SHTDN \_ REASON \_ MINOR \_ INSTALLATION \| SHTDN \_ REASON \_ FLAG \_ PLANNED    | "Anwendung: Installation (geplant)" Ein geplanter Neustart oder herunterfahren, um die Anwendungsinstallation durchzuführen.<br/>                                                                                                                              |
| SHTDN \_ REASON \_ MAJOR \_ APPLICATION \| SHTDN \_ REASON \_ MINOR \_ MAINTENANCE                                     | "Anwendung: Wartung (ungeplant)" Ein ungeplanter Neustart oder Herunterfahren zur Wartung einer Anwendung.<br/>                                                                                                                                    |
| SHTDN \_ REASON \_ MAJOR \_ APPLICATION \| SHTDN \_ REASON \_ MINOR \_ MAINTENANCE \| SHTDN \_ REASON \_ FLAG \_ PLANNED     | "Anwendung: Wartung (geplant)" Ein geplanter Neustart oder herunterfahren, um eine geplante Wartung für eine Anwendung durchzuführen.<br/>                                                                                                                  |
| SHTDN \_ REASON MAJOR APPLICATION \_ \_ \| SHTDN \_ REASON MINOR \_ \_ INSTABIL                                        | "Anwendung: Instabil" Ein ungeplanter Neustart oder Herunterfahren zur Problembehandlung einer instabilen Anwendung.<br/>                                                                                                                                     |
| SHTDN \_ REASON \_ MAJOR \_ HARDWARE \| SHTDN \_ REASON \_ MINOR \_ INSTALLATION                                       | "Hardware: Installation (ungeplant)" Ein ungeplanter Neustart oder herunterfahren, um die Hardwareinstallation zu starten oder abzuschließen.<br/>                                                                                                                     |
| SHTDN \_ REASON \_ MAJOR \_ HARDWARE \| SHTDN \_ REASON \_ MINOR \_ INSTALLATION \| SHTDN \_ REASON \_ FLAG \_ PLANNED       | "Hardware: Installation (Geplant)" Ein geplanter Neustart oder herunterfahren, um die Hardwareinstallation zu starten oder abzuschließen.<br/>                                                                                                                          |
| SHTDN \_ REASON \_ MAJOR \_ HARDWARE \| SHTDN \_ REASON \_ MINOR \_ MAINTENANCE                                        | "Hardware: Wartung (ungeplant)" Ein ungeplanter Neustart oder Herunterfahren der Hardware auf dem System.<br/>                                                                                                                               |
| SHTDN \_ REASON \_ MAJOR \_ HARDWARE \| SHTDN \_ REASON \_ MINOR \_ MAINTENANCE \| SHTDN \_ REASON \_ FLAG \_ PLANNED        | "Hardware: Wartung (geplant)" Ein geplanter Neustart oder Herunterfahren der Hardware auf dem System.<br/>                                                                                                                                    |
| SHTDN \_ REASON \_ MAJOR \_ LEGACY \_ API                                                                          | "Legacy-API heruntergefahren" Dieses Herunterfahren wurde von der [**Legacyfunktion InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna) initiiert. Anwendungen sollten die [**InitiateSystemShutdownEx-Funktion**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) verwenden.<br/> |
| SHTDN \_ REASON \_ MAJOR \_ OPERATINGSYSTEM \| SHTDN \_ REASON \_ MINOR \_ HOTFIX                                      | "Betriebssystem: Fehlerbehebung (ungeplant)" Ein ungeplanter Neustart oder herunterfahren, um eine Hot fix-Lösung zu installieren.<br/>                                                                                                                                        |
| SHTDN \_ REASON \_ MAJOR \_ OPERATINGSYSTEM \| SHTDN \_ REASON \_ MINOR \_ HOTFIX \| SHTDN \_ REASON \_ FLAG \_ PLANNED      | "Betriebssystem: Hot Fix (geplant)" Ein geplanter Neustart oder herunterfahren, um eine Hot Fix zu installieren.<br/>                                                                                                                                             |
| SHTDN \_ REASON \_ MAJOR \_ OPERATINGSYSTEM \| SHTDN \_ REASON \_ MINOR \_ RECONFIG                                    | "Betriebssystem: Neukonfiguration (ungeplant)" Ein ungeplanter Neustart oder herunterfahren, um die Betriebssystemkonfiguration zu ändern.<br/>                                                                                                        |
| SHTDN \_ REASON \_ MAJOR \_ OPERATINGSYSTEM \| SHTDN \_ REASON \_ MINOR \_ RECONFIG \| SHTDN \_ REASON \_ FLAG \_ PLANNED    | "Betriebssystem: Neukonfiguration (geplant)" Ein geplanter Neustart oder herunterfahren, um die Betriebssystemkonfiguration zu ändern.<br/>                                                                                                             |
| SHTDN \_ REASON \_ MAJOR \_ OPERATINGSYSTEM \| SHTDN \_ REASON \_ MINOR \_ SECURITYFIX                                 | "Betriebssystem: Sicherheitskorrektur (ungeplant)" Ein ungeplanter Neustart oder herunterfahren, um einen Sicherheitspatch zu installieren.<br/>                                                                                                                            |
| SHTDN \_ REASON \_ MAJOR \_ OPERATINGSYSTEM \| SHTDN \_ REASON \_ MINOR \_ SECURITYFIX \| SHTDN \_ REASON \_ FLAG \_ PLANNED | "Betriebssystem: Sicherheitskorrektur (geplant)" Ein geplanter Neustart oder herunterfahren, um einen Sicherheitspatch zu installieren.<br/>                                                                                                                                 |
| SHTDN \_ REASON \_ MAJOR \_ OPERATINGSYSTEM \| SHTDN \_ REASON \_ MINOR \_ SERVICEPACK \| SHTDN \_ REASON \_ FLAG \_ PLANNED | "Betriebssystem: Service Pack (geplant)" Ein geplanter Neustart oder herunterfahren, um ein Service Pack zu installieren.<br/>                                                                                                                                   |
| SHTDN \_ REASON \_ MAJOR \_ OPERATINGSYSTEM \| SHTDN \_ REASON \_ MINOR \_ UPGRADE \| SHTDN \_ REASON \_ FLAG \_ PLANNED     | "Betriebssystem: Upgrade (geplant)" Ein geplanter Neustart oder herunterfahren, um die Betriebssystemkonfiguration zu aktualisieren.<br/>                                                                                                                    |
| SHTDN \_ REASON \_ MAJOR \_ OTHER \| SHTDN \_ REASON \_ MINOR \_ OTHER                                                 | "Sonstige (ungeplant)" Ein ungeplantes Herunterfahren oder Neustarten.<br/>                                                                                                                                                                                 |
| SHTDN \_ REASON \_ MAJOR \_ OTHER \| SHTDN \_ REASON \_ MINOR \_ OTHER \| SHTDN \_ REASON \_ FLAG \_ PLANNED                 | "Sonstige (geplant)" Ein geplantes Herunterfahren oder Neustarten.<br/>                                                                                                                                                                                      |
| SHTDN \_ REASON \_ MAJOR \_ OTHER \| SHTDN \_ REASON \_ MINOR \_ HUNG                                                  | "Sonstiger Fehler: System reagiert nicht" Das System reagierte nicht mehr.<br/>                                                                                                                                                                  |
| SHTDN \_ REASON \_ MAJOR \_ POWER \| SHTDN \_ REASON \_ MINOR \_ CORDUNPLUGGED                                         | "Stromfehler: Netzkabel nicht angeschlossen" Der Computer wurde nicht angeschlossen.<br/>                                                                                                                                                                           |
| SHTDN \_ REASON \_ MAJOR \_ POWER \| SHTDN \_ REASON \_ MINOR \_ ENVIRONMENT                                           | "Stromausfall: Umgebung" Es ist ein Stromausfall erfolgt.<br/>                                                                                                                                                                                |
| SHTDN \_ REASON \_ MAJOR \_ SYSTEM \| SHTDN \_ REASON \_ MINOR \_ BLUESCREEN                                           | "Systemfehler: Fehler beenden": Der Computer hat ein Absturzereignis mit blauer Anzeige angezeigt.<br/>                                                                                                                                                        |
| SHTDN \_ REASON \_ MAJOR \_ SYSTEM \| SHTDN \_ REASON \_ MINOR \_ NETWORK \_ CONNECTIVITY                                | "Verlust der Netzwerkkonnektivität (ungeplant)" Der Computer muss aufgrund eines Problems mit der Netzwerkkonnektivität heruntergefahren werden.<br/>                                                                                                                    |
| SHTDN \_ REASON \_ MAJOR \_ SYSTEM \| SHTDN \_ REASON \_ MINOR \_ SECURITY                                             | "Sicherheitsproblem" Der Computer muss aufgrund eines Sicherheitsproblems heruntergefahren werden.<br/>                                                                                                                                                          |



 

Sie können auch eigene Gründe für das Herunterfahren definieren und sie der Registrierung hinzufügen. Jeder Grundcode sollte als Registrierungswert im folgenden Schlüssel gespeichert werden:**HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion Reliability \\ \\ UserDefined \\ \_ \_ \_**<default system language ID>

Dieser Schlüssel enthält Wertnamen im folgenden Format: *xxxxx*; *nnn*; *nnnnn .* Die Semikolons begrenzen die Komponenten eines Wertnamens.

<dl> <dt>

<span id="xxxxx"></span><span id="XXXXX"></span>*Xxxxx*
</dt> <dd>

Ein bis fünf der folgenden Steuerelementflags (es können keine anderen Zeichen verwendet werden).



| Flag | Beschreibung                                                                                       |
|------|---------------------------------------------------------------------------------------------------|
| P    | Geplantes Herunterfahren; andernfalls ein ungeplantes Herunterfahren.                                               |
| C    | Ein Kommentar ist erforderlich. Dieses Flag muss mit S verwendet werden.<br/>                                  |
| B    | Eine ID ist erforderlich. Dieses Flag muss mit D verwendet werden.<br/>                                      |
| E    | Zeigt das Dialogfeld zum erwarteten Herunterfahren an. Entweder S, D oder S und D müssen verwendet werden.<br/>   |
| D    | Zeigt das Dialogfeld unerwartetes Herunterfahren an. Entweder S, D oder S und D müssen verwendet werden.<br/> |



 

Die Reihenfolge, in der die Flags verwendet werden, ist nicht wichtig. CSP gibt z. B. ein geplantes Herunterfahren an, in dem das erwartete Dialogfeld zum Herunterfahren angezeigt wird und ein Kommentar erforderlich ist.

</dd> <dt>

<span id="nnn"></span><span id="NNN"></span>*Nnn*
</dt> <dd>

Hauptgrund. Diese Komponente muss eine Zahl im Bereich von 64 bis 255 sein. Der Bereich 0 bis 63 ist für die Verwendung durch das System reserviert.

</dd> <dt>

<span id="nnnnn"></span><span id="NNNNN"></span>*Nnnnn*
</dt> <dd>

Geringfügiger Grund. Diese Komponente muss im Bereich von 0 bis 65535 liegen.

</dd> </dl>

Benutzerdefinierte Gründe werden auf der Benutzeroberfläche nach der Hauptgrundnummer und dann nach der Kleineren Grundnummer sortiert. Zwei benutzerdefinierte Gründe können nicht die gleichen Haupt- und Nebengründe verwenden, es sei denn, einer ist geplant, und der andere ist ungeplant. Andernfalls verwendet das System die erste Instanz und ignoriert die anderen Instanzen.

Die Daten für jeden Registrierungswert sind zwei Zeichenfolgen, die durch \\ n \\ r getrennt sind. Die erste Zeichenfolge ist eine Titelzeichenfolge, die im Dialogfeld zum Herunterfahren angezeigt und in das Ereignisprotokoll geschrieben werden soll. Die maximale Größe beträgt 64 Zeichen. Titelzeichenfolgen müssen eindeutig sein. Benutzerdefinierte Titel können nicht mit den vom System definierten Standardtiteln oder einem anderen benutzerdefinierten Titel übereinstimmen. Die zweite Zeichenfolge ist eine Beschreibungszeichenfolge, die im Dialogfeld zum Herunterfahren angezeigt werden soll. ist optional. Die maximale Größe beträgt 256 Zeichen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[XP-Desktop-Apps \| UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2003-Desktop-Apps \|\]<br/>                         |
| Header<br/>                   | <dl> <dt>Reason.h</dt> </dl> |



 

 
