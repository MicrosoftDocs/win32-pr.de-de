---
description: Erfahren Sie mehr über die Konzepte und Features der wichtigsten Audio-APIs von Windows Vista und deren Verwendung bei der Anwendungsprogrammierung.
ms.assetid: 825c7cd7-dc66-47b6-a1b6-d10101daebb3
title: Core Audio Programming Guide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2b8f65d0c5508cd821b49a42b4b89ea42859390913a30534319d5ef7c79224f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088390"
---
# <a name="core-audio-programming-guide"></a>Core Audio Programming Guide

In diesem Abschnitt werden die Konzepte und Features der wichtigsten Audio-APIs von Windows Vista und deren Verwendung bei der Anwendungsprogrammierung erläutert.

In diesem Abschnitt werden die folgenden Themen behandelt:



| Thema                                                                                                                      | Beschreibung                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Audiokomponenten im Benutzermodus](user-mode-audio-components.md)                                                               | Über die Low-Level-Schnittstellen in den Kernaudio-APIs kann ein Client auf die Systemkomponenten zugreifen, die Audiostreams verwalten und kombinieren.                                                                        |
| [Audio im geschützten Benutzermodus (PROTECTED User Mode Audio, SOLL)](protected-user-mode-audio--puma-.md)                                                   | Beschreibt die Aktualisierungen von PROTECTED (Protected User Mode Audio), der Audio-Engine im Benutzermodus in der geschützten Umgebung (Protected Environment, PE), die eine sicherere Umgebung für die Audioverarbeitung und das Rendering bietet.              |
| [Audioendpunktgeräte](audio-endpoint-devices.md)                                                                       | Ein Audioendpunktgerät ist eine Softwareabstraktion, die benutzerfreundliche Interaktionen mit Audiogeräten wie Mikrofonen und Lautsprechern ermöglicht.                                                              |
| [Audiositzungen](audio-sessions.md)                                                                                       | Eine Audiositzung ist eine Softwareabstraktion, die es einem Client ermöglicht, eine Sammlung verwandter Audiostreams als einzelne Einheit zu verwalten.                                                                           |
| [Lautstärkeregler](volume-controls.md)                                                                                     | Das System integriert seine richtlinienbasierten Volumeeinstellungen auf logische und konsistente Weise in die Volumeeinstellungen des Benutzers.                                                                                      |
| [Streamverwaltung](stream-management.md)                                                                                 | Die Windows AudioSitzungs-API (WASAPI) stellt einem Client einen vollständigen Satz von Methoden zum Erstellen und Verwalten von Audiostreams bereit.                                                                             |
| [Gerätetopologien](device-topologies.md)                                                                                 | Mit der DeviceTopology-API kann ein Client die Audiosteuerelemente entdecken, die sich entlang der verschiedenen Datenpfade in der Audiohardware befinden.                                                                          |
| [Verwenden der IKsControl-Schnittstelle für den Zugriff auf Audioeigenschaften](using-the-ikscontrol-interface-to-access-audio-properties.md) | Eine spezialisierte Audioanwendung muss möglicherweise die IKsControl-Schnittstelle verwenden, um auf die Eigenschaften eines Audioadapters zu zugreifen.                                                                                     |
| [Interoperabilität mit Legacyaudio-APIs](interoperability-with-legacy-audio-apis.md)                                     | Wichtige Features der Kernaudio-APIs in Windows Vista können in vorhandene Anwendungen integriert werden, die DirectSound, DirectShow und die Windows-Multimediafunktionen **waveOutXxx** und **waveInXxx** verwenden. |
| [Raumklang](spatial-sound.md)                                                                                         | Bietet Anleitungen für die Verwendung von Windows Sonic, der Plattformlösung von Microsoft für die Unterstützung räumlicher Sounds auf Xbox und Windows, die sowohl Umschließen als auch Rechteerweiterungen (über oder unterhalb des Listeners) audio cues ermöglicht. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kernaudio-APIs](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



