---
description: Ab Windows Vista erhalten in Windows enthaltene System Steuerungselemente einen kanonischen Namen, der in einem API-Befehl oder in einer Befehlszeilen Anweisung zum programmgesteuerten Starten dieses Elements verwendet werden kann.
ms.assetid: A02DFC9F-646D-40d8-901C-7239A820DE2C
title: Kanonische Namen von System Steuerungselementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a55fc360b0d3db0f85a057977d1898c59d09d5cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958773"
---
# <a name="canonical-names-of-control-panel-items"></a>Kanonische Namen von System Steuerungselementen

Ab Windows Vista erhalten in Windows enthaltene System Steuerungselemente einen kanonischen Namen, der in einem [API-Befehl oder in einer Befehlszeilen Anweisung](executing-control-panel-items.md) zum programmgesteuerten Starten dieses Elements verwendet werden kann. Ab Windows 7 und Windows Server 2008 R2 können kanonische Namen in einer Gruppenrichtlinie verwendet werden, um bestimmte System Steuerungselemente auszublenden. Dieses Thema enthält Details zu den einzelnen System Steuerungselementen: kanonischer Name, Guid, Modulname und Betriebssystemversionen, die den kanonischen Namen erkennen.

> [!Note]  
> Kanonische Namen für System Steuerungselemente werden vor Windows Vista nicht unterstützt.

 

-   [Kanonische Namen der Systemsteuerung](#control-panel-canonical-names)
-   [Als veraltet markierte kanonische Name der Systemsteuerung](#deprecated-control-panel-canonical-names)
-   [Verwenden von kanonischen Namen in Gruppenrichtlinie](#using-canonical-names-in-local-group-policy)
-   [Anmerkungen](#remarks)

## <a name="control-panel-canonical-names"></a>Kanonische Namen der Systemsteuerung

Beachten Sie beim Arbeiten mit diesen Werten Folgendes:

-   In der Definition werden kanonische Namen nicht auf der Grundlage der Systemsprache geändert. Sie sind immer in englischer Sprache, auch wenn die Sprache des Systems nicht ist.
-   Nicht alle System Steuerungselemente sind in allen Arten von Fenstern vorhanden.
-   Einige System Steuerungselemente werden nur angezeigt, wenn auf dem System die richtige Hardware erkannt wird.
-   Drittanbieter können auch System Steuerungselemente hinzufügen. Die hier aufgeführten kanonischen Namen gelten nur für System Steuerungselemente, die in Windows enthalten sind.

Im folgenden finden Sie die System Steuerungselemente, die in Windows 8.1 verfügbar sind:

-   [Info-Center](#action-center)
-   [Verwaltungs Tools](#administrative-tools)
-   [Automatische Wiedergabe](#autoplay)
-   [Biometrische Geräte](#biometric-devices)
-   [BitLocker-Laufwerkverschlüsselung](#bitlocker-drive-encryption)
-   [Farbverwaltung](#color-management)
-   [Anmeldeinformationsverwaltung](#credential-manager)
-   [Datum und Uhrzeit](#date-and-time)
-   [Standardprogramme](#default-programs)
-   [Geräte-Manager](#device-manager)
-   [Geräte und Drucker](#devices-and-printers)
-   [Anzeige](#display)
-   [Center für erleichterte Bedienung](#ease-of-access-center)
-   [Family Safety](#family-safety)
-   [Dateiversionsverlauf](#file-history)
-   [Ordneroptionen](#folder-options)
-   [Schriftarten](#fonts)
-   [Heimnetzgruppe](#homegroup)
-   [Indizierungs Optionen](#indexing-options)
-   [Infrarot](#infrared)
-   [Internetoptionen](#internet-options)
-   [iSCSI-Initiator](#iscsi-initiator)
-   [iSNS-Server](#isns-server)
-   [Tastatur](#keyboard)
-   [Standorteinstellungen](#location-settings)
-   [Maus](#mouse)
-   [Mpioconfiguration](#mpioconfiguration)
-   [Netzwerk- und Freigabecenter](#network-and-sharing-center)
-   [Benachrichtigungs Bereichs Symbole](#notification-area-icons)
-   [Stift und berühren](#pen-and-touch)
-   [Personalisierung](#personalization)
-   [Telefon und Modem](#phone-and-modem)
-   [Energieoptionen](#power-options)
-   [Programme und Funktionen](#programs-and-features)
-   [Wiederherstellung](#recovery)
-   [Region](#region)
-   [RemoteApp- und Desktopverbindungen](#remoteapp-and-desktop-connections)
-   [Sound](#sound)
-   [Spracherkennung](#speech-recognition)
-   [Speicherplätze](#storage-spaces)
-   [Synchronisierungscenter](#sync-center)
-   [System](#system)
-   [Tablet PC-Einstellungen](#tablet-pc-settings)
-   [Taskleiste und Navigation](#taskbar-and-navigation)
-   [Problembehandlung](#troubleshooting)
-   ["T AppInstall"](#tsappinstall)
-   [User Accounts (Benutzerkonten)](#user-accounts)
-   [Windows Anytime Upgrade](#windows-anytime-upgrade)
-   [Windows Defender](#windows-defender)
-   [Windows-Firewall](#windows-firewall)
-   [Windows-Mobilitätscenter](#windows-mobility-center)
-   [Windows To Go](#windows-to-go)
-   [Windows Update](#windows-update)
-   [Arbeitsordner](#work-folders)

### <a name="action-center"></a>Info-Center

-   **Kanonischer Name**: Microsoft. Aktions Center
-   **GUID**: {BB64F8A7-BEE7-4E1A-AB8D-7D8273F7FDB6}
-   **Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\ActionCenterCPL.dll,-1
-   **Seiten**

    | Seitenname           | Opens                      |
    |---------------------|----------------------------|
    | Maintenancesettings | Automatische Wartung      |
    | pageproblems        | Problemberichte            |
    | pageReliabilityView | Zuverlässigkeits Monitor        |
    | pageResponseArchive | Archivierte Nachrichten          |
    | pgesettings        | Problem Berichterstattungs Einstellungen |

    

     

### <a name="administrative-tools"></a>Verwaltung

-   **Kanonischer Name**: Microsoft. AdministrativeTools
-   **GUID**: {D20EA4E1-3957-11d2-A40B-0C5020524153}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\shell32.dll,-22982

### <a name="autoplay"></a>Automatische Wiedergabe

-   **Kanonischer Name**: Microsoft. AutoPlay
-   **GUID**: {9c60de1e-e5fc-40b4-a487-460851a8d915}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\autoplay.dll,-1

### <a name="biometric-devices"></a>Biometrische Geräte

-   **Kanonischer Name**: Microsoft. biometricdevices
-   **GUID**: {0142e4d0-fb7a-11dc-ba4a-000ffe7ab428}
-   **Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\biocpl.dll,-1

### <a name="bitlocker-drive-encryption"></a>BitLocker-Laufwerkverschlüsselung

-   **Kanonischer Name**: Microsoft. bitlockerdriveencryption
-   **GUID**: {D9EF8727-CAC2-4e60-809E-86F80A666C91}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\fvecpl.dll,-1

### <a name="color-management"></a>Farbverwaltung

-   **Kanonischer Name**: Microsoft. Colormanagement
-   **GUID**: {B2C761C6-29BC-4f19-9251-E6195265BAF1}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\colorcpl.exe,-6

### <a name="credential-manager"></a>Anmeldeinformationsverwaltung

-   **Kanonischer Name**: Microsoft. kredentialmanager
-   **GUID**: {1206F5F1-0569-412C-8FEC-3204630DFB70}
-   **Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\Vault.dll,-1
-   **Seiten**

    | Seitenname                   | Opens               |
    |-----------------------------|---------------------|
    | ? Selectedvault = "kredmanvault" | Windows-Anmelde Informationen |

    

     

### <a name="date-and-time"></a>Datum und Uhrzeit

-   **Kanonischer Name**: Microsoft. DateAndTime
-   **GUID**: {E2E7934B-DCE5-43C4-9576-7FE4F75E7480}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\timedate.cpl,-51
-   **Seiten**

    | Seitenname | Opens             |
    |-----------|-------------------|
    | 1         | Weitere Uhren |

    

     

### <a name="default-programs"></a>Standardprogramme

-   **Kanonischer Name**: Microsoft. defaultprograms
-   **GUID**: {17cd9488-1228-4b2f -88ce-4298e93e0966}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\sud.dll,-1
-   **Seiten**

    | Seitenname          | Opens                |
    |--------------------|----------------------|
    | pagedefaultprogram | Standardprogramme festlegen |
    | pagefileassoc      | Zuordnungen festlegen     |

    

     

### <a name="device-manager"></a>Geräte-Manager

-   **Kanonischer Name**: Microsoft. Debug Manager
-   **GUID**: {74246bfc-4c96-11D0-ABEF -0020af6b0b7a}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\devmgr.dll,-4

### <a name="devices-and-printers"></a>Geräte und Drucker

-   **Kanonischer Name**: Microsoft. Geräte Handler
-   **GUID**: {A8A91A66-3A7D-4424-8D24-04E180695C7A}
-   **Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\DeviceCenter.dll,-1000

### <a name="display"></a>Anzeige

-   **Kanonischer Name**: Microsoft. Display
-   **GUID**: {C555438B-3C23-4769-A71F-B6D3D9B6053A}
-   **Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\Display.dll,-1
-   **Seiten**

    | Seitenname | Opens             |
    |-----------|-------------------|
    | Einstellungen  | Bildschirmauflösung |

    

     

### <a name="ease-of-access-center"></a>Center für erleichterte Bedienung

-   **Kanonischer Name**: Microsoft. easeofakcescenters
-   **GUID**: {D555645E-D4F8-4c29-A827-D93C859C4F2A}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\accessibilitycpl.dll,-10
-   **Seiten**

    | Seitenname               | Opens                                                               |
    |-------------------------|---------------------------------------------------------------------|
    | pageeasierper Click       | Vereinfachen Sie die Verwendung der Maus                                        |
    | pageeasiergesee         | Machen Sie den Computer leichter zu erkennen                                     |
    | pageeasierwithsounds    | Verwenden von Text oder visuellen Alternativen für Sounds                          |
    | "pgefilterkeyssettings"  | Einrichten von Filter Schlüsseln                                                  |
    | pagekeyboardebug | Vereinfachen der Verwendung der Tastatur                                     |
    | pagenomouonorkeyboard   | Computer ohne Maus oder Tastatur verwenden                        |
    | pagenovisual            | Verwenden des Computers ohne Anzeige                                  |
    | pagefrag scognitive  | Empfehlungen zur einfacheren Verwendung Ihres Computers erhalten (Cognitive) |
    | pagefrag \ yesight   | Empfehlungen zur einfacheren Verwendung Ihres Computers (eyesight)  |

    

     

### <a name="family-safety"></a>Family Safety

-   **Kanonischer Name**: Microsoft. Parser Controls
-   **GUID**: {96ae8d84-A250-4520-95a5-a47a7e3c548b}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\wpccpl.dll,-100
-   **Seiten**

    | Seitenname   | Opens                                  |
    |-------------|----------------------------------------|
    | pageuserhub | Auswählen eines Benutzers und Einrichten der Familien Sicherheit |

    

     

### <a name="file-history"></a>Dateiversionsverlauf

-   **Kanonischer Name**: Microsoft. File History
-   **GUID**: {F6B6E965-E9B2-444B-9286-10C9152EDBC5}
-   **Unterstütztes Betriebssystem**: Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\fhcpl.dll,-52
-   Der Datei Versionsverlauf enthält eine neuere Version des Sicherungs-und Wiederherstellungs Elements, aber der kanonische Name des älteren Elements wird nicht dem Datei Versionsverlauf zugeordnet.

### <a name="folder-options"></a>Ordneroptionen

-   **Kanonischer Name**: Microsoft. folderoptions
-   **GUID**: {6dfd7c5c-2451-11d3-A299-00c04r8ef6af}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\shell32.dll,-22985

### <a name="fonts"></a>Schriftarten

-   **Kanonischer Name**: Microsoft. Fonts
-   **GUID**: {93412589-74d4-4e4e-ad0e-e0cb621440fd}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\FontExt.dll,-8007

### <a name="homegroup"></a>Heimnetzgruppe

-   **Kanonischer Name**: Microsoft. HomeGroup
-   **GUID**: {67ca7650-96e6-4fdd-BB43-a8e774f73a57}
-   **Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\hgcpl.dll,-1

### <a name="indexing-options"></a>Indizierungsoptionen

-   **Kanonischer Name**: Microsoft. indexingoptions
-   **GUID**: {87d66a43-7b11-4a28-9811-c86ee395acb7}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\srchadmin.dll,-601

### <a name="infrared"></a>Infrarot

-   **Kanonischer Name**: Microsoft. Infrarot
-   **GUID**: {A0275511-0E86-4ECA-97C2-ECD8F1221D08}
-   **Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\irprops.cpl,-1

### <a name="internet-options"></a>Internetoptionen

-   **Kanonischer Name**: Microsoft. internetoptions
-   **GUID**: {A3DD4F92-658A-410F-84FD-6FBBBEF2FFFE}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @C: \\ Windows \\ system32 \\inetcpl.cpl,-4312
-   **Seiten**

    | Seitenname | Opens       |
    |-----------|-------------|
    | 1         | Sicherheit    |
    | 2         | Datenschutz     |
    | 3         | Inhalt     |
    | 4         | Verbindungen |
    | 5         | Programs    |
    | 6         | Erweitert    |

    

     

### <a name="iscsi-initiator"></a>iSCSI-Initiator

-   **Kanonischer Name**: Microsoft. iscsiinitiator
-   **GUID**: {A304259D-52B8-4526-8B1A-A1D6CECC8243}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\iscsicpl.dll,-5001

### <a name="isns-server"></a>iSNS-Server

-   **Kanonischer Name**: Microsoft. isnsserver
-   **GUID**: {0d2a3442-5181-4e3a-9bd4-83bd10af3d76}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\isnssrv.dll,-5005
-   Dieses System Steuerungselement wird nur in Serverversionen von Windows angezeigt.

### <a name="keyboard"></a>Tastatur

-   **Kanonischer Name**: Microsoft. Keyboard
-   **GUID**: {725be8b7-668e-4c7b-8F 90-46bdb0936430}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\main.cpl,-102

### <a name="location-settings"></a>Standorteinstellungen

-   **Kanonischer Name**: Microsoft. locationsettings
-   **GUID**: {E9950154-C418-419e-A90A-20C5287AE24B}
-   **Unterstütztes Betriebssystem**: Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\SensorsCpl.dll,-1

### <a name="mouse"></a>Maus

-   **Kanonischer Name**: Microsoft. Mouse
-   **GUID**: {6c8eec18-8d75-41b2-a177-8831d59d2d50}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\main.cpl,-100
-   **Seiten**

    | Seitenname | Opens           |
    |-----------|-----------------|
    | 1         | Zeiger        |
    | 2         | Zeiger Optionen |
    | 3         | Wheel           |
    | 4         | Hardware        |

    

     

### <a name="mpioconfiguration"></a>Mpioconfiguration

-   **Kanonischer Name**: Microsoft. mpioconfiguration
-   **GUID**: {AB3BE6AA-7561-4838-AB77-ACF8427DF426}
-   **Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\mpiocpl.dll,-1000
-   Dieses System Steuerungselement wird nur in Serverversionen von Windows angezeigt.

### <a name="network-and-sharing-center"></a>Netzwerk- und Freigabecenter

-   **Kanonischer Name**: Microsoft. networkandsharingcenter
-   **GUID**: {8e908fc9-becc-40f 6-915b-f 4ca0e70d03d}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\netcenter.dll,-1
-   **Seiten**

    | Seitenname  | Opens                     |
    |------------|---------------------------|
    | Erweitert   | Erweiterte Freigabe Einstellungen |
    | Share Media | Optionen für Medien Streaming   |

    

     

### <a name="notification-area-icons"></a>Benachrichtigungs Bereichs Symbole

-   **Kanonischer Name**: Microsoft. notificationareaicons
-   **GUID**: {05d7b0f 4-2121-4eff-BB. b-ed3g69b894d9}
-   **Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\taskbarcpl.dll,-1

### <a name="pen-and-touch"></a>Stift und berühren

-   **Kanonischer Name**: Microsoft. pandtouchscreen
-   **GUID**: {F82DF8F7-8B9F-442E-A48C-818EA735FF9B}
-   **Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\tabletpc.cpl,-10103
-   **Seiten**

    | Seitenname | Opens       |
    |-----------|-------------|
    | 1         | Schnelle Stift Bewegungen      |
    | 2         | Handwriting |

    

     

### <a name="personalization"></a>Personalization

-   **Kanonischer Name**: Microsoft. Personalization
-   **GUID**: {ED834ED6-4B5A-4bfe-8F11-A626DCB6A921}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\themecpl.dll,-1
-   **Seiten**

    | Seitenname        | Opens                |
    |------------------|----------------------|
    | pagecolorzation | Farbe und Darstellung |
    | "paarblatt"    | Desktop Hintergrund   |

    

     

### <a name="phone-and-modem"></a>Telefon und Modem

-   **Kanonischer Name**: Microsoft. phoneandmodem
-   **GUID**: {40419485-C444-4567-851a-2dd7bfa1684d}
-   **Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\telephon.cpl,-1
-   Das Fenster, in dem dieser Wert gestartet wird, wird in Windows-Versionen vor Windows 8 als "Standortinformationen" angezeigt. Die Benutzeroberfläche des Elements ändert sich ab Windows 8 erheblich.

### <a name="power-options"></a>Energieoptionen

-   **Kanonischer Name**: Microsoft. poweroptions
-   **GUID**: {025a5937-A6BE-4686-A844-36fe4bec8b6d}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\powercpl.dll,-1
-   **Seiten**

    | Seitenname          | Opens              |
    |--------------------|--------------------|
    | pageglobalsettings | Systemeinstellungen    |
    | pagePlanSettings   | Plan Einstellungen bearbeiten |

    

     

### <a name="programs-and-features"></a>Programme und Funktionen

-   **Kanonischer Name**: Microsoft. Program Sand Features
-   **GUID**: {7b81be6a-ce2b-4676-a29e-eb907a5126c5}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\appwiz.cpl,-159
-   **Seiten**

    | Seitenname                                | Opens             |
    |------------------------------------------|-------------------|
    | ::{D450A8A1-9568-45C7-9C0E-B4F9FB4537BD} | Installierte Updates |

    

     

### <a name="recovery"></a>Wiederherstellung

-   **Kanonischer Name**: Microsoft. Recovery
-   **GUID**: {9fe63afd-59cf-4419-9775-ABCC3849F861}
-   **Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\recovery.dll,-101

### <a name="region"></a>Region

-   **Kanonischer Name**: Microsoft. regionandlanguage
-   **GUID**: {62d8ed13-C9D0-4ce8-a914-47dd628bb1b0}
-   **Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\intl.cpl,-1
-   Das in Windows 7 gefundene Regions-und sprach Element war von Windows 8 getrennt. Microsoft. regionandlanguage öffnet nun das Regions Element. Verwenden Sie [Microsoft. Language](#location-settings), um das sprach Element zu starten.
-   **Seiten**

    | Seitenname | Opens          |
    |-----------|----------------|
    | 1         | Standort       |
    | 2         | Administrative |

    

     

### <a name="remoteapp-and-desktop-connections"></a>RemoteApp- und Desktopverbindungen

-   **Kanonischer Name**: Microsoft. remoteappanddesktopconnections
-   **GUID**: {241d7c96-s8bf -4s85-b01t-e2b043341a4b}
-   **Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\tsworkspace.dll,-15300

### <a name="sound"></a>Sound

-   **Kanonischer Name**: Microsoft. Sound
-   **GUID**: {F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}
-   **Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\mmsys.cpl,-300

### <a name="speech-recognition"></a>Spracherkennung

-   **Kanonischer Name**: Microsoft. Sprech Erkennung
-   **GUID**: {58e3c745-D971-4081-9034-86e34b30836a}
-   **Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\ Speech Speech \\ UX \\speechuxcpl.dll,-1

### <a name="storage-spaces"></a>Speicherplätze

-   **Kanonischer Name**: Microsoft. storagespaces
-   **GUID**: {F942C606-0914-47AB-BE56-1321B8035096}
-   **Unterstütztes Betriebssystem**: Windows 8, Windows 8.1
-   **Modulname**: @C: \\ Windows \\ system32 \\SpaceControl.dll,-1

### <a name="sync-center"></a>Synchronisierungscenter

-   **Kanonischer Name**: Microsoft. synccenter
-   **GUID**: {9c73f 5e5-7 AE7-4e32-a8e8-8d23b85255bf}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\SyncCenter.dll,-3000

### <a name="system"></a>System

-   **Kanonischer Name**: Microsoft.System
-   **GUID**: {BB06C0E4-D293-4f75-8A90-CB05B6477EEE}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\systemcpl.dll,-1

### <a name="tablet-pc-settings"></a>Tablet PC-Einstellungen

-   **Kanonischer Name**: Microsoft. tabletpcsettings
-   **GUID**: {80F 5-FECA-45b3-BC32-752c152e456e}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\tabletpc.cpl,-10100

### <a name="taskbar-and-navigation"></a>Taskleiste und Navigation

-   **Kanonischer Name**: Microsoft. Taskleiste
-   **GUID**: {0df44eaa-ff21-4412-828e-260a8728e7f1}
-   **Unterstütztes Betriebssystem**: Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\shell32.dll,-32517

### <a name="troubleshooting"></a>Problembehandlung

-   **Kanonischer Name**: Microsoft. Troubleshooting
-   **GUID**: {C58C4893-3BE0-4B45-ABB5-A63E4B8C8651}
-   **Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\DiagCpl.dll,-1
-   **Seiten**

    | Seitenname   | Opens   |
    |-------------|---------|
    | Historypage | Verlauf |

    

     

### <a name="tsappinstall"></a>"T AppInstall"

-   **Kanonischer Name**: Microsoft. tappinstall
-   **GUID**: {BAA884F4-3432-48b8-aa72-9BF20EEF31D5}
-   **Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\tsappinstall.exe,-2001

### <a name="user-accounts"></a>Benutzerkonten

-   **Kanonischer Name**: Microsoft. UserAccounts
-   **GUID**: {60632754-C523-4b62-b45c-4172da012619}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\usercpl.dll,-1

### <a name="windows-anytime-upgrade"></a>Windows Anytime Upgrade

-   **Kanonischer Name**: Microsoft. windowsanytimeupgrade
-   **GUID**: {BE122A0E-4503-11DA-8BDE-F66BAD1E3F3A}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @ $ (resourcestring). \_ SYS \_ mod \_ -Pfad),-1

### <a name="windows-defender"></a>Windows Defender

-   **Kanonischer Name**: Microsoft. windowsdefender
-   **GUID**: {D8559EB9-20C0-410E-Beda-7ED416AECC2A}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @% Program Files% \\ Windows Defender \\MsMpRes.dll,-104

### <a name="windows-firewall"></a>Windows-Firewall

-   **Kanonischer Name**: Microsoft. WindowsFirewall
-   **GUID**: {4026492f -2F 69-46b8-b9bf -5654fc07e423}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @C: \\ Windows \\ system32 \\FirewallControlPanel.dll,-12122
-   **Seiten**

    | Seitenname         | Opens        |
    |-------------------|--------------|
    | pagekonfigurireapps | Zulässige Apps |

    

     

### <a name="windows-mobility-center"></a>Windows-Mobilitätscenter

-   **Kanonischer Name**: Microsoft. MobilityCenter
-   **GUID**: {5ea4f 148-308c-46d7-98a9-49041b1dd468}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\mblctr.exe,-1002

### <a name="windows-to-go"></a>Windows To Go

-   **Kanonischer Name**: Microsoft. portableworkspacecreator
-   **GUID**: {8e0c279d-0bd1-43c3-9ebd-31c3dc5b8a77}
-   **Unterstütztes Betriebssystem**: Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\pwcreator.exe,-151

### <a name="windows-update"></a>Windows-Update

-   **Kanonischer Name**: Microsoft. windowsupdate
-   **GUID**: {36eef7db-88ad-4e81-AD49-0e313f 0c35f}
-   **Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname**: @% systemroot% \\ system32 \\wucltux.dll,-1
-   **Seiten**

    | Seitenname         | Opens               |
    |-------------------|---------------------|
    | pgesettings      | Änderung der Einstellungen     |
    | pageupdatehistory | Aktualisierungs Verlauf anzeigen |

    

     

### <a name="work-folders"></a>Arbeitsordner

-   **Kanonischer Name**: Microsoft. workfolders
-   **GUID**: {ECDB0924-4208-451E-8EE0-373C0956DE16}
-   **Unterstütztes Betriebssystem**: Windows 8.1
-   **Modulname**: @C: \\ Windows \\ system32 \\WorkfoldersControl.dll,-1

## <a name="deprecated-control-panel-canonical-names"></a>Als veraltet markierte kanonische Name der Systemsteuerung

Im folgenden werden kanonische Namen verwendet, die nicht mehr ab Windows 8.1 oder höher verwendet werden. Einige wurden vollständig entfernt. Andere wurden in folgenden Situationen neu zugeordnet:

-   Ein System Steuerungselement wurde umbenannt. Das umbenannte Element erhält einen neuen kanonischen Namen, behält aber dieselbe GUID bei. In diesem Fall wird mit dem alten kanonischen Namen das umbenannte System Steuerungselement gestartet. Beachten Sie, dass das Element, das gestartet wird, möglicherweise nicht die gleiche Benutzeroberfläche wie die ältere Version dieses Elements verwendet.
-   Die Funktionalität eines oder mehrerer System Steuerungselemente wird in ein neues Element verschoben oder konsolidiert. In diesem Fall wird der alte kanonische Name dem geeignetsten neuen System Steuerungselement zugeordnet.

> [!Note]  
> Neuzuordnungen sind aus Gründen der Abwärtskompatibilität vorhanden. Als veraltet markierte Werte sollten nicht in neuem Code verwendet werden.

 



| Der als veraltet markierte kanonische Name                                   | System Steuerungselement                | GUID                                   | Notizen                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------|-----------------------------------|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Microsoft. addhardware                                       | Hardware hinzufügen                      | {7a979262-40ce-46ff-Aeee-7884ac3b6136} | Wird [Microsoft. devicesandprinters](#devices-and-printers) ab Windows 7 zugeordnet.                                                                                                                                                                                                                                                                            |
| Microsoft. audiodebug-Themen                        | Sound                             | {F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D} | Wird [Microsoft. Sound](#sound) ab Windows 7 zugeordnet.                                                                                                                                                                                                                                                                                                        |
| Microsoft. backupandrestorecenter/Microsoft. backupandrestore | Sicherungs-und Wiederherstellungs Center         | {B98A2BEA-7D42-4558-8BD1-832F41BAC6FD} | Microsoft. backupandrestorecenter ist in Windows 7 Microsoft. backupandrestore zugeordnet. Beide werden ab Windows 8 entfernt. Verwenden Sie stattdessen [Microsoft. File History](#file-history) .                                                                                                                                                                                   |
| Microsoft. CardSpace                                         | Windows CardSpace                 | {78cb147 a-98ea-4aa6-b0df-c8681f 69341c} | Entfernt ab Windows 8.                                                                                                                                                                                                                                                                                                                                  |
| Microsoft. Desktopgadgets                                    | Desktop Gadgets                   | {37efd44d-ef8d-41b1-940d-96973a50e9e0} | Entfernt ab Windows 8.                                                                                                                                                                                                                                                                                                                                  |
| Microsoft. getprogramsonline                                 | Windows Marketplace               | {3e7efb4c-laf1-453d-89eb-56026875ef90} | Entfernt ab Windows 7.                                                                                                                                                                                                                                                                                                                                  |
| Microsoft. infraredoptions                                   | Infrarot                          | {A0275511-0E86-4ECA-97C2-ECD8F1221D08} | Wird [Microsoft. INFRAS](#infrared) von Windows 7 zugeordnet.                                                                                                                                                                                                                                                                                                  |
| Microsoft. Language                                          | Sprache                          | {BF782CC9-5A52-4A17-806C-2A894FFEEAC5} | Entfernt ab Windows 10, Version 1803                                                                                                                                                                                                                                                                                                                    |
| Microsoft. locationandothersensors                           | Speicherort und andere Sensoren        | {E9950154-C418-419e-A90A-20C5287AE24B} | Wird [Microsoft. locationsettings](#infrared) ab Windows 8 zugeordnet.                                                                                                                                                                                                                                                                                          |
| Microsoft. pandinputdevices                                | Stift-und Eingabegeräte             | {F82DF8F7-8B9F-442E-A48C-818EA735FF9B} | Wird [Microsoft. pandtouchscreen](#pen-and-touch) ab Windows 7 zugeordnet.                                                                                                                                                                                                                                                                                          |
| Microsoft. PeopleNearMe                                      | Personen in meiner Umgebung                    | {5224f 545-a443-4859-ba23-7b5a95bdc8ef} | Entfernt ab Windows 8.                                                                                                                                                                                                                                                                                                                                  |
| Microsoft. performanceingeformationandtools                    | Leistungsinformationen und-Tools | {78f 3955e-3b90-4184-bd14-5397c15f 1efc} | Entfernt ab Windows 8.1.                                                                                                                                                                                                                                                                                                                                |
| Microsoft. phoneandmudeoptions                              | Telefon und Modem                   | {40419485-C444-4567-851a-2dd7bfa1684d} | Wird [Microsoft. phoneandmodem](#phone-and-modem) ab Windows 7 zugeordnet.                                                                                                                                                                                                                                                                                      |
| Microsoft. Printers                                          | Drucker                          | {2227a280-3aea-1069-A2DE-08002b30309d} | Wird [Microsoft. devicesandprinters](#devices-and-printers) ab Windows 7 zugeordnet.                                                                                                                                                                                                                                                                            |
| Microsoft. problemreportsandsolutions                        | Problemberichte und -lösungen     | {Fcfeecae-EE1B-4849-AE50-685dcf7717ec} | Wird [Microsoft. aktioncenter](#action-center) ab Windows 7 zugeordnet.                                                                                                                                                                                                                                                                                         |
| Microsoft. regionandlanguageoptions                        | Regions- und Sprachoptionen     | {62d8ed13-C9D0-4ce8-a914-47dd628bb1b0} | Wird [Microsoft. regionandlanguage](#region) von Windows 7 zugeordnet. Beachten Sie, dass für die Region und die Sprache ab Windows 8 jeweils ein eigenes System Steuerungselement angegeben wurde. Sowohl Microsoft. regionandlanguageoptions als auch Microsoft. regionandlanguage öffnen das Regions Element zurzeit. Für den Zugriff auf das sprach Element müssen Sie [Microsoft. Language](#location-settings) verwenden. |
| Microsoft. SecurityCenter                                    | Windows-Security Center           | {087da31b-0dd3-4537-8e23-64a18591b88b} | Wird [Microsoft. aktioncenter](#action-center) ab Windows 7 zugeordnet.                                                                                                                                                                                                                                                                                         |
| Microsoft. Sprech Erkennungs Optionen                          | Optionen für die Spracherkennung        | {58e3c745-D971-4081-9034-86e34b30836a} | Wird [Microsoft. Sprech Erkennung](#speech-recognition) ab Windows 7 zugeordnet.                                                                                                                                                                                                                                                                               |
| Microsoft. taskbarandstartmenu                               | Taskleiste und Startmenü            | {0df44eaa-ff21-4412-828e-260a8728e7f1} | Wird [Microsoft. Taskbar](#speech-recognition) ab Windows 8 zugeordnet.                                                                                                                                                                                                                                                                                         |
| Microsoft. welcomecenter                                     | Willkommens Center                    | {CB1B7F8C-C50A-4176-B604-9e24dee8d4d1} | Wird Microsoft. GettingStarted in Windows 7 zugeordnet. Starten der System Steuerungs-Startseite ab Windows 8.                                                                                                                                                                                                                                                      |
| Microsoft. windowssidebug Properties                          | Windows-Sidebar-Eigenschaften        | {37efd44d-ef8d-41b1-940d-96973a50e9e0} | Wird Microsoft. Desktopgadgets in Windows 7 zugeordnet. Entfernt ab Windows 8.                                                                                                                                                                                                                                                                                   |
| Microsoft. windowsside Show                                   | Windows SideShow                  | {E95A4861-D57A-4be1-AD0F-35267E261739} | Das in Windows 8 veraltete Feature, das ab Windows 8.1 entfernt wurde.                                                                                                                                                                                                                                                                                               |



 

## <a name="using-canonical-names-in-local-group-policy"></a>Verwenden von kanonischen Namen in lokalen Gruppenrichtlinie

Ab Windows 7 können Sie kanonische Namen verwenden, um den Zugriff auf einzelne System Steuerungselemente mithilfe von Gruppenrichtlinien einzuschränken. Diese Prozedur kann in Windows Vista verwendet werden, aber Sie müssen den Modulnamen anstelle des kanonischen Namens verwenden.

### <a name="hiding-individual-control-panel-items"></a>Ausblenden einzelner System Steuerungselemente

Verwenden Sie diese Methode, wenn Sie mehr System Steuerungselemente anzeigen möchten, als Sie ausblenden möchten.

1.  Führen Sie die Datei "gpeer dit. msc" aus, um die Editor für lokale Gruppenrichtlinien zu starten. Sie können auch "Gruppenrichtlinie" auf dem Windows 8.1 Start Bildschirm eingeben und dann in den Suchergebnissen die Option **Gruppenrichtlinie bearbeiten** auswählen.
2.  Wählen Sie die Option **Benutzerkonfiguration**  >  **Administrative Vorlagen**  >  **Systemsteuerung** aus.
3.  Wählen Sie **angegebene System Steuerungselemente ausblenden** aus.
4.  Klicken Sie im Fenster **angegebene System Steuerungselemente ausblenden** auf **aktiviert**.
5.  Klicken Sie im Options Panel auf die Schaltfläche **anzeigen** , um die Liste der unzulässigen System Steuerungselemente anzuzeigen.
6.  Geben Sie im geöffneten Fenster **Inhalt anzeigen** einen kanonischen Namen in die Spalte **Wert** ein. Wiederholen Sie dies bei Bedarf.
7.  Klicken Sie auf **OK**.

### <a name="showing-individual-control-panel-items"></a>Einzelne System Steuerungselemente werden angezeigt.

Verwenden Sie diese Methode, wenn Sie mehr System Steuerungselemente ausblenden möchten, als Sie anzeigen möchten.

1.  Führen Sie die Datei "gpeer dit. msc" aus, um die Editor für lokale Gruppenrichtlinien zu starten. Sie können auch "Gruppenrichtlinie" auf dem Windows 8.1 Start Bildschirm eingeben und dann in den Suchergebnissen die Option **Gruppenrichtlinie bearbeiten** auswählen.
2.  Wählen Sie die Option **Benutzerkonfiguration**  >  **Administrative Vorlagen**  >  **Systemsteuerung** aus.
3.  Wählen Sie **nur angegebene System Steuerungselemente anzeigen** aus.
4.  Klicken Sie im Fenster **nur angegebene System Steuerungselemente anzeigen** , das geöffnet wird, auf **aktiviert**. Dadurch wird alles in der Systemsteuerung ausgeblendet.
5.  Klicken Sie im Options Panel auf die Schaltfläche **anzeigen** , um die Liste der zulässigen System Steuerungselemente anzuzeigen.
6.  Geben Sie im geöffneten Fenster **Inhalt anzeigen** einen kanonischen Namen in die Spalte **Wert** ein. Wiederholen Sie dies bei Bedarf.
7.  Klicken Sie auf **OK**.

Wenn Sie alle Einträge entfernen möchten, die Sie der Liste System Steuerungselemente anzeigen oder ausblenden hinzugefügt haben, kehren Sie zum Bildschirm in Schritt 4 zurück, und wählen Sie **nicht konfiguriert** aus, um die Liste zu löschen. Wenn Sie Ihre Einträge beibehalten, aber die Einschränkungen unterbrechen möchten, wählen Sie **deaktiviert** aus.

## <a name="remarks"></a>Bemerkungen

In der Systemsteuerung werden möglicherweise Elemente angezeigt, die hier nicht aufgeführt sind. Diese Elemente sind nicht Teil von Windows, sondern werden stattdessen bei der Installation verschiedener Software und Hardware, wie Microsoft Office oder einer Grafikkarte, hinzugefügt. Nicht-Windows-System Steuerungselemente haben möglicherweise einen kanonischen Namen. Wenn Sie den kanonischen Namen eines System Steuerungs Elements suchen möchten, das hier nicht aufgelistet ist, suchen Sie in der Registrierung unter den folgenden Pfaden:

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID of the Control Panel item}
         System.ApplicationName
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         CLSID
            {CLSID of the Control Panel item}
               System.ApplicationName
```

Weitere Informationen, die Ihnen helfen können, die erforderlichen CLSIDs zu ermitteln, finden Sie unter [Registrieren von ausführbaren System Steuerungselementen](how-to-register-an-executable-control-panel-item-registration-.md) und [Registrieren von dll-System Steuerungselementen](how-to-register-dll-control-panel-item-registration-.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ausführen von System Steuerungselementen](executing-control-panel-items.md)
</dt> <dt>

[**Iopencontrolpanel**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopencontrolpanel)
</dt> </dl>

 

 



