---
title: Microsoft Windows Media DRM-Clientstrukturen
description: Microsoft Windows Media DRM-Clientstrukturen
ms.assetid: 794de1b7-d60c-435e-9f77-c4df109b5372
keywords:
- Windows Medienformat-SDK, Strukturen
- Digital Rights Management (DRM), Strukturen
- DRM (Digital Rights Management), Strukturen
- Erweiterte APIs des DRM-Clients, Strukturen
- Erweiterte Client-APIs, Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 145381cc6d702dd338176ffa89983de137285dcd7aef946d3ece956eb450880c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447840"
---
# <a name="microsoft-windows-media-drm-client-structures"></a>Microsoft Windows Media DRM-Clientstrukturen

Die folgenden Strukturen werden von den erweiterten APIs des Windows Media DRM-Clients unterstützt.



| Struktur oder Enumeration                                                                    | Beschreibung                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ \_ SCHUTZ-IDS FÜR DRM-AUDIOAUSGABE \_**](drm-audio-output-protection-ids.md)              | Enthält eine Liste der Schutzbezeichner für die Audioausgabe.                                                                                                     |
| [**DRM \_ AUDIO \_ OUTPUT \_ PROTECTION \_ IDS \_ EX**](drm-audio-output-protection-ids-ex.md)       | Enthält eine Liste der Schutzbezeichner für die Audioausgabe. Diese Struktur erweitert **DRM \_ AUDIO OUTPUT \_ PROTECTION \_ \_ IDS** durch Hinzufügen einer Versionsnummer.          |
| [**DRM \_ COPY \_ OPL**](drmdrm-copy-opl.md)                                                   | Enthält Informationen zu den in einer Lizenz für Kopieraktionen angegebenen Ausgabeschutzebenen.                                                               |
| [**\_ \_ DRM-LIZENZSTATUSDATEN \_**](drmdrm-license-state-data.md)                              | Enthält Informationen zu den Lizenzeinschränkungen für ein DRM-Recht.                                                                                        |
| [**MINIMALE \_ \_ DRM-AUSGABESCHUTZEBENEN \_ \_**](drmdrm-minimum-output-protection-levels.md) | Enthält die minimalen Ausgabeschutzebenen (OPLs) für die Wiedergabe verschiedener Inhaltstypen.                                                                 |
| [**DRM \_ OPL \_ OUTPUT \_ IDS**](drmdrm-opl-output-ids.md)                                      | Enthält eine Reihe von OPL-Ausgabebezeichnern.                                                                                                                   |
| [**\_DRM-AUSGABESCHUTZ \_**](drm-output-protection.md)                                    | Enthält Informationen zu einer Ausgabeschutztechnologie.                                                                                                    |
| [**DRM \_ OUTPUT \_ PROTECTION \_ EX**](drm-output-protection-ex.md)                             | Enthält Informationen zu einer Ausgabeschutztechnologie. Diese Struktur erweitert **DRM \_ OUTPUT \_ PROTECTION** durch Hinzufügen einer Versionsnummer.                     |
| [**DRM \_ PLAY \_ OPL**](drmdrm-play-opl.md)                                                   | Enthält Informationen zu den opls, die in einer Lizenz für Wiedergabeaktionen angegeben sind.                                                                                   |
| [**DRM \_ PLAY \_ OPL \_ EX**](drm-play-opl-ex.md)                                               | Enthält erweiterte Informationen zu den OPLs, die in einer Lizenz für Wiedergabeaktionen angegeben sind.                                                                          |
| [**\_ \_ \_ SCHUTZ-IDS FÜR DRM-VIDEOAUSGABE \_**](drmdrm-video-output-protection-ids.md)           | Enthält ein Array von **DRM \_ VIDEO OUTPUT \_ \_ PROTECTION-Strukturen.**                                                                                            |
| [**DRM \_ VIDEO \_ OUTPUT \_ PROTECTION \_ IDS \_ EX**](drm-video-output-protection-ids-ex.md)       | Enthält ein Array von **DRM \_ VIDEO OUTPUT \_ \_ PROTECTION-Strukturen.** Diese Struktur erweitert **DRM \_ VIDEO OUTPUT \_ PROTECTION \_ \_ IDS** durch Hinzufügen einer Versionsnummer. |
| [**WM \_ BACKUP \_ RESTORE \_ STATUS**](wm-backup-restore-status.md)                             | Enthält Informationen zu einem ausstehenden Lizenzsicherungs- oder Wiederherstellungsvorgang.                                                                                      |
| [**WM \_ INDIVIDUALIZE \_ STATUS**](drmwm-individualize-status.md)                             | Enthält Informationen zu einem ausstehenden Individualisierungsprozess.                                                                                                |
| [**WMDRM \_ – \_ ANALOGE \_ VIDEOEINSCHRÄNKUNGEN**](wmdrm-analog-video-restrictions.md)               | Enthält Informationen zu einer Einschränkung für die Wiedergabe von Inhalten als analoges Video.                                                                             |
| [**WMDRM \_ ANALOG \_ VIDEO \_ RESTRICTIONS \_ EX**](wmdrm-analog-video-restrictions-ex.md)        | Enthält erweiterte Informationen zu einer Einschränkung für die Wiedergabe von Inhalten als analoges Video.                                                                    |
| [**WMDRM \_ ENCRYPT \_ SCATTER \_ BLOCK**](wmdrm-encrypt-scatter-block.md)                       | Enthält einen Datenblock, der verschlüsselt werden soll.                                                                                                                   |
| [**WMDRM \_ ENCRYPT \_ SCATTER \_ INFO**](wmdrm-encrypt-scatter-info.md)                         | Enthält Informationen, die zum Konfigurieren der [**IWMDRMEncryptScatter-Schnittstelle**](iwmdrmencryptscatter.md) für die Verwendung erforderlich sind.                                        |
| [**\_WMDRM-LIZENZFILTER \_**](wmdrm-license-filter.md)                                      | Enthält Filterinformationen zum Erstellen von Lizenzenumerationen.                                                                                           |
| [**\_ \_ WMDRM-AUSGABESCHUTZEBENEN \_**](wmdrm-output-protection-levels.md)                 | Enthält die Ausgabeschutzebenen, die von einer Lizenz zum Ausführen verschiedener Aktionen benötigt werden.                                                                    |
| [**WMDRMCryptoData**](wmdrmcryptodata.md)                                                  | Enthält Informationen über den kryptografischen Algorithmus, der zum Verschlüsseln und Entschlüsseln von Inhalten verwendet wird.                                                                 |
| [**\_WMDRMNET-RICHTLINIE**](wmdrmnet-policy.md)                                                 | Enthält die Richtlinie, die für Windows Medien-DRM für Netzwerkgerätevorgänge verwendet werden soll.                                                                        |
| [**GLOBALE ANFORDERUNGEN FÜR WMDRMNET-RICHTLINIEN \_ \_ \_**](wmdrmnet-policy-global-requirements.md)       | Enthält globale Anforderungen für Windows Medien-DRM für Netzwerkgeräte.                                                                                        |
| [**\_ \_ WMDRMNET-RICHTLINIENMINDESTUMGEBUNG \_**](wmdrmnet-policy-minimum-environment.md)       | Enthält die Mindestsicherheitsanforderungen für Windows Medien-DRM für Netzwerkgeräte.                                                                       |
| [**WMDRMNET \_ POLICY \_ TRANSCRYPTPLAY**](wmdrmnet-policy-transcryptplay.md)                  | Enthält die Richtlinieninformationen zum Wiedergeben von Inhalten mithilfe Windows Medien-DRM für Netzwerkgeräte.                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierverzeichnis**](drm-programming-reference.md)
</dt> </dl>

 

 




