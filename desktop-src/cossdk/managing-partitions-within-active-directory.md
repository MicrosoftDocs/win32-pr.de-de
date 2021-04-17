---
description: Als Alternative zur Verwaltung von Active Directory Partitionen über das Verwaltungs Tool "Active Directory Benutzer und Computer" können Sie COM+-Partitionen Programm gesteuert verwalten, indem Sie eine Reihe von COM+-Objekten in der Active Directory System Schnittstelle (ADSI) verwenden.
ms.assetid: 915b4643-cbda-433a-a383-65a6b0fd0874
title: Verwalten von Partitionen in Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6635e49b7d2833a1e6e177c25f9f2fb05ff0dff4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524176"
---
# <a name="managing-partitions-within-active-directory"></a><span data-ttu-id="95f8e-103">Verwalten von Partitionen in Active Directory</span><span class="sxs-lookup"><span data-stu-id="95f8e-103">Managing Partitions Within Active Directory</span></span>

<span data-ttu-id="95f8e-104">Als Alternative zur Verwaltung von Active Directory Partitionen über das Verwaltungs Tool "Active Directory Benutzer und Computer" können Sie COM+-Partitionen Programm gesteuert verwalten, indem Sie eine Reihe von COM+-Objekten in der Active Directory System Schnittstelle (ADSI) verwenden.</span><span class="sxs-lookup"><span data-stu-id="95f8e-104">As an alternative to managing Active Directory partitions through the Active Directory Users and Computers administrative tool, you can manage COM+ partitions programmatically through the use of a set of COM+ objects within Active Directory System Interface (ADSI).</span></span>

<span data-ttu-id="95f8e-105">Unabhängig von der administrativen Methode, die Sie für die Verwaltung von COM+-Partitionen auswählen, gibt es eine allgemeine Abfolge von Schritten, die Administratoren befolgen müssen:</span><span class="sxs-lookup"><span data-stu-id="95f8e-105">Regardless of the administrative technique you choose for managing COM+ partitions, there is a general sequence of steps that administrators must follow:</span></span>

1.  <span data-ttu-id="95f8e-106">Erstellen Sie die neuen COM+-Partitionen in Active Directory für Ihre Domäne.</span><span class="sxs-lookup"><span data-stu-id="95f8e-106">Create the new COM+ partitions within Active Directory for your domain.</span></span>
2.  <span data-ttu-id="95f8e-107">Erstellen Sie com+-Partitions Sätze innerhalb Active Directory, und ordnen Sie Sie den neu erstellten COM+-Partitionen zu.</span><span class="sxs-lookup"><span data-stu-id="95f8e-107">Create COM+ partition sets within Active Directory, and map them to your newly created COM+ partitions.</span></span>
3.  <span data-ttu-id="95f8e-108">Konfigurieren Sie Ihre Active Directory Partitionen auf dem lokalen Computer mit dem entsprechenden COM+-Objekt.</span><span class="sxs-lookup"><span data-stu-id="95f8e-108">Configure your Active Directory partitions on your local machine, using the appropriate COM+ object.</span></span> <span data-ttu-id="95f8e-109">Wenn Sie eine Active Directory Partition auf einem lokalen Computer konfigurieren, wird automatisch ein **com+-Anwendungs** Ordner in diesem Partitions Ordner erstellt.</span><span class="sxs-lookup"><span data-stu-id="95f8e-109">When you configure an Active Directory partition on a local machine, a **COM+ Applications** folder is automatically created in that partition folder.</span></span>
4.  <span data-ttu-id="95f8e-110">Installieren Sie die com+-Anwendungen in den entsprechenden COM+-Partitionen.</span><span class="sxs-lookup"><span data-stu-id="95f8e-110">Install your COM+ applications in the appropriate COM+ partitions.</span></span>

<span data-ttu-id="95f8e-111">Alle vorangehenden Schritte können Programm gesteuert mithilfe eines Satzes von Active Directory-Schnittstellen namens ADSI ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="95f8e-111">All of the preceding steps can be done programmatically, using a set of Active Directory interfaces called ADSI.</span></span> <span data-ttu-id="95f8e-112">Die verfügbaren Objekte zum Verwalten von Partitionen, die in ADSI verfügbar sind, lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="95f8e-112">The objects available for managing partitions that are available within ADSI are as follows:</span></span>

-   <span data-ttu-id="95f8e-113">DS \_ userpartitionsetlink- \_ Name</span><span class="sxs-lookup"><span data-stu-id="95f8e-113">DS\_USERPARTITIONSETLINK\_NAME</span></span>
-   <span data-ttu-id="95f8e-114">DS- \_ \_ partitionlinkname</span><span class="sxs-lookup"><span data-stu-id="95f8e-114">DS\_PARTITIONLINK\_NAME</span></span>
-   <span data-ttu-id="95f8e-115">Name der DS- \_ objectID \_</span><span class="sxs-lookup"><span data-stu-id="95f8e-115">DS\_OBJECTID\_NAME</span></span>
-   <span data-ttu-id="95f8e-116">DS \_ defaultpartitionlinkname \_</span><span class="sxs-lookup"><span data-stu-id="95f8e-116">DS\_DEFAULTPARTITIONLINK\_NAME</span></span>
-   <span data-ttu-id="95f8e-117">Name des DS- \_ Benutzer Links \_</span><span class="sxs-lookup"><span data-stu-id="95f8e-117">DS\_USERLINK\_NAME</span></span>
-   <span data-ttu-id="95f8e-118">DS \_ partitionset- \_ Name</span><span class="sxs-lookup"><span data-stu-id="95f8e-118">DS\_PARTITIONSET\_NAME</span></span>
-   <span data-ttu-id="95f8e-119">Name der DS- \_ Partition \_</span><span class="sxs-lookup"><span data-stu-id="95f8e-119">DS\_PARTITION\_NAME</span></span>

<span data-ttu-id="95f8e-120">Informationen zum Erstellen und Verwalten von COM+-Partitionen durch die Verwendung der Active Directory Benutzer und Computer und Verwaltungs Tools für Komponenten Dienste finden Sie in der Online Hilfe, die in den einzelnen Tools verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="95f8e-120">For information on creating and managing COM+ partitions through the use of the Active Directory Users and Computers and Component Services administrative tools, see the online help available from within each tool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="95f8e-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="95f8e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95f8e-122">Sammeln von Partitions Metriken</span><span class="sxs-lookup"><span data-stu-id="95f8e-122">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="95f8e-123">Konfigurieren des Partitions Caches</span><span class="sxs-lookup"><span data-stu-id="95f8e-123">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="95f8e-124">Gruppieren von Anwendungen in Partitionen</span><span class="sxs-lookup"><span data-stu-id="95f8e-124">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="95f8e-125">Verwalten von lokalen Partitionen</span><span class="sxs-lookup"><span data-stu-id="95f8e-125">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="95f8e-126">Festlegen von Administratorrechten für eine Partition</span><span class="sxs-lookup"><span data-stu-id="95f8e-126">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



