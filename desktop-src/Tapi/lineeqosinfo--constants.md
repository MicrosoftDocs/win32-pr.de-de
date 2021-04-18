---
description: Diese Konstanten werden von einem TSP verwendet, um das Ergebnis einer QoS (Quality of Service)-Anforderung zu identifizieren.
ms.assetid: 617ddbf4-212f-4990-93c2-f38f04b035ab
title: LINEEQOSINFO_ Konstanten (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 423cc6172a1c6c87c1f3bb38929f727a15dad5c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354731"
---
# <a name="lineeqosinfo_-constants"></a><span data-ttu-id="c6c21-103">Lineeqosinfo- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="c6c21-103">LINEEQOSINFO\_ Constants</span></span>

<span data-ttu-id="c6c21-104">Diese Konstanten werden von einem TSP verwendet, um das Ergebnis einer QoS (Quality of Service)-Anforderung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c6c21-104">These constants are used by a TSP to identify the result of a QoS (Quality of Service) request.</span></span>

<dl> <dt>

<span data-ttu-id="c6c21-105"><span id="LINEEQOSINFO_NOQOS"></span><span id="lineeqosinfo_noqos"></span>**lineeqosinfo- \_ noqos**</span><span class="sxs-lookup"><span data-stu-id="c6c21-105"><span id="LINEEQOSINFO_NOQOS"></span><span id="lineeqosinfo_noqos"></span>**LINEEQOSINFO\_NOQOS**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="c6c21-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c6c21-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="c6c21-107">QoS ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c6c21-107">QoS is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c6c21-108"><span id="LINEEQOSINFO_ADMISSIONFAILURE"></span><span id="lineeqosinfo_admissionfailure"></span>**lineeqosinfo- \_ admissionfailure**</span><span class="sxs-lookup"><span data-stu-id="c6c21-108"><span id="LINEEQOSINFO_ADMISSIONFAILURE"></span><span id="lineeqosinfo_admissionfailure"></span>**LINEEQOSINFO\_ADMISSIONFAILURE**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="c6c21-109">0x00000002</span><span class="sxs-lookup"><span data-stu-id="c6c21-109">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="c6c21-110">Die QoS-Anforderung konnte nicht erfüllt werden.</span><span class="sxs-lookup"><span data-stu-id="c6c21-110">The QoS request could not be met.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c6c21-111"><span id="LINEEQOSINFO_POLICYFAILURE"></span><span id="lineeqosinfo_policyfailure"></span>**lineeqosinfo \_ PolicyFailure**</span><span class="sxs-lookup"><span data-stu-id="c6c21-111"><span id="LINEEQOSINFO_POLICYFAILURE"></span><span id="lineeqosinfo_policyfailure"></span>**LINEEQOSINFO\_POLICYFAILURE**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="c6c21-112">0x00000003</span><span class="sxs-lookup"><span data-stu-id="c6c21-112">0x00000003</span></span>
</dt> <dt>



<span data-ttu-id="c6c21-113">Der angeforderte QoS-Typ wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c6c21-113">The type of QoS requested is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c6c21-114"><span id="LINEEQOSINFO_GENERICERROR"></span><span id="lineeqosinfo_genericerror"></span>**lineeqosinfo \_ genericerror**</span><span class="sxs-lookup"><span data-stu-id="c6c21-114"><span id="LINEEQOSINFO_GENERICERROR"></span><span id="lineeqosinfo_genericerror"></span>**LINEEQOSINFO\_GENERICERROR**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="c6c21-115">0x00000004</span><span class="sxs-lookup"><span data-stu-id="c6c21-115">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="c6c21-116">Nicht spezifizierter QoS-Fehler.</span><span class="sxs-lookup"><span data-stu-id="c6c21-116">Unspecified QoS error.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c6c21-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6c21-117">Requirements</span></span>



| <span data-ttu-id="c6c21-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6c21-118">Requirement</span></span> | <span data-ttu-id="c6c21-119">Wert</span><span class="sxs-lookup"><span data-stu-id="c6c21-119">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c6c21-120">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="c6c21-120">TAPI version</span></span><br/> | <span data-ttu-id="c6c21-121">Erfordert TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="c6c21-121">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="c6c21-122">Header</span><span class="sxs-lookup"><span data-stu-id="c6c21-122">Header</span></span><br/>       | <dl> <span data-ttu-id="c6c21-123"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6c21-123"><dt>Tspi.h</dt></span></span> </dl> |



 

 




