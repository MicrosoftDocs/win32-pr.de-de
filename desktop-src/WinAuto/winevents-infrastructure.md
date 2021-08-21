---
title: WinEvents-Infrastruktur
description: Das Microsoft Windows Betriebssystem enthält ein Feature namens WinEvents, mit dem Prozesse und Anwendungen, die auf dem Windows Desktop ausgeführt werden, bestimmte Arten von Informationen austauschen können.
ms.assetid: ba97b00b-4a4c-4889-ae9c-8e92eb742849
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8662cdcbfa9546ce04dc787e7089f68ba1c03137c41067c20792f7da111cf2a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563285"
---
# <a name="winevents"></a>WinEvents

Das Microsoft Windows Betriebssystem enthält ein Feature namens *WinEvents,* mit dem Prozesse und Anwendungen, die auf dem Windows Desktop ausgeführt werden, bestimmte Arten von Informationen austauschen können. Barrierefreiheitstools, die Microsoft Benutzeroberflächenautomatisierung und Microsoft Active Accessibility verwenden, gehören zu den primären Benutzern von WinEvents.

Im Kontext der Barrierefreiheit verwenden Benutzeroberflächenautomatisierung-Anbieter und Microsoft Active Accessibility-Server WinEvents, um Clients über Änderungen in einer Anwendungsoberfläche zu informieren, z. B. wenn ein Benutzeroberflächenelement erstellt oder zerstört wurde oder wenn sich ein Elementname, -zustand oder -wert geändert hat.

Dieser Abschnitt enthält Vorschläge, Richtlinien und Beispiele, um Clients bei der Verarbeitung von WinEvents zu unterstützen und Servern zu helfen, zu bestimmen, wann das entsprechende WinEvent ausgelöst werden soll.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Was sind WinEvents?](what-are-winevents.md)
-   [Registrieren einer Hookfunktion](registering-a-hook-function.md)
-   [Ereignisse auf Systemebene und Object-Level](system-level-and-object-level-events.md)
-   [In-Context- und Out-of-Context Hook-Funktionen](in-context-and-out-of-context-hook-functions.md)
-   [Schutz vor Wiederinvarianz in Hookfunktionen](guarding-against-reentrancy-in-hook-functions.md)
-   [Zuordnung von WinEvent-IDs](allocation-of-winevent-ids.md)

Eine Übersicht über den Ereignisbenachrichtigungsprozess in Microsoft Active Accessibility finden Sie unter [WinEvents](winevents-overview.md) in der [technischen Übersicht.](technical-overview.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Allgemeine Infrastruktur](common-infrastructure.md)
</dt> </dl>

 

 




