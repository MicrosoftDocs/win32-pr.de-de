---
description: Wenn ein Fehler auftritt, muss der Systemadministrator oder Supportmitarbeiter ermitteln, was den Fehler verursacht hat, versuchen, verlorene Daten wiederhergestellt zu haben, und verhindern, dass sich der Fehler wiederholt.
ms.assetid: 2a625c8a-afa2-484a-a0e3-df3ef774abe4
title: Informationen zur Ereignisprotokollierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d9f30e4f8a44594b95215d748ac5cafda6b0633eefa668d0d864362c8f3c5de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814257"
---
# <a name="about-event-logging"></a>Informationen zur Ereignisprotokollierung

Wenn ein Fehler auftritt, muss der Systemadministrator oder Supportmitarbeiter ermitteln, was den Fehler verursacht hat, versuchen, verlorene Daten wiederhergestellt zu haben, und verhindern, dass sich der Fehler wiederholt. Es ist hilfreich, wenn Anwendungen, das Betriebssystem und andere Systemdienste wichtige Ereignisse aufzeichnen, z. B. Bedingungen mit geringem Arbeitsspeicher oder übermäßige Versuche, auf einen Datenträger zu zugreifen. Der Systemadministrator kann dann das Ereignisprotokoll verwenden, um zu bestimmen, welche Bedingungen den Fehler verursacht haben, und den Kontext zu identifizieren, in dem er aufgetreten ist. Durch regelmäßiges Anzeigen des Ereignisprotokolls kann der Systemadministrator möglicherweise Probleme (z. B. eine fehlerhafte Festplatte) identifizieren, bevor sie schaden.

> [!Note]  
> Die Ereignisprotokollierungs-API wurde für Anwendungen entwickelt, die unter dem Betriebssystem Windows Server 2003, Windows XP oder Windows 2000 ausgeführt werden. In Windows Vista wurde die Ereignisprotokollierungsinfrastruktur neu gestaltet. Anwendungen, die für die Ausführung unter den Betriebssystemen Windows Vista oder höher entwickelt wurden, sollten jetzt Windows [Ereignisprotokoll](/windows/desktop/WES/windows-event-log) verwenden, um Ereignisse zu protokollieren.

 
In diesem Abschnitt wird die Programmierschnittstelle zum Schreiben und Nutzen von Ereignissen mithilfe der Ereignisprotokollierung erläutert.

-   [Ereignistypen](event-types.md)
-   [Protokollierungsrichtlinien](logging-guidelines.md)
-   [Ereignisprotokollierungselemente](event-logging-elements.md)
-   [Ereignisprotokollierungsvorgänge](event-logging-operations.md)
-   [Ereignisprotokollierungsmodell](event-logging-model.md)
-   [Sicherheit der Ereignisprotokollierung](event-logging-security.md)

> [!Note]  
> Anwendungen, die Ereignisse mit einer Größe von mehr als 64 KB auf einem computer mit Windows Server 2003, Windows XP oder Windows 2000 veröffentlichen, können keine Ereignisse auf einem Computer mit Windows Vista oder höher veröffentlichen.
