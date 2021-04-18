---
description: Unter Windows XP a später wird ein neues Befehlszeilen Tool zum Konfigurieren und Verwalten von IPv4 bereitgestellt. Dieses Tool verwendet den \# Befehl &0034; Netsh Interface IP&\# 0034; zum Konfigurieren und Verwalten von IPv4.
ms.assetid: d27eb0c2-4ae0-42d1-b92e-055a1c232e1c
title: Verwenden von IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f759d938ebebbc0ddfbb2326dfb10932c16310a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352299"
---
# <a name="using-ipv6"></a>Verwenden von IPv6

Unter Windows XP a später wird ein neues Befehlszeilen Tool zum Konfigurieren und Verwalten von IPv4 bereitgestellt. Dieses Tool verwendet den Befehl "Netsh Interface IP", um IPv4 zu konfigurieren und zu verwalten.

Unter Windows XP mit Service Pack 1 (SP1) und höher wurde dieses neue Befehlszeilen Tool verbessert, um die Konfiguration und Verwaltung von IPv6 zu unterstützen. Dieses erweiterte Tool ist der Befehl "Netsh Interface IPv6". Konfigurationsänderungen, die mithilfe der Netsh.exe Befehle vorgenommen werden, sind permanent und gehen nicht verloren, wenn der Computer oder das IPv6-Protokoll neu gestartet wird.

Der folgende Befehl ist unter Windows XP mit SP1 und höher verfügbar, um IPv6 auf einem lokalen Computer abzufragen und zu konfigurieren:

-   [Netsh.exe](netsh-exe.md)

Vor Windows XP mit Service Pack 1 (SP1) verwendeten die IPv6-Konfiguration und-Verwaltung mehrere ältere Befehlszeilen Tools zum Konfigurieren und Verwalten von IPv6. Wenn Sie diese älteren Tools verwenden, sind die IPv6-Änderungen nicht permanent und gehen verloren, wenn der Computer oder das IPv6-Protokoll neu gestartet wurde.

Die folgenden älteren Befehle sind unter Windows XP verfügbar.

-   [Net.exe](net-exe-2.md)
-   [Ipv6.exe](ipv6-exe-2.md)
-   [Ipsec6.exe](ipsec6-exe-2.md)

Diese älteren Tools wurden auch in der IPv6-Technologievorschau für Windows 2000 bereitgestellt.

Konfigurationsänderungen, die diese älteren Tools verwenden, können verwaltet werden, indem Sie als Befehlszeilen in einer Befehls Skriptdatei (. cmd) platziert werden, die nach dem Neustart des Computers oder des IPv6-Protokolls ausgeführt wird. Wenn Sie Konfigurationsänderungen nach dem Neustart automatisch wiederherstellen möchten, ist es möglich, die CMD-Datei mit den geplanten Windows-Tasks auszuführen, wenn der Computer gestartet wird.

Diese älteren Tools werden nicht unter Windows Server 2003 und höher bereitgestellt. Das Tool "Netsh Interface IPv6" wird zum Konfigurieren und Verwalten von IPv6 über die Befehlszeile unter Windows Server 2003 und höher bereitgestellt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Internet Protokoll Version 6 (IPv6)](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[IPv6-Handbuch für Windows Sockets-Anwendungen](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[IPv6-Technologievorschau für Windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> </dl>

 

 



