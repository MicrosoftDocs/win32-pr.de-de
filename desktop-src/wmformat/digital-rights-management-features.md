---
title: Features digitaler Rights Management
description: Features digitaler Rights Management
ms.assetid: c3c1e59f-8ff9-496c-8e63-0c1cf4ce7092
keywords:
- Windows Media-Format-SDK, DRM-Features
- Digital Rights Management (DRM), Features
- DRM (Digital Rights Management), Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bd9c30b350fdf430d5b20bbe112c5309ac9da4f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728009"
---
# <a name="digital-rights-management-features"></a>Features digitaler Rights Management

\[Das Windows Media DRM-Feature ist veraltet und sollte nicht verwendet werden. Verwenden Sie stattdessen [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]

Die digitale Rechteverwaltung (Digital Rights Management, DRM) ist eine Technologie, mit der Inhalts Besitzer digitale Mediendateien schützen können, indem Sie mit einem Schlüssel verschlüsselt werden (ein Datenelement, das den Inhalt sperrt und entsperrt). Zum Wiedergeben einer geschützten ASF-Datei muss ein Consumer eine separate Lizenz abrufen, die den Schlüssel enthält. Jede Lizenz enthält auch Rechte, die vom Inhalts Besitzer oder Lizenz Aussteller festgelegt werden, die angeben, wie der Consumer die Datei verwenden kann. Mithilfe der DRM-Technologie können Inhalts Besitzer Lieder, Videos und andere digitale Mediendateien über das Internet in einem geschützten Dateiformat bereitstellen und die Verwendung Ihrer digitalen Inhalte steuern. Die Microsoft DRM-Technologie wird auch vom Windows Media Rights Manager, dem Windows Media Encoder und Windows Media Player unterstützt. Weitere Hintergrundinformationen zur DRM-Technologie von Microsoft finden Sie auf der [Microsoft Windows Media](https://support.microsoft.com/help/17946/windows-media)-Website.

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

In den folgenden Abschnitten werden die wichtigsten DRM-bezogenen Features des Windows Media Format SDK erläutert.



| `Section`                                                                                            | BESCHREIBUNG                                                                                                                          |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [DRM-Grundlagen](drm-basics.md)                                                                       | Bietet eine kurze Übersicht über die DRM-Funktionalität, die vom SDK für den Windows Media-Format bereitgestellt wird.                                         |
| [DRM-Versionen](drm-versions.md)                                                                   | Beschreibt die Hauptunterschiede zwischen den Versionen des DRM-Schutzes, die für-Anwendungen verfügbar sind.                                     |
| [Live DRM](live-drm.md)                                                                           | Hier werden die Szenarien beschrieben, die durch den "on-the-the"-DRM-Schutz                                                                |
| [DRM-Individualisierung](drm-individualization.md)                                                 | Beschreibt das Anwendungs Sicherheits Upgrade, das von DRM-Inhalts Besitzern oder Lizenz Ausstellern angefordert werden kann.                                   |
| [Sichern und Wiederherstellen von DRM-Lizenzen](backing-up-and-restoring-of-drm-licenses.md)           | Beschreibt die vor-und Nachteile, die es Benutzern ermöglichen, ihre Inhalts Lizenzen zu sichern und wiederherzustellen.                                       |
| [Anzeigen von DRM-Attributen im Metadateneditor](viewing-drm-attributes-in-the-metadata-editor.md) | Beschreibt die Funktionen dieses DRM-Hilfsobjekts und der Szenarien, die unterstützt werden sollen.                                   |
| [Ausgabe Schutz Ebenen](output-protection-levels.md)                                           | In diesem Thema wird beschrieben, wie durch Ausgabe Schutz Ebenen DRM-Lizenzen der Version 10 flexibler werden                                                   |
| [Lizenz Sperrung](license-revocation.md)                                                       | Beschreibt die Lizenz Sperrung.                                                                                                        |
| [Windows Media DRM 10 für Netzwerkgeräte](windows-media-drm-10-for-network-devices.md)           | Führt Windows Media DRM 10 für Netzwerkgeräte und deren Implementierung in diesem SDK ein.                                              |
| [Microsoft Secure-Audiopfad](microsoft-secure-audio-path--deprecated.md)                         | Beschreibt die Microsoft Secure-Audiopfad-Architektur, die das höchste Maß an Schutz für geschützte Audioinhalte bietet. |
| [Wiedergabelisten brennen](playlist-burning.md)                                                           | Beschreibt die Funktion zum Brennen der Wiedergabeliste von DRM und wie Sie im Windows Media-Format-SDK unterstützt wird.                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Aktivieren DRM-Unterstützung**](enabling-drm-support.md)
</dt> <dt>

[**Features**](features.md)
</dt> </dl>

 

 