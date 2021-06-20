---
description: Erfahren Sie mehr über die Konzepte und Features der Kernaudio-APIs von Windows Vista und deren Verwendung in der Anwendungsprogrammierung.
ms.assetid: 825c7cd7-dc66-47b6-a1b6-d10101daebb3
title: Core Audio Programming Guide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f02e27206c70cca69abf263cfa49dfd439c480
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405873"
---
# <a name="core-audio-programming-guide"></a>Core Audio Programming Guide

In diesem Leitfadenabschnitt werden die Konzepte und Features der Kernaudio-APIs von Windows Vista sowie deren Verwendung in der Anwendungsprogrammierung erläutert.

In diesem Abschnitt werden die folgenden Themen behandelt:



| Thema                                                                                                                      | Beschreibung                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Benutzermodus-Audiokomponenten](user-mode-audio-components.md)                                                               | Über die Low-Level-Schnittstellen in den Kernaudio-APIs kann ein Client auf die Systemkomponenten zugreifen, die Audiostreams verwalten und mischen.                                                                        |
| [Audio im geschützten Benutzermodus (PROTECTED)](protected-user-mode-audio--puma-.md)                                                   | Beschreibt die Updates für Protected User Mode Audio (CSV), die Benutzermodus-Audio-Engine in der geschützten Umgebung (PE), die eine sicherere Umgebung für die Audioverarbeitung und das Rendering bietet.              |
| [Audioendpunktgeräte](audio-endpoint-devices.md)                                                                       | Ein Audioendpunktgerät ist eine Softwareabstraktion, die benutzerfreundliche Interaktionen mit Audiogeräten wie Mikrofonen und Lautsprechern ermöglicht.                                                              |
| [Audiositzungen](audio-sessions.md)                                                                                       | Eine Audiositzung ist eine Softwareabstraktion, die es einem Client ermöglicht, eine Sammlung verwandter Audiostreams als einzelne Einheit zu verwalten.                                                                           |
| [Lautstärkeregler](volume-controls.md)                                                                                     | Das System integriert seine richtlinienbasierten Volumeeinstellungen logisch und konsistent in die Volumeeinstellungen des Benutzers.                                                                                      |
| [Streamverwaltung](stream-management.md)                                                                                 | Die Windows-Audiositzungs-API (WASAPI) bietet einem Client einen vollständigen Satz von Methoden zum Erstellen und Verwalten von Audiostreams.                                                                             |
| [Gerätetopologien](device-topologies.md)                                                                                 | Mit der DeviceTopology-API kann ein Client die Audiosteuerelemente ermitteln, die sich entlang der verschiedenen Datenpfade in der Audiohardware befinden.                                                                          |
| [Verwenden der IKsControl-Schnittstelle für den Zugriff auf Audioeigenschaften](using-the-ikscontrol-interface-to-access-audio-properties.md) | Eine spezielle Audioanwendung muss möglicherweise die IKsControl-Schnittstelle verwenden, um auf die Eigenschaften eines Audioadapters zuzugreifen.                                                                                     |
| [Interoperabilität mit Legacy-Audio-APIs](interoperability-with-legacy-audio-apis.md)                                     | Wichtige Features der Kernaudio-APIs in Windows Vista können in vorhandene Anwendungen integriert werden, die DirectSound, DirectShow und die Windows-Multimediafunktionen **waveOutXxx** und **waveInXxx** verwenden. |
| [Raumklang](spatial-sound.md)                                                                                         | Enthält Anleitungen für die Verwendung von Windows Sonic, der Plattformlösung von Microsoft für die Unterstützung räumlicher Sound auf Xbox und Windows, die Audiohinweise sowohl umschließen als auch die Höhe (über oder unterhalb des Listeners) ermöglicht. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kernaudio-APIs](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



