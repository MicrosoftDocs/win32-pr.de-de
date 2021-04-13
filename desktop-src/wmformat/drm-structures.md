---
title: Microsoft Windows Media DRM-Client Strukturen
description: Microsoft Windows Media DRM-Client Strukturen
ms.assetid: 794de1b7-d60c-435e-9f77-c4df109b5372
keywords:
- Windows Media-Format-SDK, Strukturen
- Digital Rights Management (DRM), Strukturen
- DRM (Digital Rights Management), Strukturen
- Erweiterte APIs für den DRM-Client, Strukturen
- Erweiterte Client-APIs, Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43264c37ed9830026f87998823017d17c9d75f7e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391372"
---
# <a name="microsoft-windows-media-drm-client-structures"></a>Microsoft Windows Media DRM-Client Strukturen

Die folgenden Strukturen werden von den erweiterten APIs des Windows Media DRM-Clients unterstützt.



| Struktur oder Enumeration                                                                    | BESCHREIBUNG                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DRM \_ - \_ Audioausgabe- \_ Schutz- \_ IDs**](drm-audio-output-protection-ids.md)              | Enthält eine Liste der audioausgabeschutzbezeichner.                                                                                                     |
| [**DRM \_ - \_ audioausgabeschutz- \_ \_ IDs \_ Ex**](drm-audio-output-protection-ids-ex.md)       | Enthält eine Liste der audioausgabeschutzbezeichner. Diese Struktur erweitert **DRM \_ - \_ audioausgabeschutz- \_ \_ IDs** durch Hinzufügen einer Versionsnummer.          |
| [**DRM- \_ Kopier- \_ OPL**](drmdrm-copy-opl.md)                                                   | Enthält Informationen zu den in einer Lizenz für Kopieraktionen angegebenen Ausgabe Schutz Ebenen.                                                               |
| [**DRM- \_ Lizenz \_ Zustands \_ Daten**](drmdrm-license-state-data.md)                              | Enthält Informationen zu den Lizenz Einschränkungen für ein DRM-Recht.                                                                                        |
| [**minimale DRM- \_ \_ Ausgabe \_ Schutz \_ Ebenen**](drmdrm-minimum-output-protection-levels.md) | Enthält die minimalen Ausgabe Schutz Ebenen (opls) für die Wiedergabe verschiedener Inhaltstypen.                                                                 |
| [**DRM- \_ OPL- \_ Ausgabe- \_ IDs**](drmdrm-opl-output-ids.md)                                      | Enthält eine Reihe von OPL-Ausgabe bezeichgern.                                                                                                                   |
| [**DRM- \_ Ausgabe \_ Schutz**](drm-output-protection.md)                                    | Enthält Informationen zu einer-Ausgabe Schutz Technologie.                                                                                                    |
| [**DRM- \_ Ausgabe \_ Schutz ( \_ Ex)**](drm-output-protection-ex.md)                             | Enthält Informationen zu einer-Ausgabe Schutz Technologie. Diese Struktur erweitert den **DRM- \_ Ausgabe \_ Schutz** durch Hinzufügen einer Versionsnummer.                     |
| [**DRM- \_ Wiedergabe- \_ OPL**](drmdrm-play-opl.md)                                                   | Enthält Informationen zu den in einer Lizenz für Wiedergabe Aktionen angegebenen opls.                                                                                   |
| [**DRM \_ Play \_ OPL \_ Ex**](drm-play-opl-ex.md)                                               | Enthält erweiterte Informationen zu den in einer Lizenz für Wiedergabe Aktionen angegebenen opls.                                                                          |
| [**DRM- \_ Video- \_ Ausgabe Schutz- \_ \_ IDs**](drmdrm-video-output-protection-ids.md)           | Enthält ein Array von **DRM- \_ Video- \_ ausgabeschutzstrukturen \_** .                                                                                            |
| [**DRM- \_ Video- \_ Ausgabe Schutz- \_ \_ IDs \_ Ex**](drm-video-output-protection-ids-ex.md)       | Enthält ein Array von **DRM- \_ Video- \_ ausgabeschutzstrukturen \_** . Diese Struktur erweitert **DRM- \_ Video- \_ Ausgabe Schutz- \_ \_ IDs** durch Hinzufügen einer Versionsnummer. |
| [**\_ \_ Wiederherstellungs \_ Status der WM-Sicherung**](wm-backup-restore-status.md)                             | Enthält Informationen über eine ausstehende Lizenz Sicherung oder einen Wiederherstellungs Vorgang.                                                                                      |
| [**Status der WM- \_ Individualisierung \_**](drmwm-individualize-status.md)                             | Enthält Informationen über einen ausstehenden Individualisierungsprozess.                                                                                                |
| [**\_Einschränkungen für analoge \_ Videos \_ in WMDRM**](wmdrm-analog-video-restrictions.md)               | Enthält Informationen zu einer Einschränkung für die Wiedergabe von Inhalten als analoges Video.                                                                             |
| [**Einschränkungen für Analog zum WMDRM- \_ \_ Video \_ \_**](wmdrm-analog-video-restrictions-ex.md)        | Enthält erweiterte Informationen zu einer Einschränkung für die Wiedergabe von Inhalten als analoges Video.                                                                    |
| [**WMDRM- \_ Verschlüsselungs Punkt \_ \_ Block**](wmdrm-encrypt-scatter-block.md)                       | Enthält einen Datenblock, der verschlüsselt werden soll.                                                                                                                   |
| [**WMDRM- \_ Verschlüsselungs Punkt \_ \_ Informationen**](wmdrm-encrypt-scatter-info.md)                         | Enthält Informationen, die erforderlich sind, um die [**iwmdrmencryptscatter**](iwmdrmencryptscatter.md) -Schnittstelle zur Verwendung zu konfigurieren.                                        |
| [**WMDRM- \_ Lizenz \_ Filter**](wmdrm-license-filter.md)                                      | Enthält Filter Informationen zum Erstellen von Lizenzierungs Enumerationen.                                                                                           |
| [**WMDRM- \_ Ausgabe \_ Schutz \_ Ebenen**](wmdrm-output-protection-levels.md)                 | Enthält die ausgabeschutzgrade, die für eine Lizenz erforderlich sind, um verschiedene Aktionen auszuführen.                                                                    |
| [**Wmdrmcryptodata**](wmdrmcryptodata.md)                                                  | Enthält Informationen über den Kryptografiealgorithmus, der zum Verschlüsseln und Entschlüsseln von Inhalten verwendet wird.                                                                 |
| [**wmdrmnet- \_ Richtlinie**](wmdrmnet-policy.md)                                                 | Enthält die Richtlinie, die für Windows Media DRM für den Betrieb von Netzwerkgeräten verwendet werden soll.                                                                        |
| [**globale Anforderungen für wmdrmnet- \_ Richtlinien \_ \_**](wmdrmnet-policy-global-requirements.md)       | Enthält globale Anforderungen für Windows Media DRM für Netzwerkgeräte.                                                                                        |
| [**minimale Umgebung der wmdrmnet- \_ Richtlinie \_ \_**](wmdrmnet-policy-minimum-environment.md)       | Enthält die minimalen Sicherheitsanforderungen für Windows Media DRM für Netzwerkgeräte.                                                                       |
| [**wmdrmnet- \_ Richtlinie \_ transryptplay**](wmdrmnet-policy-transcryptplay.md)                  | Enthält die Richtlinien Informationen für die Wiedergabe von Inhalten mithilfe von Windows Media DRM für Netzwerkgeräte.                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierverzeichnis**](drm-programming-reference.md)
</dt> </dl>

 

 




