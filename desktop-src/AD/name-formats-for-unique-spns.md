---
title: Namens Formate für eindeutige SPNs
description: Ein SPN muss in der Gesamtstruktur, in der er registriert ist, eindeutig sein.
ms.assetid: dd3f9f7c-b64c-4bd8-924f-a8880ee3b71e
ms.tgt_platform: multiple
keywords:
- Namens Formate für eindeutige SPNs AD
- Dienst Prinzipal Name AD, namens Formate für
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bda13cf5a095f8f2fd7ef1a209c6f3aeebd6654
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206256"
---
# <a name="name-formats-for-unique-spns"></a><span data-ttu-id="3a5f8-105">Namens Formate für eindeutige SPNs</span><span class="sxs-lookup"><span data-stu-id="3a5f8-105">Name Formats for Unique SPNs</span></span>

<span data-ttu-id="3a5f8-106">Ein SPN muss in der Gesamtstruktur, in der er registriert ist, eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-106">An SPN must be unique in the forest in which it is registered.</span></span> <span data-ttu-id="3a5f8-107">Wenn Sie nicht eindeutig ist, tritt bei der Authentifizierung ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-107">If it is not unique, authentication will fail.</span></span> <span data-ttu-id="3a5f8-108">Die SPN-Syntax hat vier Elemente: zwei erforderliche Elemente und zwei weitere Elemente, die Sie ggf. verwenden können, um einen eindeutigen Namen zu erhalten, wie in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-108">The SPN syntax has four elements: two required elements and two additional elements that you can use, if necessary, to produce a unique name as listed in the following table.</span></span>


```C++
<service class>/<host>:<port>/<service name>
```





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3a5f8-109">Element</span><span class="sxs-lookup"><span data-stu-id="3a5f8-109">Element</span></span></th>
<th><span data-ttu-id="3a5f8-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3a5f8-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3a5f8-111">&quot;&lt;Dienstklasse&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="3a5f8-111">&quot;&lt;service class&gt;&quot;</span></span></td>
<td><span data-ttu-id="3a5f8-112">Eine Zeichenfolge, die die allgemeine Dienstklasse identifiziert. Beispiel: &quot; SQLServer &quot; .</span><span class="sxs-lookup"><span data-stu-id="3a5f8-112">A string that identifies the general class of service; for example, &quot;SqlServer&quot;.</span></span> <span data-ttu-id="3a5f8-113">Es gibt bekannte Dienst Klassennamen, wie z. b &quot; &quot; . www für einen Webdienst oder &quot; LDAP &quot; für einen Verzeichnisdienst.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-113">There are well-known service class names, such as &quot;www&quot; for a web service or &quot;ldap&quot; for a directory service.</span></span> <span data-ttu-id="3a5f8-114">Im Allgemeinen kann dies eine beliebige Zeichenfolge sein, die für die Dienstklasse eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-114">In general, this can be any string that is unique to the service class.</span></span> <span data-ttu-id="3a5f8-115">Beachten Sie, dass die SPN-Syntax einen Schrägstrich (/) zum Trennen von Elementen verwendet, sodass dieses Zeichen nicht in einem Dienst Klassennamen vorkommen kann.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-115">Be aware that the SPN syntax uses a forward slash (/) to separate elements, so this character cannot appear in a service class name.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a5f8-116">&quot;&lt;Host&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="3a5f8-116">&quot;&lt;host&gt;&quot;</span></span></td>
<td><span data-ttu-id="3a5f8-117">Der Name des Computers, auf dem der-Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-117">The name of the computer on which the service is running.</span></span> <span data-ttu-id="3a5f8-118">Dies kann ein voll qualifizierter DNS-Name oder ein NetBIOS-Name sein.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-118">This can be a fully qualified DNS name or a NetBIOS name.</span></span> <span data-ttu-id="3a5f8-119">Beachten Sie, dass NetBIOS-Namen innerhalb einer Gesamtstruktur nicht unbedingt eindeutig sind. Folglich ist ein SPN, der einen NetBIOS-Namen enthält, möglicherweise auch nicht eindeutig.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-119">Be aware that NetBIOS names are not guaranteed to be unique in a forest, so an SPN that contains a NetBIOS name may not be unique.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a5f8-120">&quot;&lt;Port&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="3a5f8-120">&quot;&lt;port&gt;&quot;</span></span></td>
<td><span data-ttu-id="3a5f8-121">Eine optionale Portnummer zur Unterscheidung zwischen mehreren Instanzen derselben Dienstklasse auf einem einzelnen Host Computer.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-121">An optional port number to differentiate between multiple instances of the same service class on a single host computer.</span></span> <span data-ttu-id="3a5f8-122">Lassen Sie diese Komponente Weg, wenn der Dienst den Standardport für die Dienstklasse verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-122">Omit this component if the service uses the default port for its service class.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a5f8-123">&quot;&lt;Dienst Name&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="3a5f8-123">&quot;&lt;service name&gt;&quot;</span></span></td>
<td><span data-ttu-id="3a5f8-124">Ein optionaler Name, der in den SPNs eines replizierungsdiensts verwendet wird, um die Daten oder Dienste zu identifizieren, die vom Dienst oder der vom Dienst bereitgestellten Domäne bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-124">An optional name used in the SPNs of a replicable service to identify the data or services provided by the service or the domain served by the service.</span></span> <span data-ttu-id="3a5f8-125">Diese Komponente kann eines der folgenden Formate aufweisen:</span><span class="sxs-lookup"><span data-stu-id="3a5f8-125">This component can have one of the following formats:</span></span>
<ul>
<li><span data-ttu-id="3a5f8-126">Der Distinguished Name oder die objectGUID eines Objekts in Active Directory Domain Services, z. b. ein Dienst Verbindungspunkt (Service Connection Point, SCP).</span><span class="sxs-lookup"><span data-stu-id="3a5f8-126">The distinguished name or objectGUID of an object in Active Directory Domain Services, such as a service connection point (SCP).</span></span></li>
<li><span data-ttu-id="3a5f8-127">Der DNS-Name der Domäne für einen Dienst, der einen angegebenen Dienst für eine Domäne als Ganzes bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-127">The DNS name of the domain for a service that provides a specified service for a domain as a whole.</span></span></li>
<li><span data-ttu-id="3a5f8-128">Der DNS-Name eines SRV-oder MX-Einsatzes.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-128">The DNS name of an SRV or MX record.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3a5f8-129">Welche Komponenten in den SPNs eines dienstanders vorhanden sind, hängt davon ab, wie der Dienst identifiziert und repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-129">The components present in a service's SPNs depend on how the service is identified and replicated.</span></span> <span data-ttu-id="3a5f8-130">Es gibt zwei grundlegende Szenarien: Host basierte Dienste und replizierungsdienste.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-130">There are two basic scenarios: host-based services and replicable services.</span></span>

## <a name="host-based-services"></a><span data-ttu-id="3a5f8-131">Host basierte Dienste</span><span class="sxs-lookup"><span data-stu-id="3a5f8-131">Host-based services</span></span>

<span data-ttu-id="3a5f8-132">Bei einem Host basierten Dienst wird die Komponente " &lt; Dienst Name &gt; " ausgelassen, da der Dienst durch die Dienstklasse und den Namen des Host Computers, auf dem der Dienst installiert ist, eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-132">For a host-based service, the "&lt;service name&gt;" component is omitted because the service is uniquely identified by the service class and the name of the host computer on which the service is installed.</span></span>


```C++
<service class>/<host>
```



<span data-ttu-id="3a5f8-133">Die Dienstklasse allein ist ausreichend, um für Clients die Funktionen zu identifizieren, die der Dienst bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-133">The service class alone is sufficient to identify for clients the features that the service provides.</span></span> <span data-ttu-id="3a5f8-134">Sie können Instanzen der Dienstklasse auf vielen Computern installieren, und jede Instanz bietet Dienste, die mit Ihrem Host Computer identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-134">You can install instances of the service class on many computers and each instance provides services that are identified with its host computer.</span></span> <span data-ttu-id="3a5f8-135">FTP und Telnet sind Beispiele für Host basierte Dienste.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-135">FTP and Telnet are examples of host-based services.</span></span> <span data-ttu-id="3a5f8-136">Die SPNs einer Host basierten Dienst Instanz können die Portnummer enthalten, wenn der Dienst einen nicht standardmäßigen Port verwendet oder mehrere Instanzen des Diensts auf dem Host vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-136">The SPNs of a host-based service instance can include the port number if the service uses a non-default port or there are multiple instances of the service on the host.</span></span>


```C++
<service class>/<host>:<port>
```



## <a name="replicable-services"></a><span data-ttu-id="3a5f8-137">Replizierungsdienste</span><span class="sxs-lookup"><span data-stu-id="3a5f8-137">Replicable services</span></span>

<span data-ttu-id="3a5f8-138">Bei einem replizierbaren Dienst kann eine oder mehrere Instanzen des Dienstanbieter (Replikate) vorhanden sein, und Clients unterscheiden sich nicht, mit welchem Replikat Sie eine Verbindung herstellen, da jeweils derselbe Dienst bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-138">For a replicable service there can be one or many instances of the service (replicas), and clients do not differentiate which replica they connect to because each provides the same service.</span></span> <span data-ttu-id="3a5f8-139">Die SPNs für jedes Replikat verfügen über die gleichen " &lt; Service Class &gt; "-und " &lt; Service Name &gt; "-Komponenten, wobei " &lt; Dienst Name &gt; " genauer identifiziert, welche Funktionen vom Dienst bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-139">The SPNs for each replica have the same "&lt;service class&gt;" and "&lt;service name&gt;" components, where "&lt;service name&gt;" identifies more specifically the features provided by the service.</span></span> <span data-ttu-id="3a5f8-140">Nur die &lt; Komponenten "Host &gt; " und " &lt; Port &gt; " unterscheiden sich von SPN zum SPN.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-140">Only the "&lt;host&gt;" and optional "&lt;port&gt;" components would vary from SPN to SPN.</span></span>


```C++
<service class>/<host>:<port>/<service name>
```



<span data-ttu-id="3a5f8-141">Ein Beispiel für einen replizierbaren Dienst ist eine Instanz eines Daten Bank Dienstanbieter, der den Zugriff auf eine angegebene Datenbank ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-141">An example of a replicable service would be an instance of a database service that provides access to a specified database.</span></span> <span data-ttu-id="3a5f8-142">In diesem Fall identifiziert " &lt; Dienstklasse &gt; " die Datenbankanwendung, und " &lt; Dienst Name &gt; " identifiziert die jeweilige Datenbank.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-142">In this case, "&lt;service class&gt;" identifies the database application and "&lt;service name&gt;" identifies the specific database.</span></span> <span data-ttu-id="3a5f8-143">" &lt; Service Name &gt; " kann der Distinguished Name eines Dienst Verbindungs Punkts (Service Connection Point, SCP) sein, der die Verbindungsdaten für die Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-143">"&lt;service name&gt;" could be the distinguished name of a service connection point (SCP) containing connection data for the database.</span></span>


```C++
MyDBService/host1.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
```



<span data-ttu-id="3a5f8-144">Wenn der NetBIOS-Name von Clients zum Verfassen eines Dienst Prinzipal namens verwendet wird, muss jedes Replikat auch einen SPN registrieren, der den NetBIOS-Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-144">If clients will use the NetBIOS name to compose a service's SPN, each replica must also register an SPN containing the NetBIOS name.</span></span>


```C++
MyDBService/host1/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3/CN=hrdb,OU=mktg,DC=example,DC=com
```



<span data-ttu-id="3a5f8-145">Ein weiteres Beispiel für einen replizierbaren Dienst ist ein Dienst, der Dienste für eine gesamte Domäne bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-145">Another example of a replicable service is one that provides services to an entire domain.</span></span> <span data-ttu-id="3a5f8-146">In diesem Fall &lt; handelt es sich bei der Komponente "Dienst Name &gt; " um den DNS-Namen der Domäne, die bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-146">In this case, the "&lt;service name&gt;" component is the DNS name of the domain being served.</span></span> <span data-ttu-id="3a5f8-147">Ein Kerberos-KDC ist ein Beispiel für diese Art von Replizierungsdienst.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-147">A Kerberos KDC is an example of this type of replicable service.</span></span>

<span data-ttu-id="3a5f8-148">Beachten Sie, dass das System bei einer Änderung des DNS-Namens eines Computers das " &lt; Host &gt; "-Element für alle registrierten SPNs für diesen Host in der Gesamtstruktur aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3a5f8-148">Be aware that if the DNS name of a computer changes, the system updates the "&lt;host&gt;" element for all registered SPNs for that host in the forest.</span></span>

 

 




