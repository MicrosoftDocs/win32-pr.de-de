---
title: RAS-Verbindungs Vorgänge
description: Windows NT und höhere Versionen stellen die rasphonebookdlg-und RasDialDlg-Funktionen bereit, die die integrierte Benutzeroberfläche zum Starten eines RAS-Verbindungs Vorgangs anzeigen.
ms.assetid: 1e0f82e1-5995-4b47-970b-e6a7ff6d52e0
keywords:
- Verbindungs Vorgänge, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e2a78d34afd5aea3670730656e97886b6a5916
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858362"
---
# <a name="ras-connection-operations"></a>RAS-Verbindungs Vorgänge

Windows NT und höhere Versionen stellen die [**rasphonebookdlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) -und [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) -Funktionen bereit, die die integrierte Benutzeroberfläche zum Starten eines RAS-Verbindungs Vorgangs anzeigen. Bei den meisten Anwendungen ist dies die bevorzugte Methode zum Starten eines RAS-Verbindungs Vorgangs. Windows 95 unterstützt diese Funktionen zurzeit nicht.

Im restlichen Teil dieses Abschnitts werden die Funktionen auf niedriger Ebene für das Starten einer RAS-Verbindung beschrieben. Diese Funktionen sind unter bothwindows NT 4,0 (und höheren Versionen) und Windows 95 verfügbar.

Eine RAS-Client Anwendung verwendet die Funktion " [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) ", um eine Verbindung mit einem RAS-Server herzustellen. Die Funktion " **rasdial** " startet den Verbindungsvorgang, der dann vom RAS-Verbindungs-Manager ausgeführt wird.

Der RAS-Verbindungs-Manager ist ein Dienst, der die Details zum Herstellen der Verbindung mit dem Remote Server behandelt. Dieser Dienst stellt dem Client auch während des Verbindungs Vorgangs Statusinformationen zur Verfügung. Der RAS-Verbindungs-Manager wird automatisch gestartet, wenn eine Anwendung die RASAPI32.DLL lädt.

Der Befehl " [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) " gibt die folgenden Informationen an, wenn ein Verbindungsvorgang gestartet wird:

-   Die [Verbindungsinformationen](phone-book-files-and-connection-information.md) , die der RAS-Verbindungs-Manager benötigt, um die Verbindung herzustellen.
-   Ein optionaler [Benachrichtigungs Handler](notification-handlers.md) , der während des Verbindungs Vorgangs Status Benachrichtigungen empfängt. Wenn der Befehl " [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) " einen Benachrichtigungs Handler angibt, ist der-Befehl [asynchron](asynchronous-operations.md). Andernfalls ist es [synchron](synchronous-operations.md).
-   Eine optionale " [**rasdialextensions**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) "-Struktur zum Aktivieren oder Deaktivieren von Erweiterungen für den [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) -Vorgang. Mithilfe der Erweiterungen kann ein RAS-Client einige Modem Einstellungen direkt aktivieren, um zu steuern, ob RAS die Präfixe und Suffixe in einem Telefonbucheintrag verwendet, und um [angehaltene Zustände](paused-states.md) während des Verbindungs Vorgangs zu unterstützen.

 

 