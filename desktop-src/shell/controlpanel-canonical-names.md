---
description: Ab Windows Vista erhalten Systemsteuerung elemente, die in Windows enthalten sind, einen kanonischen Namen, der in einem API-Aufruf oder einer Befehlszeilenanweisung verwendet werden kann, um dieses Element programmgesteuert zu starten.
ms.assetid: A02DFC9F-646D-40d8-901C-7239A820DE2C
title: Kanonische Namen von Systemsteuerung Elementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebf831bfb1cb86c41a8f97c2bfa041dad836e4b77f8fd233cb94d4a3951c38d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943470"
---
# <a name="canonical-names-of-control-panel-items"></a>Kanonische Namen von Systemsteuerung Elementen

Ab Windows Vista erhalten Systemsteuerung elemente, die in Windows enthalten sind, einen kanonischen Namen, der in einem [API-Aufruf oder einer Befehlszeilenanweisung](executing-control-panel-items.md) verwendet werden kann, um dieses Element programmgesteuert zu starten. Ab Windows 7 und Windows Server 2008 R2 können kanonische Namen in einer Gruppenrichtlinie verwendet werden, um bestimmte Systemsteuerung Elemente auszublenden. Dieses Thema enthält Details zu jedem Systemsteuerung Element: kanonischer Name, GUID, Modulname und die Betriebssystemversionen, die den kanonischen Namen erkennen.

> [!Note]  
> Kanonische Namen für Systemsteuerung Elemente werden vor Windows Vista nicht unterstützt.

 

-   [Systemsteuerung kanonische Namen](#control-panel-canonical-names)
-   [Veraltete Systemsteuerung kanonische Namen](#deprecated-control-panel-canonical-names)
-   [Verwenden kanonischer Namen in Gruppenrichtlinie](#using-canonical-names-in-local-group-policy)
-   [Anmerkungen](#remarks)

## <a name="control-panel-canonical-names"></a>Systemsteuerung Kanonische Namen

Punkte, die Sie beim Arbeiten mit diesen Werten beachten sollten:

-   Definitionsgemäß ändern sich kanonische Namen nicht basierend auf der Systemsprache. sie sind immer auf Englisch, auch wenn die Sprache des Systems nicht ist.
-   Nicht alle Systemsteuerung Elemente sind in allen Varianten von Windows vorhanden.
-   Einige Systemsteuerung Elemente werden nur angezeigt, wenn die richtige Hardware auf dem System erkannt wird.
-   Drittanbieter können auch Systemsteuerung Elemente hinzufügen. Die hier aufgeführten kanonischen Namen gelten nur für Systemsteuerung Elemente, die in Windows enthalten sind.

Im Folgenden finden Sie die Systemsteuerung Elemente, die in Windows 8.1 verfügbar sind:

-   [Info-Center](#action-center)
-   [Verwaltungstools](#administrative-tools)
-   [Autoplay](#autoplay)
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
-   [Indizierungsoptionen](#indexing-options)
-   [Infrarot](#infrared)
-   [Internetoptionen](#internet-options)
-   [iSCSI-Initiator](#iscsi-initiator)
-   [iSNS-Server](#isns-server)
-   [Tastatur](#keyboard)
-   [Standort Einstellungen](#location-settings)
-   [Maus](#mouse)
-   [MPIOConfiguration](#mpioconfiguration)
-   [Netzwerk- und Freigabecenter](#network-and-sharing-center)
-   [Symbole für den Benachrichtigungsbereich](#notification-area-icons)
-   [Stift und Toucheingabe](#pen-and-touch)
-   [Personalisierung](#personalization)
-   [Telefon und Modem](#phone-and-modem)
-   [Energieoptionen](#power-options)
-   [Programme und Features](#programs-and-features)
-   [Wiederherstellung](#recovery)
-   [Region](#region)
-   [RemoteApp- und Desktopverbindungen](#remoteapp-and-desktop-connections)
-   [Sound](#sound)
-   [Spracherkennung](#speech-recognition)
-   [Speicherplätze](#storage-spaces)
-   [Synchronisierungscenter](#sync-center)
-   [System](#system)
-   [Tablet PC Einstellungen](#tablet-pc-settings)
-   [Taskleiste und Navigation](#taskbar-and-navigation)
-   [Problembehandlung](#troubleshooting)
-   [TSAppInstall](#tsappinstall)
-   [User Accounts (Benutzerkonten)](#user-accounts)
-   [Windows Anytime Upgrade](#windows-anytime-upgrade)
-   [Windows Defender](#windows-defender)
-   [Windows-Firewall](#windows-firewall)
-   [Windows-Mobilitätscenter](#windows-mobility-center)
-   [Windows To Go](#windows-to-go)
-   [Windows Update](#windows-update)
-   [Arbeitsordner](#work-folders)

### <a name="action-center"></a>Info-Center

-   **Kanonischer Name:** Microsoft.ActionCenter
-   **GUID:**{BB64F8A7-BEE7-4E1A-AB8D-7D8273F7FDB6}
-   **Unterstütztes Betriebssystem:** Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\ActionCenterCPL.dll,-1
-   **Seiten**

    | Seitenname           | Opens                      |
    |---------------------|----------------------------|
    | MaintenanceSettings | Automatische Wartung      |
    | pageProblems        | Problemberichte            |
    | pageReliabilityView | Zuverlässigkeitsmonitor        |
    | pageResponseArchive | Archivierte Nachrichten          |
    | Pagesettings        | Problemberichterstattung Einstellungen |

    

     

### <a name="administrative-tools"></a>Verwaltung

-   **Kanonischer Name:** Microsoft.AdministrativeTools
-   **GUID:**{D20EA4E1-3957-11d2-A40B-0C5020524153}
-   **Unterstützte Betriebssysteme:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ system32 \\shell32.dll,-22982

### <a name="autoplay"></a>Automatische Wiedergabe

-   **Kanonischer Name:** Microsoft.AutoPlay
-   **GUID**: {9C60DE1E-E5FC-40f4-A487-460851A8D915}
-   **Unterstützte Betriebssysteme:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\autoplay.dll,-1

### <a name="biometric-devices"></a>Biometrische Geräte

-   **Kanonischer Name:** Microsoft.BiometricDevices
-   **GUID:**{0142e4d0-fb7a-11dc-ba4a-000ffe7ab428}
-   **Unterstütztes Betriebssystem:** Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\biocpl.dll,-1

### <a name="bitlocker-drive-encryption"></a>BitLocker-Laufwerkverschlüsselung

-   **Kanonischer Name:** Microsoft.BitLockerDriveEncryption
-   **GUID**: {D9EF8727-CAC2-4e60-809E-86F80A666C91}
-   **Unterstütztes Betriebssystem:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\fvecpl.dll,-1

### <a name="color-management"></a>Farbverwaltung

-   **Kanonischer Name:** Microsoft.ColorManagement
-   **GUID:**{B2C761C6-29BC-4f19-9251-E6195265BAF1}
-   **Unterstütztes Betriebssystem:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%systemroot% \\ system32 \\colorcpl.exe,-6

### <a name="credential-manager"></a>Anmeldeinformationsverwaltung

-   **Kanonischer Name:** Microsoft.CredentialManager
-   **GUID**: {1206F5F1-0569-412C-8FEC-3204630DFB70}
-   **Unterstütztes Betriebssystem:** Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ system32 \\Vault.dll,-1
-   **Seiten**

    | Seitenname                   | Opens               |
    |-----------------------------|---------------------|
    | ? SelectedVault=CredmanVault | Windows Anmeldeinformationen |

    

     

### <a name="date-and-time"></a>Datum und Uhrzeit

-   **Kanonischer Name:** Microsoft.DateAndTime
-   **GUID:**{E2E7934B-DCE5-43C4-9576-7FE4F75E7480}
-   **Unterstütztes Betriebssystem:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\timedate.cpl,-51
-   **Seiten**

    | Seitenname | Opens             |
    |-----------|-------------------|
    | 1         | Zusätzliche Uhren |

    

     

### <a name="default-programs"></a>Standardprogramme

-   **Kanonischer Name:** Microsoft.DefaultPrograms
-   **GUID**: {17cd9488-1228-4b2f-88ce-4298e93e0966}
-   **Unterstütztes Betriebssystem:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\sud.dll,-1
-   **Seiten**

    | Seitenname          | Opens                |
    |--------------------|----------------------|
    | pageDefaultProgram | Festlegen von Standardprogrammen |
    | pageFileAssoc      | Festlegen von Zuordnungen     |

    

     

### <a name="device-manager"></a>Geräte-Manager

-   **Kanonischer Name:** Microsoft.DeviceManager
-   **GUID:**{74246bfc-4c96-11d0-abef-0020af6b0b7a}
-   **Unterstütztes Betriebssystem:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\devmgr.dll,-4

### <a name="devices-and-printers"></a>Geräte und Drucker

-   **Kanonischer Name:** Microsoft.DevicesAndPrinters
-   **GUID:**{A8A91A66-3A7D-4424-8D24-04E180695C7A}
-   **Unterstütztes Betriebssystem:** Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%systemroot% \\ system32 \\DeviceCenter.dll,-1000

### <a name="display"></a>Anzeige

-   **Kanonischer Name:** Microsoft.Display
-   **GUID:**{C555438B-3C23-4769-A71F-B6D3D9B6053A}
-   **Unterstütztes Betriebssystem:** Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\Display.dll,-1
-   **Seiten**

    | Seitenname | Opens             |
    |-----------|-------------------|
    | Einstellung  | Bildschirmauflösung |

    

     

### <a name="ease-of-access-center"></a>Center für erleichterte Bedienung

-   **Kanonischer Name:** Microsoft.EaseOfAccessCenter
-   **GUID:**{D555645E-D4F8-4c29-A827-D93C859C4F2A}
-   **Unterstütztes Betriebssystem:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\accessibilitycpl.dll,-10
-   **Seiten**

    | Seitenname               | Opens                                                               |
    |-------------------------|---------------------------------------------------------------------|
    | pageEassierToClick       | Einfachere Verwendung der Maus                                        |
    | pageEasiaerToSee         | Einfacheres Anzeigen des Computers                                     |
    | pageEassierWithSounds    | Verwenden von Text- oder visuellen Alternativen für Sounds                          |
    | pageFilterKeysSettings  | Einrichten von Filterschlüsseln                                                  |
    | pageKeyboardEassierToUse | Vereinfachen der Verwendung der Tastatur                                     |
    | pageNoMouseOrKeyboard   | Verwenden des Computers ohne Maus oder Tastatur                        |
    | pageNoVisual            | Verwenden des Computers ohne Anzeige                                  |
    | pageQuestionsCognitive  | Erhalten von Empfehlungen zur einfacheren Verwendung Ihres Computers (cognitive) |
    | pageQuestionsEyesight   | Erhalten von Empfehlungen zur einfacheren Verwendung Ihres Computers (Sehkraft)  |

    

     

### <a name="family-safety"></a>Family Safety

-   **Kanonischer Name:** Microsoft.ParentalControls
-   **GUID:**{96AE8D84-A250-4520-95A5-A47A7E3C548B}
-   **Unterstütztes Betriebssystem:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\wpccpl.dll,-100
-   **Seiten**

    | Seitenname   | Opens                                  |
    |-------------|----------------------------------------|
    | pageUserHub | Wählen Sie einen Benutzer aus, und richten Sie Family Safety |

    

     

### <a name="file-history"></a>Dateiversionsverlauf

-   **Kanonischer Name:** Microsoft.FileHistory
-   **GUID:**{F6B6E965-E9B2-444B-9286-10C9152EDBC5}
-   **Unterstütztes Betriebssystem:** Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\fhcpl.dll,-52
-   Dateiversionsverlauf enthält eine neuere Version des Sicherungs- und Wiederherstellungselements, aber der kanonische Name dieses älteren Elements wird nicht Dateiversionsverlauf neu zuordnen.

### <a name="folder-options"></a>Ordneroptionen

-   **Kanonischer Name:** Microsoft.FolderOptions
-   **GUID:**{6DFD7C5C-2451-11d3-A299-00C04F8EF6AF}
-   **Unterstütztes Betriebssystem:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ system32 \\shell32.dll,-22985

### <a name="fonts"></a>Schriftarten

-   **Kanonischer Name:** Microsoft.Fonts
-   **GUID:**{93412589-74D4-4E4E-AD0E-E0CB621440FD}
-   **Unterstütztes Betriebssystem:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\FontExt.dll,-8007

### <a name="homegroup"></a>Heimnetzgruppe

-   **Kanonischer Name:** Microsoft.HomeGroup
-   **GUID:**{67CA7650-96E6-4FDD-BB43-A8E774F73A57}
-   **Unterstütztes Betriebssystem:** Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\hgcpl.dll,-1

### <a name="indexing-options"></a>Indizierungsoptionen

-   **Kanonischer Name:** Microsoft.IndexingOptions
-   **GUID**: {87D66A43-7B11-4A28-9811-C86EE395ACF7}
-   **Unterstütztes Betriebssystem:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\srchadmin.dll,-601

### <a name="infrared"></a>Infrarot

-   **Kanonischer Name:** Microsoft.Canon
-   **GUID**: {A0275511-0E86-4ECA-97C2-ECD8F1221D08}
-   **Unterstütztes Betriebssystem:** Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\irprops.cpl,-1

### <a name="internet-options"></a>Internetoptionen

-   **Kanonischer Name:** Microsoft.InternetOptions
-   **GUID:**{A3DD4F92-658A-410F-84FD-6FBBBEF2FFFE}
-   **Unterstütztes Betriebssystem:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:** @C: \\ Windows \\ System32 \\inetcpl.cpl,-4312
-   **Seiten**

    | Seitenname | Opens       |
    |-----------|-------------|
    | 1         | Sicherheit    |
    | 2         | Datenschutz     |
    | 3         | Content     |
    | 4         | Verbindungen |
    | 5         | Programme    |
    | 6         | Fortgeschrittene    |

    

     

### <a name="iscsi-initiator"></a>iSCSI-Initiator

-   **Kanonischer Name:** Microsoft.iSCSIInitiator
-   **GUID:**{A304259D-52B8-4526-8B1A-A1D6CECC8243}
-   **Unterstütztes Betriebssystem:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\iscsicpl.dll,-5001

### <a name="isns-server"></a>iSNS-Server

-   **Kanonischer Name:** Microsoft.iSNSServer
-   **GUID:**{0D2A3442-5181-4E3A-9BD4-83BD10AF3D76}
-   **Unterstütztes Betriebssystem:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\isnssrv.dll,-5005
-   Dieses Systemsteuerung Element wird nur in Serverversionen von Windows angezeigt.

### <a name="keyboard"></a>Tastatur

-   **Kanonischer Name:** Microsoft.Keyboard
-   **GUID:**{725BE8F7-668E-4C7B-8F90-46BDB0936430}
-   **Unterstütztes Betriebssystem:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\main.cpl,-102

### <a name="location-settings"></a>Standort Einstellungen

-   **Kanonischer Name:** Microsoft.LocationSettings
-   **GUID:**{E9950154-C418-419e-A90A-20C5287AE24B}
-   **Unterstütztes Betriebssystem:** Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\SensorsCpl.dll,-1

### <a name="mouse"></a>Maus

-   **Kanonischer Name:** Microsoft.Mouse
-   **GUID:**{6C8EEC18-8D75-41B2-A177-8831D59D2D50}
-   **Unterstütztes Betriebssystem:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\main.cpl,-100
-   **Seiten**

    | Seitenname | Opens           |
    |-----------|-----------------|
    | 1         | Zeiger        |
    | 2         | Zeigeroptionen |
    | 3         | Wheel           |
    | 4         | Hardware        |

    

     

### <a name="mpioconfiguration"></a>MPIOConfiguration

-   **Kanonischer Name:** Microsoft.MPIOConfiguration
-   **GUID:**{AB3BE6AA-7561-4838-AB77-ACF8427DF426}
-   **Unterstütztes Betriebssystem:** Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\mpiocpl.dll,-1000
-   Dieses Systemsteuerung Element wird nur in Serverversionen von Windows angezeigt.

### <a name="network-and-sharing-center"></a>Netzwerk- und Freigabecenter

-   **Kanonischer Name:** Microsoft.NetworkAndSharingCenter
-   **GUID:**{8E908FC9-BECC-40f6-915B-F4CA0E70D03D}
-   **Unterstützte Betriebssysteme:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\netcenter.dll,-1
-   **Seiten**

    | Seitenname  | Opens                     |
    |------------|---------------------------|
    | Fortgeschrittene   | Erweiterte Freigabeeinstellungen |
    | ShareMedia | Medienstreamingoptionen   |

    

     

### <a name="notification-area-icons"></a>Symbole für den Benachrichtigungsbereich

-   **Kanonischer Name:** Microsoft.NotificationAreaIcons
-   **GUID:**{05d7b0f4-2121-4eff-bf6b-ed3f69b894d9}
-   **Unterstütztes Betriebssystem:** Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\taskbarcpl.dll,-1

### <a name="pen-and-touch"></a>Stift und Toucheingabe

-   **Kanonischer Name:** Microsoft.PenAndTouch
-   **GUID:**{F82DF8F7-8B9F-442E-A48C-818EA735FF9B}
-   **Unterstütztes Betriebssystem:** Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\tabletpc.cpl,-10103
-   **Seiten**

    | Seitenname | Opens       |
    |-----------|-------------|
    | 1         | Flicks      |
    | 2         | Handwriting |

    

     

### <a name="personalization"></a>Personalization

-   **Kanonischer Name:** Microsoft.Personalization
-   **GUID**: {ED834ED6-4B5A-4bfe-8F11-A626DCB6A921}
-   **Unterstützte Betriebssysteme:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\themecpl.dll,-1
-   **Seiten**

    | Seitenname        | Opens                |
    |------------------|----------------------|
    | pageColorization | Farbe und Darstellung |
    | pageWallpaper    | Desktophintergrund   |

    

     

### <a name="phone-and-modem"></a>Telefon und Modem

-   **Kanonischer Name:** Microsoft.PhoneAndModem
-   **GUID**: {40419485-C444-4567-851A-2DD7BFA1684D}
-   **Unterstütztes Betriebssystem:** Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\telephon.cpl,-1
-   Das Fenster, in dem dieser Wert gestartet wird, trägt den Titel "Standortinformationen" in Versionen von Windows vor Windows 8. Die Benutzeroberfläche des Elements wird ab Windows 8 erheblich geändert.

### <a name="power-options"></a>Energieoptionen

-   **Kanonischer Name:** Microsoft.PowerOptions
-   **GUID:**{025A5937-A6BE-4686-A844-36FE4BEC8B6D}
-   **Unterstützte Betriebssysteme:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\powercpl.dll,-1
-   **Seiten**

    | Seitenname          | Opens              |
    |--------------------|--------------------|
    | pageGlobalSettings | Systemeinstellungen    |
    | pagePlanSettings   | Einstellungen "Plan bearbeiten" |

    

     

### <a name="programs-and-features"></a>Programme und Features

-   **Kanonischer Name:** Microsoft.ProgramsAndFeatures
-   **GUID:**{7b81be6a-ce2b-4676-a29e-eb907a5126c5}
-   **Unterstützte Betriebssysteme:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%systemroot% \\ system32 \\appwiz.cpl,-159
-   **Seiten**

    | Seitenname                                | Opens             |
    |------------------------------------------|-------------------|
    | ::{D450A8A1-9568-45C7-9C0E-B4F9FB4537BD} | Installierte Updates |

    

     

### <a name="recovery"></a>Wiederherstellung

-   **Kanonischer Name:** Microsoft.Recovery
-   **GUID**: {9FE63AFD-59CF-4419-9775-ABCC3849F861}
-   **Unterstütztes Betriebssystem:** Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\recovery.dll,-101

### <a name="region"></a>Region

-   **Kanonischer Name:** Microsoft.RegionAndLanguage
-   **GUID:**{62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}
-   **Unterstütztes Betriebssystem:** Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\intl.cpl,-1
-   Das In Windows 7 gefundene Element Region und Sprache wurde ab Windows 8 aufgeteilt. Microsoft.RegionAndLanguage startet jetzt das Element Region. Verwenden Sie [Microsoft.Language,](#location-settings)um das Sprachelement zu starten.
-   **Seiten**

    | Seitenname | Opens          |
    |-----------|----------------|
    | 1         | Standort       |
    | 2         | Administrative |

    

     

### <a name="remoteapp-and-desktop-connections"></a>RemoteApp- und Desktopverbindungen

-   **Kanonischer Name:** Microsoft.RemoteAppAndDesktopConnections
-   **GUID:**{241D7C96-F8BF-4F85-B01F-E2B043341A4B}
-   **Unterstütztes Betriebssystem:** Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\tsworkspace.dll,-15300

### <a name="sound"></a>Sound

-   **Kanonischer Name:** Microsoft.Sound
-   **GUID:**{F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}
-   **Unterstütztes Betriebssystem:** Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\mmsys.cpl,-300

### <a name="speech-recognition"></a>Spracherkennung

-   **Kanonischer Name:** Microsoft.SpeechRecognition
-   **GUID:**{58E3C745-D971-4081-9034-86E34B30836A}
-   **Unterstütztes Betriebssystem:** Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\ \\ SpeechUX \\speechuxcpl.dll,-1

### <a name="storage-spaces"></a>Speicherplätze

-   **Kanonischer Name:** Microsoft.StorageSpaces
-   **GUID:**{F942C606-0914-47AB-BE56-1321B8035096}
-   **Unterstütztes Betriebssystem:** Windows 8, Windows 8.1
-   **Modulname:** @C: \\ Windows \\ System32 \\SpaceControl.dll,-1

### <a name="sync-center"></a>Synchronisierungscenter

-   **Kanonischer Name:** Microsoft.SyncCenter
-   **GUID:**{9C73F5E5-7AE7-4E32-A8E8-8D23B85255BF}
-   **Unterstütztes Betriebssystem:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\SyncCenter.dll,-3000

### <a name="system"></a>System

-   **Kanonischer Name:** Microsoft.System
-   **GUID:**{BB06C0E4-D293-4f75-8A90-CB05B6477EEE}
-   **Unterstütztes Betriebssystem:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\systemcpl.dll,-1

### <a name="tablet-pc-settings"></a>Tablet PC-Einstellungen

-   **Kanonischer Name:** Microsoft.TabletPCSettings
-   **GUID:**{80F3F1D5-FECA-45F3-BC32-752C152E456E}
-   **Unterstütztes Betriebssystem:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\tabletpc.cpl,-10100

### <a name="taskbar-and-navigation"></a>Taskleiste und Navigation

-   **Kanonischer Name:** Microsoft.Taskbar
-   **GUID:**{0DF44EAA-FF21-4412-828E-260A8728E7F1}
-   **Unterstütztes Betriebssystem:** Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ system32 \\shell32.dll,-32517

### <a name="troubleshooting"></a>Problembehandlung

-   **Kanonischer Name:** Microsoft.Troubleshooting
-   **GUID:**{C58C4893-3BE0-4B45-ABB5-A63E4B8C8651}
-   **Unterstütztes Betriebssystem:** Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\DiagCpl.dll,-1
-   **Seiten**

    | Seitenname   | Opens   |
    |-------------|---------|
    | HistoryPage | Verlauf |

    

     

### <a name="tsappinstall"></a>TSAppInstall

-   **Kanonischer Name:** Microsoft.TSAppInstall
-   **GUID:**{BAA884F4-3432-48b8-AA72-9BF20EEF31D5}
-   **Unterstütztes Betriebssystem:** Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%systemroot% \\ system32 \\tsappinstall.exe,-2001

### <a name="user-accounts"></a>Benutzerkonten

-   **Kanonischer Name:** Microsoft.UserAccounts
-   **GUID:**{60632754-c523-4b62-b45c-4172da012619}
-   **Unterstütztes Betriebssystem:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\usercpl.dll,-1

### <a name="windows-anytime-upgrade"></a>Windows Anytime Upgrade

-   **Kanonischer Name:** Microsoft.WindowsAnytimeUpgrade
-   **GUID:**{BE122A0E-4503-11DA-8BDE-F66BAD1E3F3A}
-   **Unterstütztes Betriebssystem:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@$(resourceString. \_ SYS \_ MOD \_ PATH),-1

### <a name="windows-defender"></a>Windows Defender

-   **Kanonischer Name:** Microsoft.WindowsDefender
-   **GUID:**{D8559EB9-20C0-410E-BEDA-7ED416AECC2A}
-   **Unterstütztes Betriebssystem:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%ProgramFiles% \\ Windows Defender \\MsMpRes.dll,-104

### <a name="windows-firewall"></a>Windows-Firewall

-   **Kanonischer Name:** Microsoft.WindowsFirewall
-   **GUID:**{4026492F-2F69-46B8-B9BF-5654FC07E423}
-   **Unterstütztes Betriebssystem:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:** @C: \\ Windows \\ system32 \\FirewallControlPanel.dll,-12122
-   **Seiten**

    | Seitenname         | Opens        |
    |-------------------|--------------|
    | pageConfigureApps | Zulässige Apps |

    

     

### <a name="windows-mobility-center"></a>Windows-Mobilitätscenter

-   **Kanonischer Name:** Microsoft.MobilityCenter
-   **GUID:**{5ea4f148-308c-46d7-98a9-49041b1dd468}
-   **Unterstütztes Betriebssystem:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ system32 \\mblctr.exe,-1002

### <a name="windows-to-go"></a>Windows To Go

-   **Kanonischer Name:** Microsoft.PortableWorkspaceCreator
-   **GUID:**{8E0C279D-0BD1-43C3-9EBD-31C3DC5B8A77}
-   **Unterstütztes Betriebssystem:** Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ System32 \\pwcreator.exe,-151

### <a name="windows-update"></a>Windows-Update

-   **Kanonischer Name:** Microsoft.WindowsUpdate
-   **GUID:**{36eef7db-88ad-4e81-ad49-0e313f0c35f8}
-   **Unterstütztes Betriebssystem:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Modulname:**@%SystemRoot% \\ system32 \\wucltux.dll,-1
-   **Seiten**

    | Seitenname         | Opens               |
    |-------------------|---------------------|
    | Pagesettings      | Änderung der Einstellungen     |
    | pageUpdateHistory | Anzeigen des Updateverlaufs |

    

     

### <a name="work-folders"></a>Arbeitsordner

-   **Kanonischer Name:** Microsoft.WorkFolders
-   **GUID:**{ECDB0924-4208-451E-8EE0-373C0956DE16}
-   **Unterstütztes Betriebssystem:** Windows 8.1
-   **Modulname:** @C: \\ Windows \\ System32 \\WorkfoldersControl.dll,-1

## <a name="deprecated-control-panel-canonical-names"></a>Veraltete Systemsteuerung kanonische Namen

Im Folgenden finden Sie kanonische Namen, die ab Windows 8.1 nicht mehr verwendet werden. Einige wurden vollständig entfernt. Andere wurden in folgenden Situationen neu zugeordnet:

-   Ein Systemsteuerung wird umbenannt. Das umbenannte Element erhält einen neuen kanonischen Namen, behält aber die gleiche GUID bei. In diesem Fall startet der alte kanonische Name den umbenannten Systemsteuerung Element. Beachten Sie, dass das gestartete Element möglicherweise nicht die gleiche Benutzeroberfläche wie die ältere Version dieses Elements verwendet.
-   Die Funktionalität eines oder mehrerer Systemsteuerung Elemente wird in ein neues Element verschoben oder konsolidiert. In diesem Fall wird der alte kanonische Name dem am besten geeigneten neuen Systemsteuerung Element zugeordnet.

> [!Note]  
> Neuzuordnungen sind aus Gründen der Abwärtskompatibilität vorhanden. Sie sollten keine veralteten Werte in neuem Code verwenden.

 



| Veralteter kanonischer Name                                   | Systemsteuerung Item                | GUID                                   | Hinweise                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------|-----------------------------------|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Microsoft.AddHardware                                       | Hardware hinzufügen                      | {7A979262-40CE-46ff-AEEE-7884AC3B6136} | Karten zu [Microsoft.DevicesAndPrinters](#devices-and-printers) ab Windows 7.                                                                                                                                                                                                                                                                            |
| Microsoft.AudioDevicesAndSoundThemes                        | Sound                             | {F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D} | Karten ab Windows 7 zu [Microsoft.Sound.](#sound)                                                                                                                                                                                                                                                                                                        |
| Microsoft.BackupAndRestoreCenter/Microsoft.BackupAndRestore | Sicherungs- und Wiederherstellungscenter         | {B98A2BEA-7D42-4558-8BD1-832F41BAC6FD} | Microsoft.BackupAndRestoreCenter ist microsoft.BackupAndRestore in Windows 7 zugeordnet. Beide werden ab Windows 8 entfernt. Verwenden Sie stattdessen [Microsoft.FileHistory.](#file-history)                                                                                                                                                                                   |
| Microsoft.CardSpace                                         | Windows CardSpace                 | {78CB147A-98EA-4AA6-B0DF-C8681F69341C} | Entfernt ab Windows 8.                                                                                                                                                                                                                                                                                                                                  |
| Microsoft.DesktopGadgets                                    | Desktop-Gadgets                   | {37efd44d-ef8d-41b1-940d-96973a50e9e0} | Entfernt ab Windows 8.                                                                                                                                                                                                                                                                                                                                  |
| Microsoft.GetProgramsOnline                                 | Windows Marketplace               | {3e7efb4c-faf1-453d-89eb-56026875ef90} | Ab Windows 7 entfernt.                                                                                                                                                                                                                                                                                                                                  |
| Microsoft.Options                                   | Infrarot                          | {A0275511-0E86-4ECA-97C2-ECD8F1221D08} | Karten ab Windows 7 an [Microsoft.Zu.](#infrared)                                                                                                                                                                                                                                                                                                  |
| Microsoft.Language                                          | Sprache                          | {BF782CC9-5A52-4A17-806C-2A894FFEEAC5} | Ab Windows 10 Version 1803 entfernt                                                                                                                                                                                                                                                                                                                    |
| Microsoft.LocationAndOtherSensors                           | Positions- und andere Sensoren        | {E9950154-C418-419e-A90A-20C5287AE24B} | Karten ab Windows 8 zu [Microsoft.LocationSettings.](#infrared)                                                                                                                                                                                                                                                                                          |
| Microsoft.PenAndInputDevices                                | Stift und Eingabegeräte             | {F82DF8F7-8B9F-442E-A48C-818EA735FF9B} | Karten ab Windows 7 an [Microsoft.PenAndTouch.](#pen-and-touch)                                                                                                                                                                                                                                                                                          |
| Microsoft.PeopleNearMe                                      | Personen in meiner Umgebung                    | {5224F545-A443-4859-BA23-7B5A95BDC8EF} | Entfernt ab Windows 8.                                                                                                                                                                                                                                                                                                                                  |
| Microsoft.PerformanceInformationAndTools                    | Leistungsinformationen und Tools | {78F3955E-3B90-4184-BD14-5397C15F1EFC} | Ab Windows 8.1 entfernt.                                                                                                                                                                                                                                                                                                                                |
| Microsoft.PhoneAndModemOptions                              | Telefon und Modem                   | {40419485-C444-4567-851A-2DD7BFA1684D} | Karten zu [Microsoft.PhoneAndModem](#phone-and-modem) ab Windows 7.                                                                                                                                                                                                                                                                                      |
| Microsoft.Printer                                          | Drucker                          | {2227A280-3AEA-1069-A2DE-08002B30309D} | Karten zu [Microsoft.DevicesAndPrinters](#devices-and-printers) ab Windows 7.                                                                                                                                                                                                                                                                            |
| Microsoft.ProblemReportsAndSolutions                        | Problemberichte und -lösungen     | {FCFEECAE-EE1B-4849-AE50-685DCF7717EC} | Karten ab Windows 7 an [Microsoft.ActionCenter.](#action-center)                                                                                                                                                                                                                                                                                         |
| Microsoft.RegionalAndLanguageOptions                        | Regions- und Sprachoptionen     | {62D8ED13-C9D0-4CE8-A914-47DD628FB1B0} | Karten ab Windows 7 an [Microsoft.RegionAndLanguage.](#region) Beachten Sie, dass ab Windows 8 Region und Sprache jeweils ein eigenes Systemsteuerung Element erhalten haben. Microsoft.RegionalAndLanguageOptions und Microsoft.RegionAndLanguage öffnen derzeit das Element Region. Sie müssen [Microsoft.Language](#location-settings) verwenden, um auf das Sprachelement zuzugreifen. |
| Microsoft.SecurityCenter                                    | Windows-Sicherheit Center           | {087DA31B-0DD3-4537-8E23-64A18591F88B} | Karten ab Windows 7 an [Microsoft.ActionCenter.](#action-center)                                                                                                                                                                                                                                                                                         |
| Microsoft.SpeechRecognitionOptions                          | Spracherkennungsoptionen        | {58E3C745-D971-4081-9034-86E34B30836A} | Karten ab Windows 7 zu [Microsoft.SpeechRecognition.](#speech-recognition)                                                                                                                                                                                                                                                                               |
| Microsoft.TaskbarAndStartMenu                               | Taskleiste und Startmenü            | {0DF44EAA-FF21-4412-828E-260A8728E7F1} | Karten ab Windows 8 zu [Microsoft.Taskbar.](#speech-recognition)                                                                                                                                                                                                                                                                                         |
| Microsoft.WelcomeCenter                                     | Begrüßungscenter                    | {CB1B7F8C-C50A-4176-B604-9E24DEE8D4D1} | Karten zu Microsoft.GettingStarted in Windows 7. Startet die Systemsteuerung Startseite ab Windows 8.                                                                                                                                                                                                                                                      |
| Microsoft.WindowsSidebarProperties                          | Windows Randleisteneigenschaften        | {37efd44d-ef8d-41b1-940d-96973a50e9e0} | Karten zu Microsoft.DesktopGadgets in Windows 7. Wurde zum Windows 8.                                                                                                                                                                                                                                                                                   |
| Microsoft.WindowsSideShow                                   | Windows SideShow                  | {E95A4861-D57A-4be1-AD0F-35267E261739} | Das Feature ist in der Windows 8 veraltet und wird ab Windows 8.1.                                                                                                                                                                                                                                                                                               |



 

## <a name="using-canonical-names-in-local-group-policy"></a>Verwenden kanonischer Namen in lokalen Gruppenrichtlinie

Ab Windows 7 können Sie kanonische Namen verwenden, um den Zugriff auf einzelne Systemsteuerung elemente über eine Gruppenrichtlinie einzuschränken. Dieses Verfahren kann auch in Windows Vista verwendet werden. Sie müssen jedoch den Modulnamen anstelle des kanonischen Namens verwenden.

### <a name="hiding-individual-control-panel-items"></a>Ausblenden einzelner Systemsteuerung Elemente

Verwenden Sie diese Methode, wenn Sie mehr Systemsteuerung anzeigen möchten, als Sie ausblenden möchten.

1.  Führen Sie die Datei Gpedit.msc aus, um den Editor für lokale Gruppenrichtlinien. Sie können auch "Gruppenrichtlinie" im Windows 8.1 Startbildschirm und in den Suchergebnissen **Gruppenrichtlinie** bearbeiten auswählen.
2.  Wählen **Sie Benutzerkonfiguration**  >  **Administrative Vorlagen**  >  **Systemsteuerung.**
3.  Wählen Sie **Angegebene Elemente Systemsteuerung ausblenden aus.**
4.  Klicken Sie im fenster **Hide Specified Systemsteuerung Items** (Angegebene Elemente ausblenden), das geöffnet wird, auf **Aktiviert.**
5.  Klicken Sie **im Bereich** Optionen auf die Schaltfläche Anzeigen, um die Liste der nicht Systemsteuerung anzeigen.
6.  Geben Sie **im geöffneten Fenster** Inhalt anzeigen einen kanonischen Namen in die Spalte **Wert** ein. Wiederholen Sie dies nach Bedarf.
7.  Klicken Sie auf **OK**.

### <a name="showing-individual-control-panel-items"></a>Anzeigen einzelner Systemsteuerung Elemente

Verwenden Sie diese Methode, wenn Sie mehr Elemente Systemsteuerung, als Sie anzeigen möchten.

1.  Führen Sie die Datei Gpedit.msc aus, um den Editor für lokale Gruppenrichtlinien. Sie können auch "Gruppenrichtlinie" im Windows 8.1 Startbildschirm und in den Suchergebnissen **Gruppenrichtlinie** bearbeiten auswählen.
2.  Wählen **Sie Benutzerkonfiguration**  >  **Administrative Vorlagen**  >  **Systemsteuerung.**
3.  Wählen **Sie Show only specified Systemsteuerung items (Nur angegebene Systemsteuerung anzeigen) aus.**
4.  Klicken Sie im fenster Show Only Specified Systemsteuerung Items (Nur angegebene Elemente **anzeigen),** das geöffnet wird, auf **Aktiviert.** Dadurch wird alles im Systemsteuerung.
5.  Klicken Sie **im Bereich** Optionen auf die Schaltfläche Anzeigen, um die Liste der zulässigen Systemsteuerung anzeigen.
6.  Geben Sie **im geöffneten Fenster** Inhalt anzeigen einen kanonischen Namen in die Spalte **Wert** ein. Wiederholen Sie dies nach Bedarf.
7.  Klicken Sie auf **OK**.

Wenn Sie alle Einträge entfernen möchten, die Sie der Liste Ein- oder Ausblenden von Systemsteuerung-Elementen hinzugefügt  haben, kehren Sie zum Bildschirm in Schritt 4 zurück, und wählen Sie Nicht konfiguriert aus, um die Liste zu löschen. Wenn Sie Ihre Einträge beibehalten, aber die Einschränkungen aussetzen möchten, wählen Sie **Deaktiviert aus.**

## <a name="remarks"></a>Hinweise

Möglicherweise werden Elemente in Ihrer Systemsteuerung angezeigt, die hier nicht aufgeführt sind. Diese Elemente sind nicht Teil Windows, sondern werden stattdessen während der Installation verschiedener Software und Hardware hinzugefügt, z. B. Microsoft Office oder einer Grafikkarte. Nicht-Windows Systemsteuerung elemente können einen kanonischen Namen haben oder nicht. Um den kanonischen Namen eines Systemsteuerung, das hier nicht aufgeführt ist, suchen Sie in der Registrierung unter den folgenden Pfaden:

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

Weitere Informationen zum Erkennen der erforderlichen CLSIDs finden Sie unter How [to Register Executable Systemsteuerung Items](how-to-register-an-executable-control-panel-item-registration-.md) und How to Register DLL Systemsteuerung [Items](how-to-register-dll-control-panel-item-registration-.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ausführen Systemsteuerung Elementen](executing-control-panel-items.md)
</dt> <dt>

[**IOpenControlPanel**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopencontrolpanel)
</dt> </dl>

 

 



