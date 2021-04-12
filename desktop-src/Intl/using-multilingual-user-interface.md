---
description: Verwenden der mehrsprachigen Benutzeroberfläche
ms.assetid: caf167ad-f9a8-4093-9581-57bc507d1f6a
title: Verwenden der mehrsprachigen Benutzeroberfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287acc88d144c7775d2125cbb4a055784370d87f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218688"
---
# <a name="using-multilingual-user-interface"></a>Verwenden der mehrsprachigen Benutzeroberfläche

In diesem Abschnitt wird beschrieben, wie Sie Ihre Anwendungen mit der mehrsprachigen Benutzeroberfläche (MUI) entwerfen und implementieren. Im folgenden werden die Aspekte der MUI-Technologie erläutert, die in den meisten Phasen des Anwendungslebenszyklus berücksichtigt werden.

-   Anwendungsentwicklung, einschließlich Ressourcen Vorbereitung, Festlegen von Einstellungen für die Anwendungs Sprache, Auffinden und Laden von Ressourcen
-   Entwickeln und lokalisieren der Anwendung
-   Bereitstellen der Anwendung

Im folgenden finden Sie einige Fragen, die beim Entwerfen und Implementieren einer MUI-Anwendung zu berücksichtigen sind.

-   Welche Versionen von Windows werden von der Anwendung unterstützt?
-   In welchen Sprachen wird die Anwendung lokalisiert?
-   Sollten die Anwendungs Spracheinstellungen immer den Spracheinstellungen für das Betriebssystem entsprechen oder sollte der Anwendungs Benutzer in der Lage sein, bestimmte Sprachen festzulegen?
-   Welche Art von Benutzeroberflächen Ressourcen werden von der Anwendung verwendet, und wo werden Sie gespeichert?

In diesem Abschnitt werden folgende Themen behandelt. Die Beschreibungen nehmen eine MUI-Anwendung an, die auf Windows Vista und höher ausgerichtet ist. Die Ressourcen für diese Anwendung sind Win32-Ressourcen mit sprachspezifischen Ressourcen und ausführbarem Code, der in separaten Win32 PE-Dateien gespeichert ist. Besondere Überlegungen zur Unterstützung von Betriebssystemen vor Windows Vista oder für verschiedene Arten von Ressourcen werden nach Bedarf hinzugefügt.

-   [Vorbereiten von Ressourcen](preparing-resources.md)
-   [Festlegen der Einstellungen für die Anwendungs Sprache](setting-application-language-preferences.md)
-   [Suchen von Win32 PE-Ressourcen](locating-win32-pe-resources.md)
-   [Suchen von nicht-Win32 PE-Ressourcen](locating-non-win32-pe-resources.md)
-   [Lokalisieren von Ressourcen und entwickeln der Anwendung](localizing-resources-and-building-the-application.md)
-   [MUI: System Settings-Anwendungsbeispiel](mui-system-settings-application-sample.md)
-   [Beispiel für MUI: Application-Specific Einstellungen (Windows Vista)](mui-application-specific-settings-sample-vista.md)
-   [Beispiel für MUI: Application-Specific Einstellungen (Pre-Windows Vista)](mui-application-specific-settings-sample-pre-vista.md)

 

 



