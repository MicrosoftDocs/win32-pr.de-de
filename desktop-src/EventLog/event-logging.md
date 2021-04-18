---
description: Viele Anwendungen erfassen Fehler und Ereignisse in proprietären Fehlerprotokollen, die jeweils über ein eigenes Format und eine eigene Benutzeroberfläche verfügen.
ms.assetid: 5ec95938-ac5d-4f63-9080-2de71454eb17
title: Ereignisprotokollierung (Ereignisprotokollierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d9871fdb7c7b81bdf57a8c5de87a0a09d5a0570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351464"
---
# <a name="event-logging-event-logging"></a>Ereignisprotokollierung (Ereignisprotokollierung)

Viele Anwendungen erfassen Fehler und Ereignisse in proprietären Fehlerprotokollen, die jeweils über ein eigenes Format und eine eigene Benutzeroberfläche verfügen. Daten aus unterschiedlichen Anwendungen können nicht einfach zu einem umfassenden Bericht zusammengeführt werden, sodass Systemadministratoren oder Supportmitarbeiter eine Vielzahl von Quellen überprüfen können, um Probleme zu diagnostizieren.

Die Ereignisprotokollierung stellt eine standardmäßige, zentralisierte Methode für Anwendungen (und das Betriebssystem) zum Aufzeichnen wichtiger Software-und Hardware Ereignisse dar. Der Ereignis Protokollierungs Dienst zeichnet Ereignisse aus verschiedenen Quellen auf und speichert Sie in einer einzelnen Sammlung, die als *Ereignisprotokoll* bezeichnet wird. Der Ereignisanzeige ermöglicht Ihnen das Anzeigen von Protokollen. mithilfe der Programmierschnittstelle können Sie auch Protokolle überprüfen.

-   [Informationen zur Ereignisprotokollierung](about-event-logging.md)
-   [Verwenden der Ereignisprotokollierung](using-event-logging.md)
-   [Referenz zur Ereignisprotokollierung](event-logging-reference.md)

> [!Note]  
> Die Ereignis Protokollierungs-API wurde für Anwendungen entwickelt, die auf dem Betriebssystem Windows Server 2003, Windows XP oder Windows 2000 ausgeführt werden. In Windows Vista wurde die Infrastruktur zur Ereignisprotokollierung umgestaltet. Anwendungen, die für die Betriebssysteme Windows Vista oder höher entwickelt wurden, sollten Ereignisse mit dem [Windows-Ereignisprotokoll](/windows/desktop/WES/windows-event-log) protokollieren.
