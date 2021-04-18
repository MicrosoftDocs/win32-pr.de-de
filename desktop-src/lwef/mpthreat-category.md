---
title: MPTHREAT_CATEGORY-Enumeration (mpclient. h)
description: Mögliche Bedrohungs Kategorien.
ms.assetid: 478ED59E-5D3C-43B3-A89D-44A649EDD086
keywords:
- MPTHREAT_CATEGORY-Enumerationsfunktionen der Legacy-Windows-Umgebung
- PMPTHREAT_CATEGORY enumerationszeiger Legacy-Windows-Umgebungs Features
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
ms.openlocfilehash: 6a149ef6ce6ebadacbac6f0dd35247d793ca7000
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340993"
---
# <a name="mpthreat_category-enumeration"></a>Mpthreat- \_ kategorieenumeration

Mögliche Bedrohungs Kategorien.

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

Bedrohungs Kategorie | BESCHREIBUNG
-|-
<span id="MP_THREAT_CATEGORY_INVALID"></span><span id="mp_threat_category_invalid"></span>**MP \_ \_ \_ ungültige Bedrohungs Kategorie** | Die Bedrohungs Kategorie ist nicht vorhanden oder wurde falsch geschrieben.
<span id="MP_THREAT_CATEGORY_ADWARE"></span><span id="mp_threat_category_adware"></span>**MP \_ Bedrohungs \_ Kategorie \_ Adware** | Eine potenziell unerwünschte Anwendung, in der Ankündigungen angezeigt werden.
<span id="MP_THREAT_CATEGORY_SPYWARE"></span><span id="mp_threat_category_spyware"></span>**MP \_ \_ \_ Spyware der Bedrohungs Kategorie** | Malware, die Informationen über das Gerät oder den Benutzer ohne Zustimmung oder Wissen des Benutzers überträgt.
<span id="MP_THREAT_CATEGORY_PASSWORDSTEALER"></span><span id="mp_threat_category_passwordstealer"></span>**MP \_ Bedrohungs \_ Kategorie \_ passwordstealer** | Eine Anwendung, die ein Kennwort sammelt und/oder an einen Angreifer überträgt.
<span id="MP_THREAT_CATEGORY_TROJANDOWNLOADER"></span><span id="mp_threat_category_trojandownloader"></span>**MP- \_ Bedrohungs \_ Kategorie \_ TrojanDownloader** | Ein Trojaner, der Schadsoftware oder potenziell unerwünschte Anwendungen auf ein infiziertes Gerät herunterlädt.
<span id="MP_THREAT_CATEGORY_WORM"></span><span id="mp_threat_category_worm"></span>**MP \_ \_ \_ Wurm der Bedrohungs Kategorie** | Selbst Propagierung von Schadsoftware, die automatisch über Netzwerkverbindungen verteilt werden kann.
<span id="MP_THREAT_CATEGORY_BACKDOOR"></span><span id="mp_threat_category_backdoor"></span>**MP- \_ Bedrohungs \_ Kategorie \_ Backdoor** | Schadsoftware, mit der normale Sicherheits-und Authentifizierungsprotokolle auf einem Gerät umgangen werden.
<span id="MP_THREAT_CATEGORY_REMOTEACCESSTROJAN"></span><span id="mp_threat_category_remoteaccesstrojan"></span>**MP \_ Bedrohungs \_ Kategorie \_ remoteaccesstrojan** | Ein Trojaner, der Remote Zugriff auf einen Computer bereitstellt.
<span id="MP_THREAT_CATEGORY_TROJAN"></span><span id="mp_threat_category_trojan"></span>**MP- \_ Bedrohungs \_ Kategorie \_ Trojaner** | Schadsoftware, die sich selbst als legitime Software abfasst.
<span id="MP_THREAT_CATEGORY_EMAILFLOODER"></span><span id="mp_threat_category_emailflooder"></span>**MP \_ Bedrohungs \_ Kategorie \_ emailflooder** | Malware sendet eine große Menge an e-Mail an ein Ziel.
<span id="MP_THREAT_CATEGORY_KEYLOGGER"></span><span id="mp_threat_category_keylogger"></span>**MP \_ \_ \_ Schlüssel Protokollierung der Bedrohungs Kategorie** | Schadsoftware, die die Tastatureingaben des Benutzers aufzeichnet und möglicherweise Kenn Wörter und andere sensible Daten stehlen.
<span id="MP_THREAT_CATEGORY_DIALER"></span><span id="mp_threat_category_dialer"></span>**MP \_ Bedrohungs \_ Kategorie \_ Dialer** | Schadsoftware, die nicht autorisierte Telefonanrufe durchführt, häufig bei Premium-Tarifen.
<span id="MP_THREAT_CATEGORY_MONITORINGSOFTWARE"></span><span id="mp_threat_category_monitoringsoftware"></span>**MP \_ Bedrohungs \_ Kategorie " \_ Monitoringsoftware** " | Eine potenziell unerwünschte Anwendung, die die Benutzeraktivität überwacht, z. b. das, was der Benutzer auf der Tastatur oder den Ansichten auf dem Bildschirm eingibt.
<span id="MP_THREAT_CATEGORY_BROWSERMODIFIER"></span><span id="mp_threat_category_browsermodifier"></span>**MP \_ Bedrohungs \_ Kategorie \_ browsermodifier** | Eine potenziell unerwünschte Anwendung, mit der die Webbrowser Einstellungen ohne Zustimmung des Benutzers geändert werden.
<span id="MP_THREAT_CATEGORY_COOKIE"></span><span id="mp_threat_category_cookie"></span>**MP \_ \_ \_ Cookie der Bedrohungs Kategorie** | Daten, die von einem Webserver an einen Browser gesendet werden, sodass Informationen zum Benutzer, z. b. Webanwendungs Einstellungen, bei wiederholten Besuchen gespeichert werden.
<span id="MP_THREAT_CATEGORY_BROWSERPLUGIN"></span><span id="mp_threat_category_browserplugin"></span>**MP \_ Bedrohungs \_ Kategorie \_ Browserplugin** | Software, mit der ein Standard Webbrowser bestimmte Inhaltstypen, z. b. Mediendateien, animierte Bilder und interaktive Formulare, anzeigen und ausführen kann.
<span id="MP_THREAT_CATEGORY_AOLEXPLOIT"></span><span id="mp_threat_category_aolexploit"></span>**MP \_ Bedrohungs \_ Kategorie \_ aolexploit** | Malware, die Benutzer des AOL-Internet Diensts angreift, häufig durch Abrufen von Kenn Wörtern oder Ändern von Einstellungen.
<span id="MP_THREAT_CATEGORY_NUKER"></span><span id="mp_threat_category_nuker"></span>**MP \_ Bedrohungs \_ Kategorie \_ Nuker** | Schadsoftware, die auf ein Gerät stürzt oder weniger stabil ist.
<span id="MP_THREAT_CATEGORY_SECURITYDISABLER"></span><span id="mp_threat_category_securitydisabler"></span>**MP \_ Bedrohungs \_ Kategorie \_ securitydisabler** | Malware, die Sicherheitseinstellungen oder Produkte deaktiviert.
<span id="MP_THREAT_CATEGORY_JOKEPROGRAM"></span><span id="mp_threat_category_jokeprogram"></span>**MP \_ Bedrohungs \_ Kategorie \_ jokeprogram** | Eine Anwendung, die für einen Benutzer vorgesehen ist, ohne dass das Gerät tatsächlich beschädigt wird.
<span id="MP_THREAT_CATEGORY_HOSTILEACTIVEXCONTROL"></span><span id="mp_threat_category_hostileactivexcontrol"></span>**MP \_ Bedrohungs \_ Kategorie \_ hostileactivexcontrol** | Ein ActiveX-Steuerelement, das von einem Angreifer zum Schaden eines Geräts entworfen wurde. Ein ActiveX-Steuerelement ist eine Art von Browser-Add-on, das für Internet Explorer spezifisch ist.
<span id="MP_THREAT_CATEGORY_SOFTWAREBUNDLER"></span><span id="mp_threat_category_softwarebundler"></span>**MP \_ Bedrohungs \_ Kategorie \_ softwarebundler** | Software, mit der andere potenziell unerwünschte Anwendungen installiert werden, z. b. Adware oder Spyware. Der Lizenzvertrag der bündeln Software erfordert möglicherweise diese anderen Komponenten, damit Sie funktionieren.
<span id="MP_THREAT_CATEGORY_STEALTHNOTIFIER"></span><span id="mp_threat_category_stealthnotifier"></span>**MP \_ Bedrohungs \_ Kategorie \_ stealthnotifier** | Schadsoftware, die über eine Geheimnis Verbindung eine Verbindung mit einem Remote Server herstellt, um einen Angreifer darüber zu benachrichtigen, dass die Schadsoftware installiert wurde.
<span id="MP_THREAT_CATEGORY_SETTINGSMODIFIER"></span><span id="mp_threat_category_settingsmodifier"></span>**MP \_ Bedrohungs \_ Kategorie \_ settingsmodifier** | Eine potenziell unerwünschte Anwendung, die die Einstellungen eines Benutzers ohne das wissen oder die Zustimmung des Benutzers ändert.
<span id="MP_THREAT_CATEGORY_TOOLBAR"></span><span id="mp_threat_category_toolbar"></span>**MP \_ \_ \_ Symbolleiste** für Gefahren Kategorie | Eine potenziell unerwünschte Anwendung (Pua), mit der eine Symbolleiste im Webbrowser des Benutzers installiert wird. häufig mit zusätzlichem Pua, z. b. Adware, gebündelt.
<span id="MP_THREAT_CATEGORY_REMOTECONTROLSOFTWARE"></span><span id="mp_threat_category_remotecontrolsoftware"></span>**MP \_ Bedrohungs \_ Kategorie \_ remotecontrolsoftware** | Eine potenziell unerwünschte Anwendung, die Remote Zugriff auf ein Gerät ermöglicht.
<span id="MP_THREAT_CATEGORY_TROJANFTP"></span><span id="mp_threat_category_trojanftp"></span>**MP \_ Bedrohungs \_ Kategorie \_ trojanftp** | Ein Trojaner, der einen FTP-Server verwendet, um einem Angreifer das Hochladen oder Herunterladen von Dateien von einem Gerät zu ermöglichen.
<span id="MP_THREAT_CATEGORY_POTENTIALUNWANTEDSOFTWARE"></span><span id="mp_threat_category_potentialunwantedsoftware"></span>**MP \_ Bedrohungs \_ Kategorie " \_ potenzialunwantedsoftware** " | Wird auch als *potenziell unerwünschte Anwendung* oder *Pua* bezeichnet. Software, die sich auf eine übermäßig eindringliche Weise verhält, bei der der Benutzer möglicherweise nicht erwartet oder vollständig zugestimmt hat.
<span id="MP_THREAT_CATEGORY_ICQEXPLOIT"></span><span id="mp_threat_category_icqexploit"></span>**MP \_ Bedrohungs \_ Kategorie \_ icqexploit** | Ein Trojaner, der den Dienst für den ICQ-Messaging angreift, häufig durch Abrufen von Kenn Wörtern oder manipulieren von Einstellungen.
<span id="MP_THREAT_CATEGORY_TROJANTELNET"></span><span id="mp_threat_category_trojantelnet"></span>**MP \_ Bedrohungs \_ Kategorie \_ trojantelnet** | Ein Trojaner, der einen Telnet-Server auf dem Computer eines Benutzers ohne das wissen oder die Zustimmung des Benutzers installiert.
<span id="MP_THREAT_CATEGORY_EXPLOIT"></span><span id="mp_threat_category_exploit"></span>**MP \_ \_ \_ ausnutzen der Bedrohungs Kategorie** | Bösartiger Code, der ein Sicherheitsrisiko auf einem Gerät oder System nutzt.
<span id="MP_THREAT_CATEGORY_FILESHARINGPROGRAM"></span><span id="mp_threat_category_filesharingprogram"></span>**MP \_ Bedrohungs \_ Kategorie \_ filesharingprogram** | Eine potenziell unerwünschte Anwendung, die ein Gerät für die Peer-to-Peer-Freigabe der Gerätedateien öffnet.
<span id="MP_THREAT_CATEGORY_MALWARE_CREATION_TOOL"></span><span id="mp_threat_category_malware_creation_tool"></span>**MP \_ Bedrohungs \_ Kategorie \_ Malware \_ Erstellungs \_ Tool** | Eine Anwendung, die automatisch schädliche Dateien generieren kann.
<span id="MP_THREAT_CATEGORY_REMOTE_CONTROL_SOFTWARE"></span><span id="mp_threat_category_remote_control_software"></span>**MP \_ Bedrohungs \_ Kategorie \_ Remote \_ Steuerungs \_ Software** | Eine potenziell unerwünschte Anwendung, die den Remote Zugriff auf ein Gerät ermöglicht.
<span id="MP_THREAT_CATEGORY_TOOL"></span><span id="mp_threat_category_tool"></span>**MP \_ \_ \_ Tool zur Bedrohungs Kategorie** | Ein Hilfsprogramm, das einem Angreifer hilft, böswillige Aktionen auf einem Gerät auszuführen.
<span id="MP_THREAT_CATEGORY_TROJAN_DENIALOFSERVICE"></span><span id="mp_threat_category_trojan_denialofservice"></span>**MP \_ Bedrohungs \_ Kategorie \_ Trojaner- \_ verweialog-Dienst** | Ein Trojaner, der so konzipiert ist, dass er eine große Menge an Netzwerk Anforderungen als Teil eines Denial-of-Service-Angriffs (DOS) an ein Ziel sendet.
<span id="MP_THREAT_CATEGORY_TROJAN_DROPPER"></span><span id="mp_threat_category_trojan_dropper"></span>**MP \_ Bedrohungs \_ Kategorie \_ Trojaner- \_ dropperungs** | Ein Trojaner, der Schadsoftware oder potenziell unerwünschte Anwendungen auf einem Ziel herunterlädt und installiert.
<span id="MP_THREAT_CATEGORY_TROJAN_MASSMAILER"></span><span id="mp_threat_category_trojan_massmailer"></span>**MP \_ Bedrohungs \_ Kategorie \_ Trojaner- \_ toolmailer** | Ein Trojaner, der eine große Anzahl von e-Mails an ein Ziel sendet, um den Eingang des Ziels zu überlasten.
<span id="MP_THREAT_CATEGORY_TROJAN_MONITORINGSOFTWARE"></span><span id="mp_threat_category_trojan_monitoringsoftware"></span>**MP \_ Bedrohungs \_ Kategorie \_ Trojaner \_ Monitoringsoftware** | Ein Trojaner, der die Benutzeraktivität überwacht, z. b. das, was der Benutzer auf der Tastatur oder Ansichten auf dem Bildschirm eingibt.
<span id="MP_THREAT_CATEGORY_TROJAN_PROXYSERVER"></span><span id="mp_threat_category_trojan_proxyserver"></span>**MP \_ Bedrohungs \_ Kategorie \_ Trojaner \_ Proxyserver** | Ein von einem Trojaner installierter Proxy Server, der eine unterbrechungsfreie Internet Verbindung bereitstellt und gleichzeitig nicht autorisierten Zugriff auf das infizierte Gerät ermöglicht.
<span id="MP_THREAT_CATEGORY_VIRUS"></span><span id="mp_threat_category_virus"></span>**MP \_ Bedrohungs \_ Kategorie \_ Virus** | Schadsoftware, die in der Regel durch das infizieren anderer Dateien im System repliziert wird. Dadurch wird die Ausführung des schadsoftwarecodes und dessen Weitergabe ermöglicht, wenn diese Dateien aktiviert werden.
<span id="MP_THREAT_CATEGORY_KNOWN"></span><span id="mp_threat_category_known"></span>**MP \_ \_ \_ bekannte Bedrohungs Kategorie** | Eine nicht angegebene Malware Bedrohung.
<span id="MP_THREAT_CATEGORY_UNKNOWN"></span><span id="mp_threat_category_unknown"></span>**MP \_ Bedrohungs \_ Kategorie \_ unbekannt** | Eine nicht angegebene Malware Bedrohung, die noch nicht definiert wurde.
<span id="MP_THREAT_CATEGORY_SPP"></span><span id="mp_threat_category_spp"></span>**MP \_ \_ \_ spp der Bedrohungs Kategorie** | Antipiraterie-Technologie, die die Installation eines Windows-Produkts erfordert, muss mit Microsoft aktiviert werden.
<span id="MP_THREAT_CATEGORY_BEHAVIOR"></span><span id="mp_threat_category_behavior"></span>**MP \_ \_ \_ Verhalten der Bedrohungs Kategorie** | Ein Erkennungs Typ, der auf Dateiaktionen basiert, die häufig mit böswilligen Aktivitäten verknüpft sind.
<span id="MP_THREAT_CATEGORY_VULNERABILTIY"></span><span id="mp_threat_category_vulnerabiltiy"></span>**MP \_ Bedrohungs \_ Kategorie " \_ Vulnerability abiltiy** " | Jegliche Schwachstellen, administrative Prozesse oder Aktivitäten, durch die ein Gerät anfällig für das ausnutzen durch eine Bedrohung wird.
<span id="MP_THREAT_CATEGORY_POLICY"></span><span id="mp_threat_category_policy"></span>**MP \_ \_ \_ Richtlinien Richtlinie** | Eine Reihe von Regeln, die von einem Administrator definiert werden und die Features auf Desktop Computern und mobilen Geräten wie Software Updates steuern.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Unterstützte Mindestversion (Client) | Windows 8 (nur Desktop-Apps) |
| Unterstützte Mindestversion (Server) | Windows Server 2012 (nur Desktop-Apps) |
| Header | Mpclient. h |
