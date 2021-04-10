---
description: Der NLA-Dienstanbieter (Network Location Awareness) ist wichtig für Computer oder Geräte, die möglicherweise zwischen verschiedenen Netzwerken verschoben werden, und für die Auswahl optimaler Konfigurationen, wenn mehr als eine verfügbar ist.
ms.assetid: 307f384d-e59a-4fc5-8f6a-ed81a102df60
title: Die NLA-Rolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28034d0d08353b3e794b5a30a6900e24d214e977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215463"
---
# <a name="the-role-of-nla"></a><span data-ttu-id="f1638-103">Die NLA-Rolle</span><span class="sxs-lookup"><span data-stu-id="f1638-103">The Role of NLA</span></span>

<span data-ttu-id="f1638-104">Der NLA-Dienstanbieter (Network Location Awareness) ist wichtig für Computer oder Geräte, die möglicherweise zwischen verschiedenen Netzwerken verschoben werden, und für die Auswahl optimaler Konfigurationen, wenn mehr als eine verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f1638-104">The Network Location Awareness (NLA) service provider is vital for computers or devices that might move between different networks, and for selecting optimal configurations when more than one is available.</span></span> <span data-ttu-id="f1638-105">Beispielsweise kann ein drahtloses Computer Roaming zwischen physischen Netzwerken NLA verwenden, um die richtige Konfiguration basierend auf Informationen über die verfügbare Netzwerkverbindung zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="f1638-105">For example, a wireless computer roaming between physical networks can use NLA to determine the proper configuration based on information about its available network connection.</span></span> <span data-ttu-id="f1638-106">NLA erweist sich auch als wertvoll, wenn ein mehrfach vernetzter Computer über eine physische Verbindung mit einem Netzwerk verfügt, während auch über eine DFÜ-Verbindung oder einen Tunnel eine Verbindung mit einem anderen Netzwerk besteht.</span><span class="sxs-lookup"><span data-stu-id="f1638-106">NLA also proves valuable when a multihomed computer has a physical connection to one network while also connected to another network through a dial-up connection or a tunnel.</span></span>

<span data-ttu-id="f1638-107">In der Vergangenheit mussten Entwicklerinformationen zu einer logischen Netzwerkschnittstelle abrufen und daher Entscheidungen über die Netzwerk Konnektivität treffen, basierend auf einer Vielzahl von unterschiedlichen Netzwerkinformationen.</span><span class="sxs-lookup"><span data-stu-id="f1638-107">In the past, developers had to obtain information about a logical network interface, and therefore make decisions about network connectivity, based on a multitude of disparate network information.</span></span> <span data-ttu-id="f1638-108">In diesen Fällen mussten Entwickler die geeignete Netzwerkschnittstelle basierend auf der IP-Adresse, dem Subnetz der Schnittstelle, dem Domain Name System (DNS)-Namen, der der Schnittstelle zugeordnet ist, der Mac-Adresse einer NIC, einem drahtlos Netzwerknamen oder anderen Netzwerkinformationen auswählen.</span><span class="sxs-lookup"><span data-stu-id="f1638-108">In those circumstances, developers had to choose the appropriate network interface based on the IP address, the subnet of the interface, the Domain Name System (DNS) name associated with the interface, the MAC address of a NIC, a wireless network name, or other network information.</span></span> <span data-ttu-id="f1638-109">NLA verringert dieses Problem durch Bereitstellen einer Standardschnittstelle zum Auflisten von Informationen zu logischen Netzwerk Anlagen, Korrelieren der Informationen zu physischen Netzwerkschnittstellen Informationen und anschließende Bereitstellung von Benachrichtigungen, wenn zuvor zurückgegebene Informationen ungültig werden.</span><span class="sxs-lookup"><span data-stu-id="f1638-109">NLA alleviates this problem by supplying a standard interface for enumerating logical network attachment information, correlating it with physical network interface information, and then providing notification when previously returned information gets invalidated.</span></span>

<span data-ttu-id="f1638-110">NLA bietet die folgenden Informationen zum Netzwerk Speicherort:</span><span class="sxs-lookup"><span data-stu-id="f1638-110">NLA provides the following network location information:</span></span>

<dl> <dt>

<span data-ttu-id="f1638-111"><span id="Logical_Network_Identity"></span><span id="logical_network_identity"></span><span id="LOGICAL_NETWORK_IDENTITY"></span>Identität des logischen Netzwerks</span><span class="sxs-lookup"><span data-stu-id="f1638-111"><span id="Logical_Network_Identity"></span><span id="logical_network_identity"></span><span id="LOGICAL_NETWORK_IDENTITY"></span>Logical Network Identity</span></span>
</dt> <dd>

<span data-ttu-id="f1638-112">NLA versucht zunächst, ein logisches Netzwerk mit dem DNS-Domänen Namen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f1638-112">NLA first attempts to identify a logical network by its DNS domain name.</span></span> <span data-ttu-id="f1638-113">Wenn ein logisches Netzwerk keinen Domänen Namen hat, identifiziert NLA das Netzwerk aus benutzerdefinierten statischen Informationen, die in der Registrierung gespeichert sind, und schließlich über seine Subnetzadresse.</span><span class="sxs-lookup"><span data-stu-id="f1638-113">If a logical network does not have a domain name, NLA identifies the network from custom static information stored in the registry, and finally from its subnet address.</span></span>

</dd> <dt>

<span data-ttu-id="f1638-114"><span id="Logical_Network_Interfaces"></span><span id="logical_network_interfaces"></span><span id="LOGICAL_NETWORK_INTERFACES"></span>Logische Netzwerkschnittstellen</span><span class="sxs-lookup"><span data-stu-id="f1638-114"><span id="Logical_Network_Interfaces"></span><span id="logical_network_interfaces"></span><span id="LOGICAL_NETWORK_INTERFACES"></span>Logical Network Interfaces</span></span>
</dt> <dd>

<span data-ttu-id="f1638-115">Für jedes Netzwerk, dem ein Computer angefügt ist, stellt NLA einen *Adaptername* bereit, der eine physische Schnittstelle (z. b. eine NIC) oder eine logische Schnittstelle wie eine RAS-Verbindung eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f1638-115">For each network to which a computer is attached, NLA supplies an *AdapterName* that uniquely identifies a physical interface such as a NIC, or a logical interface such as a RAS connection.</span></span> <span data-ttu-id="f1638-116">Der Adapter Name kann dann mit Funktionen verwendet werden, die in der IP Helper-API verfügbar sind, um weitere Schnittstelleneigenschaften zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f1638-116">The AdapterName can then be used with functions available in the IP Helper API to obtain further interface characteristics.</span></span>

</dd> </dl>

<span data-ttu-id="f1638-117">NLA implementiert das logische Netzwerk als Dienstklasse mit zugeordneten Klassen-GUID und-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f1638-117">NLA implements the logical network as a service class, with an associated class GUID and properties.</span></span> <span data-ttu-id="f1638-118">Jedes logische Netzwerk, für das NLA Informationen zurückgibt, ist eine Instanz der Dienstklasse.</span><span class="sxs-lookup"><span data-stu-id="f1638-118">Each logical network for which NLA returns information is an instance of that service class.</span></span>

 

 



