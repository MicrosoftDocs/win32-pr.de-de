---
title: Filtergewichtungszuweisung
description: Jeder Filter in der Windows-Filter Plattform (Windows Filtering Platform, WFP) verfügt über eine zugeordnete Gewichtung, die bei der Filterung von Filtern verwendet wird.
ms.assetid: c78854c2-9aa1-408f-82d6-4b9e52f38e84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c77982258bb9c8ef14e22b20e28b6a3039456ae
ms.sourcegitcommit: 013de6f5280f28a9b04c3cce9387e629b07d70fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/26/2020
ms.locfileid: "104390068"
---
# <a name="filter-weight-assignment"></a><span data-ttu-id="b0f21-103">Filtergewichtungszuweisung</span><span class="sxs-lookup"><span data-stu-id="b0f21-103">Filter Weight Assignment</span></span>

<span data-ttu-id="b0f21-104">Jeder Filter in der Windows-Filter Plattform (Windows Filtering Platform, WFP) verfügt über eine zugeordnete Gewichtung, die bei der [Filterung von Filtern](filter-arbitration.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b0f21-104">Every filter in the Windows Filtering Platform (WFP) has an associated weight, which is used during [filter arbitration](filter-arbitration.md).</span></span>

<span data-ttu-id="b0f21-105">Die von der Basis Filter-Engine (BFE) verwendete Filter Gewichtung ist vom Typ " [**f \_ UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)".</span><span class="sxs-lookup"><span data-stu-id="b0f21-105">The filter weight used by the Base Filtering Engine (BFE) is of type [**FWP\_UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span> <span data-ttu-id="b0f21-106">Aufrufer haben beim Hinzufügen von Filtern drei Möglichkeiten.</span><span class="sxs-lookup"><span data-stu-id="b0f21-106">Callers have three options when adding filters.</span></span>

-   <span data-ttu-id="b0f21-107">Legen Sie die Gewichtung auf eine [**FWP- \_ UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)fest.</span><span class="sxs-lookup"><span data-stu-id="b0f21-107">Set the weight to an [**FWP\_UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span> <span data-ttu-id="b0f21-108">BFE verwendet die angegebene Gewichtung unverändert.</span><span class="sxs-lookup"><span data-stu-id="b0f21-108">BFE uses the supplied weight as is.</span></span>
-   <span data-ttu-id="b0f21-109">Legen Sie die Gewichtung auf [**FWP \_ leer**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)fest.</span><span class="sxs-lookup"><span data-stu-id="b0f21-109">Set the weight to [**FWP\_EMPTY**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span> <span data-ttu-id="b0f21-110">BFE generiert automatisch eine Gewichtung im Bereich von \[ 0, 2 ⁶ ⁰).</span><span class="sxs-lookup"><span data-stu-id="b0f21-110">BFE automatically generates a weight in the range \[0, 2⁶⁰).</span></span>
-   <span data-ttu-id="b0f21-111">Legen Sie die Gewichtung auf eine [**FWP- \_ Uint8**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) im Bereich von \[ 0 bis 15 fest \] .</span><span class="sxs-lookup"><span data-stu-id="b0f21-111">Set the weight to an [**FWP\_UINT8**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) in the range \[0, 15\].</span></span> <span data-ttu-id="b0f21-112">BFE verwendet die angegebene Gewichtung als Gewichtungs Bereichs Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="b0f21-112">BFE uses the supplied weight as a weight range identifier.</span></span>

    <span data-ttu-id="b0f21-113">BFE generiert automatisch die nieder wertigen 60 Bits (genau so, als ob die Gewichtung auf [**FWP \_ empty**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)festgelegt wurde), und verwendet dann den bereitgestellten Wert, um die vier hohen Bestell Bits festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b0f21-113">BFE automatically generates the low-order 60 bits (exactly as if the weight had been set to [**FWP\_EMPTY**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)), and then uses the supplied value to set the 4 high-order bits.</span></span> <span data-ttu-id="b0f21-114">Dadurch können Aufrufer den Gewichtungs Bereich manuell in 16 Bereiche aufteilen, während gleichzeitig die automatische Gewichtung innerhalb eines Bereichs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b0f21-114">This allows callers to manually divide the weight space into 16 ranges, while still using automatic weighting within a range.</span></span>

> [!Note]  
> <span data-ttu-id="b0f21-115">Wenn zwei oder mehr Legenden auf derselben Unterschicht registriert werden, können Probleme auftreten, wenn die gleiche Gewichtung den Filtern zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="b0f21-115">When two or more callouts are registered at the same sublayer, problems may occur when the same weight is assigned to the filters.</span></span> <span data-ttu-id="b0f21-116">Dieses Problem kann verhindert werden, indem [**Sie mithilfe von**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayeradd0)"Legenden" eine eigene Unterschicht erstellen.</span><span class="sxs-lookup"><span data-stu-id="b0f21-116">This issue can be prevented by having callouts create their own sublayer by using [**FwpmSubLayerAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayeradd0).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b0f21-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b0f21-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0f21-118">**Filtern von Gewichtungs bezeichlern**</span><span class="sxs-lookup"><span data-stu-id="b0f21-118">**Filter Weight Identifiers**</span></span>](filter-weight-identifiers.md)
</dt> </dl>

 

 




