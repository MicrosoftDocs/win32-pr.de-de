---
title: Hostnamen und IP-Adressen
description: Für TCP/IP-Netzwerke müssen Hostnamen in IP-Adressen aufgelöst werden, bevor die Adressinformationen zum Erstellen einer Verbindung verwendet werden können.
ms.assetid: f077e7d0-2e2c-4a2b-b5cd-1c7f43f7743b
keywords:
- Hostnamen und IP-Adressen SNMP
- Hostnamen, Auflösen von SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426f711be9e1fda5dc936db6628cccc21093aa09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709581"
---
# <a name="host-names-and-ip-addresses"></a><span data-ttu-id="4d50d-105">Hostnamen und IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="4d50d-105">Host Names and IP Addresses</span></span>

<span data-ttu-id="4d50d-106">Für TCP/IP-Netzwerke müssen Hostnamen in IP-Adressen aufgelöst werden, bevor die Adressinformationen zum Erstellen einer Verbindung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="4d50d-106">TCP/IP networks require host names to be resolved to IP addresses before the address information can be used to create a connection.</span></span> <span data-ttu-id="4d50d-107">Auf Computern, auf denen das Windows-Betriebssystem ausgeführt wird, wird eine Hostdatei verwendet, die zu diesem Zweck Hostnamen zu IP-Adressen zuordnet.</span><span class="sxs-lookup"><span data-stu-id="4d50d-107">Computers running on the Windows operating system use a host file that, for this purpose, maps host names to IP addresses.</span></span>

<span data-ttu-id="4d50d-108">Die Hostdatei ist eine Textdatei, die explizite Hostnamen und IP-Adressen auflistet.</span><span class="sxs-lookup"><span data-stu-id="4d50d-108">The host file is a text file that lists explicit host names and IP addresses.</span></span> <span data-ttu-id="4d50d-109">Die Hostdatei wird beim Start automatisch in den Arbeitsspeicher geladen und für den Fall, dass ein Hostname aufgelöst werden muss, angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4d50d-109">The host file is automatically loaded into memory on startup and consulted when a host name requires resolution.</span></span> <span data-ttu-id="4d50d-110">Wenn die Hostdatei nicht die zum Auflösen eines bestimmten Host namens in die IP-Adresse erforderlichen Mapping-Informationen enthält, wird eine Auflösungs Abfrage an einen DNS-Server vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="4d50d-110">If the host file does not contain the mapping information that is required to resolve a specific host name to its IP address, a resolution query is made to a DNS server.</span></span>

<span data-ttu-id="4d50d-111">SNMP verwendet Windows Internet Naming Service (WINS) für die Host Namensauflösung.</span><span class="sxs-lookup"><span data-stu-id="4d50d-111">SNMP uses the Windows Internet Naming Service (WINS) for host name resolution.</span></span> <span data-ttu-id="4d50d-112">WINS ermöglicht das Zuordnen von NetBIOS-Namen oder Computernamen zu IP-Adressen in TCP/IP-Netzwerken.</span><span class="sxs-lookup"><span data-stu-id="4d50d-112">WINS makes it possible to map NetBIOS names, or machine names, to IP addresses on TCP/IP networks.</span></span> <span data-ttu-id="4d50d-113">Wenn der Computer nicht auf einen WINS-Server zugreifen kann, verwendet der SNMP-Dienst die Hostdatei, um Hostnamen in IP-Adressen aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="4d50d-113">If the computer cannot access a WINS server, the SNMP service uses the host file to resolve host names to IP addresses.</span></span>

<span data-ttu-id="4d50d-114">Der SNMP-Dienst unterstützt die Verwendung von Hostnamen und IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="4d50d-114">The SNMP service supports the use of both host names and IP addresses.</span></span> <span data-ttu-id="4d50d-115">Wenn Sie jedoch die Möglichkeit haben, Host Namen oder IP-Adressen zur Identifizierung von Netzwerk Standorten zu verwenden, sollten die SNMP-Verwaltungs Anwendungen Hostnamen verwenden.</span><span class="sxs-lookup"><span data-stu-id="4d50d-115">However, when you have a choice between using host names or IP addresses to identify network locations, your SNMP management applications should use host names.</span></span> <span data-ttu-id="4d50d-116">Wenn Sie Hostnamen verwenden, fügen Sie der Hostdatei alle Zuordnungen von Hostnamen und IP-Adressen der teilnehmenden Systeme hinzu.</span><span class="sxs-lookup"><span data-stu-id="4d50d-116">If you use host names, add all host name and IP address mappings of the participating systems to the host file.</span></span>

 

 




