---
title: Installieren und Konfigurieren von RPC-Anwendungen
description: Wenn das Microsoft Windows-Betriebssystem auf einem Server oder Client installiert ist, werden die RPC-Laufzeitdateien von Setup automatisch installiert.
ms.assetid: cfcada3d-cf7c-42a9-9ed4-0b1bba7a98cf
keywords:
- Remote Prozedur Aufruf RPC, Tasks, installieren und Konfigurieren von Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90837261c571276a74bb3a5354c7b9a5db2da6cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471757"
---
# <a name="installing-and-configuring-rpc-applications"></a>Installieren und Konfigurieren von RPC-Anwendungen

Wenn das Microsoft Windows-Betriebssystem auf einem Server oder Client installiert ist, werden die RPC-Laufzeitdateien von Setup automatisch installiert. Es ist keine weitere RPC-Installation erforderlich. Sie müssen jedoch sicherstellen, dass die von Ihnen installierte Version von Windows alle Features unterstützt, die in der verteilten Anwendung verwendet werden.

Wenn Sie eine RPC-Anwendung auf einem Windows 3. x-oder Microsoft MS-DOS-Betriebssystem verwenden, müssen Sie die ausführbaren RPC-Laufzeitdateien auf die Windows 3. x-oder MS-DOS-Computer kopieren, die die Anwendung verwenden werden. Das Verzeichnis \\ msetups \\ RPC \_ rt16 auf der Platform Software Development Kit (SDK)-CD enthält ein Datenträger Abbild dieser Dateien zusammen mit einem Setup Programm, um die Dateien zu installieren. Verwenden Sie dieses Datenträger Image zum Erstellen eines Installations Datenträgers für die Verteilung mit der RPC-Anwendung. Sie können auch 16-Bit-Client Anwendungen verwenden, die auf MS-DOS oder Windows auf einem 32-Bit-oder 64-Bit-Windows-Betriebssystem ausgerichtet sind. Allerdings muss das Installationsprogramm Ihrer Anwendung die ausführbaren Dateien installieren, die in diesem Datenträger Image enthalten sind.

Wenn Sie eine RPC-Anwendung für einen Macintosh-Client erstellen, müssen Sie die erforderlichen Dateien zum Zeitpunkt der Erstellung mit der Anwendung verknüpfen. Es ist keine zusätzliche RPC-Installation erforderlich.

Weitere Informationen zu verteilbaren Dateien und Lizenzverträgen finden Sie unter \\ Lizenz \\Redist.txt und \\ Lizenz \\License.txt auf der Plattform-SDK-CD.

Dieser Abschnitt enthält Informationen zum Einrichten von RPC-Anwendungen auf einer Vielzahl von Hardware-und Softwareplattformen. Die Diskussion ist in den folgenden Abschnitten dargestellt:

-   [Konfigurieren des Name Service-Anbieters](configuring-the-name-service-provider.md)
-   [Registrierungsinformationen](registry-information.md)
-   [Verwenden von RPC mit Winsock-Proxy](using-rpc-with-winsock-proxy.md)
-   [SPX/IPX-Installation](spx-ipx-installation.md)
-   [Konfigurieren des Sicherheits Servers](configuring-the-security-server.md)

 

 




