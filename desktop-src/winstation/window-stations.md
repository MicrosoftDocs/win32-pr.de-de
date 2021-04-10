---
title: Fenster Stationen
description: Eine Fenster Station enthält eine Zwischenablage, eine Atom-Tabelle und ein oder mehrere Desktop Objekte. Jedes Fenster Station-Objekt ist ein Sicherungs fähiges Objekt. Wenn eine Fenster Station erstellt wird, wird Sie mit dem aufrufenden Prozess verknüpft und der aktuellen Sitzung zugewiesen.
ms.assetid: 617661e2-3b0d-42a9-9769-2ba0957c31a8
keywords:
- Fenster Station-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee2048015e4b0c687932c4d01aafe31127e2141e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039162"
---
# <a name="window-stations"></a>Fenster Stationen

Eine *Fenster Station* enthält eine Zwischenablage, eine Atom-Tabelle und ein oder mehrere [Desktop](desktops.md) Objekte. Jedes Fenster Station-Objekt ist ein Sicherungs fähiges Objekt. Wenn eine Fenster Station erstellt wird, wird Sie mit dem aufrufenden Prozess verknüpft und der aktuellen Sitzung zugewiesen.

Die *interaktive Fenster Station* ist die einzige Fenster Station, auf der eine Benutzeroberfläche angezeigt oder Benutzereingaben empfangen werden können. Sie wird der Anmelde Sitzung des interaktiven Benutzers zugewiesen und enthält das Tastatur-, Maus-und Anzeigegerät. Der Name lautet immer "WinSta0". Alle anderen Fenster Stationen sind nicht interaktiv, was bedeutet, dass Sie keine Benutzeroberfläche anzeigen oder Benutzereingaben empfangen können.

Wenn sich ein Benutzer über Remotedesktopdienste an einem Computer anmeldet, wird eine Sitzung für den Benutzer gestartet. Jede Sitzung ist mit der eigenen interaktiven Fenster Station namens "WinSta0" verknüpft. Weitere Informationen finden Sie unter [Remotedesktop-Sitzungen](/windows/desktop/TermServ/terminal-services-sessions).

Weitere Informationen zu Fenster Stationen finden Sie in den folgenden Themen:

-   [Fenster Station und Desktop Erstellung](window-station-and-desktop-creation.md)
-   [Verarbeiten der Verbindung mit einer Fenster Station](process-connection-to-a-window-station.md)
-   [Sicherheit und Zugriffsrechte für die Fenster Station](window-station-security-and-access-rights.md)

 

 