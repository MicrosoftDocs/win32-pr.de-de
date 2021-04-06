---
title: Abfrageschnittstellen
description: Zum Durchführen von Verzeichnis suchen können drei Typen von ADSI-Schnittstellen verwendet werden. Die Anwendungsumgebung und andere Anforderungen geben möglicherweise an, welche Schnittstelle verwendet wird.
ms.assetid: 42843e02-b685-492e-9046-aea460e84584
ms.tgt_platform: multiple
keywords:
- Abfrageschnittstellen ADSI
- Abfragen von ADSI, Abfrageschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805303a972b4a8140a9e632857287aeebca9b32f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855260"
---
# <a name="query-interfaces"></a><span data-ttu-id="47973-106">Abfrageschnittstellen</span><span class="sxs-lookup"><span data-stu-id="47973-106">Query Interfaces</span></span>

<span data-ttu-id="47973-107">Zum Durchführen von Verzeichnis suchen können drei Typen von ADSI-Schnittstellen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47973-107">Three types of ADSI interfaces can be used to perform directory searches.</span></span> <span data-ttu-id="47973-108">Die Anwendungsumgebung und andere Anforderungen geben möglicherweise an, welche Schnittstelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="47973-108">The application environment and other requirements may indicate which interface is used.</span></span>

-   <span data-ttu-id="47973-109">[**Idirectoriysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch).</span><span class="sxs-lookup"><span data-stu-id="47973-109">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch).</span></span> <span data-ttu-id="47973-110">**Idirector ysearch** ist eine grundlegende COM-Schnittstelle, die nur für C/C++-Programmierer verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="47973-110">**IDirectorySearch** is a basic COM interface only available to C/C++ programmers.</span></span> <span data-ttu-id="47973-111">Weitere Informationen finden Sie unter [Suchen mit der idirector ysearch-Schnittstelle](searching-with-idirectorysearch.md).</span><span class="sxs-lookup"><span data-stu-id="47973-111">For more information, see [Searching With the IDirectorySearch Interface](searching-with-idirectorysearch.md).</span></span>
-   <span data-ttu-id="47973-112">ADOs.</span><span class="sxs-lookup"><span data-stu-id="47973-112">ADO.</span></span> <span data-ttu-id="47973-113">Die ADO-Schnittstellen (ActiveX Data Object) sind Automatisierungs Schnittstellen, die OLE DB verwenden.</span><span class="sxs-lookup"><span data-stu-id="47973-113">The ActiveX Data Object (ADO) interfaces are Automation interfaces that use OLE DB.</span></span> <span data-ttu-id="47973-114">Verwenden Sie ADO für Abfragen in Anwendungen, die auf Automation basieren.</span><span class="sxs-lookup"><span data-stu-id="47973-114">Use ADO for queries within applications that rely on Automation.</span></span> <span data-ttu-id="47973-115">Dazu zählen Visual Basic Anwendungen, Active Server Seiten usw.</span><span class="sxs-lookup"><span data-stu-id="47973-115">These include Visual Basic applications, Active Server Pages, and so on.</span></span> <span data-ttu-id="47973-116">Weitere Informationen finden Sie unter [Suchen mit ActiveX Data Objects](searching-with-activex-data-objects-ado.md).</span><span class="sxs-lookup"><span data-stu-id="47973-116">For more information, see [Searching with ActiveX Data Objects](searching-with-activex-data-objects-ado.md).</span></span>
-   <span data-ttu-id="47973-117">OLE DB.</span><span class="sxs-lookup"><span data-stu-id="47973-117">OLE DB.</span></span> <span data-ttu-id="47973-118">OLE DB ist ein Satz von C/C++-Schnittstellen, mit denen Datenbanken abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="47973-118">OLE DB is a set of C/C++ interfaces used to query databases.</span></span> <span data-ttu-id="47973-119">Durch die Unterstützung dieser Schnittstellen können ADSI-Anbieter erweiterte OLE DB Features implementieren, z. b. verteilte Abfragen mit anderen OLE DB Anbietern.</span><span class="sxs-lookup"><span data-stu-id="47973-119">By supporting these interfaces, ADSI providers can implement advanced OLE DB features, such as distributed queries with other OLE DB providers.</span></span> <span data-ttu-id="47973-120">Weitere Informationen finden Sie unter [Suchen mit OLE DB](searching-with-ole-db.md).</span><span class="sxs-lookup"><span data-stu-id="47973-120">For more information, see [Searching with OLE DB](searching-with-ole-db.md).</span></span>

 

 




