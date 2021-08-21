---
description: Typen von COM+-Anwendungen
ms.assetid: 4b731f22-6837-4c03-9c8c-a76451369cf1
title: Typen von COM+-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13bf55f7c2f25c490f0806a7924d32c6cbf981e79b8461ba12fc0f95964691c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499670"
---
# <a name="types-of-com-applications"></a>Typen von COM+-Anwendungen

Es folgen die vier grundlegenden Typen von COM+-Anwendungen:

-   **Serveranwendungen.** Eine *COM+-Serveranwendung* wird in einem eigenen Prozess ausgeführt. Serveranwendungen können alle COM+-Dienste unterstützen.
-   **Bibliotheksanwendungen.** Eine *COM+-Bibliotheksanwendung* wird im Prozess des Clients ausgeführt, der sie erstellt. Genauer gesagt werden die Komponenten in einer Bibliotheksanwendung immer in den Prozess des Erstellers geladen. Bibliotheksanwendungen sind nicht explizit einem Serverprozess zugeordnet. Sie können rollenbasierte Sicherheit verwenden, unterstützen jedoch keinen Remotezugriff oder Komponenten in der Warteschlange.
-   **Anwendungsproxys.** Ein *Anwendungsproxy* ist ein Satz von Dateien, die Registrierungsinformationen enthalten, mit denen ein Client remote auf eine Serveranwendung zugreifen kann. Wenn sie auf einem Clientcomputer ausgeführt wird, schreibt eine Anwendungsproxydatei Informationen zur COM+-Serveranwendung, einschließlich CLSIDs, ProgIDs, RemoteServerName und Marshallinginformationen, auf den Clientcomputer. Der Remotezugriff auf die Serveranwendung ist dann über den Clientcomputer möglich.
-   **VORinstallierte COM+-Anwendungen**. COM+ enthält eine Reihe von vorinstallierten Anwendungen, die interne Funktionen verarbeiten. Die vorinstallierten Anwendungen werden im Ordner COM+-Anwendungen im Verwaltungstool Komponentendienste aufgeführt, können jedoch nicht geändert oder gelöscht werden. Diese Anwendungen umfassen Folgendes:
    -   .NET-Hilfsprogramme
    -   Analyzer-Steuerelement Publisher Anwendung
    -   COM+-Explorer
    -   COM+ QC Dead Letter Queue Listener
    -   COM+-Hilfsprogramme
    -   IIS In-Process-Anwendungen
    -   Out-of-Process-Poolanwendungen für IIS
    -   Systemanwendung

## <a name="notes"></a>Hinweise

Ab Windows Server 2003 ist es möglich, COM+-Anwendungen auszuführen, auch wenn die Systemanwendung deaktiviert ist. Die COM+-Anwendungen werden ausgeführt, jedoch ohne die Dienste, die normalerweise von der Systemanwendung bereitgestellt werden. Zu diesen Diensten gehören die Verwendung des Verwaltungstools "Komponentendienste" und die Nachverfolgung von Systemereignissen.

Ab Windows Server 2003 enthält die Authentifizierungsfunktion für die COM+-Systemanwendung auch den Wert EOAC \_ DISABLE \_ AAA. Dieser Wert, der AKTIVIERUNGSAKTIVATOR-Aktivierungen (AAA) deaktiviert, wird beim Starten der Systemanwendung mit der [**CoInitializeSecurity-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) verwendet. Wenn Sie die Authentifizierungsfunktion auf EOAC \_ DISABLE \_ AAA festlegen, kann eine Anwendung, die unter einem privilegierten Konto (z. B. LocalSystem) ausgeführt wird, verhindern, dass ihre Identität zum Starten nicht vertrauenswürdiger Komponenten verwendet wird.

 

 
