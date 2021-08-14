---
title: Digital Rights Management Features
description: Digital Rights Management Features
ms.assetid: c3c1e59f-8ff9-496c-8e63-0c1cf4ce7092
keywords:
- Windows Medienformat-SDK, DRM-Features
- Digital Rights Management (DRM), Features
- DRM (Digital Rights Management), Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e389efdbfd3edef3f3c881cab8482c8ed03b6bb09eb4a7773caa59b4b9b1ad4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704869"
---
# <a name="digital-rights-management-features"></a>Digital Rights Management Features

\[Die Windows Medien-DRM-Funktion ist veraltet und sollte nicht verwendet werden. Verwenden Sie stattdessen [Microsoft PlayReady.](/windows/uwp/audio-video-camera/playready-client-sdk)\]

Digital Rights Management (DRM) ist eine Technologie, mit der Inhaltsbesitzer digitale Mediendateien schützen können, indem sie sie mit einem Schlüssel verschlüsseln (einem Datenteil, der den Inhalt sperrt und entsperrt). Um eine geschützte ASF-Datei wiedergeben zu können, muss ein Consumer eine separate Lizenz mit dem Schlüssel abrufen. Jede Lizenz enthält auch Rechte, die vom Inhaltsbesitzer oder Lizenzaussteller bestimmt werden und angeben, wie der Consumer die Datei verwenden kann. Mithilfe der DRM-Technologie können Inhaltsbesitzer Titel, Videos und andere digitale Mediendateien über das Internet in einem geschützten Dateiformat bereitstellen und die Verwendung ihrer digitalen Inhalte steuern. Microsoft DRM-Technologie wird auch vom Windows Media Rights Manager, dem Windows Media Encoder und Windows Media Player unterstützt. Weitere Hintergrundinformationen zur DRM-Technologie von Microsoft finden Sie auf der [Microsoft Windows Media-Website.](https://support.microsoft.com/help/17946/windows-media)

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

In den folgenden Abschnitten werden die wichtigsten DRM-bezogenen Features des Windows Media Format SDK erläutert.



| `Section`                                                                                            | BESCHREIBUNG                                                                                                                          |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [DRM-Grundlagen](drm-basics.md)                                                                       | Bietet eine kurze Übersicht über die DRM-Funktionalität, die vom Windows Media Format SDK bereitgestellt wird.                                         |
| [DRM-Versionen](drm-versions.md)                                                                   | Beschreibt die hauptunterschiede zwischen den Versionen des DRM-Schutzes, die für Anwendungen verfügbar sind.                                     |
| [Live-DRM](live-drm.md)                                                                           | Beschreibt die Szenarien, die durch den DRM-Schutz "on the fly" ermöglicht werden.                                                                |
| [DRM-Individualisierung](drm-individualization.md)                                                 | Beschreibt das Anwendungssicherheitsupgrade, das DRM-Inhaltsbesitzer oder Lizenzaussteller benötigen können.                                   |
| [Sichern und Wiederherstellen von DRM-Lizenzen](backing-up-and-restoring-of-drm-licenses.md)           | Beschreibt die Vor- und Nachteile, die es Benutzern gestatten, ihre Inhaltslizenzen zu sichern und wiederherzustellen.                                       |
| [Anzeigen von DRM-Attributen im Metadaten-Editor](viewing-drm-attributes-in-the-metadata-editor.md) | Beschreibt die Funktionen dieses DRM-Hilfsobjekts und die Szenarien, die es unterstützen soll.                                   |
| [Ausgabeschutzebenen](output-protection-levels.md)                                           | Beschreibt, wie DRM-Lizenzen der Version 10 durch Ausgabeschutzebenen flexibler werden.                                                   |
| [Lizenzsperrung](license-revocation.md)                                                       | Beschreibt die Lizenzsperrung.                                                                                                        |
| [Windows Medien-DRM 10 für Netzwerkgeräte](windows-media-drm-10-for-network-devices.md)           | Führt Windows Media DRM 10 für Netzwerkgeräte und seine Implementierung in diesem SDK ein.                                              |
| [Microsoft Secure Audio Path](microsoft-secure-audio-path--deprecated.md)                         | Beschreibt die Microsoft Secure Audio Path-Architektur, die das höchste Maß an Schutz für geschützte Audioinhalte bietet. |
| [Wiedergabelistenwiedergabe](playlist-burning.md)                                                           | Beschreibt die Wiedergabelistenfunktion von DRM und wie sie im Windows Media Format SDK unterstützt wird.                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Aktivieren der DRM-Unterstützung**](enabling-drm-support.md)
</dt> <dt>

[**Features**](features.md)
</dt> </dl>

 

 