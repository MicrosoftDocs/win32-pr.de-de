---
title: RAS-Verbindungsvorgänge
description: Windows NT und spätere Versionen stellen die Funktionen RasPhonebookDlg und RasDialDlg bereit, die die integrierte Benutzeroberfläche zum Starten eines RAS-Verbindungsvorgang anzeigen.
ms.assetid: 1e0f82e1-5995-4b47-970b-e6a7ff6d52e0
keywords:
- Verbindungsvorgänge, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27e86ddf1586ce11f43e6b34ef15b89cb2d382b28911968f0b0f08dabd086a86
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868460"
---
# <a name="ras-connection-operations"></a>RAS-Verbindungsvorgänge

Windows NT und spätere Versionen stellen die [**Funktionen RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) und [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) bereit, die die integrierte Benutzeroberfläche zum Starten eines RAS-Verbindungsvorgang anzeigen. Für die meisten Anwendungen ist dies die bevorzugte Methode, um einen RAS-Verbindungsvorgang zu starten. Windows 95 unterstützt diese Funktionen derzeit nicht.

Im weiteren Verlauf dieses Abschnitts werden die Low-Level-Funktionen zum Starten einer RAS-Verbindung beschrieben. Diese Funktionen sind sowohl inWindows NT 4.0 (und höher) als auch Windows 95 verfügbar.

Eine RAS-Clientanwendung verwendet die [**RasDial-Funktion,**](/windows/desktop/api/Ras/nf-ras-rasdiala) um eine Verbindung mit einem RAS-Server herzustellen. Die **RasDial-Funktion** startet den Verbindungsvorgang, der dann vom Remotezugriffsserver Verbindungs-Manager.

Der Remotezugriffsdienst Verbindungs-Manager ein Dienst, der die Details zum Herstellen der Verbindung mit dem Remoteserver verarbeitet. Dieser Dienst stellt dem Client während des Verbindungsvorgang auch Statusinformationen zur Verfügung. Der Remotezugriffsserver Verbindungs-Manager automatisch gestartet, wenn eine Anwendung die RASAPI32.DLL.

Der [**RasDial-Aufruf**](/windows/desktop/api/Ras/nf-ras-rasdiala) gibt die folgenden Informationen an, wenn ein Verbindungsvorgang gestartet wird:

-   Die [Verbindungsinformationen,](phone-book-files-and-connection-information.md) die der Remotezugriffsserver Verbindungs-Manager, um die Verbindung herzustellen.
-   Ein optionaler [Benachrichtigungshandler,](notification-handlers.md) der während des Verbindungsvorgang Statusbenachrichtigungen empfängt. Wenn der [**RasDial-Aufruf**](/windows/desktop/api/Ras/nf-ras-rasdiala) einen Benachrichtigungshandler angibt, ist der Aufruf [asynchron.](asynchronous-operations.md) andernfalls ist es [synchron.](synchronous-operations.md)
-   Eine [**optionale RASDIALEXTENSIONS-Struktur**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) zum Aktivieren oder Deaktivieren von Erweiterungen für den [**RasDial-Vorgang.**](/windows/desktop/api/Ras/nf-ras-rasdiala) Die Erweiterungen ermöglichen es einem RAS-Client, einige Modemeinstellungen direkt zu aktivieren, um zu steuern, [](paused-states.md) ob RAS die Präfixe und Suffixe in einem Telefonbucheintrag verwendet, und um angehaltene Zustände während des Verbindungsbetriebs zu unterstützen.

 

 