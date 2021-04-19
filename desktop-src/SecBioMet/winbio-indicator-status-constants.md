---
title: WINBIO_INDICATOR_STATUS Konstanten (winbio \_ types. h)
description: Legen Sie eine Indikator Ampel fest.
ms.assetid: 1e00ff9d-6693-4763-8ac3-b42d2a3e987d
topic_type:
- apiref
api_name:
- WINBIO_INDICATOR_ON
- WINBIO_INDICATOR_OFF
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7693fbd2b9b37067738774d172f4bb482edb06e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343484"
---
# <a name="winbio_indicator_status-constants"></a><span data-ttu-id="0a057-103">Winbio- \_ Indikator \_ Status Konstanten</span><span class="sxs-lookup"><span data-stu-id="0a057-103">WINBIO\_INDICATOR\_STATUS Constants</span></span>

<span data-ttu-id="0a057-104">Die folgenden Werte können verwendet werden, um eine Indikator Ampel festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0a057-104">The following values can be used to set an indicator light.</span></span> <span data-ttu-id="0a057-105">Standardmäßig haben Sensoren keine Beleuchtung, aber Anwendungen können diese Werte verwenden, um Indikator Leuchten zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="0a057-105">By default, sensors will not have a light on, but applications can use these values to enable or disable indicator lights.</span></span> <span data-ttu-id="0a057-106">Der **\_ \_ Statuswert des winbio-Sensors** bietet weitere Details zum Status eines Indikator Lichts, das sich in befindet.</span><span class="sxs-lookup"><span data-stu-id="0a057-106">The **WINBIO\_SENSOR\_STATUS** value provides more detail about the status of an indicator light that is on.</span></span> <span data-ttu-id="0a057-107">Weitere Informationen finden Sie in den folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="0a057-107">For more information, see the following functions:</span></span>

-   [<span data-ttu-id="0a057-108">**Sensoradaptersetindikatorstatus**</span><span class="sxs-lookup"><span data-stu-id="0a057-108">**SensorAdapterSetIndicatorStatus**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn)
-   [<span data-ttu-id="0a057-109">**Sensoradaptergetindikatorstatus**</span><span class="sxs-lookup"><span data-stu-id="0a057-109">**SensorAdapterGetIndicatorStatus**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn)
-   [<span data-ttu-id="0a057-110">**Sensoradapterquerystatus**</span><span class="sxs-lookup"><span data-stu-id="0a057-110">**SensorAdapterQueryStatus**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn)



| <span data-ttu-id="0a057-111">Konstante</span><span class="sxs-lookup"><span data-stu-id="0a057-111">Constant</span></span>                                                                                                                                                                            | <span data-ttu-id="0a057-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0a057-112">Description</span></span>                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------|
| <span id="WINBIO_INDICATOR_ON"></span><span id="winbio_indicator_on"></span><dl> <span data-ttu-id="0a057-113"><dt>**winbio- \_ Indikator \_ für**</dt></span><span class="sxs-lookup"><span data-stu-id="0a057-113"><dt>**WINBIO\_INDICATOR\_ON**</dt></span></span> </dl>    | <span data-ttu-id="0a057-114">Der Sensor Indikator Licht ist on.</span><span class="sxs-lookup"><span data-stu-id="0a057-114">The sensor indicator light is on.</span></span><br/>  |
| <span id="WINBIO_INDICATOR_OFF"></span><span id="winbio_indicator_off"></span><dl> <span data-ttu-id="0a057-115"><dt>**winbio- \_ Indikator \_ aus**</dt></span><span class="sxs-lookup"><span data-stu-id="0a057-115"><dt>**WINBIO\_INDICATOR\_OFF**</dt></span></span> </dl> | <span data-ttu-id="0a057-116">Die Sensor Indikator Beleuchtung ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="0a057-116">The sensor indicator light is off.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0a057-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a057-117">Requirements</span></span>



| <span data-ttu-id="0a057-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a057-118">Requirement</span></span> | <span data-ttu-id="0a057-119">Wert</span><span class="sxs-lookup"><span data-stu-id="0a057-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a057-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0a057-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0a057-121">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a057-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="0a057-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0a057-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0a057-123">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a057-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="0a057-124">Header</span><span class="sxs-lookup"><span data-stu-id="0a057-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a057-125"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a057-125"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a057-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a057-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a057-127">Client Anwendungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="0a057-127">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





