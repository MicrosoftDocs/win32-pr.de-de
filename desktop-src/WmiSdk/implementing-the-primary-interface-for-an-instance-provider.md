---
title: Implementieren der primären Schnittstelle eines Instanzanbieters
description: Ein Instanzanbieter verwendet die asynchronen Methoden von IWbemServices als primäre Schnittstelle zu WMI.
ms.assetid: 80425fa8-2746-4eba-8e7d-4a61e222852a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443b095cfbb134cf031ae8e1403565bc1fa31aea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360695"
---
# <a name="implementing-an-instance-provider-primary-interface"></a><span data-ttu-id="73370-103">Implementieren der primären Schnittstelle eines Instanzanbieters</span><span class="sxs-lookup"><span data-stu-id="73370-103">Implementing an instance provider primary interface</span></span>

<span data-ttu-id="73370-104">Ein Instanzanbieter verwendet die asynchronen Methoden von [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) als primäre Schnittstelle zu WMI.</span><span class="sxs-lookup"><span data-stu-id="73370-104">An instance provider uses the asynchronous methods of [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) as the primary interface to WMI.</span></span> <span data-ttu-id="73370-105">Indem nur die Methoden implementiert werden, die die Anforderungen Ihres Instanzanbieters erfüllen, können Sie die Menge der Ressourcen verringern, die Sie codieren.</span><span class="sxs-lookup"><span data-stu-id="73370-105">By implementing only the methods that fulfill the needs of your instance provider, you can reduce the amount of resources you spend coding.</span></span> <span data-ttu-id="73370-106">Durch Implementieren von Methoden, die für andere Anbieter Typen reserviert sind, können Sie jedoch die Anzahl der von Ihnen geschriebenen Anbieter reduzieren.</span><span class="sxs-lookup"><span data-stu-id="73370-106">However, by implementing methods reserved for other types of providers, you can reduce the number of providers you write.</span></span>

<span data-ttu-id="73370-107">Da es auch von Anwendungen und Anbietern verwendet wird, um Dienste von WMI anzufordern, enthält [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) viele Methoden, die für einen Instanzanbieter irrelevant sind.</span><span class="sxs-lookup"><span data-stu-id="73370-107">Because it is also used by applications and providers to request services of WMI, [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) contains many methods that are irrelevant to an instance provider.</span></span> <span data-ttu-id="73370-108">In der folgenden Tabelle sind die **IWbemServices** -Methoden aufgelistet, die Sie für einen Instanzanbieter implementieren können.</span><span class="sxs-lookup"><span data-stu-id="73370-108">The following table lists the **IWbemServices** methods that you can implement for an instance provider.</span></span>



| <span data-ttu-id="73370-109">Methode</span><span class="sxs-lookup"><span data-stu-id="73370-109">Method</span></span>                                                                   | <span data-ttu-id="73370-110">Funktion</span><span class="sxs-lookup"><span data-stu-id="73370-110">Feature</span></span>          |
|--------------------------------------------------------------------------|------------------|
| [<span data-ttu-id="73370-111">**GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="73370-111">**GetObjectAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   | <span data-ttu-id="73370-112">Auslagerung</span><span class="sxs-lookup"><span data-stu-id="73370-112">Retrieval</span></span>        |
| [<span data-ttu-id="73370-113">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="73370-113">**PutInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               | <span data-ttu-id="73370-114">Modifikation (Modification)</span><span class="sxs-lookup"><span data-stu-id="73370-114">Modification</span></span>     |
| [<span data-ttu-id="73370-115">**Delta einstanceasync**</span><span class="sxs-lookup"><span data-stu-id="73370-115">**DeleteInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)         | <span data-ttu-id="73370-116">Löschen</span><span class="sxs-lookup"><span data-stu-id="73370-116">Deletion</span></span>         |
| [<span data-ttu-id="73370-117">**"Kreateingestanceenumasync"**</span><span class="sxs-lookup"><span data-stu-id="73370-117">**CreateInstanceEnumAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) | <span data-ttu-id="73370-118">Enumeration</span><span class="sxs-lookup"><span data-stu-id="73370-118">Enumeration</span></span>      |
| [<span data-ttu-id="73370-119">**ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="73370-119">**ExecQueryAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   | <span data-ttu-id="73370-120">Abfrageverarbeitung</span><span class="sxs-lookup"><span data-stu-id="73370-120">Query processing</span></span> |



 

<span data-ttu-id="73370-121">Für Methoden, die Sie nicht verwenden, kann der Anbieter eine Stubimplementierung bereitstellen, die den **WBEM \_ E- \_ Anbieter \_ nicht \_** unterstützt.</span><span class="sxs-lookup"><span data-stu-id="73370-121">For methods that you do not use, your provider can supply a stub implementation that returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE**.</span></span> <span data-ttu-id="73370-122">Dies schließt alle [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Methoden ein, die nicht in der obigen Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="73370-122">This includes all [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) methods not listed in the above table.</span></span>

<span data-ttu-id="73370-123">Ein einzelner Anbieter kann durch ordnungsgemäße Registrierung und Implementierung aller relevanten Methoden gleichzeitig als Klasse, Instanz und Methoden Anbieter agieren.</span><span class="sxs-lookup"><span data-stu-id="73370-123">A single provider can act simultaneously as a class, instance, and method provider by proper registration and implementation of all relevant methods.</span></span> <span data-ttu-id="73370-124">Weitere Informationen finden Sie unter [Schreiben eines Klassen Anbieters](writing-a-class-provider.md) und [Schreiben eines Methoden Anbieters](writing-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="73370-124">For more information, see [Writing a Class Provider](writing-a-class-provider.md) and [Writing a Method Provider](writing-a-method-provider.md).</span></span>

 

 



