---
title: Active Directory Server und dynamisches DNS
description: Die Active Directory Server veröffentlichen ihre Adressen so, dass Clients Sie nur mit dem Domänen Namen ermitteln können.
ms.assetid: b4928d53-2629-4ddb-bb43-ce7a187b41e2
ms.tgt_platform: multiple
keywords:
- dynamische DNS-Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971987cb73b65e46b36eda4c713054ba2796e63b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707223"
---
# <a name="active-directory-servers-and-dynamic-dns"></a><span data-ttu-id="39201-104">Active Directory Server und dynamisches DNS</span><span class="sxs-lookup"><span data-stu-id="39201-104">Active Directory Servers and Dynamic DNS</span></span>

<span data-ttu-id="39201-105">Die Active Directory Server veröffentlichen ihre Adressen so, dass Clients Sie nur mit dem Domänen Namen ermitteln können.</span><span class="sxs-lookup"><span data-stu-id="39201-105">The Active Directory servers publish their addresses such that clients can find them knowing only the domain name.</span></span> <span data-ttu-id="39201-106">Active Directory Server werden mithilfe der Dienst Ressourcen Einträge (SRV RRs) in DNS veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="39201-106">Active Directory servers are published using the Service Resource Records (SRV RRs) in DNS.</span></span> <span data-ttu-id="39201-107">SRV RR ist ein DNS-Datensatz, der verwendet wird, um den Namen eines diensdienstanbieter der Adresse eines Servers zuzuordnen, der den Dienst anbietet.</span><span class="sxs-lookup"><span data-stu-id="39201-107">The SRV RR is a DNS record used to map the name of a service to the address of a server that offers the service.</span></span> <span data-ttu-id="39201-108">Der Name eines SRV RR hat folgendes Format:</span><span class="sxs-lookup"><span data-stu-id="39201-108">The name of a SRV RR is in this form:</span></span>


```C++
<service>.<protocol>.<domain>
```



<span data-ttu-id="39201-109">Active Directory Server bieten den LDAP-Dienst über das TCP-Protokoll, sodass veröffentlichte Namen "LDAP. TCP <domain> " lauten.</span><span class="sxs-lookup"><span data-stu-id="39201-109">Active Directory servers offer the LDAP service over the TCP protocol so that published names are "ldap.tcp.<domain>".</span></span> <span data-ttu-id="39201-110">Daher ist SRV RR für fabrikam.com "LDAP.TCP.fabrikam.com".</span><span class="sxs-lookup"><span data-stu-id="39201-110">Thus, the SRV RR for fabrikam.com is "ldap.tcp.fabrikam.com".</span></span> <span data-ttu-id="39201-111">Zusätzliche Daten über SRV RR geben die Priorität und Gewichtung für den Server an, sodass Clients den besten Server für Ihre Anforderungen auswählen können.</span><span class="sxs-lookup"><span data-stu-id="39201-111">Additional data about the SRV RR indicates the priority and weight for the server, enabling clients to choose the best server for their needs.</span></span>

<span data-ttu-id="39201-112">Wenn ein Active Directory Server installiert ist, verwendet er Dynamic DNS, um sich selbst zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="39201-112">When an Active Directory server is installed, it uses Dynamic DNS to publish itself.</span></span> <span data-ttu-id="39201-113">Da TCP/IP-Adressen geändert werden können, überprüfen Server in regelmäßigen Abständen ihre Registrierungen, um sicherzustellen, dass Sie korrekt sind, und aktualisieren Sie ggf..</span><span class="sxs-lookup"><span data-stu-id="39201-113">Because TCP/IP addresses are subject to change, servers periodically verify their registrations to be sure they are correct, and update them if necessary.</span></span>

<span data-ttu-id="39201-114">Dynamic DNS ist eine neuere Ergänzung zum DNS-Standard.</span><span class="sxs-lookup"><span data-stu-id="39201-114">Dynamic DNS is a recent addition to the DNS standard.</span></span> <span data-ttu-id="39201-115">Dynamic DNS definiert ein Protokoll zum dynamischen Aktualisieren eines DNS-Servers mit neuen Daten.</span><span class="sxs-lookup"><span data-stu-id="39201-115">Dynamic DNS defines a protocol for dynamically updating a DNS server with new data.</span></span> <span data-ttu-id="39201-116">Vor dem dynamischen DNS mussten Administratoren die von DNS-Servern gespeicherten Datensätze manuell konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="39201-116">Prior to Dynamic DNS, administrators were required to manually configure the records stored by DNS servers.</span></span>

 

 




