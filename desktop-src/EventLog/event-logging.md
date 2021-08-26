---
description: Viele Anwendungen zeichnen Fehler und Ereignisse in proprietären Fehlerprotokollen auf, die jeweils über ein eigenes Format und eine eigene Benutzeroberfläche verfügen.
ms.assetid: 5ec95938-ac5d-4f63-9080-2de71454eb17
title: Ereignisprotokollierung (Ereignisprotokollierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8894c7a6d038efdc317611ca6284f62d99c82ebc767b6f96f83931803a887185
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927840"
---
# <a name="event-logging-event-logging"></a>Ereignisprotokollierung (Ereignisprotokollierung)

Viele Anwendungen zeichnen Fehler und Ereignisse in proprietären Fehlerprotokollen auf, die jeweils über ein eigenes Format und eine eigene Benutzeroberfläche verfügen. Daten aus verschiedenen Anwendungen können nicht einfach in einem vollständigen Bericht zusammengeführt werden, sodass Systemadministratoren oder Supportmitarbeiter eine Vielzahl von Quellen überprüfen müssen, um Probleme zu diagnostizieren.

Die Ereignisprotokollierung bietet eine standardmäßige, zentralisierte Möglichkeit für Anwendungen (und das Betriebssystem), wichtige Software- und Hardwareereignisse aufzuzeichnen. Der Ereignisprotokollierungsdienst zeichnet Ereignisse aus verschiedenen Quellen auf und speichert sie in einer einzelnen Sammlung, die als *Ereignisprotokoll* bezeichnet wird. Mit dem Ereignisanzeige können Sie Protokolle anzeigen. Mit der Programmierschnittstelle können Sie auch Protokolle untersuchen.

-   [Informationen zur Ereignisprotokollierung](about-event-logging.md)
-   [Verwenden der Ereignisprotokollierung](using-event-logging.md)
-   [Ereignisprotokollierungsreferenz](event-logging-reference.md)

> [!Note]  
> Die Ereignisprotokollierungs-API wurde für Anwendungen entwickelt, die unter dem Betriebssystem Windows Server 2003, Windows XP oder Windows 2000 ausgeführt werden. In Windows Vista wurde die Infrastruktur für die Ereignisprotokollierung neu gestaltet. Anwendungen, die auf Windows Vista oder höher ausgeführt werden sollen, sollten [Windows Ereignisprotokoll](/windows/desktop/WES/windows-event-log) verwenden, um Ereignisse zu protokollieren.
