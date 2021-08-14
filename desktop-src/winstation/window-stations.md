---
title: Fensterstationen
description: Eine Fensterstation enthält eine Zwischenablage, eine Atomtabelle und mindestens ein Desktopobjekt. Jedes Fensterstationsobjekt ist ein sicherungsfähiges Objekt. Wenn eine Fensterstation erstellt wird, wird sie dem aufrufenden Prozess zugeordnet und der aktuellen Sitzung zugewiesen.
ms.assetid: 617661e2-3b0d-42a9-9769-2ba0957c31a8
keywords:
- Fensterstationsobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d55e43a0db21b23a6704949f0d72a184c9034f625689b800814ac8a93891b7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199691"
---
# <a name="window-stations"></a>Fensterstationen

Eine *Fensterstation* enthält eine Zwischenablage, eine Atomtabelle und mindestens ein [Desktopobjekt.](desktops.md) Jedes Fensterstationsobjekt ist ein sicherungsfähiges Objekt. Wenn eine Fensterstation erstellt wird, wird sie dem aufrufenden Prozess zugeordnet und der aktuellen Sitzung zugewiesen.

Die *interaktive Fensterstation* ist die einzige Fensterstation, die eine Benutzeroberfläche anzeigen oder Benutzereingaben empfangen kann. Sie wird der Anmeldesitzung des interaktiven Benutzers zugewiesen und enthält die Tastatur, die Maus und das Anzeigegerät. Sie hat immer den Namen "WinSta0". Alle anderen Fensterstationen sind nicht interaktiv, was bedeutet, dass sie keine Benutzeroberfläche anzeigen oder Benutzereingaben empfangen können.

Wenn sich ein Benutzer mithilfe von Remotedesktopdienste bei einem Computer anmeldet, wird eine Sitzung für den Benutzer gestartet. Jede Sitzung ist einer eigenen interaktiven Fensterstation namens "WinSta0" zugeordnet. Weitere Informationen finden Sie unter [Remotedesktop Sitzungen.](/windows/desktop/TermServ/terminal-services-sessions)

Weitere Informationen zu Fensterstationen finden Sie in den folgenden Themen:

-   [Window Station and Desktop Creation](window-station-and-desktop-creation.md)
-   [Verarbeiten der Verbindung mit einer Fensterstation](process-connection-to-a-window-station.md)
-   [Sicherheit und Zugriffsrechte für Window Station](window-station-security-and-access-rights.md)

 

 