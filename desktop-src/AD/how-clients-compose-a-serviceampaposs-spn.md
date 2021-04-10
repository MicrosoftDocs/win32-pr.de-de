---
title: Funktionsweise eines Dienst-SPN durch Clients
description: Um einen Dienst zu authentifizieren, stellt eine Client Anwendung einen SPN für die Dienst Instanz dar, mit der eine Verbindung hergestellt werden muss.
ms.assetid: cf6c491a-d84d-4c9c-bd69-1f2264f395b6
ms.tgt_platform: multiple
keywords:
- Zusammenstellen eines Dienst-SPN-AD durch Clients
- Dienst Prinzipal Name AD, wie Clients den SPN eines Dienstanbieter verfassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd8aa599b6d8238017897c9383bab188ce144e0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947385"
---
# <a name="how-clients-compose-a-services-spn"></a><span data-ttu-id="3ea54-105">Funktionsweise eines Dienst-SPN durch Clients</span><span class="sxs-lookup"><span data-stu-id="3ea54-105">How Clients Compose a Service's SPN</span></span>

<span data-ttu-id="3ea54-106">Um einen Dienst zu authentifizieren, stellt eine Client Anwendung einen SPN für die Dienst Instanz dar, mit der eine Verbindung hergestellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="3ea54-106">To authenticate a service, a client application composes an SPN for the service instance to which it must connect.</span></span> <span data-ttu-id="3ea54-107">Die Client Anwendung kann die [**dsmakespn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) -Funktion verwenden, um einen SPN zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3ea54-107">The client application can use the [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) function to compose an SPN.</span></span> <span data-ttu-id="3ea54-108">Der Client gibt die Komponenten des SPN mit bekannten Daten oder Daten an, die aus anderen Quellen als dem Dienst selbst abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="3ea54-108">The client specifies the components of the SPN using known data or data retrieved from sources other than the service itself.</span></span>

<span data-ttu-id="3ea54-109">Die Form eines SPN ist wie in der folgenden Form dargestellt:</span><span class="sxs-lookup"><span data-stu-id="3ea54-109">The form of an SPN is as shown in the following form:</span></span>


```C++
<service class>/<host>:<port>/<service name>
```



<span data-ttu-id="3ea54-110">In dieser Form sind " &lt; Service Class &gt; " und " &lt; Host &gt; " erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3ea54-110">In this form, "&lt;service class&gt;" and "&lt;host&gt;" are required.</span></span> <span data-ttu-id="3ea54-111">" &lt; Port &gt; " und " &lt; Dienst Name &gt; " sind optional.</span><span class="sxs-lookup"><span data-stu-id="3ea54-111">"&lt;port&gt;" and "&lt;service name&gt;" optional.</span></span>

<span data-ttu-id="3ea54-112">In der Regel erkennt der Client den &lt; &gt; Teil des Namens "Service Class" und erkennt, welche der optionalen Komponenten in den SPN eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3ea54-112">Typically, the client recognizes the "&lt;service class&gt;" part of the name, and recognizes which of the optional components to include in the SPN.</span></span> <span data-ttu-id="3ea54-113">Der Client kann die Komponenten des SPN von Quellen abrufen, z. b. einem Dienst Verbindungspunkt (Service Connection Point, SCP) oder Benutzereingaben.</span><span class="sxs-lookup"><span data-stu-id="3ea54-113">The client can retrieve components of the SPN from sources such as a service connection point (SCP) or user input.</span></span> <span data-ttu-id="3ea54-114">Beispielsweise kann der Client das **servicednsname** -Attribut des Dienst Verbindungs Punkts eines Diensts lesen, um die " &lt; Host"-Komponente zu erhalten &gt; .</span><span class="sxs-lookup"><span data-stu-id="3ea54-114">For example, the client can read the **serviceDNSName** attribute of a service's SCP to get the "&lt;host&gt;" component.</span></span> <span data-ttu-id="3ea54-115">Das **servicednsname** -Attribut enthält entweder den DNS-Namen des Servers, auf dem die Dienst Instanz ausgeführt wird, oder den DNS-Namen von SRV-Datensätzen, die die Hostdaten für Dienst Replikate enthalten.</span><span class="sxs-lookup"><span data-stu-id="3ea54-115">The **serviceDNSName** attribute contains either the DNS name of the server on which the service instance is running or the DNS name of SRV records containing the host data for service replicas.</span></span> <span data-ttu-id="3ea54-116">Die " &lt; Service Name &gt; "-Komponente, die nur für replizierungsdienste verwendet wird, kann der Distinguished Name des Dienst Verbindungs Diensts, der DNS-Name der Domäne, die vom Dienst bereitgestellt wird, oder der DNS-Name der SRV-oder MX-Einträge sein.</span><span class="sxs-lookup"><span data-stu-id="3ea54-116">The "&lt;service name&gt;" component, used only for replicable services, can be the distinguished name of the service's SCP, the DNS name of the domain served by the service, or the DNS name of SRV or MX records.</span></span>

<span data-ttu-id="3ea54-117">Weitere Informationen und ein Codebeispiel zum Erstellen eines SPN für einen Dienst finden Sie unter [How a Client authenticates a SCP-based Windows Sockets Service](how-a-client-authenticates-an-scp-based-windows-sockets-service.md).</span><span class="sxs-lookup"><span data-stu-id="3ea54-117">For more information and a code example used to compose an SPN for a service, see [How a Client Authenticates an SCP-based Windows Sockets Service](how-a-client-authenticates-an-scp-based-windows-sockets-service.md).</span></span>

<span data-ttu-id="3ea54-118">Weitere Informationen und eine Beschreibung der SPN-Komponenten finden Sie unter [namens Formate für eindeutige SPNs](name-formats-for-unique-spns.md).</span><span class="sxs-lookup"><span data-stu-id="3ea54-118">For more information and a description of the SPN components, see [Name Formats for Unique SPNs](name-formats-for-unique-spns.md).</span></span>

 

 




