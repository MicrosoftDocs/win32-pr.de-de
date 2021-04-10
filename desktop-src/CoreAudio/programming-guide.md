---
description: Programmierhandbuch
ms.assetid: 825c7cd7-dc66-47b6-a1b6-d10101daebb3
title: Leitfaden zur Kern Audioprogrammierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb99369058983ebac7205053efdf967bbb8c36d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214264"
---
# <a name="core-audio-programming-guide"></a>Leitfaden zur Kern Audioprogrammierung

In diesem Leitfaden werden die Konzepte und Features der Kerncode-APIs von Windows Vista erläutert und beschrieben, wie Sie in der Anwendungsprogrammierung verwendet werden.

In diesem Abschnitt werden die folgenden Themen behandelt:



| Thema                                                                                                                      | BESCHREIBUNG                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Benutzermodusaudiokomponenten](user-mode-audio-components.md)                                                               | Über die Low-Level-Schnittstellen in den kernaudioapis kann ein Client auf die Systemkomponenten zugreifen, die Audiostreams verwalten und mischen.                                                                        |
| [Geschützter benutzermodusaudiodatei (Puma)](protected-user-mode-audio--puma-.md)                                                   | In diesem Thema werden die Aktualisierungen für die Audioverarbeitung (Protected User Mode, Puma) des benutzermodusaudiomoduls in der geschützten Umgebung (PE) beschrieben, das eine sicherere Umgebung für die Audioverarbeitung und das Rendering bereitstellt.              |
| [Audioendpunktgeräte](audio-endpoint-devices.md)                                                                       | Bei einem audioendpunktgerät handelt es sich um eine Software Abstraktion, die benutzerfreundliche Interaktionen mit Audiogeräten wie z. b. Mikrofon und Referenten ermöglicht.                                                              |
| [Audiositzungen](audio-sessions.md)                                                                                       | Eine Audiositzung ist eine Software Abstraktion, die es einem Client ermöglicht, eine Sammlung verwandter Audiostreams als einzelne Einheit zu verwalten.                                                                           |
| [Lautstärkeregler](volume-controls.md)                                                                                     | Das System integriert seine Richtlinien basierten Volumeeinstellungen auf logische und konsistente Weise mit den Volumeeinstellungen des Benutzers.                                                                                      |
| [Datenstrom Verwaltung](stream-management.md)                                                                                 | Die Windows-audiositzungs-API (WASAPI) stellt einen Client mit einem kompletten Satz von Methoden zum Erstellen und Verwalten von Audiodatenströmen bereit.                                                                             |
| [Gerätetopologien](device-topologies.md)                                                                                 | Mit der-API für die Geräte-API kann ein Client die Audiosteuerelemente ermitteln, die sich entlang der verschiedenen Daten Pfade in der Audiohardware befinden.                                                                          |
| [Verwenden der ikscontrol-Schnittstelle für den Zugriff auf Audioeigenschaften](using-the-ikscontrol-interface-to-access-audio-properties.md) | Eine spezialisierte Audioanwendung muss möglicherweise die "ikscontrol"-Schnittstelle verwenden, um auf die Eigenschaften eines audioadapters zuzugreifen.                                                                                     |
| [Interoperabilität mit Legacy-audioapis](interoperability-with-legacy-audio-apis.md)                                     | Die wichtigsten Features der kernaudio-APIs in Windows Vista können in vorhandene Anwendungen integriert werden, die DirectSound, DirectShow und die Windows- **multimediawaveoutxxx** -und **waveinxxx** -Funktionen verwenden. |
| [Raumklang](spatial-sound.md)                                                                                         | Bietet Anleitungen für die Verwendung von Windows Sonic, der Plattform auf Platt Form Ebene von Microsoft für räumliche Audiounterstützung auf Xbox und Windows und ermöglicht sowohl das umschließen als auch das erhöhen (oberhalb oder unterhalb der Listener) Audiohinweise. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kernaudioapis](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



