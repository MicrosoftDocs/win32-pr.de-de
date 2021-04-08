---
description: Die Kategorie "Light" der Sensor \_ Kategorie \_ enthält Sensoren, die Informationen zu den Merkmalen des Lichts bereitstellen.
ms.assetid: 0327bda5-f1d7-476d-9f0f-f4d60a6a106f
title: SENSOR_CATEGORY_LIGHT (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca14bba297a8f445312873fc810e7d0b5ba13a4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862263"
---
# <a name="sensor_category_light"></a><span data-ttu-id="e60ec-103">Sensor \_ Kategorie \_ hell</span><span class="sxs-lookup"><span data-stu-id="e60ec-103">SENSOR\_CATEGORY\_LIGHT</span></span>

<span data-ttu-id="e60ec-104">Die Kategorie "Light" der Sensor \_ Kategorie \_ enthält Sensoren, die Informationen zu den Merkmalen des Lichts bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e60ec-104">The SENSOR\_CATEGORY\_LIGHT category contains sensors that provide information about characteristics of light.</span></span>

<span data-ttu-id="e60ec-105">**Platt Form definierte Sensor Typen**</span><span class="sxs-lookup"><span data-stu-id="e60ec-105">**Platform-Defined Sensor Types**</span></span>

<span data-ttu-id="e60ec-106">Diese Kategorie enthält die folgenden Platt Form definierten Sensortypen.</span><span class="sxs-lookup"><span data-stu-id="e60ec-106">This category includes the following platform-defined sensor types.</span></span>



| <span data-ttu-id="e60ec-107">Sensortyp</span><span class="sxs-lookup"><span data-stu-id="e60ec-107">Sensor type</span></span>                                                                                                                                                                                                                                                                                     | <span data-ttu-id="e60ec-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e60ec-108">Description</span></span>                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------|
| <span id="SENSOR_TYPE_AMBIENT_LIGHT"></span><span id="sensor_type_ambient_light"></span><dl> <span data-ttu-id="e60ec-109"><dt>**Sensor \_ Typ \_ AMBIENT \_ Light**</dt> <dt>{97F 115c8-599a-4153-8894-D2D12899918A}</dt></span><span class="sxs-lookup"><span data-stu-id="e60ec-109"><dt>**SENSOR\_TYPE\_AMBIENT\_LIGHT**</dt> <dt>{97F115C8-599A-4153-8894-D2D12899918A}</dt></span></span> </dl> | <span data-ttu-id="e60ec-110">Umgebungslichtsensoren.</span><span class="sxs-lookup"><span data-stu-id="e60ec-110">Ambient light sensors.</span></span><br/> |



<span data-ttu-id="e60ec-111">**Platt Form definierte Datenfelder**</span><span class="sxs-lookup"><span data-stu-id="e60ec-111">**Platform-Defined Data Fields**</span></span>

<span data-ttu-id="e60ec-112">Platt Form definierte Eigenschafts Schlüssel für diese Kategorie basieren auf der \_ hell-GUID des Sensor Datentyps \_ \_ \_ :</span><span class="sxs-lookup"><span data-stu-id="e60ec-112">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_LIGHT\_GUID:</span></span>

<span data-ttu-id="e60ec-113">{E4C77CE2-DCB7-46E9-8439-4FEC548833A6}</span><span class="sxs-lookup"><span data-stu-id="e60ec-113">{E4C77CE2-DCB7-46E9-8439-4FEC548833A6}</span></span>

<span data-ttu-id="e60ec-114">Diese Kategorie enthält die folgenden Platt Form definierten Datenfelder.</span><span class="sxs-lookup"><span data-stu-id="e60ec-114">This category includes the following platform-defined data fields.</span></span>



| <span data-ttu-id="e60ec-115">Name und PID des Daten Felds</span><span class="sxs-lookup"><span data-stu-id="e60ec-115">Data field name and PID</span></span>                                                                                                                                                                                                                                                                                                | <span data-ttu-id="e60ec-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e60ec-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_LIGHT_CHROMACITY__"></span><span id="sensor_data_type_light_chromacity__"></span><dl> <span data-ttu-id="e60ec-117"><dt> **Sensor \_ \_ Datentyp \_ Light \_ chromacity**</dt> <dt>(PID = 4)</dt></span><span class="sxs-lookup"><span data-stu-id="e60ec-117"><dt>**SENSOR\_DATA\_TYPE\_LIGHT\_CHROMACITY** </dt> <dt> (PID = 4) </dt></span></span> </dl>                     | <span data-ttu-id="e60ec-118">**VT \_ Vector \| VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="e60ec-118">**VT\_VECTOR\|VT\_UI1**</span></span><br/> <span data-ttu-id="e60ec-119">Die Chromaticity als Gezähltes Array von float-Werten.</span><span class="sxs-lookup"><span data-stu-id="e60ec-119">Chromaticity as a counted array of float values.</span></span><br/> <span data-ttu-id="e60ec-120">Daten für Vektor Typen werden immer als **VT \_ UI1** (ein Array von Zeichen ohne Vorzeichen, 1 Byte Zeichen) serialisiert.</span><span class="sxs-lookup"><span data-stu-id="e60ec-120">Data for vector types is always serialized as **VT\_UI1** (an array of unsigned, 1-byte characters).</span></span> <span data-ttu-id="e60ec-121">Dieses Datenfeld enthält tatsächlich jeden Wert als einen IEEE 4-Byte-Real Wert (**VT \_ R4**).</span><span class="sxs-lookup"><span data-stu-id="e60ec-121">This data field actually contains each value as an IEEE 4-byte real value (**VT\_R4**).</span></span><br/> <span data-ttu-id="e60ec-122">Weitere Informationen zum Arbeiten mit Arrays finden Sie unter [Abrufen von Vektor Typen](retrieving-vector-types.md).</span><span class="sxs-lookup"><span data-stu-id="e60ec-122">For information about working with arrays, see [Retrieving Vector Types](retrieving-vector-types.md).</span></span><br/> |
| <span id="SENSOR_DATA_TYPE_LIGHT_LEVEL_LUX"></span><span id="sensor_data_type_light_level_lux"></span><dl> <span data-ttu-id="e60ec-123"><dt>**Sensor \_ Data \_ Type \_ Light \_ Level \_ Lux**</dt> <dt> (PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="e60ec-123"><dt>**SENSOR\_DATA\_TYPE\_LIGHT\_LEVEL\_LUX**</dt> <dt> (PID = 2) </dt></span></span> </dl>                            | <span data-ttu-id="e60ec-124">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="e60ec-124">**VT\_R4**</span></span><br/> <span data-ttu-id="e60ec-125">Beleuchtungs Ebene in Lux.</span><span class="sxs-lookup"><span data-stu-id="e60ec-125">Illuminance level, in lux.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SENSOR_DATA_TYPE_LIGHT_TEMPERATURE_KELVIN"></span><span id="sensor_data_type_light_temperature_kelvin"></span><dl> <span data-ttu-id="e60ec-126"><dt>**Sensor \_ \_Datentyp \_ Licht \_ Temperatur \_ Kelvin**</dt> <dt> (PID = 3)</dt></span><span class="sxs-lookup"><span data-stu-id="e60ec-126"><dt>**SENSOR\_DATA\_TYPE\_LIGHT\_TEMPERATURE\_KELVIN**</dt> <dt> (PID = 3) </dt></span></span> </dl> | <span data-ttu-id="e60ec-127">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="e60ec-127">**VT\_R4**</span></span><br/> <span data-ttu-id="e60ec-128">Farbtemperatur in Grad Kelvin.</span><span class="sxs-lookup"><span data-stu-id="e60ec-128">Color temperature, in degrees Kelvin.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |



## <a name="requirements"></a><span data-ttu-id="e60ec-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e60ec-129">Requirements</span></span>



| <span data-ttu-id="e60ec-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e60ec-130">Requirement</span></span> | <span data-ttu-id="e60ec-131">Wert</span><span class="sxs-lookup"><span data-stu-id="e60ec-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e60ec-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e60ec-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e60ec-133">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e60ec-133">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e60ec-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e60ec-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e60ec-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e60ec-135">None supported</span></span><br/>                                                            |
| <span data-ttu-id="e60ec-136">Header</span><span class="sxs-lookup"><span data-stu-id="e60ec-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e60ec-137"><dt>Sensoren. h</dt></span><span class="sxs-lookup"><span data-stu-id="e60ec-137"><dt>Sensors.h</dt></span></span> </dl> |



 

 




