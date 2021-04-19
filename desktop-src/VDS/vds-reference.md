---
description: In diesem Abschnitt wird die Anwendungsprogrammierschnittstelle für den virtuellen Datenträger Dienst (Virtual Disk Service, VDS) beschrieben.
ms.assetid: d00fc772-331f-4d71-a418-e34acdfb6652
title: VDS-Referenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 369111add0b3f4b7e2742c764a6cbf8b1d8bfdd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349276"
---
# <a name="vds-reference"></a><span data-ttu-id="1979a-103">VDS-Referenz</span><span class="sxs-lookup"><span data-stu-id="1979a-103">VDS Reference</span></span>

<span data-ttu-id="1979a-104">\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]</span><span class="sxs-lookup"><span data-stu-id="1979a-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="1979a-105">In diesem Abschnitt wird die Anwendungsprogrammierschnittstelle für den virtuellen Datenträger Dienst (Virtual Disk Service, VDS) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1979a-105">This section describes the application programming interface to the Virtual Disk Service (VDS).</span></span>

<span data-ttu-id="1979a-106">Anwendungsentwickler verwenden die Schnittstellen, Strukturen, Enumerationen und symbolischen Konstanten in dieser API, um Speicher – von Datenträgern zu Speicherarrays abzufragen und zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="1979a-106">Application developers use the interfaces, structures, enumerations, and symbolic constants in this API to query and configure storage—from disks to storage arrays.</span></span> <span data-ttu-id="1979a-107">Eine ausführliche Betrachtung der Beziehung zwischen VDS-Typen finden Sie unter [VDS-Objektmodell](vds-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="1979a-107">For a detailed look at the relationship among VDS types, see the [VDS Object Model](vds-object-model.md).</span></span>

<span data-ttu-id="1979a-108">Speicherhersteller implementieren viele der Schnittstellen, die in diesem Abschnitt definiert sind.</span><span class="sxs-lookup"><span data-stu-id="1979a-108">Storage manufacturers implement many of the interfaces defined in this section.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1979a-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="1979a-109">In this Section</span></span>

<dl> <dt>

[<span data-ttu-id="1979a-110">VDS-Konstanten</span><span class="sxs-lookup"><span data-stu-id="1979a-110">VDS Constants</span></span>](vds-constants.md)
</dt> <dd>

<span data-ttu-id="1979a-111">Listet die symbolischen Konstanten in der VDS-API auf.</span><span class="sxs-lookup"><span data-stu-id="1979a-111">Lists the symbolic constants in the VDS API.</span></span>

</dd> <dt>

[<span data-ttu-id="1979a-112">VDS-Datentypen</span><span class="sxs-lookup"><span data-stu-id="1979a-112">VDS Data Types</span></span>](vds-data-types.md)
</dt> <dd>

<span data-ttu-id="1979a-113">Listet die Datentypen auf, die mit VDS verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1979a-113">Lists the data types used with VDS.</span></span>

</dd> <dt>

[<span data-ttu-id="1979a-114">VDS-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="1979a-114">VDS Enumerations</span></span>](vds-enumerations.md)
</dt> <dd>

<span data-ttu-id="1979a-115">Beschreibt die mit VDS verwendeten Enumerationen.</span><span class="sxs-lookup"><span data-stu-id="1979a-115">Describes the enumerations used with VDS.</span></span>

</dd> <dt>

[<span data-ttu-id="1979a-116">VDS-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1979a-116">VDS Interfaces</span></span>](vds-interfaces.md)
</dt> <dd>

<span data-ttu-id="1979a-117">Beschreibt die VDS-Schnittstellen und die von Ihnen bereitgestellten Methoden.</span><span class="sxs-lookup"><span data-stu-id="1979a-117">Describes VDS interfaces and the methods they expose.</span></span>

</dd> <dt>

[<span data-ttu-id="1979a-118">VDS-Strukturen</span><span class="sxs-lookup"><span data-stu-id="1979a-118">VDS Structures</span></span>](vds-structures.md)
</dt> <dd>

<span data-ttu-id="1979a-119">Beschreibt die Strukturen, die als Parameter an VDS-Methoden übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="1979a-119">Describes the structures passed as parameters to VDS methods.</span></span>

</dd> <dt>

[<span data-ttu-id="1979a-120">Allgemeine Rückgabe Codes für den Dienst für virtuelle Datenträger</span><span class="sxs-lookup"><span data-stu-id="1979a-120">Virtual Disk Service Common Return Codes</span></span>](virtual-disk-service-common-return-codes.md)
</dt> <dd>

<span data-ttu-id="1979a-121">Beschreibt die häufigsten Fehlercodes, die für VDS spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="1979a-121">Describes the most common error codes that are specific to VDS.</span></span>

</dd> <dt>

[<span data-ttu-id="1979a-122">Glossar zum Dienst für virtuelle Datenträger</span><span class="sxs-lookup"><span data-stu-id="1979a-122">Virtual Disk Service Glossary</span></span>](virtual-disk-service-glossary-all.md)
</dt> <dd>

<span data-ttu-id="1979a-123">Glossar der technischen Begriffe, die in der VDS-Dokumentation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1979a-123">Glossary of technical terms used in VDS documentation.</span></span>

</dd> </dl>

 

 
