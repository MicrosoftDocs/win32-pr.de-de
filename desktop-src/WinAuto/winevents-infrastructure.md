---
title: WinEvents-Infrastruktur
description: Das Microsoft Windows-Betriebssystem enthält eine Funktion mit dem Namen "WinEvents", mit der Prozesse und Anwendungen, die auf dem Windows-Desktop ausgeführt werden, bestimmte Arten von Informationen austauschen können.
ms.assetid: ba97b00b-4a4c-4889-ae9c-8e92eb742849
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8846582a6d18f304cc08e3cb13ddb444cb278d7
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "103720015"
---
# <a name="winevents"></a>WinEvents

Das Microsoft Windows-Betriebssystem enthält eine Funktion mit dem Namen " *WinEvents*", mit der Prozesse und Anwendungen, die auf dem Windows-Desktop ausgeführt werden, bestimmte Arten von Informationen austauschen können. Barrierefreiheits Tools, die Microsoft UI Automation und Microsoft Active Accessibility verwenden, gehören zu den Haupt Benutzern der WinEvents.

Im Kontext der Barrierefreiheit verwenden Benutzeroberflächenautomatisierungs-Anbieter und Microsoft Active Accessibility-Server WinEvents, um Clients über Änderungen in der Benutzeroberfläche einer Anwendung zu benachrichtigen, z. b. Wenn ein Benutzeroberflächen Element erstellt oder zerstört wurde oder wenn sich Elementname,-Zustand oder-Wert geändert hat.

Dieser Abschnitt enthält Vorschläge, Richtlinien und Beispiele zum unterstützen von Clients bei der Handhabung von WinEvents und zur Unterstützung von Servern, die das entsprechende WinEvent-Ereignis auslöst.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Was sind WinEvents?](what-are-winevents.md)
-   [Registrieren einer Hook-Funktion](registering-a-hook-function.md)
-   [Ereignisse auf System Ebene und Object-Level](system-level-and-object-level-events.md)
-   [Kontext-und Out-of-Context-Hook-Funktionen](in-context-and-out-of-context-hook-functions.md)
-   [Schutz vor erneuten eintreten in Hook-Funktionen](guarding-against-reentrancy-in-hook-functions.md)
-   [Zuordnung von WinEvent-IDs](allocation-of-winevent-ids.md)

Eine Übersicht über den Ereignis Benachrichtigungs Prozess in Microsoft Active Accessibility finden Sie unter [WinEvents](winevents-overview.md) in der [technischen Übersicht](technical-overview.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Allgemeine Infrastruktur](common-infrastructure.md)
</dt> </dl>

 

 




