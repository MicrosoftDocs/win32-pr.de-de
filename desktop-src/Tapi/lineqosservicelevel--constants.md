---
description: Diese Konstanten werden von einem TSP verwendet, um den Typ einer erforderlichen QoS-Ebene (Quality of Service) zu identifizieren.
ms.assetid: 9fc3f6eb-7103-43c5-84f8-3842757e5be7
title: LINEQOSSERVICELEVEL_ Konstanten (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c0629715e461a15e21e1730f86edb61d83d60db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356024"
---
# <a name="lineqosservicelevel_-constants"></a><span data-ttu-id="cacfc-103">Lineqosservicelevel- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="cacfc-103">LINEQOSSERVICELEVEL\_ Constants</span></span>

<span data-ttu-id="cacfc-104">Diese Konstanten werden von einem TSP verwendet, um den Typ einer erforderlichen QoS-Ebene (Quality of Service) zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="cacfc-104">These constants are used by a TSP to identify the type of a QoS (Quality of Service) level required.</span></span>

<dl> <dt>

<span data-ttu-id="cacfc-105"><span id="LINEQOSSERVICELEVEL_NEEDED"></span><span id="lineqosservicelevel_needed"></span>**lineqosservicelevel \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="cacfc-105"><span id="LINEQOSSERVICELEVEL_NEEDED"></span><span id="lineqosservicelevel_needed"></span>**LINEQOSSERVICELEVEL\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="cacfc-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="cacfc-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="cacfc-107">Die geforderte Quality of Service Level ist eine Voraussetzung.</span><span class="sxs-lookup"><span data-stu-id="cacfc-107">The quality of service level requested is a requirement.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cacfc-108"><span id="LINEQOSSERVICELEVEL_IFAVAILABLE"></span><span id="lineqosservicelevel_ifavailable"></span>**lineqosservicelevel \_ ifavailable**</span><span class="sxs-lookup"><span data-stu-id="cacfc-108"><span id="LINEQOSSERVICELEVEL_IFAVAILABLE"></span><span id="lineqosservicelevel_ifavailable"></span>**LINEQOSSERVICELEVEL\_IFAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="cacfc-109">0x00000002</span><span class="sxs-lookup"><span data-stu-id="cacfc-109">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="cacfc-110">Die erforderliche Quality of Service Level, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cacfc-110">The quality of service level required, if available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cacfc-111"><span id="LINEQOSSERVICELEVEL_BESTEFFORT"></span><span id="lineqosservicelevel_besteffort"></span>**lineqosservicelevel \_ BestEffort**</span><span class="sxs-lookup"><span data-stu-id="cacfc-111"><span id="LINEQOSSERVICELEVEL_BESTEFFORT"></span><span id="lineqosservicelevel_besteffort"></span>**LINEQOSSERVICELEVEL\_BESTEFFORT**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="cacfc-112">0x00000003</span><span class="sxs-lookup"><span data-stu-id="cacfc-112">0x00000003</span></span>
</dt> <dt>



<span data-ttu-id="cacfc-113">Die Qualität der Service Level ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cacfc-113">The quality of service level required is "best effort."</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cacfc-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cacfc-114">Requirements</span></span>



| <span data-ttu-id="cacfc-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cacfc-115">Requirement</span></span> | <span data-ttu-id="cacfc-116">Wert</span><span class="sxs-lookup"><span data-stu-id="cacfc-116">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="cacfc-117">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="cacfc-117">TAPI version</span></span><br/> | <span data-ttu-id="cacfc-118">Erfordert TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="cacfc-118">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="cacfc-119">Header</span><span class="sxs-lookup"><span data-stu-id="cacfc-119">Header</span></span><br/>       | <dl> <span data-ttu-id="cacfc-120"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="cacfc-120"><dt>Tspi.h</dt></span></span> </dl> |



 

 




