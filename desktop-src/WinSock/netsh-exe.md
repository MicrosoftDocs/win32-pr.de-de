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
# <a name="netshexe"></a>Netsh.exe

Die Netsh-Befehle für IPv6 stellen ein Befehlszeilen Tool bereit, mit dem Sie IPv6-Schnittstellen, Adressen, Caches und Routen Abfragen und konfigurieren können. Die Netsh Interface-IPv6-Befehle werden unter Windows XP mit Service Pack 1 (SP1) und höher unterstützt.

Netsh.exe verfügt über viele Unterbefehle für IPv6. Eine umfassende Liste der Optionen für Netsh Interface IPv6 ist an der Eingabeaufforderung unter Windows XP mit SP1 und höher verfügbar, indem Sie Folgendes eingeben:

**Netsh Interface IPv6/?**

Die Dokumentation zu allen **netsh** -Befehlen für IPv6 ist auch online auf TechNet verfügbar. Weitere Informationen zu **netsh** unter Windows Server 2008 finden Sie unter [Netsh Commands for Interface (IPv4 und IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770948(v=ws.10)). Weitere Informationen zu **netsh** unter Windows Server 2003 finden Sie unter [Netsh-Befehle für Schnitt](/previous-versions/windows/it-pro/windows-server-2003/cc740203(v=ws.10))stellen-IPv6.

Im folgenden finden Sie einige häufig verwendete Befehle für IPv6, obwohl viele weitere Befehle unterstützt werden:

<dl> <dt>

<span id="netsh_interface_ipv6_add_address"></span><span id="NETSH_INTERFACE_IPV6_ADD_ADDRESS"></span>**Netsh Interface IPv6-Adresse hinzufügen**
</dt> <dd>

Fügt einer bestimmten Schnittstelle auf dem lokalen Computer eine IPv6-Adresse hinzu. Dieser Befehl enthält unter Optionsparameter, die angegeben werden müssen.

</dd> <dt>

<span id="netsh_interface_ipv6_add_dns"></span><span id="NETSH_INTERFACE_IPV6_ADD_DNS"></span>**Netsh Interface IPv6 Add DNS**
</dt> <dd>

Fügt der statisch konfigurierten Liste von DNS-Servern für die angegebene Schnittstelle auf dem lokalen Computer eine IPv6-Adresse des DNS-Servers hinzu. Dieser Befehl enthält unter Optionsparameter, die angegeben werden müssen.

</dd> <dt>

<span id="netsh_interface_ipv6_add_route"></span><span id="NETSH_INTERFACE_IPV6_ADD_ROUTE"></span>**Netsh Interface IPv6-Add-Route**
</dt> <dd>

Fügt eine Route für eine angegebene IPv6-Präfix Adresse auf dem lokalen Computer hinzu. Dieser Befehl enthält unter Optionsparameter, die angegeben werden müssen.

</dd> <dt>

<span id="netsh_interface_ipv6_delete_address"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ADDRESS"></span>**Netsh Interface IPv6-Adresse löschen**
</dt> <dd>

Löscht die angegebene IPv6-Adresse aus einer bestimmten Schnittstelle auf dem lokalen Computer. Dieser Befehl enthält unter Optionsparameter, die angegeben werden müssen.

</dd> <dt>

<span id="netsh_interface_ipv6_delete_dns"></span><span id="NETSH_INTERFACE_IPV6_DELETE_DNS"></span>**Netsh Interface IPv6-DNS löschen**
</dt> <dd>

Löscht eine DNS-Server Adresse aus der statisch konfigurierten Liste der DNS-Server für die angegebene Schnittstelle auf dem lokalen Computer. Dieser Befehl enthält unter Optionsparameter, die angegeben werden müssen.

</dd> <dt>

<span id="netsh_interface_ipv6_delete_interface"></span><span id="NETSH_INTERFACE_IPV6_DELETE_INTERFACE"></span>**Netsh Interface IPv6-Schnittstelle zum Löschen**
</dt> <dd>

Löscht eine angegebene Schnittstelle aus dem IPv6-Stapel auf dem lokalen Computer. Dieser Befehl enthält unter Optionsparameter, die angegeben werden müssen.

</dd> <dt>

<span id="netsh_interface_ipv6_delete_route"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ROUTE"></span>**IPv6-Route zum Löschen von Netsh Interface**
</dt> <dd>

Löscht eine Route für eine angegebene IPv6-Präfix Adresse auf dem lokalen Computer. Dieser Befehl enthält unter Optionsparameter, die angegeben werden müssen.

</dd> <dt>

<span id="netsh_interface_ipv6_dump"></span><span id="NETSH_INTERFACE_IPV6_DUMP"></span>**IPv6-Dump für Netsh Interface**
</dt> <dd>

Erstellt ein-Skript, das die Befehle zum Erstellen der aktuellen Konfiguration enthält. Wird dieses Skript in einer Datei gespeichert, kann es verwendet werden, um geänderte Konfigurationseinstellungen wiederherzustellen.

</dd> <dt>

<span id="netsh_interface_ipv6_install"></span><span id="NETSH_INTERFACE_IPV6_INSTALL"></span>**Netsh Interface IPv6-Installation**
</dt> <dd>

Installiert das IPv6-Protokoll auf dem lokalen Computer.

</dd> <dt>

<span id="netsh_interface_ipv6_renew"></span><span id="NETSH_INTERFACE_IPV6_RENEW"></span>**Netsh Interface IPv6 Renew**
</dt> <dd>

Startet die IPv6-Schnittstellen auf dem lokalen Computer neu.

</dd> <dt>

<span id="netsh_interface_ipv6_reset"></span><span id="NETSH_INTERFACE_IPV6_RESET"></span>**Netsh Interface IPv6 Reset**
</dt> <dd>

Setzt den IPv6-Konfigurations Status auf dem lokalen Computer zurück.

</dd> <dt>

<span id="netsh_interface_ipv6_show_global"></span><span id="NETSH_INTERFACE_IPV6_SHOW_GLOBAL"></span>**Netsh Interface IPv6 Show Global**
</dt> <dd>

Zeigt die globalen Konfigurationsparameter für IPv6 auf dem lokalen Computer an.

</dd> <dt>

<span id="netsh_interface_ipv6_show_address"></span><span id="NETSH_INTERFACE_IPV6_SHOW_ADDRESS"></span>**Netsh Interface IPv6 Show Address**
</dt> <dd>

Zeigt alle IPv6-Adressen oder alle IPv6-Adressen an einer bestimmten Schnittstelle auf dem lokalen Computer an. Dieser Befehl enthält unter Optionsparameter, die möglicherweise angegeben werden müssen.

</dd> <dt>

<span id="netsh_interface_ipv6_uninstall"></span><span id="NETSH_INTERFACE_IPV6_UNINSTALL"></span>**Netsh Interface IPv6 deinstallieren**
</dt> <dd>

Deinstalliert das IPv6-Protokoll auf dem lokalen Computer.

</dd> </dl>

## <a name="netsh-commands-for-ipv4"></a>Netsh-Befehle für IPv4

Ähnliche Netsh-Befehle sind für IPv4 verfügbar. Eine umfassende Liste der Optionen für Netsh-Befehle für die Verwendung mit IPv4 ist an der Eingabeaufforderung unter Windows XP mit SP1 und höher verfügbar, indem Folgendes eingegeben wird:

**Netsh Interface IP/?**

Die Dokumentation zu allen Netsh-Befehlen für IPv4 ist auch online auf TechNet verfügbar. Weitere Informationen finden Sie unter [Netsh-Befehle für Schnittstellen-IP](/previous-versions/windows/it-pro/windows-server-2003/cc738592(v=ws.10)) .

 

 
