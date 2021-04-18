---
description: Typen von com+-Anwendungen
ms.assetid: 4b731f22-6837-4c03-9c8c-a76451369cf1
title: Typen von com+-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fb365863ee2b2fbe41997facdf21d84866af1f6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344611"
---
# <a name="types-of-com-applications"></a>Typen von com+-Anwendungen

Im folgenden sind die vier grundlegenden Typen von com+-Anwendungen aufgeführt:

-   **Server Anwendungen.** Eine com+- *Serveranwendung* wird in einem eigenen Prozess ausgeführt. Server Anwendungen können alle com+-Dienste unterstützen.
-   **Bibliotheksanwendungen.** Eine com+- *Bibliotheks Anwendung* wird im Prozess des Clients ausgeführt, von dem Sie erstellt wird. Genauer gesagt werden die Komponenten in einer Bibliotheks Anwendung immer in den Prozess des Erstellers geladen. Bibliotheksanwendungen sind nicht explizit einem Server Prozess zugeordnet. Sie können rollenbasierte Sicherheit verwenden, aber keinen Remote Zugriff oder in die Warteschlange eingereihten Komponenten unterstützen.
-   **Anwendungs Proxys.** Bei einem *Anwendungs Proxy* handelt es sich um einen Satz von Dateien mit Registrierungsinformationen, die einem Client den Remote Zugriff auf eine Serveranwendung ermöglichen. Wenn die Anwendung auf einem Client Computer ausgeführt wird, werden Informationen über die COM+-Serveranwendung, einschließlich CLSIDs, ProgIDs, Remoteservername und Marshallinginformationen, auf den Client Computer geschrieben. Auf die Serveranwendung kann dann vom Client Computer aus Remote zugegriffen werden.
-   **Vorinstallierte com+-Anwendungen**. Com+ umfasst eine Reihe von vorinstallierten Anwendungen, die interne Funktionen verarbeiten. Die vorinstallierten Anwendungen sind im Ordner "com+-Anwendungen" im Verwaltungs Programm "Komponenten Dienste" aufgeführt, können jedoch nicht geändert oder gelöscht werden. Zu diesen Anwendungen zählen die folgenden:
    -   .Net-Hilfsprogramme
    -   Analysesteuerelement-Verleger Anwendung
    -   Com+-Explorer
    -   Anqueue-Listener für com+-QC
    -   Com+-Hilfsprogramme
    -   IIS-In-Process Anwendungen
    -   In einem Pool zusammengefasste IIS-Anwendungen
    -   System Anwendung

## <a name="notes"></a>Notizen

Ab Windows Server 2003 ist es möglich, com+-Anwendungen auszuführen, auch wenn die System Anwendung deaktiviert ist. Die com+-Anwendungen werden jedoch ohne die Dienste, die normalerweise von der System Anwendung bereitgestellt werden, ausgeführt. Diese Dienste umfassen die Verwendung des Verwaltungs Programms Komponenten Dienste und der System Ereignis Verfolgung.

Ebenso wie Windows Server 2003 enthält die Authentifizierungsfunktion für die com+-System Anwendung den Wert eoac- \_ deaktivierte \_ AAA. Dieser Wert, der Aktivierungen von Aktivierungen durch aktivierte Aktivierungen deaktiviert, wird zusammen mit der [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) -Funktion verwendet, wenn die System Anwendung gestartet wird. Wenn Sie die Authentifizierungsfunktion auf eoac \_ deaktivieren, \_ kann eine Anwendung, die unter einem privilegierten Konto (z. b. LocalSystem) ausgeführt wird, verhindern, dass Ihre Identität verwendet wird, um nicht vertrauenswürdige Komponenten zu starten.

 

 
