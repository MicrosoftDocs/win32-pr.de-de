---
description: Wenn ein Fehler auftritt, muss der Systemadministrator oder der Supportmitarbeiter feststellen, was den Fehler verursacht hat. es muss versucht werden, verlorene Daten wiederherzustellen und den Fehler zu verhindern.
ms.assetid: 2a625c8a-afa2-484a-a0e3-df3ef774abe4
title: Informationen zur Ereignisprotokollierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1104a4b54d2989cb329b665e20fd273766e57209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041843"
---
# <a name="about-event-logging"></a>Informationen zur Ereignisprotokollierung

Wenn ein Fehler auftritt, muss der Systemadministrator oder der Supportmitarbeiter feststellen, was den Fehler verursacht hat. es muss versucht werden, verlorene Daten wiederherzustellen und den Fehler zu verhindern. Es ist hilfreich, wenn Anwendungen, das Betriebssystem und andere Systemdienste wichtige Ereignisse aufzeichnen, z. b. Bedingungen mit geringem Arbeitsspeicher oder übermäßig viele Zugriffsversuche auf einen Datenträger. Der Systemadministrator kann dann das Ereignisprotokoll verwenden, um zu bestimmen, welche Bedingungen den Fehler verursacht haben, und den Kontext zu identifizieren, in dem er aufgetreten ist. Wenn Sie das Ereignisprotokoll in regelmäßigen Abständen anzeigen, kann der Systemadministrator möglicherweise Probleme erkennen (z. b. eine fehlerhafte Festplatte), bevor diese Schaden anrichten.

> [!Note]  
> Die Ereignis Protokollierungs-API wurde für Anwendungen entwickelt, die auf dem Betriebssystem Windows Server 2003, Windows XP oder Windows 2000 ausgeführt werden. In Windows Vista wurde die Infrastruktur zur Ereignisprotokollierung umgestaltet. Anwendungen, die für die Betriebssysteme Windows Vista oder höher entwickelt wurden, sollten jetzt das [Windows-Ereignisprotokoll](/windows/desktop/WES/windows-event-log) verwenden, um Ereignisse zu protokollieren.

 
In diesem Abschnitt wird die Programmierschnittstelle zum Schreiben und Verarbeiten von Ereignissen mithilfe der Ereignisprotokollierung erläutert.

-   [Ereignistypen](event-types.md)
-   [Protokollierungs Richtlinien](logging-guidelines.md)
-   [Ereignis Protokollierungs Elemente](event-logging-elements.md)
-   [Ereignis Protokollierungs Vorgänge](event-logging-operations.md)
-   [Ereignis Protokollierungs Modell](event-logging-model.md)
-   [Sicherheit der Ereignisprotokollierung](event-logging-security.md)

> [!Note]  
> Anwendungen, die Ereignisse veröffentlichen, die auf einem Computer mit Windows Server 2003, Windows XP oder Windows 2000 mehr als 64 Kilobyte haben, können Ereignisse auf Computern mit Windows Vista oder höher nicht veröffentlichen.
