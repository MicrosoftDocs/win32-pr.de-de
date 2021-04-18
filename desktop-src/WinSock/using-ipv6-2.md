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
# <a name="using-ipv6"></a><span data-ttu-id="016c8-104">Verwenden von IPv6</span><span class="sxs-lookup"><span data-stu-id="016c8-104">Using IPv6</span></span>

<span data-ttu-id="016c8-105">Unter Windows XP a später wird ein neues Befehlszeilen Tool zum Konfigurieren und Verwalten von IPv4 bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="016c8-105">On Windows XP a later, a new command-line tool is provided for configuring and managing IPv4.</span></span> <span data-ttu-id="016c8-106">Dieses Tool verwendet den Befehl "Netsh Interface IP", um IPv4 zu konfigurieren und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="016c8-106">This tool uses the "netsh interface ip" command for configuring and managing IPv4.</span></span>

<span data-ttu-id="016c8-107">Unter Windows XP mit Service Pack 1 (SP1) und höher wurde dieses neue Befehlszeilen Tool verbessert, um die Konfiguration und Verwaltung von IPv6 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="016c8-107">On Windows XP with Service Pack 1 (SP1) and later, this new command-line tool was enhanced to support the configuration and management of IPv6.</span></span> <span data-ttu-id="016c8-108">Dieses erweiterte Tool ist der Befehl "Netsh Interface IPv6".</span><span class="sxs-lookup"><span data-stu-id="016c8-108">This enhanced tool is the "netsh interface ipv6" command.</span></span> <span data-ttu-id="016c8-109">Konfigurationsänderungen, die mithilfe der Netsh.exe Befehle vorgenommen werden, sind permanent und gehen nicht verloren, wenn der Computer oder das IPv6-Protokoll neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="016c8-109">Configuration changes made using the Netsh.exe commands are permanent and are not lost when the computer or the IPv6 protocol is restarted.</span></span>

<span data-ttu-id="016c8-110">Der folgende Befehl ist unter Windows XP mit SP1 und höher verfügbar, um IPv6 auf einem lokalen Computer abzufragen und zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="016c8-110">The following command is available on Windows XP with SP1 and later to query and configure IPv6 on a local computer:</span></span>

-   [<span data-ttu-id="016c8-111">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="016c8-111">Netsh.exe</span></span>](netsh-exe.md)

<span data-ttu-id="016c8-112">Vor Windows XP mit Service Pack 1 (SP1) verwendeten die IPv6-Konfiguration und-Verwaltung mehrere ältere Befehlszeilen Tools zum Konfigurieren und Verwalten von IPv6.</span><span class="sxs-lookup"><span data-stu-id="016c8-112">Prior to Windows XP with Service Pack 1 (SP1), IPv6 configuration and management used several older command-line tools to configure and manage IPv6.</span></span> <span data-ttu-id="016c8-113">Wenn Sie diese älteren Tools verwenden, sind die IPv6-Änderungen nicht permanent und gehen verloren, wenn der Computer oder das IPv6-Protokoll neu gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="016c8-113">Using these older tools, the IPv6 changes are not permanent and are lost when the computer or the IPv6 protocol was restarted.</span></span>

<span data-ttu-id="016c8-114">Die folgenden älteren Befehle sind unter Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="016c8-114">The following older commands are available on Windows XP</span></span>

-   [<span data-ttu-id="016c8-115">Net.exe</span><span class="sxs-lookup"><span data-stu-id="016c8-115">Net.exe</span></span>](net-exe-2.md)
-   [<span data-ttu-id="016c8-116">Ipv6.exe</span><span class="sxs-lookup"><span data-stu-id="016c8-116">Ipv6.exe</span></span>](ipv6-exe-2.md)
-   [<span data-ttu-id="016c8-117">Ipsec6.exe</span><span class="sxs-lookup"><span data-stu-id="016c8-117">Ipsec6.exe</span></span>](ipsec6-exe-2.md)

<span data-ttu-id="016c8-118">Diese älteren Tools wurden auch in der IPv6-Technologievorschau für Windows 2000 bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="016c8-118">These older tools were also provided in the IPv6 Technology Preview for Windows 2000</span></span>

<span data-ttu-id="016c8-119">Konfigurationsänderungen, die diese älteren Tools verwenden, können verwaltet werden, indem Sie als Befehlszeilen in einer Befehls Skriptdatei (. cmd) platziert werden, die nach dem Neustart des Computers oder des IPv6-Protokolls ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="016c8-119">Configuration changes using these older tools could be maintained by placing them as command lines in a command script file (.cmd) that is run after restarting the computer or the IPv6 protocol.</span></span> <span data-ttu-id="016c8-120">Wenn Sie Konfigurationsänderungen nach dem Neustart automatisch wiederherstellen möchten, ist es möglich, die CMD-Datei mit den geplanten Windows-Tasks auszuführen, wenn der Computer gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="016c8-120">To reinstate configuration changes automatically after restarting, is was possible to use the Windows Scheduled Tasks to run the .cmd file when the computer starts.</span></span>

<span data-ttu-id="016c8-121">Diese älteren Tools werden nicht unter Windows Server 2003 und höher bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="016c8-121">These older tools are not provided on Windows Server 2003 and later.</span></span> <span data-ttu-id="016c8-122">Das Tool "Netsh Interface IPv6" wird zum Konfigurieren und Verwalten von IPv6 über die Befehlszeile unter Windows Server 2003 und höher bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="016c8-122">The "netsh interface ipv6" tool is provided for configuring and managing IPv6 from the command-line on Windows Server 2003 and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="016c8-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="016c8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="016c8-124">Internet Protokoll Version 6 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="016c8-124">Internet Protocol Version 6 (IPv6)</span></span>](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[<span data-ttu-id="016c8-125">IPv6-Handbuch für Windows Sockets-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="016c8-125">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="016c8-126">IPv6-Technologievorschau für Windows 2000</span><span class="sxs-lookup"><span data-stu-id="016c8-126">IPv6 Technology Preview for Windows 2000</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> </dl>

 

 



