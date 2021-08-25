---
title: Microsoft Windows Media DRM-Clientschnittstellen
description: Microsoft Windows Media DRM-Clientschnittstellen
ms.assetid: 27bbc33f-8102-4db2-bbc6-1a1da92bac80
keywords:
- Windows Medienformat-SDK, Schnittstellen
- Digital Rights Management (DRM), Schnittstellen
- DRM (Digital Rights Management), Schnittstellen
- ERWEITERTE APIs für DEN DRM-Client, Schnittstellen
- Erweiterte Client-APIs, Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972224decdad339876e4f72c40cad5b3ba28de98446ff358fd36cb7f86bee0af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931100"
---
# <a name="microsoft-windows-media-drm-client-interfaces"></a>Microsoft Windows Media DRM-Clientschnittstellen

In der folgenden Tabelle werden die Schnittstellen beschrieben, die von den Windows Media DRM-Client-APIs unterstützt werden.



| Schnittstelle                                                                    | BESCHREIBUNG                                                                                                     |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**IDRMStatusCallback**](idrmstatuscallback.md)                             | Enthält die Definition für einen Statusrückruf, den Sie implementieren können, um asynchrone DRM-Vorgänge zu verarbeiten.     |
| [**IWMDRMDecrypt**](iwmdrmdecrypt.md)                                       | Stellt eine Methode zum Entschlüsseln von Inhalt zur Auswahl.                                                                       |
| [**IWMDRMEncrypt**](iwmdrmencrypt.md)                                       | Stellt eine Methode zum Verschlüsseln von Daten an Ort und Stelle zur Auswahl.                                                                 |
| [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md)                         | Verschlüsselt Daten aus nicht zusammenhängenden Blöcken.                                                                       |
| [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)                         | Erweiterung der **INTERFACE FÜR DEN 1000-000-000-Generator,** die eine Methode zum Abbrechen asynchroner Vorgänge bietet. |
| [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md)       | Ermöglicht das Abrufen erweiterter Statusinformationen zum Fortschritt der Individualisierung.                       |
| [**IWMDRMLicense**](iwmdrmlicense.md)                                       | Stellt eine oder mehrere Lizenzen im lokalen Lizenzspeicher dar.                                                     |
| [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) | Ermöglicht das Abrufen ausführlicher Statusinformationen zu einer Lizenzsicherung oder einem Wiederherstellungsvorgang.                   |
| [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)                   | Aktiviert Verwaltungsvorgänge für den lokalen Lizenzspeicher.                                                      |
| [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)                   | Stellt zusätzliche Verwaltungsoptionen für den lokalen Lizenzspeicher zur Verfügung.                                             |
| [**IWMDRMLicenseQuery**](iwmdrmlicensequery.md)                             | Ermöglicht Anwendungen das Abfragen der Rechte und des Lizenzstatus für eine geschützte Datei.                                |
| [**IWMDRMNetReceiver**](iwmdrmnetreceiver.md)                               | Stellt die erforderlichen Methoden zum Erstellen einer Microsoft Windows Media DRM für Empfängeranwendung für Netzwerkgeräte zur Verfügung.          |
| [**IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)                         | Stellt die erforderlichen Methoden zum Erstellen einer Microsoft Windows Media DRM for Network Devices-Senderanwendung zur Verfügung.       |
| [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) | Stellt Methoden zum Aktivieren des Lizenzerwerbs mit Benutzereingriffen zur                                        |
| [**IWMDRMProvider**](iwmdrmprovider.md)                                     | Erstellt die anderen Objekte der erweiterten APIs des Microsoft Windows Media DRM-Clients.                              |
| [**IWMDRMSecurity**](iwmdrmsecurity.md)                                     | Verwaltet verschiedene sicherheitsbezogene Prozesse für den Clientcomputer und das DRM-Subsystem.                           |
| [**IWMDRMSecurity**](iwmdrmsecurity.md)                                     | Verwaltet die Sperrung und Erneuerung von Komponenten.                                                                       |
| [**IWMSecureBuffer**](iwmsecurebuffer.md)                                   | Aktiviert die Verschlüsselung und Entschlüsselung von Puffern.                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierverzeichnis**](drm-programming-reference.md)
</dt> </dl>

 

 




