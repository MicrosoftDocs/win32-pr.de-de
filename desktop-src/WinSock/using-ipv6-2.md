---
description: Auf Windows XP wird ein neues Befehlszeilentool zum Konfigurieren und Verwalten von IPv4 bereitgestellt. Dieses Tool verwendet den befehl &\# 0034;netsh interface ip&\# 0034; zum Konfigurieren und Verwalten von IPv4.
ms.assetid: d27eb0c2-4ae0-42d1-b92e-055a1c232e1c
title: Verwenden von IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 675441d1ae18e287541ad4c354aca19c3779fb14f3630ac1636cd360024fcd31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559206"
---
# <a name="using-ipv6"></a>Verwenden von IPv6

Auf Windows XP wird ein neues Befehlszeilentool zum Konfigurieren und Verwalten von IPv4 bereitgestellt. Dieses Tool verwendet den Befehl "netsh interface ip" zum Konfigurieren und Verwalten von IPv4.

Auf Windows XP mit Service Pack 1 (SP1) und höher wurde dieses neue Befehlszeilentool erweitert, um die Konfiguration und Verwaltung von IPv6 zu unterstützen. Dieses erweiterte Tool ist der Befehl "netsh interface ipv6". Konfigurationsänderungen, die mithilfe der befehle Netsh.exe vorgenommen werden, sind dauerhaft und gehen nicht verloren, wenn der Computer oder das IPv6-Protokoll neu gestartet wird.

Der folgende Befehl ist auf Windows XP mit SP1 und höher verfügbar, um IPv6 auf einem lokalen Computer abzufragen und zu konfigurieren:

-   [Netsh.exe](netsh-exe.md)

Vor Windows XP mit Service Pack 1 (SP1) wurden für die IPv6-Konfiguration und -Verwaltung mehrere ältere Befehlszeilentools verwendet, um IPv6 zu konfigurieren und zu verwalten. Mit diesen älteren Tools sind die IPv6-Änderungen nicht dauerhaft und gehen verloren, wenn der Computer oder das IPv6-Protokoll neu gestartet wurde.

Die folgenden älteren Befehle sind auf Windows XP verfügbar.

-   [Net.exe](net-exe-2.md)
-   [Ipv6.exe](ipv6-exe-2.md)
-   [Ipsec6.exe](ipsec6-exe-2.md)

Diese älteren Tools wurden auch in der IPv6-Technologievorschau für Windows 2000 bereitgestellt.

Konfigurationsänderungen mit diesen älteren Tools können beibehalten werden, indem sie als Befehlszeilen in einer Befehlsskriptdatei (CMD) platziert werden, die nach dem Neustart des Computers oder des IPv6-Protokolls ausgeführt wird. Um Konfigurationsänderungen nach dem Neustart automatisch wiederherzustellen, war es möglich, die Windows Geplante Aufgaben zu verwenden, um die CMD-Datei auszuführen, wenn der Computer gestartet wird.

Diese älteren Tools werden auf Windows Server 2003 und höher nicht bereitgestellt. Das Tool "netsh interface ipv6" wird zum Konfigurieren und Verwalten von IPv6 über die Befehlszeile auf Windows Server 2003 und höher bereitgestellt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Internetprotokoll Version 6 (IPv6)](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[IPv6-Leitfaden für Windows Sockets-Anwendungen](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[IPv6 Technology Preview für Windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> </dl>

 

 



