---
description: Die Netsh-Befehle für IPv6 stellen ein Befehlszeilen Tool bereit, mit dem Sie IPv6-Schnittstellen, Adressen, Caches und Routen Abfragen und konfigurieren können. Die Netsh Interface-IPv6-Befehle werden unter Windows XP mit Service Pack 1 (SP1) und höher unterstützt.
ms.assetid: 68e17a55-4dd5-40cd-8996-25fa278ddd19
title: Netsh.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aab092def0dc12071ee9dd62fd7554a53c9a7f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129145"
---
# <a name="netshexe"></a><span data-ttu-id="fef9e-104">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="fef9e-104">Netsh.exe</span></span>

<span data-ttu-id="fef9e-105">Die Netsh-Befehle für IPv6 stellen ein Befehlszeilen Tool bereit, mit dem Sie IPv6-Schnittstellen, Adressen, Caches und Routen Abfragen und konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="fef9e-105">The Netsh commands for IPv6 provide a command-line tool that you can use to query and configure IPv6 interfaces, address, caches, and routes.</span></span> <span data-ttu-id="fef9e-106">Die Netsh Interface-IPv6-Befehle werden unter Windows XP mit Service Pack 1 (SP1) und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fef9e-106">The Netsh interface IPv6 commands are supported on Windows XP with Service Pack 1 (SP1) and later.</span></span>

<span data-ttu-id="fef9e-107">Netsh.exe verfügt über viele Unterbefehle für IPv6.</span><span class="sxs-lookup"><span data-stu-id="fef9e-107">Netsh.exe has many subcommands for IPv6.</span></span> <span data-ttu-id="fef9e-108">Eine umfassende Liste der Optionen für Netsh Interface IPv6 ist an der Eingabeaufforderung unter Windows XP mit SP1 und höher verfügbar, indem Sie Folgendes eingeben:</span><span class="sxs-lookup"><span data-stu-id="fef9e-108">A complete list of options for Netsh Interface IPv6 is available from the command prompt on Windows XP with SP1 and later by typing the following:</span></span>

<span data-ttu-id="fef9e-109">**Netsh Interface IPv6/?**</span><span class="sxs-lookup"><span data-stu-id="fef9e-109">**netsh interface ipv6 /?**</span></span>

<span data-ttu-id="fef9e-110">Die Dokumentation zu allen **netsh** -Befehlen für IPv6 ist auch online auf TechNet verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fef9e-110">Documentation on all of the **netsh** commands for IPv6 is also available online on Technet.</span></span> <span data-ttu-id="fef9e-111">Weitere Informationen zu **netsh** unter Windows Server 2008 finden Sie unter [Netsh Commands for Interface (IPv4 und IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770948(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="fef9e-111">For more information on **netsh** on Windows Server 2008, please see [Netsh commands for Interface (IPv4 and IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770948(v=ws.10)).</span></span> <span data-ttu-id="fef9e-112">Weitere Informationen zu **netsh** unter Windows Server 2003 finden Sie unter [Netsh-Befehle für Schnitt](/previous-versions/windows/it-pro/windows-server-2003/cc740203(v=ws.10))stellen-IPv6.</span><span class="sxs-lookup"><span data-stu-id="fef9e-112">For more information on **netsh** on Windows Server 2003, please see [Netsh commands for Interface IPv6](/previous-versions/windows/it-pro/windows-server-2003/cc740203(v=ws.10)).</span></span>

<span data-ttu-id="fef9e-113">Im folgenden finden Sie einige häufig verwendete Befehle für IPv6, obwohl viele weitere Befehle unterstützt werden:</span><span class="sxs-lookup"><span data-stu-id="fef9e-113">The following are a few commonly used commands for IPv6, although many other commands are supported:</span></span>

<dl> <dt>

<span data-ttu-id="fef9e-114"><span id="netsh_interface_ipv6_add_address"></span><span id="NETSH_INTERFACE_IPV6_ADD_ADDRESS"></span>**Netsh Interface IPv6-Adresse hinzufügen**</span><span class="sxs-lookup"><span data-stu-id="fef9e-114"><span id="netsh_interface_ipv6_add_address"></span><span id="NETSH_INTERFACE_IPV6_ADD_ADDRESS"></span>**netsh interface ipv6 add address**</span></span>
</dt> <dd>

<span data-ttu-id="fef9e-115">Fügt einer bestimmten Schnittstelle auf dem lokalen Computer eine IPv6-Adresse hinzu.</span><span class="sxs-lookup"><span data-stu-id="fef9e-115">Adds an IPv6 address to a specific interface on the local computer.</span></span> <span data-ttu-id="fef9e-116">Dieser Befehl enthält unter Optionsparameter, die angegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="fef9e-116">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="fef9e-117"><span id="netsh_interface_ipv6_add_dns"></span><span id="NETSH_INTERFACE_IPV6_ADD_DNS"></span>**Netsh Interface IPv6 Add DNS**</span><span class="sxs-lookup"><span data-stu-id="fef9e-117"><span id="netsh_interface_ipv6_add_dns"></span><span id="NETSH_INTERFACE_IPV6_ADD_DNS"></span>**netsh interface ipv6 add dns**</span></span>
</dt> <dd>

<span data-ttu-id="fef9e-118">Fügt der statisch konfigurierten Liste von DNS-Servern für die angegebene Schnittstelle auf dem lokalen Computer eine IPv6-Adresse des DNS-Servers hinzu.</span><span class="sxs-lookup"><span data-stu-id="fef9e-118">Adds a DNS server IPv6 address to the statically-configured list of DNS servers for the specified interface on the local computer.</span></span> <span data-ttu-id="fef9e-119">Dieser Befehl enthält unter Optionsparameter, die angegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="fef9e-119">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="fef9e-120"><span id="netsh_interface_ipv6_add_route"></span><span id="NETSH_INTERFACE_IPV6_ADD_ROUTE"></span>**Netsh Interface IPv6-Add-Route**</span><span class="sxs-lookup"><span data-stu-id="fef9e-120"><span id="netsh_interface_ipv6_add_route"></span><span id="NETSH_INTERFACE_IPV6_ADD_ROUTE"></span>**netsh interface ipv6 add route**</span></span>
</dt> <dd>

<span data-ttu-id="fef9e-121">Fügt eine Route für eine angegebene IPv6-Präfix Adresse auf dem lokalen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="fef9e-121">Adds a route for a specified IPv6 prefix address on the local computer.</span></span> <span data-ttu-id="fef9e-122">Dieser Befehl enthält unter Optionsparameter, die angegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="fef9e-122">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="fef9e-123"><span id="netsh_interface_ipv6_delete_address"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ADDRESS"></span>**Netsh Interface IPv6-Adresse löschen**</span><span class="sxs-lookup"><span data-stu-id="fef9e-123"><span id="netsh_interface_ipv6_delete_address"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ADDRESS"></span>**netsh interface ipv6 delete address**</span></span>
</dt> <dd>

<span data-ttu-id="fef9e-124">Löscht die angegebene IPv6-Adresse aus einer bestimmten Schnittstelle auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="fef9e-124">Deletes the specified IPv6 address from a specific interface on the local computer.</span></span> <span data-ttu-id="fef9e-125">Dieser Befehl enthält unter Optionsparameter, die angegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="fef9e-125">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="fef9e-126"><span id="netsh_interface_ipv6_delete_dns"></span><span id="NETSH_INTERFACE_IPV6_DELETE_DNS"></span>**Netsh Interface IPv6-DNS löschen**</span><span class="sxs-lookup"><span data-stu-id="fef9e-126"><span id="netsh_interface_ipv6_delete_dns"></span><span id="NETSH_INTERFACE_IPV6_DELETE_DNS"></span>**netsh interface ipv6 delete dns**</span></span>
</dt> <dd>

<span data-ttu-id="fef9e-127">Löscht eine DNS-Server Adresse aus der statisch konfigurierten Liste der DNS-Server für die angegebene Schnittstelle auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="fef9e-127">Deletes a DNS server address from the statically-configured list of DNS servers for the specified interface on the local computer.</span></span> <span data-ttu-id="fef9e-128">Dieser Befehl enthält unter Optionsparameter, die angegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="fef9e-128">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="fef9e-129"><span id="netsh_interface_ipv6_delete_interface"></span><span id="NETSH_INTERFACE_IPV6_DELETE_INTERFACE"></span>**Netsh Interface IPv6-Schnittstelle zum Löschen**</span><span class="sxs-lookup"><span data-stu-id="fef9e-129"><span id="netsh_interface_ipv6_delete_interface"></span><span id="NETSH_INTERFACE_IPV6_DELETE_INTERFACE"></span>**netsh interface ipv6 delete interface**</span></span>
</dt> <dd>

<span data-ttu-id="fef9e-130">Löscht eine angegebene Schnittstelle aus dem IPv6-Stapel auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="fef9e-130">Deletes a specified interface from the IPv6 stack on the local computer.</span></span> <span data-ttu-id="fef9e-131">Dieser Befehl enthält unter Optionsparameter, die angegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="fef9e-131">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="fef9e-132"><span id="netsh_interface_ipv6_delete_route"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ROUTE"></span>**IPv6-Route zum Löschen von Netsh Interface**</span><span class="sxs-lookup"><span data-stu-id="fef9e-132"><span id="netsh_interface_ipv6_delete_route"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ROUTE"></span>**netsh interface ipv6 delete route**</span></span>
</dt> <dd>

<span data-ttu-id="fef9e-133">Löscht eine Route für eine angegebene IPv6-Präfix Adresse auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="fef9e-133">Deletes a route for a specified IPv6 prefix address on the local computer.</span></span> <span data-ttu-id="fef9e-134">Dieser Befehl enthält unter Optionsparameter, die angegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="fef9e-134">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="fef9e-135"><span id="netsh_interface_ipv6_dump"></span><span id="NETSH_INTERFACE_IPV6_DUMP"></span>**IPv6-Dump für Netsh Interface**</span><span class="sxs-lookup"><span data-stu-id="fef9e-135"><span id="netsh_interface_ipv6_dump"></span><span id="NETSH_INTERFACE_IPV6_DUMP"></span>**netsh interface ipv6 dump**</span></span>
</dt> <dd>

<span data-ttu-id="fef9e-136">Erstellt ein-Skript, das die Befehle zum Erstellen der aktuellen Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="fef9e-136">Creates a script that contains the commands to create the current configuration.</span></span> <span data-ttu-id="fef9e-137">Wird dieses Skript in einer Datei gespeichert, kann es verwendet werden, um geänderte Konfigurationseinstellungen wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="fef9e-137">If saved to a file, this script can be used to restore altered configuration settings.</span></span>

</dd> <dt>

<span data-ttu-id="fef9e-138"><span id="netsh_interface_ipv6_install"></span><span id="NETSH_INTERFACE_IPV6_INSTALL"></span>**Netsh Interface IPv6-Installation**</span><span class="sxs-lookup"><span data-stu-id="fef9e-138"><span id="netsh_interface_ipv6_install"></span><span id="NETSH_INTERFACE_IPV6_INSTALL"></span>**netsh interface ipv6 install**</span></span>
</dt> <dd>

<span data-ttu-id="fef9e-139">Installiert das IPv6-Protokoll auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="fef9e-139">Installs the IPv6 protocol on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="fef9e-140"><span id="netsh_interface_ipv6_renew"></span><span id="NETSH_INTERFACE_IPV6_RENEW"></span>**Netsh Interface IPv6 Renew**</span><span class="sxs-lookup"><span data-stu-id="fef9e-140"><span id="netsh_interface_ipv6_renew"></span><span id="NETSH_INTERFACE_IPV6_RENEW"></span>**netsh interface ipv6 renew**</span></span>
</dt> <dd>

<span data-ttu-id="fef9e-141">Startet die IPv6-Schnittstellen auf dem lokalen Computer neu.</span><span class="sxs-lookup"><span data-stu-id="fef9e-141">Restarts the IPv6 interfaces on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="fef9e-142"><span id="netsh_interface_ipv6_reset"></span><span id="NETSH_INTERFACE_IPV6_RESET"></span>**Netsh Interface IPv6 Reset**</span><span class="sxs-lookup"><span data-stu-id="fef9e-142"><span id="netsh_interface_ipv6_reset"></span><span id="NETSH_INTERFACE_IPV6_RESET"></span>**netsh interface ipv6 reset**</span></span>
</dt> <dd>

<span data-ttu-id="fef9e-143">Setzt den IPv6-Konfigurations Status auf dem lokalen Computer zurück.</span><span class="sxs-lookup"><span data-stu-id="fef9e-143">Resets the IPv6 configuration state on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="fef9e-144"><span id="netsh_interface_ipv6_show_global"></span><span id="NETSH_INTERFACE_IPV6_SHOW_GLOBAL"></span>**Netsh Interface IPv6 Show Global**</span><span class="sxs-lookup"><span data-stu-id="fef9e-144"><span id="netsh_interface_ipv6_show_global"></span><span id="NETSH_INTERFACE_IPV6_SHOW_GLOBAL"></span>**netsh interface ipv6 show global**</span></span>
</dt> <dd>

<span data-ttu-id="fef9e-145">Zeigt die globalen Konfigurationsparameter für IPv6 auf dem lokalen Computer an.</span><span class="sxs-lookup"><span data-stu-id="fef9e-145">Displays the global configuration parameters for IPv6 on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="fef9e-146"><span id="netsh_interface_ipv6_show_address"></span><span id="NETSH_INTERFACE_IPV6_SHOW_ADDRESS"></span>**Netsh Interface IPv6 Show Address**</span><span class="sxs-lookup"><span data-stu-id="fef9e-146"><span id="netsh_interface_ipv6_show_address"></span><span id="NETSH_INTERFACE_IPV6_SHOW_ADDRESS"></span>**netsh interface ipv6 show address**</span></span>
</dt> <dd>

<span data-ttu-id="fef9e-147">Zeigt alle IPv6-Adressen oder alle IPv6-Adressen an einer bestimmten Schnittstelle auf dem lokalen Computer an.</span><span class="sxs-lookup"><span data-stu-id="fef9e-147">Displays all IPv6 addresses or all IPv6 addresses on a specific interface on the local computer.</span></span> <span data-ttu-id="fef9e-148">Dieser Befehl enthält unter Optionsparameter, die möglicherweise angegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="fef9e-148">This command has suboption parameters that may need to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="fef9e-149"><span id="netsh_interface_ipv6_uninstall"></span><span id="NETSH_INTERFACE_IPV6_UNINSTALL"></span>**Netsh Interface IPv6 deinstallieren**</span><span class="sxs-lookup"><span data-stu-id="fef9e-149"><span id="netsh_interface_ipv6_uninstall"></span><span id="NETSH_INTERFACE_IPV6_UNINSTALL"></span>**netsh interface ipv6 uninstall**</span></span>
</dt> <dd>

<span data-ttu-id="fef9e-150">Deinstalliert das IPv6-Protokoll auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="fef9e-150">Uninstalls the IPv6 protocol on the local computer.</span></span>

</dd> </dl>

## <a name="netsh-commands-for-ipv4"></a><span data-ttu-id="fef9e-151">Netsh-Befehle für IPv4</span><span class="sxs-lookup"><span data-stu-id="fef9e-151">Netsh commands for IPv4</span></span>

<span data-ttu-id="fef9e-152">Ähnliche Netsh-Befehle sind für IPv4 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fef9e-152">Similar Netsh commands are available for IPv4.</span></span> <span data-ttu-id="fef9e-153">Eine umfassende Liste der Optionen für Netsh-Befehle für die Verwendung mit IPv4 ist an der Eingabeaufforderung unter Windows XP mit SP1 und höher verfügbar, indem Folgendes eingegeben wird:</span><span class="sxs-lookup"><span data-stu-id="fef9e-153">A complete list of options for Netsh commands for use with IPv4 is available from the command prompt on Windows XP with SP1 and later by typing the following:</span></span>

<span data-ttu-id="fef9e-154">**Netsh Interface IP/?**</span><span class="sxs-lookup"><span data-stu-id="fef9e-154">**netsh interface ip /?**</span></span>

<span data-ttu-id="fef9e-155">Die Dokumentation zu allen Netsh-Befehlen für IPv4 ist auch online auf TechNet verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fef9e-155">Documentation on all of the Netsh commands for IPv4 is also available online on Technet.</span></span> <span data-ttu-id="fef9e-156">Weitere Informationen finden Sie unter [Netsh-Befehle für Schnittstellen-IP](/previous-versions/windows/it-pro/windows-server-2003/cc738592(v=ws.10)) .</span><span class="sxs-lookup"><span data-stu-id="fef9e-156">For more information, please see [Netsh commands for Interface IP](/previous-versions/windows/it-pro/windows-server-2003/cc738592(v=ws.10))</span></span>

 

 
