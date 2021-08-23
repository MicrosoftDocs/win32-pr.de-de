---
description: Gibt den Grund für den Fehler eines WLAN-Vorgangs an.
ms.assetid: 7b267f0b-b3f7-4729-bab4-de3bdd0a35a2
title: WLAN_REASON_CODE (Wlanapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f24b0ab902610408eb7b80b4a962fcc81d4598244714b8f30f0ebf350a7e628
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064560"
---
# <a name="wlan_reason_code"></a>\_ \_ WLAN-GRUNDCODE

Der **TYP WLAN REASON \_ \_ CODE** gibt an, warum ein WLAN-Vorgang fehlgeschlagen ist.

Sie können die [**WlanReasonCodeToString-Funktion**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring) verwenden, um einen numerischen Grundcode (z. B. 0x00050007) seiner Textbe bedeutung zu zuordnen. Sie können auch die Nachschlagetabelle verwenden, um den numerischen Wert des Grundcodes zu interpretieren. Informationen zum Anzeigen der Nachschlagetabelle finden Sie in Anhang E: Zuordnung von Grundcodes zu Ereignismeldungen im Dokument Troubleshooting [Windows Vista 802.11 Wireless Connections](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10)).


```C++
typedef DWORD WLAN_REASON_CODE, *PWLAN_REASON_CODE;
```



In der folgenden Tabelle sind allgemeine Fehlercodes aufgeführt.



| Ursachencode                 | Bedeutung                            |
|-----------------------------|------------------------------------|
| WLAN \_ REASON \_ CODE \_ SUCCESS | Der Vorgang ist erfolgreich.            |
| \_WLAN-GRUNDCODE \_ \_ UNBEKANNT | Die Ursache für den Fehler ist unbekannt. |



 

In der folgenden Tabelle sind fehlercodes für die automatische Konfiguration aufgeführt.



| Ursachencode                                  | Bedeutung                                         |
|----------------------------------------------|-------------------------------------------------|
| WLAN \_ REASON CODE NETWORK NOT COMPATIBLE \_ \_ (WLAN-GRUNDCODE: \_ NETZWERK NICHT \_ KOMPATIBEL) | Das Drahtlosnetzwerk ist nicht kompatibel.         |
| \_ \_ WLAN-GRUNDCODEPROFIL \_ NICHT \_ \_ KOMPATIBEL | Das Drahtlosnetzwerkprofil ist nicht kompatibel. |



 

In der folgenden Tabelle sind die Fehlercodes für automatische Verbindungen aufgeführt.



| Ursachencode                                                | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_WLAN-GRUNDCODE \_ KEINE AUTOMATISCHE \_ \_ \_ VERBINDUNG                   | Das Profil gibt keine automatische Verbindung an.                                                                                                                                                                                                                                                                                                                                                                                                               |
| \_WLAN-GRUNDCODE \_ NICHT \_ \_ SICHTBAR                           | Das Drahtlosnetzwerk ist nicht sichtbar.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| WLAN \_ REASON \_ CODE \_ GP \_ DENIED                             | Das Drahtlosnetzwerk wird durch eine Gruppenrichtlinie blockiert.                                                                                                                                                                                                                                                                                                                                                                                                        |
| WLAN \_ REASON \_ CODE \_ USER \_ DENIED                           | Das Drahtlosnetzwerk wird vom Benutzer blockiert.                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_WLAN-GRUNDCODE \_ \_ BSS-TYP \_ NICHT \_ \_ ZULÄSSIG                | Der BSS-Typ (Basic Service Set) ist auf diesem Drahtlosadapter nicht zulässig.                                                                                                                                                                                                                                                                                                                                                                               |
| \_ \_ WLAN-GRUNDCODE \_ IN DER \_ \_ FEHLERLISTE                       | Das Drahtlosnetzwerk befindet sich in der Fehlerliste.                                                                                                                                                                                                                                                                                                                                                                                                             |
| WLAN \_ REASON \_ CODE \_ IN \_ BLOCKED \_ LIST                      | Das Drahtlosnetzwerk befindet sich in der Liste der blockierten Netzwerke.                                                                                                                                                                                                                                                                                                                                                                                                            |
| WLAN \_ REASON \_ CODE \_ SSID \_ LIST \_ TOO \_ LONG                  | Die Größe der Liste der Dienstsatzbezeichner (Service Set Identifiers, SSID) überschreitet die maximale Größe, die vom Adapter unterstützt wird.                                                                                                                                                                                                                                                                                                                                                  |
| FEHLER BEIM \_ \_ WLAN-GRUNDCODE \_ FÜR DEN \_ \_ VERBINDUNGSAUFRUF                    | Der MsM-Verbindungsaufruf (Media Specific Module) schlägt fehl.                                                                                                                                                                                                                                                                                                                                                                                                     |
| FEHLER BEIM \_ \_ WLAN-GRUNDCODESCAN-AUFRUF \_ \_ \_                       | Der MSM-Überprüfungsaufruf schlägt fehl.                                                                                                                                                                                                                                                                                                                                                                                                                                |
| WLAN \_ REASON CODE NETWORK NOT AVAILABLE \_ \_ (WLAN-GRUNDCODENETZWERK \_ NICHT \_ VERFÜGBAR)                | Das angegebene Netzwerk ist nicht verfügbar. Dieser Grundcode wird auch verwendet, wenn ein Konflikt zwischen funktionen besteht, die in einem XML-Profil und einer Schnittstelle und/oder Netzwerkfunktionen angegeben sind. Wenn ein Profil beispielsweise die Verwendung von WPA2 angibt, wenn die NIC nur WPA unterstützt, wird dieser Fehlercode zurückgegeben. Wenn ein Profil die Verwendung des FIPS-Modus angibt, wenn die NIC den FIPS-Modus nicht unterstützt, wird dieser Fehlercode zurückgegeben.<br/> |
| WLAN \_ REASON CODE PROFILE CHANGED OR DELETED (WLAN-GRUNDCODEPROFIL \_ GEÄNDERT ODER \_ \_ \_ \_ GELÖSCHT)          | Das Profil wurde geändert oder gelöscht, bevor die Verbindung hergestellt wurde.                                                                                                                                                                                                                                                                                                                                                                               |
| NICHT \_ ÜBEREINSTIMMENDE \_ WLAN-URSACHECODESCHLÜSSEL \_ \_                          | Der Profilschlüssel passt nicht zum Netzwerkschlüssel.                                                                                                                                                                                                                                                                                                                                                                                                         |
| WLAN \_ REASON CODE USER NOT RESPOND (WLAN-GRUNDCODE: \_ BENUTZER REAGIERT \_ \_ \_ NICHT)                     | Der Benutzer reagiert nicht.                                                                                                                                                                                                                                                                                                                                                                                                                             |
| WLAN \_ REASON CODE AP PROFILE NOT ALLOWED FOR CLIENT (WLAN-GRUNDCODE-AP-PROFIL \_ FÜR CLIENT NICHT \_ \_ \_ \_ \_ \_ ZULÄSSIG) | Eine Anwendung hat versucht, ein drahtlos gehostetes Netzwerkprofil auf einen physischen Drahtlosnetzwerkadapter mithilfe der [**WlanSetProfile-Funktion**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) und nicht auf ein virtuelles Gerät anzuwenden.                                                                                                                                                                                                                                                    |
| WLAN \_ REASON CODE AP PROFILE NOT ALLOWED (WLAN-GRUNDCODE-AP-PROFIL \_ NICHT \_ \_ \_ \_ ZULÄSSIG)              | Eine Anwendung hat versucht, ein drahtlos gehostetes Netzwerkprofil auf einen physischen Drahtlosnetzwerkadapter mithilfe der [**WlanSetProfile-Funktion**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) und nicht auf ein virtuelles Gerät anzuwenden.                                                                                                                                                                                                                                                    |



 

In der folgenden Tabelle werden Fehlercodes für die Profilvalidierung aufgeführt.



| Ursachencode                                                    | Bedeutung                                                                                                                                                                                                                                       |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ WLAN-GRUNDCODE: \_ \_ UNGÜLTIGES \_ PROFILSCHEMA                   | Das Profil ist gemäß dem Schema ungültig.                                                                                                                                                                                                  |
| WLAN \_ REASON CODE PROFILE MISSING (WLAN-GRUNDCODEPROFIL \_ \_ \_ FEHLT)                           | Das WLANProfile-Element fehlt.                                                                                                                                                                                                           |
| \_WLAN-GRUNDCODE \_ \_ \_ UNGÜLTIGER \_ PROFILNAME                     | Der Name des Profils ist ungültig.                                                                                                                                                                                                           |
| \_WLAN-GRUNDCODE \_ \_ \_ UNGÜLTIGER \_ PROFILTYP                     | Der Profiltyp ist ungültig.                                                                                                                                                                                                           |
| WLAN \_ REASON \_ CODE \_ INVALID \_ PHY \_ TYPE                         | Der PHY-Typ ist ungültig.                                                                                                                                                                                                                      |
| WLAN \_ REASON \_ CODE \_ MSM SECURITY MISSING (WLAN-GRUNDCODE: \_ MSM-SICHERHEIT \_ FEHLT)                     | Die MSM-Sicherheitseinstellungen fehlen.                                                                                                                                                                                                        |
| \_WLAN-GRUNDCODE \_ \_ IHV-SICHERHEIT \_ NICHT \_ \_ UNTERSTÜTZT              | Die Sicherheitseinstellungen des unabhängigen Hardwareanbieters (Independent Hardware Vendor, IHV) fehlen.                                                                                                                                                                          |
| WLAN \_ REASON \_ CODE \_ IHV \_ OUI \_ MISMATCH                         | Die Organisationseinheit des IHV-Profils hat nicht mit der Adapter-OUI überein übereinbeigt.                                                                                                                                                                                       |
| WLAN \_ REASON \_ CODE \_ IHV \_ OUI \_ MISSING                          | Die IHV-OEI-Einstellungen fehlen.                                                                                                                                                                                                             |
| WLAN \_ REASON CODE IHV SETTINGS MISSING (WLAN-GRUNDCODE: \_ \_ IHV-EINSTELLUNGEN \_ \_ FEHLEN)                     | Die IHV-Sicherheitseinstellungen fehlen.                                                                                                                                                                                                        |
| WLAN \_ REASON CODE IHV CONNECTIVITY NOT SUPPORTED (WLAN-GRUNDCODE: \_ \_ IHV-KONNEKTIVITÄT \_ WIRD NICHT \_ \_ UNTERSTÜTZT)          | Eine Anwendung hat versucht, ein IHV-Profil auf einen Adapter anzuwenden, der keine IHV-Konnektivitätseinstellungen unterstützt.                                                                                                                                   |
| WLAN \_ REASON \_ CODE \_ CONFLICT \_ SECURITY                         | Der Konflikt mit den Sicherheitseinstellungen.                                                                                                                                                                                                               |
| WLAN \_ REASON CODE SECURITY MISSING \_ \_ (WLAN-GRUNDCODESICHERHEIT \_ FEHLT)                          | Die Sicherheitseinstellungen fehlen.                                                                                                                                                                                                            |
| \_WLAN-GRUNDCODE \_ \_ \_ UNGÜLTIGER BSS-TYP \_                         | Der BSS-Typ ist ungültig.                                                                                                                                                                                                                    |
| \_WLAN-GRUNDCODE \_ \_ \_ UNGÜLTIGER ADHOC-VERBINDUNGSMODUS \_ \_           | Die automatische Verbindung kann für ein Ad-hoc-Netzwerk nicht festgelegt werden.                                                                                                                                                                                     |
| WLAN \_ REASON \_ CODE \_ NON \_ BROADCAST \_ SET \_ FOR \_ ADHOC            | Nicht-Broadcast kann für ein Ad-hoc-Netzwerk nicht festgelegt werden.                                                                                                                                                                                            |
| WLAN \_ REASON \_ CODE \_ AUTO \_ SWITCH \_ SET \_ FOR \_ ADHOC              | Der automatische Switch kann für ein Ad-hoc-Netzwerk nicht festgelegt werden.                                                                                                                                                                                              |
| WLAN \_ REASON \_ CODE \_ AUTO \_ SWITCH \_ SET \_ FOR \_ MANUAL \_ CONNECTION | Der automatische Switch kann für ein manuelles Verbindungsprofil nicht festgelegt werden.                                                                                                                                                                                    |
| WLAN \_ REASON \_ CODE \_ IHV \_ SECURITY \_ ONEX \_ MISSING               | Die IHV 802.1X-Sicherheitseinstellungen fehlen.                                                                                                                                                                                                 |
| WLAN \_ REASON \_ CODE \_ PROFILE \_ SSID \_ INVALID                     | Die SSID im Profil ist ungültig oder fehlt.                                                                                                                                                                                                |
| \_ \_ WLAN-GRUNDCODE \_ ZU VIELE \_ \_ SSID                            | Im Profil wurden zu viele SSIDs angegeben.                                                                                                                                                                                                 |
| WLAN \_ REASON CODE IHV CONNECTIVITY NOT SUPPORTED (WLAN-GRUNDCODE: \_ \_ IHV-KONNEKTIVITÄT \_ WIRD NICHT \_ \_ UNTERSTÜTZT)          |                                                                                                                                                                                                                                               |
| WLAN \_ REASON \_ CODE \_ BAD \_ MAX \_ NUMBER \_ OF \_ CLIENTS \_ FOR \_ AP     | Eine Anwendung hat versucht, mithilfe der [**WlanSetProfile-Funktion**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) ein drahtlos gehostetes Netzwerkprofil auf eine physische Netzwerkadapter-NIC anzuwenden, und einen unzulässigen Wert für die maximal zulässige Anzahl von Clients angegeben. |
| \_WLAN-GRUNDCODE \_ \_ UNGÜLTIGER \_ KANAL                           | Der angegebene Kanal ist ungültig.                                                                                                                                                                                                             |
| WLAN \_ REASON CODE OPERATION MODE NOT SUPPORTED (WLAN-GRUNDCODEBETRIEBSMODUS \_ WIRD NICHT \_ \_ \_ \_ UNTERSTÜTZT)            |                                                                                                                                                                                                                                               |
| WLAN \_ REASON \_ CODE \_ AUTO \_ AP \_ PROFILE \_ NOT \_ ALLOWED            | Interner Betriebssystemfehler beim drahtlos gehosteten Netzwerk.                                                                                                                                                                 |
| \_WLAN-GRUNDCODE \_ AUTOMATISCHE VERBINDUNG \_ NICHT \_ \_ \_ ZULÄSSIG             |                                                                                                                                                                                                                                               |



 

In der folgenden Tabelle sind fehlercodes für die MSM-Netzwerkinkompatibilität aufgeführt.



| Ursachencode                                            | Bedeutung                                                          |
|--------------------------------------------------------|------------------------------------------------------------------|
| WLAN \_ REASON \_ CODE \_ UNSUPPORTED \_ SECURITY \_ SET \_ BY \_ OS | Die Sicherheitseinstellungen werden vom Betriebssystem nicht unterstützt. |
| WLAN \_ REASON \_ CODE \_ UNSUPPORTED \_ SECURITY \_ SET         | Die Sicherheitseinstellungen werden nicht unterstützt.                         |
| WLAN \_ REASON \_ CODE \_ BSS \_ TYPE \_ UNMATCH                 | Der BSS-Typ ist nicht übereinstimmend.                                     |
| WLAN \_ REASON \_ CODE \_ PHY \_ TYPE \_ UNMATCH                 | Der PHY-Typ ist nicht übereinstimmend.                                     |
| WLAN \_ REASON \_ CODE \_ DATARATE \_ UNMATCH                  | Die Datenrate ist nicht übereinstimmend.                                    |



 

In der folgenden Tabelle sind Fehlercodes für MSM-Verbindungsfehler aufgeführt.



| Ursachencode                                       | Bedeutung                                                                                                      |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| WLAN \_ REASON \_ CODE \_ USER \_ CANCELLED               | Der Benutzer hat den Vorgang abgebrochen.                                                                             |
| FEHLER BEI \_ DER \_ WLAN-GRUNDCODE-ZUORDNUNG \_ \_          | Der Treiber wurde während der Zuordnung getrennt.                                                                       |
| TIMEOUT \_ BEI \_ DER WLAN-GRUNDCODE-ZUORDNUNG \_ \_          | Time out der Zuordnung.                                                                                       |
| FEHLER BEI \_ \_ WLAN-URSACHECODE \_ VOR DER \_ \_ SICHERHEIT        | Sicherheitsfehler vor der Zuordnung.                                                                            |
| SICHERHEITSFEHLER BEIM STARTEN \_ \_ DES \_ \_ WLAN-GRUNDCODES \_      | Fehler beim Starten der Sicherheit nach der Zuordnung.                                                                  |
| FEHLER BEI \_ DER \_ WLAN-URSACHECODESICHERHEIT \_ \_             | Die Sicherheit endet mit einem Fehler.                                                                               |
| TIMEOUT \_ FÜR \_ WLAN-GRUNDCODESICHERHEIT \_ \_             | Bei Einem Sicherheitsvorgang wird ein Zeitsendvorgang durchgeführt.                                                                                |
| FEHLER BEIM ROAMING \_ \_ DES WLAN-GRUNDCODES \_ \_              | Treiber beim Roaming getrennt.                                                                           |
| \_WLAN-URSACHE: \_ \_ CODEROAMING-SICHERHEITSFEHLER \_ \_    | Fehler beim Starten der Sicherheit für das Roaming.                                                                        |
| WLAN \_ REASON \_ CODE \_ ADHOC \_ SECURITY \_ FAILURE      | Fehler beim Starten der Sicherheit für ad hoc-Peers.                                                                    |
| \_ \_ WLAN-GRUNDCODETREIBER \_ \_ GETRENNT          | Treiber getrennt.                                                                                         |
| FEHLER BEIM \_ \_ WLAN-GRUNDCODETREIBERVORGANG \_ \_ \_    | Der Treiber konnte einige Vorgänge nicht ausführen.                                                                    |
| WLAN \_ REASON CODE IHV NOT AVAILABLE (WLAN-GRUNDCODE- \_ \_ IHV \_ NICHT \_ VERFÜGBAR)           | Der IHV-Dienst ist nicht verfügbar.                                                                            |
| WLAN \_ REASON \_ CODE IHV NOT RESPONDING (WLAN-GRUNDCODE: \_ IHV \_ REAGIERT \_ NICHT)          | Bei der Antwort des IHV-Diensts ist ein Time out erfolgt.                                                                 |
| WLAN \_ REASON \_ CODE \_ DISCONNECT \_ TIMEOUT           | Time out waiting for the driver to disconnect. (Timed out waiting for the driver to disconnect. (Time out beim Warten auf die Trennung des Treibers.                                                              |
| WLAN REASON CODE INTERNAL FAILURE (INTERNER FEHLER IM \_ \_ \_ WLAN-GRUNDCODE) \_             | Ein interner Fehler hat verhindert, dass der Vorgang abgeschlossen wurde.                                              |
| TIMEOUT \_ DER \_ WLAN-GRUNDCODE-UI-ANFORDERUNG \_ \_ \_          | Bei einer Benutzerinteraktionsanforderung ist ein Time out erfolgt.                                                                        |
| \_ \_ WLAN-GRUNDCODE: \_ \_ ZU VIELE \_ \_ SICHERHEITSVERSUCHE | Roaming zu häufig. Die Nachsicherheit wurde nach fünf Versuchen nicht abgeschlossen.                                         |
| FEHLER BEIM \_ STARTEN \_ DES \_ WLAN-GRUNDCODES DER \_ AP \_         | Es ist ein interner Betriebssystemfehler aufgetreten, der zu einem Fehler beim Starten des drahtlos gehosteten Netzwerks führte. |



 

In der folgenden Tabelle sind die MSM-Sicherheitsfehlercodes aufgeführt.



| Ursachencode                                                             | Bedeutung                                                                                                                                                                                   |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ INVALID \_ KEY \_ INDEX                | Der angegebene Schlüsselindex ist ungültig.                                                                                                                                                         |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ PSK \_ PRESENT                       | Schlüssel erforderlich, PSK vorhanden.                                                                                                                                                                |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ KEY \_ LENGTH                        | Ungültige Schlüssellänge.                                                                                                                                                                       |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ PSK \_ LENGTH                        | Ungültige PSK-Länge.                                                                                                                                                                       |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ NO \_ AUTH \_ CIPHER \_ SPECIFIED        | Es wurden keine Authentifizierungs-/Verschlüsselungspaare angegeben.                                                                                                                                                           |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ TOO \_ MANY \_ AUTH \_ CIPHER \_ SPECIFIED | Es wurden zu viele Authentifizierungs-/Verschlüsselungspaare angegeben.                                                                                                                                                     |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ DUPLICATE \_ AUTH \_ CIPHER            | Das Profil enthält ein doppeltes Authentifizierungs-/Verschlüsselungspaar.                                                                                                                                              |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ RAWDATA \_ INVALID                   | Profilrohdaten sind ungültig.                                                                                                                                                              |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ INVALID \_ AUTH \_ CIPHER              | Ungültige Kombination aus Authentifizierung und Verschlüsselung.                                                                                                                                                          |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ ONEX \_ DISABLED                     | 802.1X ist deaktiviert, wenn es aktiviert werden muss.                                                                                                                                        |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ ONEX \_ ENABLED                      | 802.1X wird aktiviert, wenn es deaktiviert werden muss.                                                                                                                                        |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ INVALID \_ PMKCACHE \_ MODE            | Ungültiger PMK-Cachemodus.                                                                                                                                                                   |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ INVALID \_ PMKCACHE \_ SIZE            | Ungültige PMK-Cachegröße.                                                                                                                                                                   |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ INVALID \_ PMKCACHE \_ TTL             | Ungültige PMK-Cache-TTL.                                                                                                                                                                    |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ INVALID \_ PREAUTH \_ MODE             | Ungültiger Vorauthentifizierungsmodus.                                                                                                                                                                     |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ INVALID \_ PREAUTH \_ THROTTLE         | Ungültige Vorauthentifizierungsdrosselung.                                                                                                                                                                 |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ PREAUTH \_ ONLY \_ ENABLED             | Die Vorauthentifizierung ist aktiviert, wenn der PMK-Cache deaktiviert ist.                                                                                                                                               |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ CAPABILITY \_ NETWORK                         | Fehler beim Funktionsabgleich im Netzwerk.                                                                                                                                                    |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ CAPABILITY \_ NIC                             | Fehler beim Funktionsabgleich bei der NIC.                                                                                                                                                        |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ CAPABILITY \_ PROFILE                         | Fehler beim Funktionsabgleich beim Profil.                                                                                                                                                    |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ CAPABILITY \_ DISCOVERY                       | Das Netzwerk unterstützt keinen angegebenen Funktionstyp.                                                                                                                                       |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ PASSPHRASE \_ CHAR                   | Die Passphrase enthält ein ungültiges Zeichen.                                                                                                                                                    |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ KEYMATERIAL \_ CHAR                  | Schlüsselmaterial enthält ungültiges Zeichen.                                                                                                                                                  |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ WRONG \_ KEYTYPE                     | Der angegebene Schlüsseltyp passt nicht zum Schlüsselmaterial.                                                                                                                                   |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ MIXED \_ CELL                                 | Eine gemischte Zelle wird vermutet. Der AP signalisiert nicht, dass er mit einem datenschutzfähigen Profil kompatibel ist.                                                                                  |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ AUTH \_ TIMERS \_ INVALID              | Die Anzahl der Authentifizierungs-Timer oder die Im Profil angegebene Anzahl von Timeouts ist ungültig.                                                                                        |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ INVALID \_ GKEY \_ INTV                | Das im Profil angegebene Aktualisierungsintervall für Gruppenschlüssel ist ungültig.                                                                                                                        |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ TRANSITION \_ NETWORK                         | Ein "Übergangsnetzwerk" wird vermutet. Legacy 802.11-Sicherheit wird für den nächsten Authentifizierungsversuch verwendet.                                                                                  |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ KEY \_ UNMAPPED \_ CHAR                | Der Schlüssel enthält Zeichen, die nicht im ASCII-Zeichensatz enthalten sind.                                                                                                                      |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ CAPABILITY \_ PROFILE \_ AUTH                   | Fehler beim Funktionsabgleich, weil das Netzwerk die Authentifizierungsmethode im Profil nicht unterstützt.                                                                                 |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ CAPABILITY \_ PROFILE \_ CIPHER                 | Fehler beim Funktionsabgleich, weil das Netzwerk den Verschlüsselungsalgorithmus im Profil nicht unterstützt.                                                                                      |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ SAFE \_ MODE                         | Der FIPS 140-2-Moduswert im Profil ist ungültig.                                                                                                                                          |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ CAPABILITY \_ PROFILE \_ SAFE \_ MODE \_ NIC        | Das Profil erfordert den FIPS 140-2-Modus, der von der Netzwerkschnittstellenkarte (NIC) nicht unterstützt wird.                                                                                                 |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ CAPABILITY \_ PROFILE \_ SAFE \_ MODE \_ NW         | Das Profil erfordert den FIPS 140-2-Modus, der vom Netzwerk nicht unterstützt wird.                                                                                                                      |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ UNSUPPORTED \_ AUTH                  | Profil gibt einen nicht unterstützten Authentifizierungsmechanismus an.                                                                                                                               |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ UNSUPPORTED \_ CIPHER                | Profil gibt eine nicht unterstützte Verschlüsselung an.                                                                                                                                                  |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ UI \_ REQUEST \_ FAILURE                        | Fehler beim Einreiten der Benutzeroberflächenanforderung in die Warteschlange.                                                                                                                                               |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ CAPABILITY \_ MFP \_ NW \_ NIC                    | Das WLAN erfordert Management Frame Protection (MFP), und die Netzwerkschnittstelle unterstützt MFP nicht. Weitere Informationen finden Sie in der IEEE 802.11w-Zusatzänderung zum Standard 802.11. |



 

In der folgenden Tabelle sind die MSM-Verbindungsfehlercodes aufgeführt.



| Ursachencode                                             | Bedeutung                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ AUTH \_ START \_ TIMEOUT        | Die 802.1X-Authentifizierung wurde nicht innerhalb der konfigurierten Zeit gestartet.                                                      |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ AUTH \_ SUCCESS \_ TIMEOUT      | Die 802.1X-Authentifizierung wurde nicht innerhalb der konfigurierten Zeit abgeschlossen.                                                   |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ KEY \_ START \_ TIMEOUT         | Der dynamische Schlüsselaustausch wurde nicht innerhalb der konfigurierten Zeit gestartet.                                                       |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ KEY \_ SUCCESS \_ TIMEOUT       | Der dynamische Schlüsselaustausch wurde nicht innerhalb der konfigurierten Zeit abgeschlossen.                                                    |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ M3 \_ MISSING \_ KEY \_ DATA      | Nachricht 3 von 4-Wege-Handshake enthält keine Schlüsseldaten.                                                                    |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ M3 \_ MISSING \_ IE             | Nachricht 3 von 4-Wege-Handshake hat keinen IE.                                                                          |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ M3 \_ MISSING \_ GRP \_ KEY       | Nachricht 3 von 4-Wege-Handshake hat keinen GRP-Schlüssel.                                                                     |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PR \_ IE \_ MATCHING            | Fehler beim Abgleich der Sicherheitsfunktionen von IE in M3.                                                               |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ SEC \_ IE \_ MATCHING           | Fehler beim Abgleich der Sicherheitsfunktionen der sekundären IE in M3.                                                     |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ NO \_ PAIRWISE \_ KEY           | Ein paarweiser Schlüssel war erforderlich, aber der Zugriffspunkt (Access Point, AP) hat nur Gruppenschlüssel konfiguriert.                                        |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ G1 \_ MISSING \_ KEY \_ DATA      | Nachricht 1 des Gruppenschlüsselhandshakes enthält keine Schlüsseldaten.                                                                |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ G1 \_ MISSING \_ GRP \_ KEY       | Nachricht 1 des Gruppenschlüsselhandshakes enthält keinen Gruppenschlüssel.                                                               |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PEER \_ INDICATED \_ INSECURE   | AP setzt sicheres Bit zurück, nachdem die Verbindung gesichert wurde.                                                                |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ NO \_ AUTHENTICATOR           | 802.1X gibt an, dass kein Authentator, aber für das Profil ein Authentator erforderlich ist.                                   |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ NIC \_ FAILURE                | Fehler beim Konfigurieren von Einstellungen für die NIC.                                                                                 |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ CANCELLED                   | Der Vorgang wurde von einem Aufrufer abgebrochen.                                                                              |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ KEY \_ FORMAT                 | Das eingegebene Schlüsselformat hat kein gültiges Format.                                                                     |
| WLAN \_ REASON \_ CODE \_ MSMSEC DOWNGRADE DETECTED (WLAN-GRUNDCODE: \_ MSMSEC-HERABSTUFUNG \_ ERKANNT)         | Es wurde ein Sicherheits downgrade erkannt.                                                                               |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PSK \_ MISMATCH \_ SUSPECTED    | Ein PSK-Konflikt wird vermutet.                                                                                     |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ FORCED \_ FAILURE             | Es ist ein erzwungener Fehler auftrat, da die Verbindungsmethode nicht sicher war.                                         |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ M3 TOO MANY \_ \_ \_ RSNI        | Nachricht 3 von 4-Wege-Handshake enthält zu viele RSN-IE (RSN).                                                     |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ M2 \_ MISSING \_ KEY \_ DATA      | Nachricht 2 von 4-Wege-Handshake enthält keine Schlüsseldaten (RSN Adhoc).                                                        |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ M2 \_ MISSING \_ IE             | Nachricht 2 von 4-Wege-Handshake hat keine IE (RSN Adhoc).                                                              |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ AUTH \_ WCN \_ COMPLETED        |                                                                                                                  |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ SECURITY \_ UI \_ FAILURE       | Fehler bei der Anforderung der Sicherheitsbenutzeroberfläche, weil die Anforderung nicht in die Warteschlange eingereiht werden konnte oder weil der Benutzer die Anforderung abgebrochen hat. |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ M3 \_ MISSING \_ MGMT \_ GRP \_ KEY | Message 3 of 4 way handshake has no Mgmt Group Key (RSN).                                                        |
| \_WLAN-GRUNDCODE \_ \_ MSMSEC \_ G1 \_ \_ FEHLENDER \_ MGMT-GRP-SCHLÜSSEL \_ | Nachricht 1 des Gruppenschlüsselhandshakes enthält keinen Gruppenverwaltungsschlüssel.                                                    |



 

In der folgenden Tabelle sind 802.1X-Ursachencodes aufgeführt. Schemaelemente mit dem Namen unten werden im OneX-Schema definiert und im WLAN-Profil angegeben.



| Ursachencode                                         | Bedeutung                                                                                                                                                                            |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ONEX \_ KANN BENUTZER NICHT \_ \_ IDENTIFIZIEREN \_                    | Für die 802.1X-Authentifizierung ist kein Benutzer verfügbar. Dieser Fehler kann auftreten, wenn die Computerauthentifizierung deaktiviert ist und kein Benutzer am Computer angemeldet ist.                              |
| \_ONEX-IDENTITÄT \_ NICHT \_ GEFUNDEN                          | Die 802.1X-Identität wurde nicht gefunden.                                                                                                                                            |
| ONEX \_ UI DISABLED (ONEX-BENUTZEROBERFLÄCHE \_ DEAKTIVIERT)                                  | Die Authentifizierung konnte nur über die Benutzeroberfläche abgeschlossen werden, und diese Schnittstelle konnte nicht angezeigt werden.                                                                       |
| \_ONEX-EAP-FEHLER \_ \_ EMPFANGEN                        | Fehler bei der EAP-Authentifizierung.                                                                                                                                                     |
| ONEX \_ AUTHENTICATOR \_ NICHT MEHR \_ \_ VORHANDEN            | Der 802.1X-Authentifikator wurde aus dem Netzwerk entfernt.                                                                                                                               |
| \_ONEX-PROFILVERSION \_ \_ WIRD NICHT \_ UNTERSTÜTZT              | Die angegebene Version des OneX-Profils wird nicht unterstützt.                                                                                                                         |
| \_ONEX-PROFIL \_ \_ UNGÜLTIGE LÄNGE                      | Das OneX-Profil hat eine ungültige Länge.                                                                                                                                            |
| ONEX \_ PROFILE DISALLOWED EAP TYPE (ONEX-PROFIL \_ NICHT ZULÄSSIGER \_ \_ EAP-TYP)                | Der im OneX-Profil angegebene EAP-Typ (möglicherweise vom EAPType-Element bereitgestellt) ist nicht zulässig.                                                                               |
| UNGÜLTIGER \_ \_ \_ EAP-TYP \_ \_ ODER \_ FLAG FÜR ONEX-PROFIL         | Der im OneX-Profil angegebene EAP-Typ (möglicherweise vom EAPType-Element bereitgestellt) ist ungültig, oder eines der EAP-Flags (möglicherweise im EAPConfig-Element angegeben) ist ungültig. |
| \_ONEX-PROFIL \_ UNGÜLTIGE \_ \_ ONEX-FLAGS                 | Die Suppliplizierungsflags (möglicherweise im EAPConfig-Element angegeben) im OneX-Profil sind ungültig.                                                                                 |
| \_ONEX-PROFIL \_ UNGÜLTIGER \_ \_ TIMERWERT                | Ein im OneX-Profil angegebener Timer (möglicherweise vom element heldPeriod, authPeriod oder startPeriod bereitgestellt) ist ungültig.                                                        |
| \_ONEX-PROFIL \_ – UNGÜLTIGER \_ SUPPLI SUPPLI SUPPLIPLI MODE \_            | Der im OneX-Profil angegebene Supplizierungsmodus (möglicherweise vom suppli suppli supplimode-Element bereitgestellt) ist ungültig.                                                                    |
| \_ONEX-PROFIL \_ – UNGÜLTIGER \_ AUTHENTIFIZIERUNGSMODUS \_                  | Der im OneX-Profil angegebene (möglicherweise vom authMode-Element bereitgestellte) Authentifizierungsmodus ist ungültig.                                                                      |
| \_ONEX-PROFIL \_ \_ UNGÜLTIGE \_ EAP-VERBINDUNGSEIGENSCHAFTEN \_ | Die im OneX-Profil angegebenen Verbindungseigenschaften (möglicherweise vom EAPConfig-Element bereitgestellt) sind ungültig.                                                                  |



 

## <a name="remarks"></a>Hinweise

Eine begrenzte Anzahl von Ursachencodes wird auf Windows XP mit Service Pack 3 (SP3) und in der WLAN-API für Windows XP mit Service Pack 2 (SP2) unterstützt. Für Windows XP mit SP3 und für die WLAN-API für Windows XP mit SP2 werden folgende Fehlercodes für die Profilvalidierung unterstützt:

-   \_WLAN-GRUNDCODE \_ \_ \_ UNGÜLTIGES \_ PROFILSCHEMA
-   \_WLAN: \_ \_ GRUNDCODEPROFIL \_ FEHLT
-   WLAN \_ REASON \_ CODE \_ PROFILE \_ SSID \_ INVALID

Die MSM-Sicherheitsfehlercodes, die auf Windows XP mit SP3 und in der Wlan-API für Windows XP mit SP2 unterstützt werden, sind wie folgt:

-   WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ INVALID \_ KEY \_ INDEX
-   WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ KEY \_ LENGTH
-   WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ PSK \_ LENGTH
-   WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ INVALID \_ AUTH \_ CIPHER
-   \_WLAN-GRUNDCODE \_ \_ MSMSEC-PROFIL \_ \_ ONEX \_ DEAKTIVIERT
-   WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ ONEX \_ ENABLED
-   WLAN \_ REASON \_ CODE \_ MSMSEC \_ CAPABILITY \_ NETWORK
-   WLAN \_ REASON \_ CODE \_ MSMSEC \_ CAPABILITY \_ NIC
-   WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ KEYMATERIAL \_ CHAR
-   \_WLAN-GRUNDCODE \_ \_ MSMSEC-PROFIL \_ \_ \_ FALSCHER KEYTYPE

Die 802.1x-Fehlercodes, die auf Windows XP mit SP3 und in der Wireless LAN-API für Windows XP mit SP2 unterstützt werden, sind wie folgt:

-   \_ONEX-PROFIL \_ \_ UNGÜLTIGE LÄNGE
-   UNGÜLTIGER \_ \_ \_ EAP-TYP \_ \_ ODER \_ FLAG FÜR ONEX-PROFIL
-   \_ONEX-PROFIL \_ – UNGÜLTIGER \_ AUTHENTIFIZIERUNGSMODUS \_
-   \_ONEX-PROFIL \_ \_ UNGÜLTIGE \_ EAP-VERBINDUNGSEIGENSCHAFTEN \_

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP nur mit \[ SP3-Desktop-Apps\]<br/>                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                 |
| Verteilbare Komponente<br/>          | WLAN-API für Windows XP mit SP2<br/>                                  |
| Header<br/>                   | <dl> <dt>Wlanapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**WlanReasonCodeToString**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring)
</dt> <dt>

[**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)
</dt> </dl>

 

 
