---
title: WINBIO_ORIENTATION Konstanten (winbio \_ types. h)
description: Die folgenden Konstanten geben die möglichen Kamera Ausrichtungen an, die von der sensorkomponente als obligatorisch angegeben werden.
ms.assetid: E44A6F17-5F38-47C7-947B-FB6FB79B1217
topic_type:
- apiref
api_name:
- WINBIO_ORIENTATION_UNSPECIFIED
- WINBIO_ORIENTATION_LANDSCAPE
- WINBIO_ORIENTATION_PORTRAIT
- WINBIO_ORIENTATION_ANY
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e5c3a3150819eff6311c03b8cd279fad7dcf398
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859299"
---
# <a name="winbio_orientation-constants"></a><span data-ttu-id="4f431-103">Winbio- \_ Orientierungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="4f431-103">WINBIO\_ORIENTATION Constants</span></span>

<span data-ttu-id="4f431-104">Die folgenden Konstanten geben die möglichen Kamera Ausrichtungen an, die von der sensorkomponente als obligatorisch angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4f431-104">The following constants specify the possible camera orientations that the sensor component specifies as mandatory.</span></span>



| <span data-ttu-id="4f431-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="4f431-105">Constant/value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="4f431-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f431-106">Description</span></span>                                                         |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------|
| <span id="WINBIO_ORIENTATION_UNSPECIFIED"></span><span id="winbio_orientation_unspecified"></span><dl> <span data-ttu-id="4f431-107"><dt>**Winbio \_ Ausrichtung \_ nicht angegeben**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4f431-107"><dt>**WINBIO\_ORIENTATION\_UNSPECIFIED**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="4f431-108">Es wurde keine obligatorische Ausrichtung für die Kamera angegeben.</span><span class="sxs-lookup"><span data-stu-id="4f431-108">A mandatory orientation for the camera is not specified.</span></span><br/> |
| <span id="WINBIO_ORIENTATION_LANDSCAPE"></span><span id="winbio_orientation_landscape"></span><dl> <span data-ttu-id="4f431-109"><dt>**Winbio \_ Orientierungs \_ Landschaft**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4f431-109"><dt>**WINBIO\_ORIENTATION\_LANDSCAPE**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="4f431-110">Die quer Ausrichtung ist für die Kamera erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4f431-110">The landscape orientation is required for the camera.</span></span><br/>    |
| <span id="WINBIO_ORIENTATION_PORTRAIT"></span><span id="winbio_orientation_portrait"></span><dl> <span data-ttu-id="4f431-111"><dt>**Winbio \_ Orientation \_**</dt> -Hochformat <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4f431-111"><dt>**WINBIO\_ORIENTATION\_PORTRAIT**</dt> <dt>2</dt></span></span> </dl>          | <span data-ttu-id="4f431-112">Die Hochformat Ausrichtung ist für die Kamera erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4f431-112">The portrait orientation is required for the camera.</span></span><br/>     |
| <span id="WINBIO_ORIENTATION_ANY"></span><span id="winbio_orientation_any"></span><dl> <span data-ttu-id="4f431-113"><dt>**Winbio \_ Ausrichtung \_ alle**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4f431-113"><dt>**WINBIO\_ORIENTATION\_ANY**</dt> <dt>3</dt></span></span> </dl>                         | <span data-ttu-id="4f431-114">Jede Ausrichtung ist für die Kamera zulässig.</span><span class="sxs-lookup"><span data-stu-id="4f431-114">Any orientation is permitted for the camera.</span></span><br/>             |



## <a name="requirements"></a><span data-ttu-id="4f431-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f431-115">Requirements</span></span>



| <span data-ttu-id="4f431-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f431-116">Requirement</span></span> | <span data-ttu-id="4f431-117">Wert</span><span class="sxs-lookup"><span data-stu-id="4f431-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f431-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4f431-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4f431-119">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f431-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="4f431-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4f431-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4f431-121">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f431-121">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="4f431-122">Header</span><span class="sxs-lookup"><span data-stu-id="4f431-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f431-123"><dt>Winbio \_ types. h (Include winbio. h für Client Anwendungen oder winbio \_ Adapters. h für Adapter)</dt></span><span class="sxs-lookup"><span data-stu-id="4f431-123"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f431-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f431-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f431-125">**Informationen zum erweiterten winbio- \_ \_ Sensor \_**</span><span class="sxs-lookup"><span data-stu-id="4f431-125">**WINBIO\_EXTENDED\_SENSOR\_INFO**</span></span>](winbio-extended-sensor-info.md)
</dt> </dl>

 

 





