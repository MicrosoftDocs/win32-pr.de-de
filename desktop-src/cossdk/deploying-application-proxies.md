---
description: Für den Remote Zugriff auf eine COM+-Serveranwendung von einem anderen (Client-) Computer aus muss auf dem Client Computer eine Teilmenge der Attribute der Serveranwendung installiert sein, einschließlich Proxy-/Stub-DLLs und Typbibliotheken für DCOM/QC Interface Remoting.
ms.assetid: 293b424c-4cd4-43a9-9b56-687c753a34f2
title: Anwendungs Proxys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5e6439574602005ca53917945fa9005f8959b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958627"
---
# <a name="deploying-application-proxies"></a>Anwendungs Proxys

Für den Remote Zugriff auf eine COM+-Serveranwendung von einem anderen (Client-) Computer aus muss auf dem Client Computer eine Teilmenge der Attribute der Serveranwendung installiert sein, einschließlich Proxy-/Stub-DLLs und Typbibliotheken für DCOM/QC Interface Remoting. Diese Teilmenge wird als *Anwendungs Proxy* bezeichnet.

Mithilfe des Verwaltungs Tools Komponenten Dienste können Sie eine COM+-Serveranwendung problemlos als Anwendungs Proxy exportieren. Damit com+ einen Anwendungs Proxy generiert, ist es wichtig, dass alle Komponenten in der Serveranwendung installiert und nicht importiert wurden. (Weitere Informationen zu diesem Unterschied finden Sie unter [Importieren von Komponenten](importing-components.md).) Dadurch wird sichergestellt, dass die Anwendung alle notwendigen Registrierungsinformationen enthält.

> [!Note]  
> Es wird empfohlen, dass Sie die Schnittstellendefinitionen von den Klassen Implementierungen trennen. Andernfalls enthält der in com+-Anwendungs Proxy enthaltene Satz von DLLs oder Typbibliotheken tatsächlichen Servercode.

 

Von com+ generierte Anwendungs Proxys sind Windows Installer Installationspakete. Nach der Installation werden die Anwendungs Proxys in der Systemsteuerung des Client Computers unter Software angezeigt (es sei denn, die MSI-Datei wird mit einem Windows Installer Authoring Tool geändert).

## <a name="remote-access-via-application-proxies"></a>Remote Zugriff über Anwendungs Proxys

Beim Erstellen eines Anwendungs Proxys bietet com+ automatisch die folgenden Informationen, die erforderlich sind, damit der Anwendungs Proxy Remote auf eine COM+-Serveranwendung zugreifen kann:

-   Klassen Identitätsinformationen (CLSIDs und ProgIDs). Ein Anwendungs Proxy unterstützt bis zu zwei ProgIDs.
-   Anwendungs Identität und die Beziehung zwischen Klassen und Anwendungen (AppID).
-   Standortinformationen pro Anwendung (Remote Server Name).
-   Marshalling von Informationen für alle Schnittstellen, die von der Anwendung verfügbar gemacht werden (z. b. Typbibliotheken und Proxy/Stub).
-   MSMQ-Warteschlangen Namen und-Bezeichner (wenn der Dienst in der Warteschlange für die Anwendung aktiviert ist).
-   Attribute für Klassen, Schnittstellen und Methoden, ausgenommen Rollen Informationen.
-   Anwendungs Attribute.

## <a name="installing-application-proxies-on-other-operating-systems"></a>Installieren von Anwendungs Proxys unter anderen Betriebssystemen

Im Gegensatz zu com+-Server Anwendungen können Anwendungs Proxys unter allen Betriebssystemen installiert werden, die DCOM unterstützen (und Windows Installer). Auf Computern, auf denen com+ nicht ausgeführt wird, wird nur die Teilmenge der für DCOM-Remoting erforderlichen Informationen installiert. Diese Informationen werden in der Windows-Registrierung installiert (mit den HKEY \_ \_ -Klassen root, AppID/CLSID-Schlüsseln).

> [!Note]  
> Bei der Installation eines Anwendungs Proxys (MSI-Datei) auf Computern, auf denen com+ nicht ausgeführt wird, muss Windows Installer auf diesen Computern ausgeführt werden. Es wird empfohlen, dass Entwickler die Windows Installer verteilbare Datei (instmsi.exe) zusammen mit der MSI-Datei Ihrer Anwendung liefern. Dadurch wird sichergestellt, dass Systemadministratoren Windows Installer verfügbar sind, wenn Anwendungs Proxys auf Clients bereitgestellt werden, die nicht com+ ausführen.

 

Auf Computern, auf denen com+ ausgeführt wird, werden die Anwendungs Proxy Informationen im com+-Katalog installiert und im Verwaltungs Programmkomponenten Dienste angezeigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Installationspakete für COM+-Anwendungen werden erstellt.](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[Der com+-Katalog](the-com--catalog.md)
</dt> <dt>

[Das Hilfsprogramm zur Comrepl-Replikation](the-comrepl-replication-utility.md)
</dt> </dl>

 

 



