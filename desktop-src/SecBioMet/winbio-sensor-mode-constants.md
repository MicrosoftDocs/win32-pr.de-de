---
title: WINBIO_SENSOR_MODE Konstanten (winbio \_ types. h)
description: Legen Sie den Sensor Adapter Modus fest.
ms.assetid: fceaed5c-de59-4da7-9d7a-adeef353292f
topic_type:
- apiref
api_name:
- WINBIO_SENSOR_UNKNOWN_MODE
- WINBIO_SENSOR_BASIC_MODE
- WINBIO_SENSOR_ADVANCED_MODE
- WINBIO_SENSOR_NAVIGATION_MODE
- WINBIO_SENSOR_SLEEP_MODE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fedf419a64b3629d0cccbcb3d56de31a4adf383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743672"
---
# <a name="winbio_sensor_mode-constants"></a><span data-ttu-id="42abc-103">Winbio- \_ Sensor \_ Modus-Konstanten</span><span class="sxs-lookup"><span data-stu-id="42abc-103">WINBIO\_SENSOR\_MODE Constants</span></span>

<span data-ttu-id="42abc-104">Die folgenden Werte werden in der [**sensoradaptersetmode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn) -Funktion verwendet, um den Sensor Adapter Modus festzulegen.</span><span class="sxs-lookup"><span data-stu-id="42abc-104">The following values are used in the [**SensorAdapterSetMode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn) function to set the sensor adapter mode.</span></span>



| <span data-ttu-id="42abc-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="42abc-105">Constant</span></span>                                                                                                                                                                                                        | <span data-ttu-id="42abc-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42abc-106">Description</span></span>                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_SENSOR_UNKNOWN_MODE"></span><span id="winbio_sensor_unknown_mode"></span><dl> <span data-ttu-id="42abc-107"><dt>**\_ \_ unbekannter \_ Modus des winbio-Sensors**</dt></span><span class="sxs-lookup"><span data-stu-id="42abc-107"><dt>**WINBIO\_SENSOR\_UNKNOWN\_MODE**</dt></span></span> </dl>          | <span data-ttu-id="42abc-108">Der Betriebsmodus ist nicht bekannt.</span><span class="sxs-lookup"><span data-stu-id="42abc-108">The operating mode is not known.</span></span><br/>                                                                                                                    |
| <span id="WINBIO_SENSOR_BASIC_MODE"></span><span id="winbio_sensor_basic_mode"></span><dl> <span data-ttu-id="42abc-109"><dt>**\_ \_ Basis \_ Modus des winbio-Sensors**</dt></span><span class="sxs-lookup"><span data-stu-id="42abc-109"><dt>**WINBIO\_SENSOR\_BASIC\_MODE**</dt></span></span> </dl>                | <span data-ttu-id="42abc-110">Betreiben Sie den Sensor im Standardmodus.</span><span class="sxs-lookup"><span data-stu-id="42abc-110">Operate the sensor in basic mode.</span></span> <span data-ttu-id="42abc-111">Der Sensor fungiert nur als Erfassungsgerät.</span><span class="sxs-lookup"><span data-stu-id="42abc-111">The sensor acts only as a capture device.</span></span> <span data-ttu-id="42abc-112">Alle vorhandenen integrierten Verarbeitungs-oder Speicherfunktionen werden nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="42abc-112">Any onboard processing or storage capabilities that exist are not used.</span></span><br/> |
| <span id="WINBIO_SENSOR_ADVANCED_MODE"></span><span id="winbio_sensor_advanced_mode"></span><dl> <span data-ttu-id="42abc-113"><dt>**Erweiterter Modus des winbio- \_ Sensors \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="42abc-113"><dt>**WINBIO\_SENSOR\_ADVANCED\_MODE**</dt></span></span> </dl>       | <span data-ttu-id="42abc-114">Betreiben Sie den Sensor im erweiterten Modus.</span><span class="sxs-lookup"><span data-stu-id="42abc-114">Operate the sensor in advanced mode.</span></span> <span data-ttu-id="42abc-115">Der Sensor kann Beispiele erfassen und übereinstimmende und Speicherfunktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="42abc-115">The sensor can capture samples and perform matching and storage functions.</span></span><br/>                                     |
| <span id="WINBIO_SENSOR_NAVIGATION_MODE"></span><span id="winbio_sensor_navigation_mode"></span><dl> <span data-ttu-id="42abc-116"><dt>**winbio- \_ Sensor- \_ Navigations \_ Modus**</dt></span><span class="sxs-lookup"><span data-stu-id="42abc-116"><dt>**WINBIO\_SENSOR\_NAVIGATION\_MODE**</dt></span></span> </dl> | <span data-ttu-id="42abc-117">Betreiben Sie den Sensor als Mauspad.</span><span class="sxs-lookup"><span data-stu-id="42abc-117">Operate the sensor as a mouse pad.</span></span> <span data-ttu-id="42abc-118">Dies wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="42abc-118">This is not currently supported.</span></span><br/>                                                                                 |
| <span id="WINBIO_SENSOR_SLEEP_MODE"></span><span id="winbio_sensor_sleep_mode"></span><dl> <span data-ttu-id="42abc-119"><dt>**winbio- \_ Sensor-Standbymodus \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="42abc-119"><dt>**WINBIO\_SENSOR\_SLEEP\_MODE**</dt></span></span> </dl>                | <span data-ttu-id="42abc-120">Betreiben Sie den Sensor im Energiesparmodus.</span><span class="sxs-lookup"><span data-stu-id="42abc-120">Operate the sensor in sleep mode.</span></span><br/>                                                                                                                   |



## <a name="requirements"></a><span data-ttu-id="42abc-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42abc-121">Requirements</span></span>



| <span data-ttu-id="42abc-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42abc-122">Requirement</span></span> | <span data-ttu-id="42abc-123">Wert</span><span class="sxs-lookup"><span data-stu-id="42abc-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42abc-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42abc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="42abc-125">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42abc-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="42abc-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42abc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="42abc-127">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42abc-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="42abc-128">Header</span><span class="sxs-lookup"><span data-stu-id="42abc-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="42abc-129"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42abc-129"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42abc-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42abc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42abc-131">Client Anwendungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="42abc-131">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





