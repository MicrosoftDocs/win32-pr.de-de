---
title: Verwenden von Teredo in Windows XP
ms.assetid: 21590e3b-03de-48a4-b142-5d1934dacc38
description: Weitere Informationen finden Sie unter Verwenden von Teredo in Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f29abb2b4056564be29708ceb00742b37d363d7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050516"
---
# <a name="using-teredo-in-windows-xp"></a>Verwenden von Teredo in Windows XP

Um den Teredo-Client oder das Host spezifische Relay auf Computern mit Windows XP mit Service Pack 1 (SP1) mit dem erweiterten Netzwerk Paket, Windows XP mit Service Pack 2 (SP2), Windows Server 2003 mit Service Pack 1 (SP1) oder Windows Server 2003 mit Service Pack 2 (SP2) zu verwenden, muss ein Anwendungsentwickler die folgenden Schritte ausführen:

-   Stellen Sie sicher, dass die Anwendung mit IPv6 kompatibel ist, indem Sie neue Windows Sockets 2-Programmier Elemente (Funktionen und Strukturen) verwenden, die sowohl IPv4 als auch IPv6 unterstützen. Weitere Informationen finden Sie im [IPv6-Handbuch für Windows Sockets-Anwendungen](../winsock/ipv6-guide-for-windows-sockets-applications-2.md).
-   Aktivieren Sie die Verwendung von Teredo in der Anwendung \_ , indem Sie die \_ Option Windows Sockets Socket für IPv6-Schutz Ebene auf die \_ \_ Ebene uneingeschränkte Schutz Ebene festlegen. Weitere Informationen finden Sie unter [Verwenden der IPv6- \_ Schutz \_ Ebene](/previous-versions/aa916826(v=msdn.10)). Sie können diese Option auch über die [System .net. Sockets](/dotnet/api/system.net.sockets?view=netcore-3.1) .NET Framework-Klasse festlegen.
-   Erstellen Sie eine Ausnahme für die Windows-Firewall, um nicht angeforderten eingehenden Teredo-Datenverkehr zuzulassen. Verwenden Sie die [Windows-Firewall](/previous-versions/windows/desktop/ics/windows-firewall-start-page) -APIs, um eine Port Ausnahme für den für Teredo-Datenverkehr zugewiesenen UDP-Port zu erstellen. Weitere Informationen und Beispiele, die die erforderlichen Sicherheits-und Datenverkehrs Aspekte für Teredo beschreiben, finden [Sie unter Verwenden von Teredo](using-teredo.md).

Um sicherzustellen, dass Teredo zur Verwendung bei der Anwendungs Ausführung verfügbar ist, sollten Anwendungsentwickler während der Installation der Anwendung folgende Aktionen ausführen:

-   Installieren Sie IPv6 mit dem Befehl **Netsh Interface IPv6 install** . Die Windows-Firewall schützt den Computer des Benutzers vor nicht angeforderten eingehenden IPv6-Datenverkehr auf die gleiche Weise wie IPv4-Datenverkehr.
-   Aktivieren Sie Teredo mit dem Befehl **Netsh Interface IPv6 Set Teredo Client** .

Optional können Sie testen, ob IPv6 bei jedem Ausführen der Anwendung und bei Bedarf installiert wird. Außerdem sollten Sie den Benutzer darüber informieren, dass IPv6 installiert ist und Teredo aktiviert ist.

 

 
