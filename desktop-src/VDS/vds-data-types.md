---
description: Die von VDS unterstützten Datentypen definieren Funktions Rückgabewerte, Funktionsparameter und Strukturmember. Datentypen definieren die Größe und Bedeutung dieser Elemente.
ms.assetid: f17e8c7e-e3cb-49ca-9060-2299dda55770
title: VDS-Datentypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a868606110d9cf1c3cad5c3036789d041a5d86c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359539"
---
# <a name="vds-data-types"></a><span data-ttu-id="9212f-104">VDS-Datentypen</span><span class="sxs-lookup"><span data-stu-id="9212f-104">VDS Data Types</span></span>

<span data-ttu-id="9212f-105">\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]</span><span class="sxs-lookup"><span data-stu-id="9212f-105">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="9212f-106">Die von VDS unterstützten Datentypen definieren Funktions Rückgabewerte, Funktionsparameter und Strukturmember.</span><span class="sxs-lookup"><span data-stu-id="9212f-106">The data types supported by VDS define function return values, function parameters, and structure members.</span></span> <span data-ttu-id="9212f-107">Datentypen definieren die Größe und Bedeutung dieser Elemente.</span><span class="sxs-lookup"><span data-stu-id="9212f-107">Data types define the size and meaning of these elements.</span></span>



| <span data-ttu-id="9212f-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9212f-108">Data type</span></span>                                                                                      | <span data-ttu-id="9212f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9212f-109">Description</span></span>                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9212f-110"><span id="VDS_OBJECT_ID"></span><span id="vds_object_id"></span>**VDS- \_ Objekt- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="9212f-110"><span id="VDS_OBJECT_ID"></span><span id="vds_object_id"></span>**VDS\_OBJECT\_ID**</span></span><br/> | <span data-ttu-id="9212f-111">VDS-Objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="9212f-111">VDS object ID.</span></span> <span data-ttu-id="9212f-112">Diese Werte sind in Neustarts nicht garantiert eindeutig.</span><span class="sxs-lookup"><span data-stu-id="9212f-112">These values are not guaranteed to be unique across reboots.</span></span> <br/> <span data-ttu-id="9212f-113">Dieser Typ wird in "VDS. h" (vdshwprv. h für Hardware Anbieter) als GUID deklariert.</span><span class="sxs-lookup"><span data-stu-id="9212f-113">This type is declared in Vds.h (VdsHwPrv.h for hardware providers) as a GUID.</span></span> <br/> |
| <span data-ttu-id="9212f-114"><span id="VDS_PATH_ID"></span><span id="vds_path_id"></span>**VDS- \_ Pfad- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="9212f-114"><span id="VDS_PATH_ID"></span><span id="vds_path_id"></span>**VDS\_PATH\_ID**</span></span><br/>       | <span data-ttu-id="9212f-115">VDS-Pfad-ID für Multipfad-e/a (MPIO).</span><span class="sxs-lookup"><span data-stu-id="9212f-115">VDS path ID for multipath I/O (MPIO).</span></span> <br/> <span data-ttu-id="9212f-116">Dieser Typ wird in "VDS. h" (vdshwprv. h für Hardware Anbieter) als UINT64 deklariert.</span><span class="sxs-lookup"><span data-stu-id="9212f-116">This type is declared in Vds.h (VdsHwPrv.h for hardware providers) as a UINT64.</span></span><br/>                                      |



 

 

