---
title: Verbindungs-Manager
description: Kunden, die benutzerdefinierte Dialer mithilfe der Remotezugriffsdienst-API entwickeln möchten, können Microsoft Verbindungs-Manager und die Verbindungs-Manager-Verwaltungskit untersuchen.
ms.assetid: c3227aea-ba36-44f6-b69d-2c6aa4be360e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc20979ecd99f904aef158738d49ce1e5bc5a25309288db83dfc99de05959234
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791584"
---
# <a name="connection-manager"></a>Verbindungs-Manager

Kunden, die benutzerdefinierte Dialer mithilfe der Remotezugriffsdienst-API entwickeln möchten, können Microsoft Verbindungs-Manager und die Verbindungs-Manager-Verwaltungskit untersuchen. Verbindungs-Manager ist der von Microsoft verwaltete Remotezugriffsclient. Sie ermöglicht es einem Administrator, ein Remotezugriffskonfigurationspaket zu erstellen, das an die Remotebenutzer des Administrators verteilt werden soll. Weitere Informationen zu Verbindungs-Manager und der Verbindungs-Manager-Verwaltungskit finden Sie in der Onlinehilfe für Microsoft Windows 2000 Server und höhere Betriebssysteme.

Den Quellcode für ein Beispiel Verbindungs-Manager benutzerdefinierte Aktion finden Sie im vollständigen Platform Software Development Kit (SDK). Das Plattform-SDK kann auf der [Microsoft-Website](https://msdn.microsoft.com/windowsserver/bb980924.aspx)heruntergeladen werden. Nach der Installation lautet der Pfad zum Beispielcode %Install Path% \\ Microsoft SDK \\ Samples \\ netds Ras \\ \\ ConnectionManager. %Install Path% legt das Basisinstallationsverzeichnis des Plattform-SDK fest (z. B. C: \\ Programme).

Benutzerdefinierte Aktionen ermöglichen es dem Remotezugriffsclient, bestimmte Aktionen an verschiedenen Stellen im Verbindungsprozess durchzuführen. Die im Beispiel gezeigte benutzerdefinierte Aktion passt automatisch die Proxyserverkonfiguration für eine Verbindung basierend auf der Serveradresse der Verbindung an. Kunden können dieses Beispiel als Ausgangspunkt für die Erstellung ihrer eigenen benutzerdefinierten Aktionen verwenden.

 

 




