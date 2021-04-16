---
description: Gibt den Grund an, warum ein WLAN-Vorgang fehlgeschlagen ist.
ms.assetid: 7b267f0b-b3f7-4729-bab4-de3bdd0a35a2
title: WLAN_REASON_CODE (wlanapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba0ae705244541063564431809cffa953a0f3fd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530164"
---
# <a name="wlan_reason_code"></a>WLAN-Ursachen \_ \_ Code

Der **WLAN- \_ Grund \_ Codetyp** gibt den Grund an, warum ein WLAN-Vorgang fehlgeschlagen ist.

Sie können die [**wlanreasoncodedestring**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring) -Funktion verwenden, um einen numerischen Grund Code (z. b. 0x00050007) der Text Bedeutung zuzuordnen. Sie können die Nachschlage Tabelle auch verwenden, um den numerischen Wert des Grund Codes zu interpretieren. Informationen zum Anzeigen der Nachschlage Tabelle finden Sie unter Anhang E: Mapping of Reason Codes to Event Messages im Dokument [Troubleshooting Windows Vista 802,11 Wireless Connections](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10)).


```C++
typedef DWORD WLAN_REASON_CODE, *PWLAN_REASON_CODE;
```



In der folgenden Tabelle sind allgemeine Fehlercodes aufgeführt.



| Ursachencode                 | Bedeutung                            |
|-----------------------------|------------------------------------|
| WLAN- \_ Grund \_ Code \_ Erfolg | Der Vorgang ist erfolgreich.            |
| der WLAN- \_ Grund ist \_ \_ unbekannt. | Der Grund für den Fehler ist unbekannt. |



 

In der folgenden Tabelle sind die automatischen Konfigurationsfehler Codes aufgeführt.



| Ursachencode                                  | Bedeutung                                         |
|----------------------------------------------|-------------------------------------------------|
| WLAN- \_ reason- \_ Code \_ Netzwerk \_ nicht \_ kompatibel | Das Drahtlos Netzwerk ist nicht kompatibel.         |
| das WLAN- \_ Grund \_ Code \_ Profil ist \_ nicht \_ kompatibel. | Das Drahtlos Netzwerk Profil ist nicht kompatibel. |



 

In der folgenden Tabelle sind die automatischen Verbindungsfehler Codes aufgeführt.



| Ursachencode                                                | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WLAN- \_ reason \_ Code \_ keine \_ automatische \_ Verbindung                   | Das Profil gibt keine automatische Verbindung an.                                                                                                                                                                                                                                                                                                                                                                                                               |
| der WLAN-Ursachen \_ \_ Code ist \_ nicht \_ sichtbar                           | Das Drahtlos Netzwerk ist nicht sichtbar.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| der WLAN-Ursachen \_ \_ Code wurde \_ \_ verweigert.                             | Das Drahtlos Netzwerk wird durch eine Gruppenrichtlinie blockiert.                                                                                                                                                                                                                                                                                                                                                                                                        |
| der WLAN-Ursachen \_ \_ Code wurde \_ \_ verweigert.                           | Das Drahtlos Netzwerk wird vom Benutzer blockiert.                                                                                                                                                                                                                                                                                                                                                                                                            |
| der WLAN-Ursachen \_ \_ Code \_ BSS- \_ Typ \_ \_ ist unzulässig.                | Der grundlegende Service Set-Typ (BSS) ist auf diesem drahtlos Adapter nicht zulässig.                                                                                                                                                                                                                                                                                                                                                                               |
| WLAN-Ursachen \_ \_ Code in fehlerhafter \_ \_ \_ Liste                       | Das Drahtlos Netzwerk befindet sich in der Fehlerliste.                                                                                                                                                                                                                                                                                                                                                                                                             |
| WLAN-Ursachen \_ \_ Code \_ in \_ blockierter \_ Liste                      | Das Drahtlos Netzwerk befindet sich in der Liste blockiert.                                                                                                                                                                                                                                                                                                                                                                                                            |
| der \_ WLAN \_ -Ursachen Code \_ SSID- \_ Liste ist \_ zu \_ lang                  | Die Größe der Liste der Service Set Identifier (SSID) überschreitet die maximale Größe, die vom Adapter unterstützt wird.                                                                                                                                                                                                                                                                                                                                                  |
| WLAN- \_ reason \_ Code Connect- \_ \_ Rückruf \_ schlägt fehl                    | Der Verbindungs Rückruf für medienspezifische Module (MSM) schlägt fehl.                                                                                                                                                                                                                                                                                                                                                                                                     |
| der WLAN-Grund für die \_ \_ Code Überprüfung \_ \_ \_ schlägt fehl                       | Der MSM-Scan-Befehl schlägt fehl.                                                                                                                                                                                                                                                                                                                                                                                                                                |
| WLAN- \_ reason- \_ Code \_ Netzwerk \_ nicht \_ verfügbar                | Das angegebene Netzwerk ist nicht verfügbar. Dieser Grund wird auch verwendet, wenn ein Konflikt zwischen den in einem XML-Profil und einer Schnittstelle und/oder Netzwerkfunktionen angegebenen Funktionen vorliegt. Wenn ein Profil z. b. die Verwendung von WPA2 angibt, wenn die NIC nur WPA unterstützt, wird dieser Fehlercode zurückgegeben. Wenn ein Profil die Verwendung des Modus "fps" angibt, wenn die NIC den PPS-Modus nicht unterstützt, wird dieser Fehlercode zurückgegeben.<br/> |
| WLAN- \_ Grund \_ Code \_ Profil \_ geändert \_ oder \_ gelöscht          | Das Profil wurde geändert oder gelöscht, bevor die Verbindung hergestellt wurde.                                                                                                                                                                                                                                                                                                                                                                               |
| WLAN- \_ Grund für \_ Code \_ Schlüssel stimmt nicht \_ überein.                          | Der Profil Schlüssel stimmt nicht mit dem Netzwerkschlüssel identisch.                                                                                                                                                                                                                                                                                                                                                                                                         |
| der WLAN- \_ Grund \_ Code \_ Benutzer \_ \_ antwortet nicht.                     | Der Benutzer antwortet nicht.                                                                                                                                                                                                                                                                                                                                                                                                                             |
| WLAN- \_ Grund \_ Code-AP-Profil ist \_ \_ \_ \_ \_ für Client nicht zulässig \_ . | Eine Anwendung hat versucht, mithilfe der [**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) -Funktion anstelle eines virtuellen Geräts ein drahtlos gehostetes Netzwerk Profil auf einen physischen Drahtlos Netzwerkadapter anzuwenden.                                                                                                                                                                                                                                                    |
| WLAN- \_ Grund \_ Code-AP- \_ \_ Profil \_ nicht \_ zulässig              | Eine Anwendung hat versucht, mithilfe der [**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) -Funktion anstelle eines virtuellen Geräts ein drahtlos gehostetes Netzwerk Profil auf einen physischen Drahtlos Netzwerkadapter anzuwenden.                                                                                                                                                                                                                                                    |



 

In der folgenden Tabelle sind die Fehlercodes für die Profil Validierung aufgeführt.



| Ursachencode                                                    | Bedeutung                                                                                                                                                                                                                                       |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ ungültiges \_ Profil \_ Schema für den WLAN-Reason Code                   | Das Profil ist gemäß dem Schema ungültig.                                                                                                                                                                                                  |
| WLAN- \_ Grund \_ Code \_ Profil \_ fehlt.                           | Das wlanprofile-Element fehlt.                                                                                                                                                                                                           |
| WLAN-Ursachen \_ \_ Code \_ ungültiger \_ Profil \_ Name.                     | Der Name des Profils ist ungültig.                                                                                                                                                                                                           |
| WLAN-Ursachen \_ \_ Code \_ ungültiger \_ \_ Profiltyp.                     | Der Typ des Profils ist ungültig.                                                                                                                                                                                                           |
| der WLAN-Ursachen \_ \_ Code ist \_ ungültig \_ \_ .                         | Der PHY-Typ ist ungültig.                                                                                                                                                                                                                      |
| die MSM-Sicherheit für den WLAN- \_ Grund \_ \_ \_ \_ fehlt.                     | Die MSM-Sicherheitseinstellungen fehlen.                                                                                                                                                                                                        |
| WLAN-Ursachen \_ \_ Code \_ IHV- \_ Sicherheit \_ \_ wird nicht unterstützt              | Die Sicherheitseinstellungen für den unabhängigen Hardwarehersteller (IHV) fehlen.                                                                                                                                                                          |
| WLAN-Ursachen \_ \_ Code \_ IHV \_ Oui \_ stimmt nicht überein.                         | Das IHV-Profil "Oui" entsprach nicht dem Adapter "Oui".                                                                                                                                                                                       |
| der WLAN-Ursachen \_ \_ Code \_ IHV \_ Oui \_ fehlt.                          | Die IHV-Oui-Einstellungen fehlen.                                                                                                                                                                                                             |
| der WLAN-Grund für die \_ \_ \_ IHV- \_ Einstellungen \_ fehlt.                     | Die IHV-Sicherheitseinstellungen fehlen.                                                                                                                                                                                                        |
| WLAN-Ursachen \_ \_ Code- \_ IHV- \_ Konnektivität \_ nicht \_ unterstützt          | Eine Anwendung hat versucht, ein IHV-Profil auf einen Adapter anzuwenden, der keine IHV-Konnektivitätseinstellungen unterstützt.                                                                                                                                   |
| Sicherheit des WLAN-Ursachen \_ \_ Codes \_ \_                         | Der Sicherheits Einstellungs Konflikt.                                                                                                                                                                                                               |
| Sicherheit für den WLAN- \_ Grund \_ \_ \_ fehlt                          | Die Sicherheitseinstellungen fehlen.                                                                                                                                                                                                            |
| WLAN-Ursachen \_ \_ Code \_ ungültiger \_ BSS- \_ Typ                         | Der BSS-Typ ist ungültig.                                                                                                                                                                                                                    |
| WLAN \_ \_ -Ursachen Code \_ ungültiger \_ Ad-hoc- \_ Verbindungs \_ Modus           | Die automatische Verbindung kann für ein Ad-hoc-Netzwerk nicht festgelegt werden.                                                                                                                                                                                     |
| WLAN \_ \_ -Ursachen \_ Code \_ nicht \_ \_ für \_ Ad-hoc-Broadcast festgelegt            | Nicht-Broadcast kann für ein Ad-hoc-Netzwerk nicht festgelegt werden.                                                                                                                                                                                            |
| \_ \_ \_ automatischer \_ Switch für den WLAN \_ -Grund \_ für \_ Ad-hoc festgelegt              | Der automatische Switch kann für ein Ad-hoc-Netzwerk nicht festgelegt werden.                                                                                                                                                                                              |
| \_ \_ \_ Automatischer Verbindungswechsel für den WLAN-Grund \_ \_ für die \_ \_ Manuelle \_ Verbindung | Der automatische Switch kann nicht für ein manuelles Verbindungsprofil festgelegt werden.                                                                                                                                                                                    |
| WLAN-Ursachen \_ \_ Code \_ IHV \_ Security \_ Onex \_ fehlt               | Die IHV 802.1 x-Sicherheitseinstellungen fehlen.                                                                                                                                                                                                 |
| die \_ SSID für das WLAN \_ -Grund Code Profil ist \_ \_ \_ ungültig                     | Die SSID im Profil ist ungültig oder fehlt.                                                                                                                                                                                                |
| WLAN-Ursachen \_ \_ Code \_ zu \_ viele \_ SSID                            | Im Profil wurden zu viele SSIDs angegeben.                                                                                                                                                                                                 |
| WLAN-Ursachen \_ \_ Code- \_ IHV- \_ Konnektivität \_ nicht \_ unterstützt          |                                                                                                                                                                                                                                               |
| WLAN-Ursachen Code ungültige \_ \_ \_ \_ Maximale \_ Anzahl \_ von \_ Clients \_ für \_ AP     | Eine Anwendung hat versucht, mithilfe der [**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) -Funktion ein drahtlos gehostetes Netzwerk Profil auf eine physische Netzwerkadapter-NIC anzuwenden und einen unzulässigen Wert für die maximal zulässige Anzahl von Clients anzugeben. |
| \_ \_ \_ Ungültiger Kanal für den WLAN-Grund \_                           | Der angegebene Kanal ist ungültig.                                                                                                                                                                                                             |
| der WLAN-Ursachen \_ \_ Code \_ Vorgangs \_ Modus \_ \_ wird nicht unterstützt.            |                                                                                                                                                                                                                                               |
| WLAN-Grund für das \_ \_ \_ automatische \_ AP-Profil ist \_ \_ nicht \_ zulässig            | Interner Betriebssystem Fehler beim drahtlos gehosteten Netzwerk.                                                                                                                                                                 |
| die automatische Verbindung mit dem WLAN- \_ Grund ist \_ \_ \_ \_ nicht \_ zulässig.             |                                                                                                                                                                                                                                               |



 

In der folgenden Tabelle sind Fehlercodes für die MSM-Netzwerk Inkompatibilität aufgeführt.



| Ursachencode                                            | Bedeutung                                                          |
|--------------------------------------------------------|------------------------------------------------------------------|
| \_ \_ \_ \_ vom Betriebssystem nicht unterstützter Sicherheits \_ Satz \_ für den \_ WLAN-Grund | Die Sicherheitseinstellungen werden vom Betriebssystem nicht unterstützt. |
| \_ \_ \_ nicht unterstützter \_ Sicherheits \_ Satz für den WLAN-Reason Code         | Die Sicherheitseinstellungen werden nicht unterstützt.                         |
| \_ \_ \_ \_ \_ nicht Übereinstimmung des WLAN-Ursachen Codes                 | Der BSS-Typ stimmt nicht mit.                                     |
| \_ \_ \_ \_ \_ nicht Übereinstimmung bei WLAN-Grund Code-PHY                 | Der PHY-Typ stimmt nicht mit.                                     |
| WLAN- \_ Grund für \_ Code \_ Datarate \_ stimmen nicht zu                  | Die Datenrate stimmt nicht mit ab.                                    |



 

In der folgenden Tabelle sind Fehlercodes für MSM-Verbindungsfehler aufgeführt.



| Ursachencode                                       | Bedeutung                                                                                                      |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Benutzer des WLAN-Ursachen \_ \_ Codes \_ \_ abgebrochen               | Der Benutzer hat den Vorgang abgebrochen.                                                                             |
| Zuordnungs Fehler bei der WLAN- \_ Ursache \_ \_ \_          | Der Treiber wurde beim Zuordnen getrennt.                                                                       |
| Zeitüberschreitung bei der WLAN- \_ Ursache \_ \_ \_          | Timeout bei der Zuordnung.                                                                                       |
| WLAN-Ursachen \_ \_ Code \_ vor \_ Sicherheits \_ Fehlern        | Sicherheitsfehler vor der Zuordnung.                                                                            |
| \_Fehler beim \_ Starten \_ der \_ Sicherheit \_ für den WLAN-Grund      | Fehler beim Starten der Sicherheit nach der Zuordnung.                                                                  |
| \_ \_ \_ Sicherheits \_ Fehler bei der WLAN-Ursache             | Sicherheit endet mit einem Fehler.                                                                               |
| WLAN-Ursachen \_ \_ Code \_ Sicherheits \_ Timeout             | Timeout für Sicherheits Vorgang.                                                                                |
| \_Fehler beim \_ \_ Roaming \_ des WLAN-Grunds              | Der Treiber wurde beim Roaming getrennt.                                                                           |
| WLAN- \_ Grund für \_ \_ roamingsicherheitsfehler \_ \_    | Fehler beim Starten der Sicherheit für das Roaming.                                                                        |
| WLAN \_ \_ -Ursachen Code \_ Ad-hoc- \_ Sicherheits \_ Fehler      | Fehler beim Starten der Sicherheit für den Ad-hoc-Peer.                                                                    |
| WLAN-Ursachen \_ \_ Code \_ Treiber \_ getrennt          | Der Treiber wurde getrennt.                                                                                         |
| Fehler des WLAN-Ursachen \_ \_ Code \_ Treibers \_ \_    | Fehler beim Ausführen einiger Vorgänge durch den Treiber.                                                                    |
| der WLAN-Ursachen \_ \_ Code \_ IHV ist \_ nicht \_ verfügbar.           | Der IHV-Dienst ist nicht verfügbar.                                                                            |
| der WLAN-Ursachen \_ \_ Code \_ antwortet IHV \_ nicht \_ .          | Timeout bei der Antwort des IHV-Dienstanbieter.                                                                 |
| Timeout für WLAN-Ursachen \_ \_ Code \_ Trennung \_           | Timeout beim Warten auf die Trennung des Treibers.                                                              |
| \_ \_ \_ interner \_ Fehler im WLAN-Grund             | Ein interner Fehler hat den Abschluss des Vorgangs verhindert.                                              |
| Timeout für den WLAN-Grund für die \_ \_ \_ Benutzeroberfläche \_ \_          | Timeout bei der Anforderung einer Benutzerinteraktion.                                                                        |
| WLAN-Ursachen \_ \_ Code \_ zu \_ viele \_ Sicherheits \_ Versuche | Roaming zu oft. Die Post-Sicherheit wurde nach fünf versuchen nicht abgeschlossen.                                         |
| Fehler beim Starten des WLAN- \_ Grund \_ Codes \_ \_ \_         | Ein interner Betriebssystem Fehler ist aufgetreten, der zu einem Fehler beim Starten des drahtlos gehosteten Netzwerks geführt hat. |



 

In der folgenden Tabelle sind die MSM-Sicherheitsfehler Codes aufgeführt.



| Ursachencode                                                             | Bedeutung                                                                                                                                                                                   |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WLAN- \_ Grund \_ Code- \_ msmsec- \_ Profil \_ ungültiger \_ Schlüssel \_ Index                | Der angegebene Schlüssel Index ist ungültig.                                                                                                                                                         |
| WLAN- \_ Grund \_ Code- \_ msmsec- \_ Profil- \_ PSK \_ vorhanden                       | Schlüssel erforderlich, PSK vorhanden.                                                                                                                                                                |
| Schlüssellänge für WLAN- \_ Grund \_ Code des \_ msmsec- \_ Profils \_ \_                        | Ungültige Schlüssellänge.                                                                                                                                                                       |
| WLAN- \_ Grund \_ Code- \_ msmsec- \_ Profil \_ Länge PSK \_                        | Ungültige PSK-Länge.                                                                                                                                                                       |
| WLAN- \_ Grund \_ Code- \_ msmsec- \_ Profil keine Authentifizierungs \_ \_ \_ Verschlüsselung \_ angegeben        | Es wurden keine Authentifizierungs-/Chiffre Paare angegeben.                                                                                                                                                           |
| WLAN- \_ reason \_ Code \_ msmsec- \_ Profil \_ zu viele Authentifizierungs \_ \_ \_ Chiffre \_ angegeben | Es wurden zu viele Authentifizierungs-/Chiffre Paare angegeben.                                                                                                                                                     |
| WLAN- \_ Grund \_ Code- \_ msmsec- \_ Profil \_ duplikatauthentifizierung duplizieren \_ \_            | Das Profil enthält ein doppeltes Authentifizierungs-/Chiffre Paar.                                                                                                                                              |
| WLAN- \_ Grund \_ Code- \_ msmsec- \_ Profil \_ rawData \_ ungültig                   | Profil Rohdaten sind ungültig.                                                                                                                                                              |
| WLAN- \_ Grund \_ Code- \_ msmsec- \_ Profil \_ ungültige Authentifizierungs \_ \_ Chiffre              | Ungültige Authentifizierung/Chiffre Kombination.                                                                                                                                                          |
| WLAN- \_ Grund \_ Code- \_ msmsec- \_ Profil \_ Onex \_ deaktiviert                     | 802.1 x ist deaktiviert, wenn es aktiviert werden muss.                                                                                                                                        |
| WLAN- \_ Grund \_ Code- \_ msmsec- \_ Profil \_ Onex \_ aktiviert                      | 802.1 x ist aktiviert, wenn es deaktiviert werden muss.                                                                                                                                        |
| WLAN- \_ Grund \_ Code- \_ msmsec- \_ Profil \_ ungültiger \_ pmkcache- \_ Modus            | Ungültiger PMK-Cache Modus.                                                                                                                                                                   |
| WLAN- \_ Grund \_ Code- \_ msmsec- \_ Profil \_ ungültige \_ pmkcache- \_ Größe            | Ungültige PMK-Cache Größe.                                                                                                                                                                   |
| WLAN- \_ Grund \_ Code- \_ msmsec- \_ Profil \_ ungültige \_ pmkcache- \_ TTL             | Ungültige PMK-Cache Gültigkeitsdauer.                                                                                                                                                                    |
| WLAN- \_ Grund \_ Code- \_ msmsec- \_ Profil \_ ungültiger \_ PreAuth- \_ Modus             | Ungültiger PreAuth-Modus.                                                                                                                                                                     |
| WLAN- \_ Grund \_ Code- \_ msmsec- \_ Profil \_ ungültige \_ PreAuth- \_ Drosselung         | Ungültige PreAuth-Drosselung.                                                                                                                                                                 |
| WLAN- \_ Grund \_ Code- \_ msmsec- \_ Profil- \_ Vorauthentifizierung ist \_ nur \_ aktiviert.             | PreAuth aktiviert, wenn der PMK-Cache deaktiviert ist.                                                                                                                                               |
| WLAN- \_ reason \_ Code- \_ msmsec-Funktions \_ \_ Netzwerk                         | Fehler bei der Funktions Übereinstimmung im Netzwerk.                                                                                                                                                    |
| WLAN- \_ Grund \_ Code- \_ msmsec- \_ Funktions- \_ NIC                             | Fehler bei der Funktions Übereinstimmung bei NIC.                                                                                                                                                        |
| WLAN-Ursachen \_ \_ Code- \_ msmsec-Funktions \_ \_ Profil                         | Fehler bei der Funktions Übereinstimmung im Profil.                                                                                                                                                    |
| Ermittlung \_ der \_ \_ msmsec- \_ Funktionen \_ für den WLAN-Grund                       | Der angegebene Funktionstyp wird vom Netzwerk nicht unterstützt.                                                                                                                                       |
| WLAN- \_ Grund \_ Code- \_ msmsec- \_ Profil \_ Passphrase \_ Char                   | Die Passphrase enthält ein ungültiges Zeichen.                                                                                                                                                    |
| WLAN- \_ Grund \_ Code- \_ msmsec- \_ Profil \_ Keymaterial \_ Char                  | Das Schlüsselmaterial enthält ein ungültiges Zeichen.                                                                                                                                                  |
| WLAN- \_ reason \_ Code- \_ msmsec- \_ Profil \_ falscher \_ KeyType                     | Der angegebene Schlüsseltyp stimmt nicht mit dem Schlüsselmaterial identisch.                                                                                                                                   |
| Kombination aus WLAN- \_ Grund \_ Code \_ msmsec \_ gemischte \_ Zelle                                 | Eine gemischte Zelle wird vermutet. Der Zugriffspunkt weist nicht darauf hin, dass er mit einem Datenschutz fähigen Profil kompatibel ist.                                                                                  |
| WLAN-Ursachen \_ \_ Code \_ msmsec \_ Profil \_ auth- \_ Timer \_ ungültig              | Die Anzahl von authentifizierungtimern oder die im Profil angegebene Anzahl von Timeouts ist ungültig.                                                                                        |
| WLAN \_ \_ -Grund Code \_ -msmsec \_ -Profil \_ ungültiger \_ GKEY \_ -INTV                | Das im Profil angegebene Update Intervall für Gruppenschlüssel ist ungültig.                                                                                                                        |
| WLAN- \_ reason \_ Code- \_ msmsec- \_ Übergangs \_ Netzwerk                         | Ein "Übergangs Netzwerk" wird vermutet. Die Legacy-802,11-Sicherheit wird für den nächsten Authentifizierungs Versuch verwendet.                                                                                  |
| WLAN- \_ Grund \_ Code- \_ msmsec- \_ Profil \_ Schlüssel \_ nicht zugeordnet \_                | Der Schlüssel enthält Zeichen, die nicht im ASCII-Zeichensatz enthalten sind.                                                                                                                      |
| WLAN- \_ reason \_ Code \_ msmsec-Funktions \_ \_ Profil Authentifizierung \_                   | Fehler bei der Funktions Übereinstimmung, weil das Netzwerk die Authentifizierungsmethode im Profil nicht unterstützt.                                                                                 |
| WLAN- \_ Grund \_ Code- \_ msmsec- \_ Fähigkeits \_ Profil \_ Chiffre                 | Fehler bei der Funktions Übereinstimmung, weil das Netzwerk den Verschlüsselungsalgorithmus im Profil nicht unterstützt.                                                                                      |
| Internet- \_ reason \_ Code- \_ msmsec- \_ Profil \_ sicherer \_ Modus                         | Der Wert des FPS 140-2-Modus im Profil ist ungültig.                                                                                                                                          |
| WLAN- \_ Grund \_ Code- \_ msmsec- \_ Fähigkeits \_ Profil- \_ \_ \_ NIC        | Das Profil erfordert den Modus "fps 140-2", der von der Netzwerkschnittstellenkarte (NIC) nicht unterstützt wird.                                                                                                 |
| WLAN- \_ Grund \_ Code- \_ msmsec- \_ Fähigkeits \_ Profil \_ sicherer \_ Modus \_ NW         | Das Profil erfordert den Modus "fps 140-2", der vom Netzwerk nicht unterstützt wird.                                                                                                                      |
| WLAN- \_ Grund \_ Code- \_ msmsec- \_ Profil \_ nicht unterstützte \_ Authentifizierung                  | Profile gibt eine nicht unterstützte Authentifizierungsmethode an.                                                                                                                               |
| WLAN- \_ Grund \_ Code- \_ msmsec- \_ Profil \_ wird nicht unterstützt \_ Chiffre                | Profile gibt eine nicht unterstützte Chiffre an.                                                                                                                                                  |
| WLAN-Ursachen \_ \_ Code \_ msmsec \_ UI- \_ Anforderungs \_ Fehler                        | Fehler beim hinzustellen der Benutzeroberflächen Anforderung.                                                                                                                                               |
| WLAN- \_ reason \_ Code \_ msmsec- \_ Funktion \_ MFP-NW- \_ \_ NIC                    | Das drahtlose LAN erfordert den Management Frame-Schutz (MFP), und die Netzwerkschnittstelle unterstützt MFP nicht. Weitere Informationen finden Sie unter IEEE 802.11 w-Zusatz zum 802,11-Standard. |



 

In der folgenden Tabelle sind MSM-Verbindungsfehler Codes aufgeführt.



| Ursachencode                                             | Bedeutung                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| WLAN-Ursachen \_ \_ Code \_ msmsec \_ auth \_ Start \_ Timeout        | die 802.1 x-Authentifizierung wurde nicht innerhalb der konfigurierten Zeit gestartet.                                                      |
| WLAN-Ursachen \_ \_ Code \_ msmsec \_ auth \_ Erfolgs \_ Timeout      | die 802.1 x-Authentifizierung wurde nicht innerhalb der konfigurierten Zeit beendet.                                                   |
| WLAN- \_ reason \_ Code- \_ \_ \_ Start \_ Timeout für msmsec-Schlüssel         | Der dynamische Schlüsselaustausch wurde nicht innerhalb der konfigurierten Zeit gestartet.                                                       |
| Erfolgs Timeout für den WLAN-Grund für den \_ \_ \_ msmsec- \_ Schlüssel \_ \_       | Der dynamische Schlüsselaustausch konnte nicht innerhalb der konfigurierten Zeit beendet werden.                                                    |
| WLAN- \_ Grund \_ Code \_ msmsec \_ m3 \_ fehlende \_ Schlüssel \_ Daten      | Nachricht 3 von 4-Wege-Handshake hat keine Schlüsseldaten.                                                                    |
| WLAN- \_ Grund \_ Code \_ msmsec \_ m3 \_ fehlende \_ IE             | Nachricht 3 von 4-Wege-Handshake hat keine IE.                                                                          |
| WLAN- \_ Grund \_ Code \_ msmsec \_ m3 \_ fehlender GRP- \_ \_ Schlüssel       | Nachricht 3 von 4-Wege-Handshake hat keinen GRP-Schlüssel.                                                                     |
| WLAN-Ursachen \_ \_ Code \_ msmsec \_ PR- \_ IE \_ -Abgleich            | Fehler beim Abgleichen der Sicherheitsfunktionen von IE in m3.                                                               |
| WLAN- \_ Grund \_ Code \_ msmsec \_ Sek. \_ IE \_ -Abgleich           | Fehler beim Abgleichen der Sicherheitsfunktionen des sekundären Internet Explorer in m3.                                                     |
| WLAN-Ursachen \_ \_ Code \_ msmsec \_ nicht \_ paar Weise \_ Schlüssel           | Erfordert einen paar weisen Schlüssel, aber Zugriffspunkt (Access Point, AP) hat nur Gruppenschlüssel konfiguriert.                                        |
| WLAN-Ursachen \_ \_ Code \_ msmsec \_ G1 \_ fehlende \_ Schlüssel \_ Daten      | Die Meldung 1 des Gruppenschlüssel Handshakes weist keine Schlüsseldaten auf.                                                                |
| WLAN-Ursachen \_ \_ Code \_ msmsec \_ G1 \_ fehlender \_ GRP- \_ Schlüssel       | Die Meldung 1 des Gruppenschlüssel Handshakes hat keinen Gruppenschlüssel.                                                               |
| WLAN-Ursachen \_ \_ Code \_ msmsec- \_ Peer hat \_ \_ unsicher angegeben   | Zurücksetzen des sicheren Bits nach dem Sichern der Verbindung                                                                |
| WLAN-Ursachen \_ \_ Code \_ msmsec \_ No \_ Authenticator           | 802.1 x hat angegeben, dass kein Authentifikator vorhanden ist, aber das Profil erfordert ein solches.                                   |
| WLAN-Ursachen \_ \_ Code \_ msmsec \_ NIC- \_ Fehler                | Fehler bei den Grundeinstellungen für die NIC.                                                                                 |
| WLAN-Ursachen \_ \_ Code- \_ msmsec \_ abgebrochen                   | Der Vorgang wurde von einem Aufrufer abgebrochen.                                                                              |
| WLAN- \_ Grund \_ Code- \_ msmsec- \_ Schlüssel \_ Format                 | Das eingegebene Schlüsselformat weist kein gültiges Format auf.                                                                     |
| der WLAN-Grund für die \_ \_ \_ msmsec-Herabstufung wurde \_ \_ erkannt         | Ein sicherheitsdowngrade wurde erkannt.                                                                               |
| WLAN-Ursachen \_ \_ Code \_ msmsec \_ PSK-Konflikt \_ \_ vermutet    | Es wird ein PSK-Konflikt vermutet.                                                                                     |
| \_Fehler beim \_ \_ \_ erzwungenen \_ WLAN-Ursachen Code             | Ein erzwungener Fehler ist aufgetreten, da die Verbindungsmethode nicht sicher war.                                         |
| WLAN-Ursachen \_ \_ Code \_ msmsec \_ m3 \_ zu \_ viele \_ rsnie        | Nachricht 3 von 4-Wege-Handshake enthält zu viele RSN-IE (RSN).                                                     |
| WLAN- \_ Grund \_ Code \_ msmsec \_ m2 \_ fehlende \_ Schlüssel \_ Daten      | Nachricht 2 von 4-Wege-Handshake hat keine Schlüsseldaten (RSN Adhoc).                                                        |
| WLAN-Ursachen \_ \_ Code \_ msmsec \_ m2 \_ fehlende \_ IE             | Nachricht 2 von 4-Wege-Handshake hat keine IE (RSN Adhoc).                                                              |
| WLAN-Ursachen \_ \_ Code \_ msmsec \_ auth \_ WCN \_ abgeschlossen        |                                                                                                                  |
| WLAN-Ursachen \_ \_ Code \_ msmsec \_ Sicherheits \_ Benutzeroberfläche \_ Fehler       | Fehler bei der Benutzeroberflächen Anforderung, weil die Anforderung nicht in die Warteschlange eingereiht werden konnte oder weil der Benutzer die Anforderung abgebrochen hat. |
| WLAN- \_ Grund \_ Code \_ msmsec \_ m3 \_ fehlender \_ Mgmt-GRP- \_ \_ Schlüssel | Nachricht 3 von 4-Wege-Handshake hat keinen Mgmt-Gruppenschlüssel (RSN).                                                        |
| WLAN- \_ reason \_ Code \_ msmsec \_ G1 \_ fehlender \_ Mgmt-GRP- \_ \_ Schlüssel | Die Meldung 1 der Gruppenschlüssel Hand Shake weist keinen Gruppen Verwaltungs Schlüssel auf.                                                    |



 

In der folgenden Tabelle sind die 802.1 x-Ursachen Codes aufgeführt. Schema Elemente, die nachstehend benannt sind, werden im Onex-Schema definiert und im WLAN-Profil angegeben.



| Ursachencode                                         | Bedeutung                                                                                                                                                                            |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| der \_ Benutzer kann von Onex nicht \_ \_ identifiziert \_ werden.                    | Es ist kein Benutzer für die 802.1 x-Authentifizierung verfügbar. Dieser Fehler kann auftreten, wenn die Computer Authentifizierung deaktiviert ist und kein Benutzer am Computer angemeldet ist.                              |
| Onex- \_ Identität \_ nicht \_ gefunden.                          | Die 802.1 x-Identität konnte nicht gefunden werden.                                                                                                                                            |
| Onex- \_ Benutzeroberfläche \_ deaktiviert                                  | Die Authentifizierung konnte nur über die Benutzeroberfläche abgeschlossen werden, und diese Schnittstelle konnte nicht angezeigt werden.                                                                       |
| Onex- \_ EAP- \_ Fehler \_ empfangen                        | Die EAP-Authentifizierung ist fehlgeschlagen.                                                                                                                                                     |
| der Onex- \_ Authentifikator ist \_ nicht \_ mehr \_ vorhanden.            | Der 802.1 x-Authentifikator wurde vom Netzwerk entfernt.                                                                                                                               |
| Onex- \_ Profil \_ Version \_ nicht \_ unterstützt              | Die angegebene Version des Onex-Profils wird nicht unterstützt.                                                                                                                         |
| \_ \_ ungültige Länge des Onex-Profils \_                      | Das Onex-Profil weist eine ungültige Länge auf.                                                                                                                                            |
| nicht zulässiger \_ \_ \_ EAP- \_ Typ des Onex-Profils                | Der im Onex-Profil angegebene EAP-Typ (möglicherweise vom eaptype-Element bereitgestellt) ist nicht zulässig.                                                                               |
| Onex- \_ Profil \_ ungültiger \_ EAP- \_ Typ oder- \_ \_ Flag.         | Der im Onex-Profil angegebene EAP-Typ (möglicherweise vom eaptype-Element bereitgestellt) ist ungültig, oder eines der EAP-Flags (möglicherweise im eapconfig-Element angegeben) ist ungültig. |
| Onex- \_ Profil \_ ungültige \_ Onex- \_ Flags.                 | Die Supplicant-Flags (möglicherweise im eapconfig-Element bereitgestellt) im Onex-Profil sind ungültig.                                                                                 |
| Onex- \_ Profil \_ ungültiger \_ Zeitgeber \_ Wert                | Ein im Onex-Profil festgelegter Timer (möglicherweise vom heldperiod-, authperiod-oder startperiod-Element bereitgestellt) ist ungültig.                                                        |
| Onex- \_ Profil \_ ungültiger \_ Supplicant- \_ Modus            | Der im Onex-Profil angegebene Supplicant-Modus (möglicherweise vom supplicantmode-Element bereitgestellt) ist ungültig.                                                                    |
| Onex- \_ Profil \_ Ungültiger Authentifizierungs \_ \_ Modus.                  | Der im Onex-Profil angegebene Authentifizierungsmodus (möglicherweise vom authmode-Element bereitgestellt) ist ungültig.                                                                      |
| Onex- \_ Profil \_ ungültige \_ EAP- \_ Verbindungs \_ Eigenschaften. | Die im Onex-Profil angegebenen Verbindungs Eigenschaften (möglicherweise vom eapconfig-Element bereitgestellt) sind ungültig.                                                                  |



 

## <a name="remarks"></a>Bemerkungen

Unter Windows XP mit Service Pack 3 (SP3) und in der Wireless LAN-API für Windows XP mit Service Pack 2 (SP2) werden eine begrenzte Anzahl von Grund Codes unterstützt. Die Profil Überprüfungs-Fehlercodes, die unter Windows XP mit SP3 und in der Wireless LAN-API für Windows XP mit SP2 unterstützt werden, lauten wie folgt:

-   \_ \_ \_ ungültiges \_ Profil \_ Schema für den WLAN-Reason Code
-   WLAN- \_ Grund \_ Code \_ Profil \_ fehlt.
-   die \_ SSID für das WLAN \_ -Grund Code Profil ist \_ \_ \_ ungültig

Die MSM-Sicherheitsfehler Codes, die unter Windows XP mit SP3 und in der Wireless LAN-API für Windows XP mit SP2 unterstützt werden, lauten wie folgt:

-   WLAN- \_ Grund \_ Code- \_ msmsec- \_ Profil \_ ungültiger \_ Schlüssel \_ Index
-   Schlüssellänge für WLAN- \_ Grund \_ Code des \_ msmsec- \_ Profils \_ \_
-   WLAN- \_ Grund \_ Code- \_ msmsec- \_ Profil \_ Länge PSK \_
-   WLAN- \_ Grund \_ Code- \_ msmsec- \_ Profil \_ ungültige Authentifizierungs \_ \_ Chiffre
-   WLAN- \_ Grund \_ Code- \_ msmsec- \_ Profil \_ Onex \_ deaktiviert
-   WLAN- \_ Grund \_ Code- \_ msmsec- \_ Profil \_ Onex \_ aktiviert
-   WLAN- \_ reason \_ Code- \_ msmsec-Funktions \_ \_ Netzwerk
-   WLAN- \_ Grund \_ Code- \_ msmsec- \_ Funktions- \_ NIC
-   WLAN- \_ Grund \_ Code- \_ msmsec- \_ Profil \_ Keymaterial \_ Char
-   WLAN- \_ reason \_ Code- \_ msmsec- \_ Profil \_ falscher \_ KeyType

Die 802.1 x-Fehlercodes, die unter Windows XP mit SP3 und in der Wireless LAN-API für Windows XP mit SP2 unterstützt werden, lauten wie folgt:

-   \_ \_ ungültige Länge des Onex-Profils \_
-   Onex- \_ Profil \_ ungültiger \_ EAP- \_ Typ oder- \_ \_ Flag.
-   Onex- \_ Profil \_ Ungültiger Authentifizierungs \_ \_ Modus.
-   Onex- \_ Profil \_ ungültige \_ EAP- \_ Verbindungs \_ Eigenschaften.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]<br/>                  |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                 |
| Verteilbare Komponente<br/>          | Drahtlose LAN-API für Windows XP mit SP2<br/>                                  |
| Header<br/>                   | <dl> <dt>Wlanapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wlanreasoncodedestring**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring)
</dt> <dt>

[**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)
</dt> </dl>

 

 
