---
description: Verwenden des com+-CRM in einer Cluster Umgebung
ms.assetid: 753461c5-880c-4df0-b552-b962dc06524f
title: Verwenden des com+-CRM in einer Cluster Umgebung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a05ff281748c35128349ef5d0d0f43d7beae86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342239"
---
# <a name="using-the-com-crm-in-a-cluster-environment"></a><span data-ttu-id="7bb53-103">Verwenden des com+-CRM in einer Cluster Umgebung</span><span class="sxs-lookup"><span data-stu-id="7bb53-103">Using the COM+ CRM in a Cluster Environment</span></span>

<span data-ttu-id="7bb53-104">Wenn Sie com+-CRMs für die Arbeit in Cluster Umgebungen entwickeln, besteht der wichtigste Faktor darin, zu berücksichtigen, ob ein bestimmtes CRM den Knoten des Clusters, auf dem er ausgeführt wird, interessiert.</span><span class="sxs-lookup"><span data-stu-id="7bb53-104">When developing COM+ CRMs to work in cluster environments, the main factor to consider is whether a specific CRM cares which node of the cluster it is operating on.</span></span> <span data-ttu-id="7bb53-105">Wenn die vom CRM verwaltete Ressource z. b. das Dateisystem oder die Registrierung des Computers ist, gelten alle Änderungen speziell für den Knoten, auf dem die CRM-Serveranwendung zu diesem Zeitpunkt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7bb53-105">For example, if the resource managed by the CRM is the machine file system or registry, any changes are specific to the node that the CRM server application is running on at the time.</span></span> <span data-ttu-id="7bb53-106">In diesem Fall wäre es nicht wünschenswert, ein Failover der CRM-Serveranwendung auf einen anderen Knoten durchzusetzen.</span><span class="sxs-lookup"><span data-stu-id="7bb53-106">In this case, failover of the CRM server application to another node would not be desirable.</span></span> <span data-ttu-id="7bb53-107">In einem anderen Fall, in dem das CRM einige Ressourcen verwaltet, die dem Cluster gemeinsam sind, ist das Failover der CRM-Serveranwendung auf einen anderen Knoten hilfreich.</span><span class="sxs-lookup"><span data-stu-id="7bb53-107">In a different case, where the CRM is managing some resource common to the cluster, failover of the CRM server application to another node is useful.</span></span>

<span data-ttu-id="7bb53-108">Der Standardverzeichnis Pfad für CRM-Protokolldateien ist dasselbe Verzeichnis wie die DTC-Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="7bb53-108">The default directory location for CRM log files is the same directory as the DTC log file.</span></span> <span data-ttu-id="7bb53-109">In Clustern wird die DTC-Protokolldatei auf einem freigegebenen Datenträger platziert, für den ein Failover zwischen den Knoten des Clusters ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7bb53-109">On clusters, the DTC log file is placed on a shared disk that is failed over between the nodes of the cluster.</span></span> <span data-ttu-id="7bb53-110">Dies bedeutet, dass das Standardverhalten für CRM-Server Anwendungen für ein Failover zwischen den Knoten des Clusters verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7bb53-110">This means that the default behavior for CRM server applications is to failover between nodes of the cluster.</span></span> <span data-ttu-id="7bb53-111">Wenn ein bestimmtes CRM das alternative Verhalten des Failovers zwischen Knoten erfordert, sollte daher der Speicherort der CRM-Protokolldatei für diese bestimmte CRM-Serveranwendung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="7bb53-111">Therefore, if a specific CRM requires the alternative behavior of not failing over between nodes, the location of the CRM log file for that particular CRM server application should be changed.</span></span>

<span data-ttu-id="7bb53-112">Wenn außerdem ein Failover für die CRM-Anwendung erforderlich ist, sollte es als generische Anwendung in einer Clustergruppe konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="7bb53-112">In addition, if failover is required for the CRM application, it should be configured as a generic application in a cluster group.</span></span> <span data-ttu-id="7bb53-113">Die Abhängigkeit sollte DTC lauten.</span><span class="sxs-lookup"><span data-stu-id="7bb53-113">Its dependency should be DTC.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7bb53-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7bb53-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bb53-115">Kompensierende com+-Ressourcen-Manager Konzepte</span><span class="sxs-lookup"><span data-stu-id="7bb53-115">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



