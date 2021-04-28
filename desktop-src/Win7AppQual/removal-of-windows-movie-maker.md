---
description: Entfernen von Windows-Movie Maker
ms.assetid: af55e570-0f24-4376-905a-3b879d5f3a1c
title: Entfernen von Windows-Movie Maker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36df5ffe4498e05de9fcbbaadf49f8fc32c91b0f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116268"
---
# <a name="removal-of-windows-movie-maker"></a>Entfernen von Windows-Movie Maker

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** – Windows 7  
**Server** – Windows Server 2008 R2  









## <a name="feature-impact"></a>Auswirkungen auf Features

 **Schweregrad –** Hoch  
**Häufigkeit** – Mittel  


## <a name="description"></a>BESCHREIBUNG

Microsoft ist veraltet und entfernt das Hilfsprogramm Windows Movie Maker. Dies schließt Folgendes ein:

-   Alle Einstiegspunkte zu Windows Movie Maker (z. B. Startmenü, Start > Ausführen)
-   Alle Binärdateien, die von Windows Movie Maker verwendet wurden (alles, was sich in %ProgramFiles% \\ Movie Maker befand)

Die Movie Maker Projektdateien eines Benutzers verbleiben jedoch auf dem System und sind für andere Anwendungen zugänglich, die dieses Dateiformat unterstützen.

## <a name="manifestation"></a>Manifestation

Das Entfernen von Windows Movie Maker führt zu folgendem Ergebnis:

-   Jeder Versuch, Windows Movie Maker mit den Befehlszeilenargumenten zu starten, schlägt fehl.
-   Alle Plug-Ins, die installiert wurden, um neue Transformationen und Animationen zu aktivieren, bleiben installiert, werden jedoch nicht für den Endbenutzer verfügbar gemacht.

## <a name="solution"></a>Lösung

Um in Zukunft über eine solche Funktionalität zu verfügen, muss ein Benutzer eine ähnliche Anwendung von Microsoft oder einem anderen Softwareanbieter installieren.

 

 



