---
title: Löschen einer Anwendungsverzeichnis Partition
description: Eine Anwendungsverzeichnis Partition wird gelöscht, indem das CrossRef-Objekt gelöscht wird, das die Anwendungsverzeichnis Partition darstellt.
ms.assetid: bc7986c1-5a11-440c-924e-dc525b5cb78f
ms.tgt_platform: multiple
keywords:
- Löschen einer Anwendungsverzeichnis-Partitions Anzeige
- Anwendungsverzeichnis Partitionen AD, löschen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd52ef99323ee7463a4733210314e02d911f0d66
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724576"
---
# <a name="deleting-an-application-directory-partition"></a><span data-ttu-id="596af-105">Löschen einer Anwendungsverzeichnis Partition</span><span class="sxs-lookup"><span data-stu-id="596af-105">Deleting an Application Directory Partition</span></span>

<span data-ttu-id="596af-106">Eine Anwendungsverzeichnis Partition wird gelöscht, indem das [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekt gelöscht wird, das die Anwendungsverzeichnis Partition darstellt.</span><span class="sxs-lookup"><span data-stu-id="596af-106">An application directory partition is deleted by deleting the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object that represents the application directory partition.</span></span> <span data-ttu-id="596af-107">Wenn das Löschen des **CrossRef** -Objekts auf einen Domänen Controller repliziert wird, der über ein Replikat der Anwendungsverzeichnis Partition verfügt, löscht die KCC das lokale Replikat der Anwendungsverzeichnis Partition.</span><span class="sxs-lookup"><span data-stu-id="596af-107">When the deletion of the **crossRef** object replicates to a domain controller that has a replica of the application directory partition, the KCC will delete the local replica of the application directory partition.</span></span> <span data-ttu-id="596af-108">Dies bewirkt schließlich, dass alle Replikate der Anwendungsverzeichnis Partition gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="596af-108">This eventually causes all replicas of the application directory partition to be deleted.</span></span>

<span data-ttu-id="596af-109">Wenn das [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekt gelöscht wird, löscht der Active Directory Server das [**domainDns**](/windows/desktop/ADSchema/c-domaindns) -Objekt, das beim Erstellen der Anwendungsverzeichnis Partition erstellt wurde, und löscht alle Objekte in der Anwendungsverzeichnis Partition.</span><span class="sxs-lookup"><span data-stu-id="596af-109">When the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object is deleted, the Active Directory server will delete the [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) object that was created when the application directory partition was created, as well as deleting all objects in the application directory partition.</span></span> <span data-ttu-id="596af-110">Keines der Objekte in der Anwendungsverzeichnis Partition wird gelöscht, wenn Sie gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="596af-110">None of the objects in the application directory partition are tombstoned when they deleted.</span></span>

<span data-ttu-id="596af-111">Wenn eine Anwendungsverzeichnis Partition gelöscht wird, ist es sehr schwierig, Sie wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="596af-111">When an application directory partition is deleted, it is very difficult to restore it.</span></span> <span data-ttu-id="596af-112">Zum Wiederherstellen einer Anwendungsverzeichnis Partition ist es erforderlich, eine Sicherung mit einem Replikat der Anwendungsverzeichnis Partition wiederherzustellen, das [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekt zu suchen, das die Anwendungsverzeichnis Partition darstellt, und das **CrossRef** -Objekt autoritativ wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="596af-112">To restore an application directory partition, it is necessary to restore a backup that has a replica of the application directory partition, find the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object that represents the application directory partition and authoritatively restore the **crossRef** object.</span></span>

<span data-ttu-id="596af-113">**Führen Sie die folgenden Schritte aus, um eine Anwendungsverzeichnis Partition und deren Replikate zu löschen.**</span><span class="sxs-lookup"><span data-stu-id="596af-113">**To delete an application directory partition and its replicas, perform the following steps**</span></span>

1.  <span data-ttu-id="596af-114">Durchsuchen Sie den Container Partitionen nach einem [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekt, das einen [**NCName**](/windows/desktop/ADSchema/a-ncname) -Attribut Wert aufweist, der gleich dem Distinguished Name der Anwendungsverzeichnis Partition ist.</span><span class="sxs-lookup"><span data-stu-id="596af-114">Search the Partitions container for a [**crossRef**](/windows/desktop/ADSchema/c-crossref) object that has an [**nCName**](/windows/desktop/ADSchema/a-ncname) attribute value that is equal to the distinguished name of the application directory partition.</span></span>
2.  <span data-ttu-id="596af-115">Löschen Sie das [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="596af-115">Delete the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object.</span></span>

<span data-ttu-id="596af-116">Weitere Informationen finden Sie unter [Beispiel Code zum Löschen einer Anwendungsverzeichnis Partition](example-code-for-deleting-an-application-directory-partition.md).</span><span class="sxs-lookup"><span data-stu-id="596af-116">For more information, see [Example Code for Deleting an Application Directory Partition](example-code-for-deleting-an-application-directory-partition.md).</span></span>

 

 