---
title: Installieren und Konfigurieren von RPC-Anwendungen
description: Wenn das Microsoft Windows-Betriebssystem auf einem Server oder Client installiert ist, installiert Setup automatisch die RPC-Laufzeitdateien.
ms.assetid: cfcada3d-cf7c-42a9-9ed4-0b1bba7a98cf
keywords:
- Remoteprozeduraufruf-RPC, Aufgaben, Installieren und Konfigurieren von Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf5cf5d408e2b23042074031ce0307b3a13cf3461df31cc39899b0315f99e8c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020440"
---
# <a name="installing-and-configuring-rpc-applications"></a>Installieren und Konfigurieren von RPC-Anwendungen

Wenn das Microsoft Windows-Betriebssystem auf einem Server oder Client installiert ist, installiert Setup automatisch die RPC-Laufzeitdateien. Es ist keine weitere RPC-Installation erforderlich. Sie müssen jedoch sicherstellen, dass die Version von Windows, die Sie installieren, alle Funktionen unterstützt, die in Ihrer verteilten Anwendung verwendet werden.

Wenn Sie eine RPC-Anwendung auf einem Windows 3.x- oder Microsoft MS-DOS-Betriebssystem verwenden, müssen Sie die ausführbaren RPC-Laufzeitdateien auf die Windows 3.x- oder MS-DOS-Computer kopieren, die die Anwendung verwenden. Das Verzeichnis mstools rpc rt16 auf der CD des \\ Platform Software Development Kit \\ (SDK) enthält ein Datenträgerimage dieser Dateien sowie ein Setupprogramm zum Installieren \_ der Dateien. Verwenden Sie dieses Datenträgerimage, um einen Installationsdatenträger für die Verteilung mit Ihrer RPC-Anwendung zu erstellen. Sie können auch 16-Bit-Clientanwendungen für MS-DOS oder Windows auf einem 32-Bit-/64-Bit-Betriebssystem Windows verwenden. Das Installationsprogramm Ihrer Anwendung muss jedoch die ausführbaren Dateien installieren, die in diesem Datenträgerimage enthalten sind.

Wenn Sie eine RPC-Anwendung für einen Macintosh-Client erstellen, müssen Sie die erforderlichen Dateien zur Buildzeit mit der Anwendung verknüpfen. Es ist keine zusätzliche RPC-Installation erforderlich.

Weitere Informationen zu weiterverteilten Dateien und Lizenzverträgen finden Sie unter LIZENZ-Redist.txt und LIZENZLicense.txt \\ \\ auf der \\ \\ Plattform-SDK-CD.

Dieser Abschnitt enthält Informationen zum Einrichten von RPC-Anwendungen auf einer Vielzahl von Hardware- und Softwareplattformen. Die Diskussion wird in den folgenden Abschnitten erläutert:

-   [Konfigurieren des Namensdienstanbieters](configuring-the-name-service-provider.md)
-   [Registrierungsinformationen](registry-information.md)
-   [Verwenden von RPC mit Winsock-Proxy](using-rpc-with-winsock-proxy.md)
-   [SPX/IPX-Installation](spx-ipx-installation.md)
-   [Konfigurieren des Sicherheitsservers](configuring-the-security-server.md)

 

 




