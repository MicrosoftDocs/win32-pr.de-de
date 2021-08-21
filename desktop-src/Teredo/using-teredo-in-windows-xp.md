---
title: Verwenden von Teredo in Windows XP
ms.assetid: 21590e3b-03de-48a4-b142-5d1934dacc38
description: 'Weitere Informationen zu: Verwenden von Teredo in Windows XP'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b488a4825fba8371082d3e538b365e8ec666d000b70ee61d34a640c22775ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118856957"
---
# <a name="using-teredo-in-windows-xp"></a>Verwenden von Teredo in Windows XP

Um den Teredo-Client oder das hostspezifische Relay auf Computern zu verwenden, auf denen Windows XP mit Service Pack 1 (SP1) mit dem Erweiterten Netzwerkpaket, Windows XP mit Service Pack 2 (SP2), Windows Server 2003 mit Service Pack 1 (SP1) oder Windows Server 2003 mit Service Pack 2 (SP2) ausgeführt wird, muss ein Anwendungsentwickler folgende Schritte ausführen:

-   Stellen Sie sicher, dass die Anwendung mit IPv6 kompatibel ist, indem Sie neue Windows Sockets 2-Programmierelemente (Funktionen und Strukturen) verwenden, die sowohl IPv4 als auch IPv6 unterstützen. Weitere Informationen finden Sie im [IPv6-Handbuch für Windows Sockets-Anwendungen.](../winsock/ipv6-guide-for-windows-sockets-applications-2.md)
-   Aktivieren Sie die Verwendung von Teredo in Ihrer Anwendung, indem Sie die Socketoption IPV6 \_ PROTECTION \_ LEVEL Windows Sockets auf die STUFE \_ \_ UNEINGESCHRÄNKTE SCHUTZEBENE festlegen. Weitere Informationen finden Sie unter [Verwenden von IPV6 \_ PROTECTION \_ LEVEL](/previous-versions/aa916826(v=msdn.10)). Sie können diese Option auch über die [System.Net.Sockets](/dotnet/api/system.net.sockets?view=netcore-3.1) .NET Framework-Klasse festlegen.
-   Erstellen Sie eine Ausnahme für die Windows Firewall, um nicht angeforderten eingehenden Teredo-Datenverkehr zuzulassen. Verwenden Sie die Windows Firewall-APIs, um eine Portausnahme für den UDP-Port zu erstellen, der für Teredo-Datenverkehr zugewiesen ist. [](/previous-versions/windows/desktop/ics/windows-firewall-start-page) Weitere Informationen und Beispiele zu den erforderlichen Sicherheits- und Datenverkehrsüberlegungen für Teredo finden Sie unter [Verwenden von Teredo.](using-teredo.md)

Um sicherzustellen, dass Teredo bei der Ausführung der Anwendung zur Verfügung steht, sollten Anwendungsentwickler während der Installation der Anwendung Folgendes tun:

-   Installieren Sie IPv6 mit dem **Befehl netsh interface ipv6 install.** Windows Die Firewall schützt den Computer des Benutzers auf die gleiche Weise wie IPv4-Datenverkehr vor unerwünschtem eingehendem IPv6-Datenverkehr.
-   Aktivieren Sie Teredo mit dem **Befehl netsh interface ipv6 set teredo client.**

Optional können Sie testen, ob IPv6 bei jeder Ausführung Ihrer Anwendung installiert wird, IPv6 installiert und Teredo bei Bedarf aktiviert wird. Sie sollten den Benutzer auch darüber informieren, dass IPv6 installiert und Teredo aktiviert wird.

 

 
