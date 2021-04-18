---
title: Microsoft Windows Media DRM-Client Schnittstellen
description: Microsoft Windows Media DRM-Client Schnittstellen
ms.assetid: 27bbc33f-8102-4db2-bbc6-1a1da92bac80
keywords:
- Windows Media-Format-SDK, Schnittstellen
- Digital Rights Management (DRM), Schnittstellen
- DRM (Digital Rights Management), Schnittstellen
- Erweiterte APIs des DRM-Clients, Schnittstellen
- Erweiterte Client-APIs, Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4e259ef5b8ef410db072a7f942d139f682bc90
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391373"
---
# <a name="microsoft-windows-media-drm-client-interfaces"></a>Microsoft Windows Media DRM-Client Schnittstellen

In der folgenden Tabelle werden die von den Windows Media DRM-Client-APIs unterstützten Schnittstellen beschrieben.



| Schnittstelle                                                                    | BESCHREIBUNG                                                                                                     |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**Idrmstatus Callback**](idrmstatuscallback.md)                             | Stellt die Definition für einen Status Rückruf bereit, den Sie implementieren können, um asynchrone DRM-Vorgänge zu verarbeiten.     |
| [**Iwmdrmentschlüsseln**](iwmdrmdecrypt.md)                                       | Stellt eine Methode für das Entschlüsseln von Inhalten bereit.                                                                       |
| [**Iwmdrmencrypt**](iwmdrmencrypt.md)                                       | Bietet eine Methode zum Verschlüsseln von Daten an Ort und Stelle.                                                                 |
| [**Iwmdrmencryptscatter**](iwmdrmencryptscatter.md)                         | Verschlüsselt Daten aus nicht zusammenhängenden Blöcken.                                                                       |
| [**Iwmdrmeventgenerator**](iwmdrmeventgenerator.md)                         | Erweiterung der **imfmediaeventgenerator** -Schnittstelle, die eine Methode zum Abbrechen von asynchronen Vorgängen bereitstellt. |
| [**Iwmdrmindividualizationstatus**](iwmdrmindividualizationstatus.md)       | Ermöglicht das Abrufen erweiterter Statusinformationen über den Fortschritt der Individual alisierung.                       |
| [**Iwmdrmlicense**](iwmdrmlicense.md)                                       | Stellt eine oder mehrere Lizenzen im lokalen Lizenz Speicher dar.                                                     |
| [**Iwmdrmlicenabbackuprestorestatus**](iwmdrmlicensebackuprestorestatus.md) | Ermöglicht das Abrufen detaillierter Statusinformationen zu einer Lizenz Sicherung oder eines Wiederherstellungs Vorgangs.                   |
| [**Iwmdrmlicenabmanagement**](iwmdrmlicensemanagement.md)                   | Aktiviert Verwaltungsvorgänge für den lokalen Lizenz Speicher.                                                      |
| [**Iwmdrmlicenabmanagement**](iwmdrmlicensemanagement.md)                   | Stellt zusätzliche Verwaltungs Optionen für den lokalen Lizenz Speicher bereit.                                             |
| [**Iwmdrmlicensequery**](iwmdrmlicensequery.md)                             | Ermöglicht es Anwendungen, die Rechte und den Lizenzstatus für eine geschützte Datei abzufragen.                                |
| [**Iwmdrmnetreceiver**](iwmdrmnetreceiver.md)                               | Stellt Methoden bereit, die zum Erstellen einer Empfänger Anwendung für Microsoft Windows Media DRM für Netzwerkgeräte erforderlich sind.          |
| [**Iwmdrmnettransmitter**](iwmdrmnettransmitter.md)                         | Stellt Methoden bereit, die zum Erstellen einer Microsoft Windows Media DRM for Network Devices-übermittleranwendung erforderlich sind.       |
| [**Iwmdrmnonsilentlicenseaquisition**](iwmdrmnonsilentlicenseaquisition.md) | Stellt Methoden bereit, die den Erwerb von Lizenzen mit Benutzereingriff ermöglichen.                                        |
| [**Iwmdrmprovider**](iwmdrmprovider.md)                                     | Erstellt die anderen Objekte der erweiterten APIs für den Microsoft Windows Media DRM-Client.                              |
| [**Iwmdrmsecurity**](iwmdrmsecurity.md)                                     | Verwaltet verschiedene sicherheitsbezogene Prozesse für den Client Computer und das DRM-Subsystem.                           |
| [**Iwmdrmsecurity**](iwmdrmsecurity.md)                                     | Verwaltet die Sperrung und Verlängerung der Komponente.                                                                       |
| [**Iwmsecurebuffer**](iwmsecurebuffer.md)                                   | Aktiviert die Verschlüsselung und Entschlüsselung von Puffern.                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierverzeichnis**](drm-programming-reference.md)
</dt> </dl>

 

 




