---
title: MPTHREAT_CATEGORY-Enumeration (MpClient.h)
description: Mögliche Bedrohungskategorien.
ms.assetid: 478ED59E-5D3C-43B3-A89D-44A649EDD086
keywords:
- MPTHREAT_CATEGORY enumeration Legacy Windows Environment Features (Legacy-Windows-Umgebungsfeatures)
- PMPTHREAT_CATEGORY-Enumerationszeiger Legacy Windows-Umgebungsfeatures
topic_type:
- apiref
api_name:
- MPTHREAT_CATEGORY
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70cfd95de751d51be3ab4b61bc361687738422a6d31c234576e812efcd57bd4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975970"
---
# <a name="mpthreat_category-enumeration"></a>MPTHREAT \_ CATEGORY-Enumeration

Mögliche Bedrohungskategorien.

## <a name="syntax"></a>Syntax

```C++
typedef enum tagMPTHREAT_CATEGORY {
  MP_THREAT_CATEGORY_INVALID                    = 0,
  MP_THREAT_CATEGORY_ADWARE                     = 1,
  MP_THREAT_CATEGORY_SPYWARE                    = 2,
  MP_THREAT_CATEGORY_PASSWORDSTEALER            = 3,
  MP_THREAT_CATEGORY_TROJANDOWNLOADER           = 4,
  MP_THREAT_CATEGORY_WORM                       = 5,
  MP_THREAT_CATEGORY_BACKDOOR                   = 6,
  MP_THREAT_CATEGORY_REMOTEACCESSTROJAN         = 7,
  MP_THREAT_CATEGORY_TROJAN                     = 8,
  MP_THREAT_CATEGORY_EMAILFLOODER               = 9,
  MP_THREAT_CATEGORY_KEYLOGGER                  = 10,
  MP_THREAT_CATEGORY_DIALER                     = 11,
  MP_THREAT_CATEGORY_MONITORINGSOFTWARE         = 12,
  MP_THREAT_CATEGORY_BROWSERMODIFIER            = 13,
  MP_THREAT_CATEGORY_COOKIE                     = 14,
  MP_THREAT_CATEGORY_BROWSERPLUGIN              = 15,
  MP_THREAT_CATEGORY_AOLEXPLOIT                 = 16,
  MP_THREAT_CATEGORY_NUKER                      = 17,
  MP_THREAT_CATEGORY_SECURITYDISABLER           = 18,
  MP_THREAT_CATEGORY_JOKEPROGRAM                = 19,
  MP_THREAT_CATEGORY_HOSTILEACTIVEXCONTROL      = 20,
  MP_THREAT_CATEGORY_SOFTWAREBUNDLER            = 21,
  MP_THREAT_CATEGORY_STEALTHNOTIFIER            = 22,
  MP_THREAT_CATEGORY_SETTINGSMODIFIER           = 23,
  MP_THREAT_CATEGORY_TOOLBAR                    = 24,
  MP_THREAT_CATEGORY_REMOTECONTROLSOFTWARE      = 25,
  MP_THREAT_CATEGORY_TROJANFTP                  = 26,
  MP_THREAT_CATEGORY_POTENTIALUNWANTEDSOFTWARE  = 27,
  MP_THREAT_CATEGORY_ICQEXPLOIT                 = 28,
  MP_THREAT_CATEGORY_TROJANTELNET               = 29,
  MP_THREAT_CATEGORY_EXPLOIT                    = 30,
  MP_THREAT_CATEGORY_FILESHARINGPROGRAM         = 31,
  MP_THREAT_CATEGORY_MALWARE_CREATION_TOOL      = 32,
  MP_THREAT_CATEGORY_REMOTE_CONTROL_SOFTWARE    = 33,
  MP_THREAT_CATEGORY_TOOL                       = 34,
  MP_THREAT_CATEGORY_TROJAN_DENIALOFSERVICE     = 36,
  MP_THREAT_CATEGORY_TROJAN_DROPPER             = 37,
  MP_THREAT_CATEGORY_TROJAN_MASSMAILER          = 38,
  MP_THREAT_CATEGORY_TROJAN_MONITORINGSOFTWARE  = 39,
  MP_THREAT_CATEGORY_TROJAN_PROXYSERVER         = 40,
  MP_THREAT_CATEGORY_VIRUS                      = 42,
  MP_THREAT_CATEGORY_KNOWN                      = 43,
  MP_THREAT_CATEGORY_UNKNOWN                    = 44,
  MP_THREAT_CATEGORY_SPP                        = 45,
  MP_THREAT_CATEGORY_BEHAVIOR                   = 46,
  MP_THREAT_CATEGORY_VULNERABILTIY              = 47,
  MP_THREAT_CATEGORY_POLICY                     = 48
} MPTHREAT_CATEGORY, *PMPTHREAT_CATEGORY;
```

## <a name="constants"></a>Konstanten

Bedrohungskategorie | BESCHREIBUNG
-|-
<span id="MP_THREAT_CATEGORY_INVALID"></span><span id="mp_threat_category_invalid"></span>**MP \_ \_BEDROHUNGSKATEGORIE \_ UNGÜLTIG** | Die Bedrohungskategorie ist nicht vorhanden oder wurde falsch geschrieben.
<span id="MP_THREAT_CATEGORY_ADWARE"></span><span id="mp_threat_category_adware"></span>**MP \_ \_ \_ BEDROHUNGSKATEGORIE(EN)** | Eine potenziell unerwünschte Anwendung, die Ankündigungen anzeigt.
<span id="MP_THREAT_CATEGORY_SPYWARE"></span><span id="mp_threat_category_spyware"></span>**MP \_ \_BEDROHUNGSKATEGORIE \_ SPYWARE** | Schadsoftware, die Informationen über das Gerät oder den Benutzer ohne Zustimmung oder Kenntnis des Benutzers überträgt.
<span id="MP_THREAT_CATEGORY_PASSWORDSTEALER"></span><span id="mp_threat_category_passwordstealer"></span>**MP \_ \_BEDROHUNGSKATEGORIE \_ PASSWORDSTEALER** | Eine Anwendung, die ein Kennwort sammelt und/oder an einen Angreifer überträgt.
<span id="MP_THREAT_CATEGORY_TROJANDOWNLOADER"></span><span id="mp_threat_category_trojandownloader"></span>**MP \_ THREAT \_ CATEGORY \_ TROJANDOWNLOADER** | Ein Trojaner, der Schadsoftware oder potenziell unerwünschte Anwendungen auf ein infiziertes Gerät herunterlädt.
<span id="MP_THREAT_CATEGORY_WORM"></span><span id="mp_threat_category_worm"></span>**MP \_ \_BEDROHUNGSKATEGORIE \_ WORM** | Selbstverbreitende Schadsoftware, die sich automatisch über Netzwerkverbindungen verteilen kann.
<span id="MP_THREAT_CATEGORY_BACKDOOR"></span><span id="mp_threat_category_backdoor"></span>**MP \_ THREAT \_ CATEGORY \_ BACKDOOR** | Schadsoftware, mit der normale Sicherheits- und Authentifizierungsprotokolle auf einem Gerät umgangen werden können.
<span id="MP_THREAT_CATEGORY_REMOTEACCESSTROJAN"></span><span id="mp_threat_category_remoteaccesstrojan"></span>**MP \_ \_BEDROHUNGSKATEGORIE \_ REMOTEACCESSTROJAN** | Ein Trojaner, der Remotezugriff auf einen Computer ermöglicht.
<span id="MP_THREAT_CATEGORY_TROJAN"></span><span id="mp_threat_category_trojan"></span>**MP \_ THREAT \_ CATEGORY \_ TROJAN** | Schadsoftware, die sich selbst als legitime Software ausdrungen hat.
<span id="MP_THREAT_CATEGORY_EMAILFLOODER"></span><span id="mp_threat_category_emailflooder"></span>**MP \_ \_BEDROHUNGSKATEGORIE \_ EMAILFLOODER** | Schadsoftware sendet eine große Menge von E-Mails an ein Ziel.
<span id="MP_THREAT_CATEGORY_KEYLOGGER"></span><span id="mp_threat_category_keylogger"></span>**MP \_ \_THREAT CATEGORY \_ KEYLOGGER** | Schadsoftware, die Tastatureingaben des Benutzers aufzeichnet und möglicherweise Kennwörter und andere sensible Daten stiehlt.
<span id="MP_THREAT_CATEGORY_DIALER"></span><span id="mp_threat_category_dialer"></span>**MP \_ \_ \_ BEDROHUNGSKATEGORIE DIALER** | Schadsoftware, die nicht autorisierte Telefonanrufe tätigen kann, häufig zu Premium-Tarifen.
<span id="MP_THREAT_CATEGORY_MONITORINGSOFTWARE"></span><span id="mp_threat_category_monitoringsoftware"></span>**MP \_ \_ÜBERWACHUNG DER BEDROHUNGSKATEGORIESOFTWARE \_** | Eine potenziell unerwünschte Anwendung, die Benutzeraktivitäten überwacht, z. B. die Eingaben des Benutzers auf der Tastatur oder ansichten auf dem Bildschirm.
<span id="MP_THREAT_CATEGORY_BROWSERMODIFIER"></span><span id="mp_threat_category_browsermodifier"></span>**MP \_ \_BEDROHUNGSKATEGORIE \_ BROWSERMODIFIER** | Eine potenziell unerwünschte Anwendung, die Webbrowsereinstellungen ohne Zustimmung des Benutzers ändert.
<span id="MP_THREAT_CATEGORY_COOKIE"></span><span id="mp_threat_category_cookie"></span>**MP \_ \_ \_ BEDROHUNGSKATEGORIECOOKIE** | Daten, die ein Webserver an einen Browser sendet, sodass bei wiederholten Besuchen Informationen zum Benutzer gespeichert werden können, z. B. Webanwendungseinstellungen.
<span id="MP_THREAT_CATEGORY_BROWSERPLUGIN"></span><span id="mp_threat_category_browserplugin"></span>**MP \_ \_BEDROHUNGSKATEGORIE \_ BROWSERPLUGIN** | Software, mit der ein Standardwebbrowser bestimmte Inhaltstypen wie Mediendateien, animierte Bilder und interaktive Formulare anzeigen und ausführen kann.
<span id="MP_THREAT_CATEGORY_AOLEXPLOIT"></span><span id="mp_threat_category_aolexploit"></span>**MP \_ \_BEDROHUNGSKATEGORIE \_ AOLEXPLOIT** | Schadsoftware, die Benutzer des AOL-Internetdiensts angreift, häufig durch Abrufen von Kennwörtern oder Ändern von Einstellungen.
<span id="MP_THREAT_CATEGORY_NUKER"></span><span id="mp_threat_category_nuker"></span>**MP \_ \_BEDROHUNGSKATEGORIE \_ NUKER** | Schadsoftware, die entwickelt wurde, um ein Gerät abzustürzen oder es weniger stabil zu machen.
<span id="MP_THREAT_CATEGORY_SECURITYDISABLER"></span><span id="mp_threat_category_securitydisabler"></span>**MP \_ \_ \_ BEDROHUNGSKATEGORIE SICHERHEITDISABLER** | Schadsoftware, die Sicherheitseinstellungen oder Produkte deaktiviert.
<span id="MP_THREAT_CATEGORY_JOKEPROGRAM"></span><span id="mp_threat_category_jokeprogram"></span>**MP \_ \_BEDROHUNGSKATEGORIE \_ :WIESPROGRAM AUS** | Eine Anwendung, die entwickelt wurde, um einen Benutzer zu belauschen oder zu veralten, ohne das Gerät tatsächlich zu beeinträchtigen.
<span id="MP_THREAT_CATEGORY_HOSTILEACTIVEXCONTROL"></span><span id="mp_threat_category_hostileactivexcontrol"></span>**MP \_ \_BEDROHUNGSKATEGORIE \_ " VERFEINERLICHACTIVEXCONTROL"** | Ein ActiveX Steuerelement, das von einem Angreifer entwickelt wurde, um ein Gerät zu beschädigen. Ein ActiveX Steuerelement ist eine Art browserspezifisches Add-On für Internet Explorer.
<span id="MP_THREAT_CATEGORY_SOFTWAREBUNDLER"></span><span id="mp_threat_category_softwarebundler"></span>**MP \_ \_BEDROHUNGSKATEGORIE \_ SOFTWAREBUNDLER** | Software, die andere potenziell unerwünschte Anwendungen installiert, z. B. Spyware oder Spyware. Der Lizenzvertrag der Bündelungssoftware kann diese anderen Komponenten erfordern, damit sie funktionieren.
<span id="MP_THREAT_CATEGORY_STEALTHNOTIFIER"></span><span id="mp_threat_category_stealthnotifier"></span>**MP \_ \_BEDROHUNGSKATEGORIE \_ "BEDROHUNGSBESCHRIFTUNG"** | Schadsoftware, die über eine verdeckte Verbindung eine Verbindung mit einem Remoteserver herstellt, um einen Angreifer darüber zu informieren, dass die Schadsoftware installiert wurde.
<span id="MP_THREAT_CATEGORY_SETTINGSMODIFIER"></span><span id="mp_threat_category_settingsmodifier"></span>**MP \_ \_EINSTELLUNGEN FÜR BEDROHUNGSKATEGORIENMODIFIER \_** | Eine potenziell unerwünschte Anwendung, die die Einstellungen eines Benutzers ohne das Wissen oder die Zustimmung des Benutzers ändert.
<span id="MP_THREAT_CATEGORY_TOOLBAR"></span><span id="mp_threat_category_toolbar"></span>**MP \_ \_ \_ SYMBOLLEISTE "BEDROHUNGSKATEGORIE"** | Eine potenziell unerwünschte Anwendung (PUA), die eine Symbolleiste im Webbrowser des Benutzers installiert; werden häufig mit zusätzlichem PUA gebündelt, z. B. mit Einem Paket.
<span id="MP_THREAT_CATEGORY_REMOTECONTROLSOFTWARE"></span><span id="mp_threat_category_remotecontrolsoftware"></span>**MP \_ \_BEDROHUNGSKATEGORIE \_ REMOTECONTROLSOFTWARE** | Eine potenziell unerwünschte Anwendung, die Remotezugriff auf ein Gerät bereitstellt.
<span id="MP_THREAT_CATEGORY_TROJANFTP"></span><span id="mp_threat_category_trojanftp"></span>**MP \_ \_BEDROHUNGSKATEGORIE \_ "TROJANFTP"** | Ein Trojaner, der einen FTP-Server verwendet, um einem Angreifer das Hochladen oder Herunterladen von Dateien von einem Gerät zu ermöglichen.
<span id="MP_THREAT_CATEGORY_POTENTIALUNWANTEDSOFTWARE"></span><span id="mp_threat_category_potentialunwantedsoftware"></span>**MP \_ \_BEDROHUNGSKATEGORIE \_ POTENTIALUNWANTEDSOFTWARE** | Wird auch als *potenziell unerwünschte Anwendung* oder *PUA* bezeichnet. Software, die sich möglicherweise übermäßig aufdringlich verhält, was der Benutzer möglicherweise nicht erwartet oder vollständig zugestimmt hat.
<span id="MP_THREAT_CATEGORY_ICQEXPLOIT"></span><span id="mp_threat_category_icqexploit"></span>**MP \_ \_BEDROHUNGSKATEGORIE \_ ICQEXPLOIT** | Ein Trojaner, der den ICQ-Messagingdienst angreift, häufig durch Abrufen von Kennwörtern oder Manipulieren von Einstellungen.
<span id="MP_THREAT_CATEGORY_TROJANTELNET"></span><span id="mp_threat_category_trojantelnet"></span>**MP \_ \_BEDROHUNGSKATEGORIE \_ "TROJANTELNET"** | Ein Trojaner, der einen Telnet-Server ohne Wissen oder Zustimmung des Benutzers auf dem Computer eines Benutzers installiert.
<span id="MP_THREAT_CATEGORY_EXPLOIT"></span><span id="mp_threat_category_exploit"></span>**MP \_ \_ \_ BEDROHUNGSKATEGORIE EXPLOIT** | Bösartiger Code, der ein Sicherheitsrisiko auf einem Gerät oder System nutzt.
<span id="MP_THREAT_CATEGORY_FILESHARINGPROGRAM"></span><span id="mp_threat_category_filesharingprogram"></span>**MP \_ \_BEDROHUNGSKATEGORIE \_ FILESHARINGPROGRAM** | Eine potenziell unerwünschte Anwendung, die ein Gerät für die Peer-zu-Peer-Freigabe der Gerätedateien öffnet.
<span id="MP_THREAT_CATEGORY_MALWARE_CREATION_TOOL"></span><span id="mp_threat_category_malware_creation_tool"></span>**MP \_ \_TOOL \_ ZUM ERSTELLEN VON \_ SCHADSOFTWARE \_ DER BEDROHUNGSKATEGORIE** | Eine Anwendung, die automatisch schädliche Dateien generieren kann.
<span id="MP_THREAT_CATEGORY_REMOTE_CONTROL_SOFTWARE"></span><span id="mp_threat_category_remote_control_software"></span>**MP \_ \_BEDROHUNGSKATEGORIE \_ \_ \_ REMOTESTEUERUNGSSOFTWARE** | Eine potenziell unerwünschte Anwendung, die den Remotezugriff auf ein Gerät ermöglicht.
<span id="MP_THREAT_CATEGORY_TOOL"></span><span id="mp_threat_category_tool"></span>**MP \_ \_ \_ TOOL "BEDROHUNGSKATEGORIE"** | Ein Hilfsprogramm, das einem Angreifer hilft, böswillige Aktionen auf einem Gerät auszuführen.
<span id="MP_THREAT_CATEGORY_TROJAN_DENIALOFSERVICE"></span><span id="mp_threat_category_trojan_denialofservice"></span>**MP \_ \_BEDROHUNGSKATEGORIE: \_ TROJAN \_ DENIALOFSERVICE** | Ein Trojaner, der im Rahmen eines Denial-of-Service-Angriffs (DoS) eine große Menge von Netzwerkanforderungen an ein Ziel senden soll.
<span id="MP_THREAT_CATEGORY_TROJAN_DROPPER"></span><span id="mp_threat_category_trojan_dropper"></span>**MP \_ \_BEDROHUNGSKATEGORIE \_ " TROJAN \_ DROPPER"** | Ein Trojaner, der Schadsoftware oder potenziell unerwünschte Anwendungen auf einem Ziel herunterlädt und installiert.
<span id="MP_THREAT_CATEGORY_TROJAN_MASSMAILER"></span><span id="mp_threat_category_trojan_massmailer"></span>**MP \_ \_BEDROHUNGSKATEGORIE: \_ TROJAN \_ MASSMAILER** | Ein Trojaner, der ein großes Volumen von E-Mails an ein Ziel sendet, das dazu dient, den Posteingang des Ziels zu überlasten.
<span id="MP_THREAT_CATEGORY_TROJAN_MONITORINGSOFTWARE"></span><span id="mp_threat_category_trojan_monitoringsoftware"></span>**MP \_ \_BEDROHUNGSKATEGORIE: \_ ÜBERWACHUNG VON \_ ÜBERWACHUNGSSOFTWARE FÜR BEDROHUNGEN** | Ein Trojaner, der Benutzeraktivitäten überwacht, z. B. die Eingaben des Benutzers auf der Tastatur oder ansichten auf dem Bildschirm.
<span id="MP_THREAT_CATEGORY_TROJAN_PROXYSERVER"></span><span id="mp_threat_category_trojan_proxyserver"></span>**MP \_ \_BEDROHUNGSKATEGORIE \_ "TROJAN \_ PROXYSERVER"** | Ein Proxyserver, der von einem Trojaner installiert wurde, der eine scheinbar unterbrechungsfreie Internetverbindung bereitstellt und gleichzeitig nicht autorisierten Zugriff auf das infizierte Gerät zulässt.
<span id="MP_THREAT_CATEGORY_VIRUS"></span><span id="mp_threat_category_virus"></span>**MP \_ \_BEDROHUNGSKATEGORIE \_ VIRUS** | Schadsoftware, die repliziert wird, häufig durch Fecting anderer Dateien im System, wodurch die Ausführung des Schadsoftwarecodes und dessen Weitergabe ermöglicht wird, wenn diese Dateien aktiviert werden.
<span id="MP_THREAT_CATEGORY_KNOWN"></span><span id="mp_threat_category_known"></span>**MP \_ \_BEDROHUNGSKATEGORIE \_ BEKANNT** | Eine nicht angegebene Bedrohung durch Schadsoftware.
<span id="MP_THREAT_CATEGORY_UNKNOWN"></span><span id="mp_threat_category_unknown"></span>**MP \_ \_BEDROHUNGSKATEGORIE \_ UNBEKANNT** | Eine nicht angegebene Bedrohung durch Schadsoftware, die noch nicht definiert wurde.
<span id="MP_THREAT_CATEGORY_SPP"></span><span id="mp_threat_category_spp"></span>**MP \_ \_ \_ BEDROHUNGSKATEGORIE-SPP** | Antikonforme Technologie, die jede Installation eines Windows Produkts erfordert, muss mit Microsoft aktiviert werden.
<span id="MP_THREAT_CATEGORY_BEHAVIOR"></span><span id="mp_threat_category_behavior"></span>**MP \_ VERHALTEN \_ DER \_ BEDROHUNGSKATEGORIE** | Ein Erkennungstyp, der auf Dateiaktionen basiert, die häufig schädlichen Aktivitäten zugeordnet sind.
<span id="MP_THREAT_CATEGORY_VULNERABILTIY"></span><span id="mp_threat_category_vulnerabiltiy"></span>**MP \_ \_ \_ BEDROHUNGSKATEGORIE NERABILTIY** | Jede Schwachstelle, jeder Verwaltungsprozess oder jede Aktivität, die ein Gerät anfällig macht, von einer Bedrohung ausgenutzt zu werden.
<span id="MP_THREAT_CATEGORY_POLICY"></span><span id="mp_threat_category_policy"></span>**MP \_ RICHTLINIE \_ FÜR \_ BEDROHUNGSKATEGORIEN** | Eine Gruppe von Regeln, die von einem Administrator definiert werden, die Features auf Desktop- und mobilen Geräten steuern, z. B. Softwareupdates.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Unterstützte Mindestversion (Client) | Windows 8 (nur Desktop-Apps) |
| Unterstützte Mindestversion (Server) | Windows Server 2012 (nur Desktop-Apps) |
| Header | MpClient.h |
