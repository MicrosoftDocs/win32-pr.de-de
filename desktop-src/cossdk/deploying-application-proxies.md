---
description: Für den Remotezugriff auf eine COM+-Serveranwendung von einem anderen (Client-)Computer aus muss auf dem Clientcomputer eine Teilmenge der Attribute der Serveranwendung installiert sein, einschließlich Proxy-/Stub-DLLs und Typbibliotheken für DCOM-/QC-Schnittstellenremoting.
ms.assetid: 293b424c-4cd4-43a9-9b56-687c753a34f2
title: Bereitstellen von Anwendungsproxys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e651338e4bd89cb4fe5cb77789e5e10392f62e065da0f61ec4ea19f7cca312b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547989"
---
# <a name="deploying-application-proxies"></a>Bereitstellen von Anwendungsproxys

Für den Remotezugriff auf eine COM+-Serveranwendung von einem anderen (Client-)Computer aus muss auf dem Clientcomputer eine Teilmenge der Attribute der Serveranwendung installiert sein, einschließlich Proxy-/Stub-DLLs und Typbibliotheken für DCOM-/QC-Schnittstellenremoting. Diese Teilmenge wird als *Anwendungsproxy* bezeichnet.

Über das Verwaltungstool Komponentendienste können Sie ganz einfach eine COM+-Serveranwendung als Anwendungsproxy exportieren. Damit COM+ einen Anwendungsproxy generieren kann, ist es wichtig, dass alle Komponenten in der Serveranwendung installiert und nicht importiert wurden. (Weitere Informationen zu diesem Unterschied finden Sie unter [Importieren von Komponenten](importing-components.md).) Dadurch wird sichergestellt, dass die Anwendung alle erforderlichen Registrierungsinformationen enthält.

> [!Note]  
> Es wird empfohlen, die Schnittstellendefinitionen von den Klassenimplementierungen zu trennen. Andernfalls enthält der Im COM+-Anwendungsproxy enthaltene Satz von DLLs oder Typbibliotheken tatsächlichen Servercode.

 

Anwendungsproxys, die von COM+ generiert werden, sind Windows Installationspakete des Installationsprogramms. Nach der Installation werden die Anwendungsproxys in der Systemsteuerung Software des Clientcomputers angezeigt (es sei denn, die .msi Datei wird mit einem Windows Installer-Erstellungstool geändert).

## <a name="remote-access-via-application-proxies"></a>Remotezugriff über Anwendungsproxys

Beim Generieren eines Anwendungsproxys stellt COM+ automatisch die folgenden Informationen bereit, die erforderlich sind, damit der Anwendungsproxy remote auf eine COM+-Serveranwendung zugreifen kann:

-   Klassenidentitätsinformationen (CLSIDs und ProgIDs). Ein Anwendungsproxy unterstützt bis zu zwei ProgIDs.
-   Anwendungsidentität und Beziehung von Klassen zu Anwendungen (AppID).
-   Standortinformationen pro Anwendung (Remoteservername).
-   Marshallen von Informationen für alle Schnittstellen, die von der Anwendung verfügbar gemacht werden (z. B. Typbibliotheken und Proxys/Stubs).
-   MSMQ-Warteschlangennamen und -Bezeichner (wenn der Dienst mit den komponenten in der Warteschlange für die Anwendung aktiviert ist).
-   Klassen-, Schnittstellen- und Methodenattribute ohne Rolleninformationen.
-   Anwendungsattribute.

## <a name="installing-application-proxies-on-other-operating-systems"></a>Installieren von Anwendungsproxys unter anderen Betriebssystemen

Im Gegensatz zu COM+-Serveranwendungen können Anwendungsproxys auf jedem Betriebssystem installiert werden, das DCOM (und Windows Installer) unterstützt. Auf Computern, auf denen COM+ nicht ausgeführt wird, wird nur die Teilmenge der Informationen installiert, die für DCOM-Remoting erforderlich sind. Diese Informationen werden in der Windows-Registrierung installiert (mit den Schlüsseln HKEY \_ CLASSES \_ ROOT, APPID/CLSID).

> [!Note]  
> Wenn Sie einen Anwendungsproxy (.msi-Datei) auf Computern installieren, auf denen COM+ nicht ausgeführt wird, muss Windows Installer auf diesen Computern ausgeführt werden. Es wird empfohlen, dass Entwickler die verteilbare Windows Installer-Datei (instmsi.exe) zusammen mit der .msi-Datei ihrer Anwendung versenden. Dadurch wird sichergestellt, dass Systemadministratoren Windows Installer zur Verfügung haben, wenn Anwendungsproxys auf Clients bereitgestellt werden, auf denen COM+ nicht ausgeführt wird.

 

Auf Computern, auf denen COM+ ausgeführt wird, werden die Anwendungsproxyinformationen im COM+-Katalog installiert und im Verwaltungstool Komponentendienste angezeigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von Installationspaketen für COM+-Anwendungen](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[Der COM+-Katalog](the-com--catalog.md)
</dt> <dt>

[Das COMREPL-Replikationshilfsprogramm](the-comrepl-replication-utility.md)
</dt> </dl>

 

 



