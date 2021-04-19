---
description: Die Grund Codes für das Herunterfahren werden von den Funktionen ExitWindowsEx und initiatesystemshutdownetx im Parameter dwReason verwendet. Eine maximale Anzahl von \_ Grund Zahlen, \_ Warum Codes vom System verarbeitet werden. Die max. \_ NUM- \_ Gründe sind in Reason. h definiert.
ms.assetid: db1ecee0-40eb-4761-b5d8-9cc3c1c98cdf
title: Grund Codes für das Herunterfahren des Systems (Reason. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ee2b8b2795dcf350d627b3cf59f85eb374a22cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348247"
---
# <a name="system-shutdown-reason-codes"></a>Grund Codes zum Herunterfahren des Systems

Die Grund Codes für das Herunterfahren werden von den Funktionen [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) und [**initiatesystemshutdownetx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) im Parameter *dwReason* verwendet.

Eine maximale Anzahl von \_ Grund Zahlen, \_ Warum Codes vom System verarbeitet werden. Die max. \_ NUM- \_ Gründe sind in Reason. h definiert.

Im folgenden finden Sie die wichtigsten Grund-Flags. Sie geben den Typ des allgemeinen Problems an.



| Konstante/Wert                                                                                                                                                                                                                                                                                 | BESCHREIBUNG                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SHTDN_REASON_MAJOR_APPLICATION"></span><span id="shtdn_reason_major_application"></span><dl> <dt>**Shtdn \_ Grund für die \_ Haupt \_ Anwendung**</dt> <dt>0x00040000</dt> </dl>             | Anwendungsproblem.<br/>                                                                                                                                      |
| <span id="SHTDN_REASON_MAJOR_HARDWARE"></span><span id="shtdn_reason_major_hardware"></span><dl> <dt>**Shtdn \_ Grund \_ Haupt \_ Hardware**</dt> <dt>0x00010000 bis</dt> </dl>                      | Hardware Problem.<br/>                                                                                                                                         |
| <span id="SHTDN_REASON_MAJOR_LEGACY_API"></span><span id="shtdn_reason_major_legacy_api"></span><dl> <dt>**Shtdn \_ Grund für die Hauptversion der \_ \_ Legacy- \_ API**</dt> <dt>0x00070000</dt> </dl>               | Die Funktion " [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna) " wurde anstelle von " [**initiatesystemshutdownetx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa)" verwendet.<br/> |
| <span id="SHTDN_REASON_MAJOR_OPERATINGSYSTEM"></span><span id="shtdn_reason_major_operatingsystem"></span><dl> <dt>**Shtdn \_ Grund \_ Haupt \_ OperatingSystem**</dt> <dt>0x00020000</dt> </dl> | Betriebssystem Problem.<br/>                                                                                                                                 |
| <span id="SHTDN_REASON_MAJOR_OTHER"></span><span id="shtdn_reason_major_other"></span><dl> <dt>**Shtdn \_ Grund \_ \_ sonstige andere**</dt> <dt>0x00000000</dt> </dl>                               | Anderes Problem.<br/>                                                                                                                                            |
| <span id="SHTDN_REASON_MAJOR_POWER"></span><span id="shtdn_reason_major_power"></span><dl> <dt>**Shtdn \_ Grund \_ Haupt \_ Leistung**</dt> <dt>0x00060000</dt> </dl>                               | Stromausfall.<br/>                                                                                                                                          |
| <span id="SHTDN_REASON_MAJOR_SOFTWARE"></span><span id="shtdn_reason_major_software"></span><dl> <dt>**Shtdn \_ Hauptursache der \_ \_ Software**</dt> <dt>0x00030000</dt> </dl>                      | Software Problem.<br/>                                                                                                                                         |
| <span id="SHTDN_REASON_MAJOR_SYSTEM"></span><span id="shtdn_reason_major_system"></span><dl> <dt>**Shtdn \_ Grund \_ Haupt \_ System**</dt> <dt>0x00050000</dt> </dl>                            | System Fehler.<br/>                                                                                                                                         |



Im folgenden sind die hilfspaltenflags angegeben. Sie ändern das angegebene Hauptgrund Kennzeichen. Sie können einen beliebigen kleinen Grund in Verbindung mit jedem Hauptgrund verwenden, aber einige Kombinationen sind nicht sinnvoll.



| Konstante/Wert                                                                                                                                                                                                                                                                                                    | BESCHREIBUNG                               |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------|
| <span id="SHTDN_REASON_MINOR_BLUESCREEN"></span><span id="shtdn_reason_minor_bluescreen"></span><dl> <dt>**Shtdn \_ Grund \_ kleiner \_ Bluescreen**</dt> <dt>0x0000000f</dt> </dl>                                   | Absturz Ereignis des blauen Bildschirms.<br/>       |
| <span id="SHTDN_REASON_MINOR_CORDUNPLUGGED"></span><span id="shtdn_reason_minor_cordunplugged"></span><dl> <dt>**Shtdn \_ Grund, \_ geringfügige \_ cordunangeschlossen**</dt> <dt>0x0000000b</dt> </dl>                          | Packt.<br/>                     |
| <span id="SHTDN_REASON_MINOR_DISK"></span><span id="shtdn_reason_minor_disk"></span><dl> <dt>**Shtdn \_ Grund für \_ geringfügige \_ Festplatte**</dt> <dt>0x00000007</dt> </dl>                                                     | auswählen.<br/>                          |
| <span id="SHTDN_REASON_MINOR_ENVIRONMENT"></span><span id="shtdn_reason_minor_environment"></span><dl> <dt>**Shtdn \_ Reason \_ neben \_ Umgebung**</dt> <dt>0x0000000c</dt> </dl>                                | Umgebung.<br/>                   |
| <span id="SHTDN_REASON_MINOR_HARDWARE_DRIVER"></span><span id="shtdn_reason_minor_hardware_driver"></span><dl> <dt>**Shtdn \_ Grund für den \_ geringfügigen \_ Hardware \_ Treiber**</dt> <dt>0x0000000d</dt> </dl>                   | Trei.<br/>                        |
| <span id="SHTDN_REASON_MINOR_HOTFIX"></span><span id="shtdn_reason_minor_hotfix"></span><dl> <dt>**Shtdn \_ Grund \_ kleiner \_ Hotfix**</dt> <dt>0x00000011</dt> </dl>                                               | Hotfix.<br/>                       |
| <span id="SHTDN_REASON_MINOR_HOTFIX_UNINSTALL"></span><span id="shtdn_reason_minor_hotfix_uninstall"></span><dl> <dt>**Shtdn \_ Grund für \_ kleinere \_ Hotfix- \_ Deinstallation**</dt> <dt>0x00000017</dt> </dl>                | Hotfix-deinstalstallation.<br/>        |
| <span id="SHTDN_REASON_MINOR_HUNG"></span><span id="shtdn_reason_minor_hung"></span><dl> <dt>**Shtdn \_ Reason \_ Minor \_**</dt> hat <dt>0x00000005 bei der</dt> nicht reagiert. </dl>                                                     | Reagiert.<br/>                  |
| <span id="SHTDN_REASON_MINOR_INSTALLATION"></span><span id="shtdn_reason_minor_installation"></span><dl> <dt>**Shtdn \_ Reason \_ Minor \_ Installation**</dt> <dt>0x00000002</dt> </dl>                             | Die Installation.<br/>                  |
| <span id="SHTDN_REASON_MINOR_MAINTENANCE"></span><span id="shtdn_reason_minor_maintenance"></span><dl> <dt>**Shtdn \_ Grund für \_ geringfügige \_ Wartung**</dt> <dt>0x00000001</dt> </dl>                                | Unterhalt.<br/>                   |
| <span id="SHTDN_REASON_MINOR_MMC"></span><span id="shtdn_reason_minor_mmc"></span><dl> <dt>**Shtdn \_ Grund für \_ kleinere \_ MMC**</dt> <dt>0x00000019</dt> </dl>                                                        | MMC-Problem.<br/>                     |
| <span id="SHTDN_REASON_MINOR_NETWORK_CONNECTIVITY"></span><span id="shtdn_reason_minor_network_connectivity"></span><dl> <dt>**Shtdn \_ Grund für \_ kleinere \_ Netzwerk \_ Konnektivität**</dt> <dt>0x00000014</dt> </dl>    | Netzwerkkonnektivität<br/>          |
| <span id="SHTDN_REASON_MINOR_NETWORKCARD"></span><span id="shtdn_reason_minor_networkcard"></span><dl> <dt>**Shtdn \_ Grund \_ \_ nebennetzwerk Karte**</dt> <dt>0x00000009</dt> </dl>                                | Netzwerkkarte.<br/>                  |
| <span id="SHTDN_REASON_MINOR_OTHER"></span><span id="shtdn_reason_minor_other"></span><dl> <dt>**Shtdn \_ Reason \_ Minor \_ other**</dt> <dt>0x00000000</dt> </dl>                                                  | Anderes Problem.<br/>                   |
| <span id="SHTDN_REASON_MINOR_OTHERDRIVER"></span><span id="shtdn_reason_minor_otherdriver"></span><dl> <dt>**Shtdn \_ Reason \_ Minor \_ otherdriver**</dt> <dt>0x0000000e</dt> </dl>                                | Anderes Treiber Ereignis.<br/>            |
| <span id="SHTDN_REASON_MINOR_POWER_SUPPLY"></span><span id="shtdn_reason_minor_power_supply"></span><dl> <dt>**Shtdn \_ Grund für \_ kleinere \_ Strom \_ Versorgung**</dt> <dt>0x0000000A</dt> </dl>                            | Netzteil.<br/>                  |
| <span id="SHTDN_REASON_MINOR_PROCESSOR"></span><span id="shtdn_reason_minor_processor"></span><dl> <dt>**Shtdn \_ Reason \_ Minor \_ Processor**</dt> <dt>0x00000008</dt> </dl>                                      | Prozessor<br/>                     |
| <span id="SHTDN_REASON_MINOR_RECONFIG"></span><span id="shtdn_reason_minor_reconfig"></span><dl> <dt>**Shtdn \_ Reason \_ Minor \_ reconfig**</dt> <dt>0x00000004</dt> </dl>                                         | Neu konfigurieren.<br/>                   |
| <span id="SHTDN_REASON_MINOR_SECURITY"></span><span id="shtdn_reason_minor_security"></span><dl> <dt>**Shtdn \_ Reason \_ Minor \_ Security**</dt> <dt>0x00000013</dt> </dl>                                         | Sicherheitsproblem.<br/>                |
| <span id="SHTDN_REASON_MINOR_SECURITYFIX"></span><span id="shtdn_reason_minor_securityfix"></span><dl> <dt>**Shtdn \_ Reason \_ Minor \_ SecurityFix**</dt> <dt>0x00000012</dt> </dl>                                | Sicherheitspatches.<br/>                |
| <span id="SHTDN_REASON_MINOR_SECURITYFIX_UNINSTALL"></span><span id="shtdn_reason_minor_securityfix_uninstall"></span><dl> <dt>**Shtdn \_ Reason \_ Minor \_ SecurityFix \_ deinstallieren**</dt> von <dt>0x00000018</dt> </dl> | Neuinstallation des Sicherheitspatches.<br/> |
| <span id="SHTDN_REASON_MINOR_SERVICEPACK"></span><span id="shtdn_reason_minor_servicepack"></span><dl> <dt>**Shtdn \_ Reason \_ Minor \_ Servicepack**</dt> <dt>0x00000010</dt> </dl>                                | Service Pack.<br/>                  |
| <span id="SHTDN_REASON_MINOR_SERVICEPACK_UNINSTALL"></span><span id="shtdn_reason_minor_servicepack_uninstall"></span><dl> <dt>**Shtdn \_ Reason \_ Minor \_ Servicepack \_ deinstallieren**</dt> von <dt>0x00000016</dt> </dl> | Service Pack-Installation.<br/>   |
| <span id="SHTDN_REASON_MINOR_TERMSRV"></span><span id="shtdn_reason_minor_termsrv"></span><dl> <dt>**Shtdn \_ Reason \_ Minor \_ termsrv**</dt> <dt>0x00000020</dt> </dl>                                            | Terminal Dienste.<br/>             |
| <span id="SHTDN_REASON_MINOR_UNSTABLE"></span><span id="shtdn_reason_minor_unstable"></span><dl> <dt>**Shtdn \_ Reason \_ geringfügig \_ instabil**</dt> <dt>0x00000006</dt> </dl>                                         | Lem.<br/>                      |
| <span id="SHTDN_REASON_MINOR_UPGRADE"></span><span id="shtdn_reason_minor_upgrade"></span><dl> <dt>**Shtdn \_ Grund für \_ geringfügige \_ Upgrades**</dt> <dt>0x00000003</dt> </dl>                                            | Upgrade:<br/>                       |
| <span id="SHTDN_REASON_MINOR_WMI"></span><span id="shtdn_reason_minor_wmi"></span><dl> <dt>**Shtdn \_ Reason \_ Minor \_ WMI**</dt> <dt>0x00000015</dt> </dl>                                                        | WMI-Problem.<br/>                     |



Die folgenden optionalen Flags stellen zusätzliche Informationen über das Ereignis bereit.



| Konstante/Wert                                                                                                                                                                                                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SHTDN_REASON_FLAG_USER_DEFINED"></span><span id="shtdn_reason_flag_user_defined"></span><dl> <dt>**Shtdn \_ Reason \_ Flag \_ Benutzer \_ definiertes**</dt> <dt>0x40000000</dt> </dl> | Der Grund Code wird vom Benutzer definiert. Weitere Informationen finden Sie unter Definieren eines benutzerdefinierten Ursachen Codes. <br/> Wenn dieses Flag nicht vorhanden ist, wird der Grund Code vom System definiert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SHTDN_REASON_FLAG_PLANNED"></span><span id="shtdn_reason_flag_planned"></span><dl> <dt>**Shtdn \_ Reason \_ Flag \_ geplant**</dt> <dt>0x80000000</dt> </dl>                 | Das Herunterfahren wurde geplant. Das System generiert eine SSD-Datei (Systemstatus Daten). Diese Datei enthält Systemstatus Informationen, wie z. b. die Prozesse, Threads, die Speicherauslastung und die Konfiguration. <br/> Wenn dieses Flag nicht vorhanden ist, wurde das Herunterfahren nicht geplant. Benachrichtigungs-und Bericht Erstellungs Optionen werden durch eine Reihe von Richtlinien gesteuert. Nach der Anmeldung zeigt das System z. b. ein Dialogfeld an, das das ungeplante Herunterfahren meldet, wenn die Richtlinie aktiviert ist. Eine SSD-Datei wird nur erstellt, wenn die SSD-Richtlinie auf dem System aktiviert ist. Der Administrator kann [Windows-Fehlerberichterstattung](../wer/windows-error-reporting.md) verwenden, um die SSD-Daten an einen zentralen Speicherort oder an Microsoft zu senden.<br/> |



## <a name="remarks"></a>Bemerkungen

Die folgenden Kombinationen werden vom System erkannt. Die Tabelle gibt die Zeichenfolge an, die in der Ereignisprotokollierung für das Herunterfahren angezeigt wird, und bietet eine ausführlichere Beschreibung. Die Standard Zeichenfolge ist, dass kein Titel gefunden werden konnte.



| Kombination                                                                                                | BESCHREIBUNG                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| shtdn \_ reason \_ Haupt \_ Anwendung \| shtdn \_ reason \_ Minor \_ nicht reagiert                                            | "Anwendung: nicht reagierend" ein ungeplanter Neustart oder Herunterfahren, um Probleme mit einer nicht reagierenden Anwendung zu beheben.<br/>                                                                                                                             |
| shtdn \_ reason \_ Haupt \_ Anwendung \| shtdn Reason-Grund Kennzeichen Grund \_ \_ \_ \| \_ \_ Flag \_ geplant    | "Application: Installation (geplant)" ein geplantes Neustart oder Herunterfahren zum Ausführen der Anwendungs Installation.<br/>                                                                                                                              |
| shtdn-Grund Hauptursache für die \_ \_ Haupt \_ \| \_ \_ sächliches \_ Arbeiten von Anwendungen                                     | "Anwendung: Wartung (nicht geplant)" ein ungeplanter Neustart oder Herunterfahren für den Betrieb einer Anwendung.<br/>                                                                                                                                    |
| shtdn \_ reason \_ Haupt \_ Anwendung \| shtdn \_ Reason Grund- \_ \_ \| shtdn \_ Grund \_ Flag \_ geplant     | "Anwendung: Wartung (geplant)" ein geplantes Neustart oder Herunterfahren, um eine geplante Wartung für eine Anwendung auszuführen.<br/>                                                                                                                  |
| shtdn \_ reason \_ hauptsächlich schwerwiegendes \_ Anwendungs- \| shtdn \_ reason \_ \_                                        | "Anwendung: instabil" ein ungeplanter Neustart oder Herunterfahren, um Probleme mit einer instabilen Anwendung zu beheben.<br/>                                                                                                                                     |
| shtdn- \_ Grund Hauptursache der \_ Haupt Hardware- \_ \| shtdn- \_ \_ \_ Installation                                       | "Hardware: Installation (nicht geplant)" ein ungeplanter Neustart oder Herunterfahren, um die Hardware Installation zu starten oder abzuschließen.<br/>                                                                                                                     |
| shtdn \_ reason \_ Haupt \_ Hardware \| shtdn \_ reason \_ \_ \| hilfshtdn \_ Grund \_ Flag \_ geplant       | "Hardware: Installation (geplant)" ein geplantes Neustart oder Herunterfahren, um die Hardware Installation zu starten oder abzuschließen.<br/>                                                                                                                          |
| shtdn \_ reason \_ Haupt \_ Hardware- \| shtdn \_ Grund für \_ geringfügige \_ Wartung                                        | "Hardware: Wartung (nicht geplant)" ein ungeplanter Neustart oder Herunterfahren für die Dienst Hardware auf dem System.<br/>                                                                                                                               |
| shtdn \_ reason \_ Haupt \_ Hardware- \| shtdn \_ Grundursache für \_ geringfügige \_ Wartung \| shtdn \_ reason \_ Flag \_ geplant        | "Hardware: Wartung (geplant)" ein geplanter Neustart oder Herunterfahren für die Dienst Hardware im System.<br/>                                                                                                                                    |
| shtdn \_ reason-Hauptversion der \_ Legacy- \_ \_ API                                                                          | Das Herunterfahren der Legacy-API wurde durch die Legacy Funktion [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna) initiiert. Anwendungen sollten die [**initiatesystemshutdownetx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) -Funktion verwenden.<br/> |
| shtdn \_ reason \_ Haupt \_ OperatingSystem \| shtdn \_ reason \_ geringfügige \_ Hotfix                                      | "Betriebs System: Hotfix (nicht geplant)" ein ungeplanter Neustart oder Herunterfahren, um einen Hotfix zu installieren.<br/>                                                                                                                                        |
| shtdn \_ reason \_ Haupt \_ OperatingSystem \| shtdn \_ reason \_ Grund \_ Flag für \| shtdn- \_ Grund \_ Flag \_ geplant      | "Betriebs System: Hotfix (geplant)" ein geplantes Neustart oder Herunterfahren, um einen Hotfix zu installieren.<br/>                                                                                                                                             |
| shtdn \_ reason \_ Haupt \_ OperatingSystem \| shtdn \_ reason \_ geringfügige \_ Neukonfiguration                                    | "Betriebssystem: Neukonfiguration (nicht geplant)" ein ungeplanter Neustart oder Herunterfahren, um die Betriebs Systemkonfiguration zu ändern.<br/>                                                                                                        |
| shtdn \_ reason \_ Haupt \_ OperatingSystem \| shtdn \_ reason \_ Grund \_ Flag für grundlegenden reconfig- \| shtdn \_ \_ \_ geplant    | "Betriebssystem: Neukonfiguration (geplant)" ein geplantes Neustart oder Herunterfahren, um die Betriebs Systemkonfiguration zu ändern.<br/>                                                                                                             |
| shtdn \_ reason \_ Haupt \_ OperatingSystem \| shtdn \_ reason \_ geringfügige \_ SecurityFix                                 | "Betriebs System: Sicherheitskorrektur (nicht geplant)" ein ungeplanter Neustart oder Herunterfahren zur Installation eines Sicherheitspatches.<br/>                                                                                                                            |
| shtdn \_ reason \_ Haupt- \_ OperatingSystem \| shtdn Reason grundlegenden \_ \_ \_ SecurityFix \| shtdn \_ reason \_ Flag \_ geplant | "Betriebs System: Sicherheitskorrektur (geplant)" ein geplantes Neustart oder Herunterfahren zum Installieren eines Sicherheitspatches.<br/>                                                                                                                                 |
| shtdn \_ reason \_ Haupt \_ OperatingSystem \| shtdn \_ reason \_ Grund \_ \| kennflag für shtdn-shtdn \_ \_ \_ geplant | "Betriebs System: Service Pack (geplant)" ein geplantes Neustart oder Herunterfahren, um eine Service Pack zu installieren.<br/>                                                                                                                                   |
| shtdn \_ reason \_ Haupt \_ OperatingSystem \| shtdn Reason Grund für das \_ \_ \_ \| shtdn \_ reason \_ Flag \_ geplant     | "Betriebssystem: Upgrade (geplant)" ein geplantes Neustart oder Herunterfahren, um die Betriebs Systemkonfiguration zu aktualisieren.<br/>                                                                                                                    |
| shtdn \_ - \_ Grund \_ Haupt \| sächlich anderer shtdn- \_ Grund \_ \_                                                 | "Sonstige (ungeplante)" ein nicht geplantes Herunterfahren oder Neustarten.<br/>                                                                                                                                                                                 |
| shtdn- \_ Grund \_ Haupt \_ sächliches shtdn-Grund, \| \_ \_ \_ andere \| shtdn Reason \_ \_ Flag \_ geplant                 | "Other (geplant)" ein geplantes Herunterfahren oder Neustarten.<br/>                                                                                                                                                                                      |
| shtdn-Grund, schwerwiegendes \_ \_ \_ \| shtdn- \_ Grund \_ gering \_                                                  | "Anderer Fehler: das System reagiert nicht". das System reagiert nicht mehr.<br/>                                                                                                                                                                  |
| shtdn \_ reason \_ Haupt \_ Grund für den Strom \| shtdn, \_ \_ geringfügige \_ cordunangeschlossen                                         | "Stromausfall: Kabel Kabel"<br/>                                                                                                                                                                           |
| shtdn \_ reason \_ Hauptgrund für den Hauptgrund für den \_ Strom- \| shtdn \_ \_ \_                                           | "Stromausfall: Umgebung" bei einem Stromausfall.<br/>                                                                                                                                                                                |
| shtdn \_ reason \_ schwerwiegendes \_ System \| shtdn \_ reason \_ geringfügige \_ Bluescreen                                           | "System Fehler: Fehler beim Abbrechen". der Computer hat ein Absturz Ereignis auf einem blauen Bildschirm angezeigt.<br/>                                                                                                                                                        |
| shtdn-Grund Hauptursache für die \_ \_ Haupt \_ \| \_ \_ sächliches System \_ -shtdn \_                                | "Verlust der Netzwerk Konnektivität (ungeplant)" der Computer muss aufgrund eines Problems mit der Netzwerk Konnektivität heruntergefahren werden.<br/>                                                                                                                    |
| shtdn \_ reason \_ Haupt \_ System- \| shtdn \_ Grund \_ geringfügige \_ Sicherheit                                             | "Sicherheitsproblem" der Computer muss aufgrund eines Sicherheitsproblems heruntergefahren werden.<br/>                                                                                                                                                          |



 

Sie können auch eigene Gründe für das Herunterfahren definieren und Sie der Registrierung hinzufügen. Jeder Ursachen Code sollte als Registrierungs Wert im folgenden Schlüssel gespeichert werden:**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Zuverlässigkeit \\ UserDefined \\<Standard \_ Systemsprachen- \_ \_ ID>**

Dieser Schlüssel enthält Wertnamen der folgenden Form: *XXXXX*; *nnn*; *NNNNN*. Durch Semikolons werden die Komponenten eines Werte namens getrennt.

<dl> <dt>

<span id="xxxxx"></span><span id="XXXXX"></span>*xxxxx*
</dt> <dd>

Ein bis fünf der folgenden steuerungflags (es können keine anderen Zeichen verwendet werden).



| Flag | Beschreibung                                                                                       |
|------|---------------------------------------------------------------------------------------------------|
| P    | Geplantes Herunterfahren; andernfalls ein ungeplantes Herunterfahren.                                               |
| C    | Ein Kommentar ist erforderlich. Dieses Flag muss mit S verwendet werden.<br/>                                  |
| B    | Eine ID ist erforderlich. Dieses Flag muss mit D verwendet werden.<br/>                                      |
| E    | Zeigt das Dialogfeld erwartetes Herunterfahren an. Entweder s, D oder sowohl s als auch d müssen verwendet werden.<br/>   |
| D    | Zeigt das Dialogfeld unerwartetes Herunterfahren an. Entweder s, D oder sowohl s als auch d müssen verwendet werden.<br/> |



 

Die Reihenfolge, in der die Flags verwendet werden, ist nicht wichtig. Beispielsweise gibt CSP ein geplantes Herunterfahren an, in dem das erwartete Dialogfeld zum Herunterfahren angezeigt wird, und ein Kommentar ist erforderlich.

</dd> <dt>

<span id="nnn"></span><span id="NNN"></span>*nnn*
</dt> <dd>

Hauptgrund. Diese Komponente muss eine Zahl im Bereich 64-255 sein. Der Bereich 0-63 ist für die Verwendung durch das System reserviert.

</dd> <dt>

<span id="nnnnn"></span><span id="NNNNN"></span>*nnnnn*
</dt> <dd>

Der kleinere Grund. Diese Komponente muss im Bereich 0-65535 liegen.

</dd> </dl>

Benutzerdefinierte Gründe werden in der Benutzeroberfläche nach Hauptursache und dann nach Nebenzahl sortiert. Zwei benutzerdefinierte Gründe können dieselben Haupt-und neben sächlicheren Gründe verwenden, es sei denn, eine ist geplant, und die andere ist nicht geplant. Andernfalls wird die erste Instanz vom System verwendet und die anderen ignoriert.

Die Daten für die einzelnen Registrierungs Werte sind zwei Zeichen folgen, die durch \\ n r getrennt sind \\ . Die erste Zeichenfolge ist eine Titel Zeichenfolge, die im Dialogfeld zum Herunterfahren angezeigt und in das Ereignisprotokoll geschrieben wird. Die maximale Größe beträgt 64 Zeichen. Titel Zeichenfolgen müssen eindeutig sein. Benutzerdefinierte Titel können nicht mit den vom System definierten Standard Titeln oder mit einem anderen benutzerdefinierten Titel verglichen werden. Die zweite Zeichenfolge ist eine Beschreibungs Zeichenfolge, die im Dialogfeld zum Herunterfahren angezeigt wird. Dies ist optional. Die maximale Größe beträgt 256 Zeichen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[UWP-Apps für Windows XP-Desktop-Apps \|\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 \[ -Desktop-Apps \| UWP-apps\]<br/>                         |
| Header<br/>                   | <dl> <dt>Reason. h</dt> </dl> |



 

 
