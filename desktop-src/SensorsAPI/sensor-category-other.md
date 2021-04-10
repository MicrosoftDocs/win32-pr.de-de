---
description: Die Kategorie \_ \_ andere Kategorie des Sensors enthält Sensoren, die die benutzerdefinierte Klasse im HID-Klassen Treiber unterstützen.
ms.assetid: 866F7BF4-15CC-4F69-9510-B5858D47C4D0
title: SENSOR_CATEGORY_OTHER (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e26ece66ae74e873c48cd973cc447beec2dd8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041666"
---
# <a name="sensor_category_other"></a><span data-ttu-id="fcfbd-103">\_andere Sensor Kategorie \_</span><span class="sxs-lookup"><span data-stu-id="fcfbd-103">SENSOR\_CATEGORY\_OTHER</span></span>

<span data-ttu-id="fcfbd-104">Die Kategorie \_ \_ andere Kategorie des Sensors enthält Sensoren, die die benutzerdefinierte Klasse im HID-Klassen Treiber unterstützen.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-104">The SENSOR\_CATEGORY\_OTHER category contains sensors that support the Custom class in the HID Class driver.</span></span>

<dl> <dt>

<span data-ttu-id="fcfbd-105"><span id="SENSOR_TYPE_CUSTOM"></span><span id="sensor_type_custom"></span>**\_ \_ benutzerdefinierter Sensortyp**</span><span class="sxs-lookup"><span data-stu-id="fcfbd-105"><span id="SENSOR_TYPE_CUSTOM"></span><span id="sensor_type_custom"></span>**SENSOR\_TYPE\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcfbd-106">{E83AF229-8640-4D18-A213-E22675EBB2C3}</span><span class="sxs-lookup"><span data-stu-id="fcfbd-106">{E83AF229-8640-4D18-A213-E22675EBB2C3}</span></span>
</dt> <dt>



<span data-ttu-id="fcfbd-107">Benutzerdefinierter Sensor, der die benutzerdefinierte-Klasse im HID-Klassen Treiber unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-107">Custom sensor that supports the Custom class in the HID Class driver.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="fcfbd-108">**Platt Form definierte Datenfelder**</span><span class="sxs-lookup"><span data-stu-id="fcfbd-108">**Platform-Defined Data Fields**</span></span>

<span data-ttu-id="fcfbd-109">Platt Form definierte Eigenschafts Schlüssel für diese Kategorie basieren auf der \_ \_ \_ benutzerdefinierten GUID des Sensor Datentyps \_ :</span><span class="sxs-lookup"><span data-stu-id="fcfbd-109">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_CUSTOM\_GUID:</span></span>

<span data-ttu-id="fcfbd-110">{B14C764F-07CF-41E8-9D82-EBE3D0776A6F}</span><span class="sxs-lookup"><span data-stu-id="fcfbd-110">{B14C764F-07CF-41E8-9D82-EBE3D0776A6F}</span></span>

<span data-ttu-id="fcfbd-111">Diese Kategorie enthält die folgenden Platt Form definierten Datenfelder.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-111">This category includes the following platform-defined data fields.</span></span>



| <span data-ttu-id="fcfbd-112">Name und PID des Daten Felds</span><span class="sxs-lookup"><span data-stu-id="fcfbd-112">Data field name and PID</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="fcfbd-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fcfbd-113">Description</span></span>                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_CUSTOM_USAGE"></span><span id="sensor_data_type_custom_usage"></span><dl> <span data-ttu-id="fcfbd-114"><dt>**Sensor \_ \_ \_ Benutzerdefinierte \_ Verwendung des Datentyps**</dt> <dt> (PID = 5)</dt></span><span class="sxs-lookup"><span data-stu-id="fcfbd-114"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_USAGE**</dt> <dt> (PID = 5) </dt></span></span> </dl>                          | <span data-ttu-id="fcfbd-115">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="fcfbd-115">**VT\_UI4**</span></span><br/> <span data-ttu-id="fcfbd-116">Eine versteckte Verwendung, die zur Unterscheidung mehrerer, benutzerdefinierter Sensoren verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-116">A HID usage which can be used to distinguish multiple, custom sensors.</span></span><br/> |
| <span id="SENSOR_DATA_TYPE_CUSTOM_BOOLEAN_ARRAY"></span><span id="sensor_data_type_custom_boolean_array"></span><dl> <span data-ttu-id="fcfbd-117"><dt>**Sensor \_ \_ \_ Benutzerdefiniertes \_ Boolesches \_ Array des Datentyps**</dt> <dt> (PID = 6)</dt></span><span class="sxs-lookup"><span data-stu-id="fcfbd-117"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_BOOLEAN\_ARRAY**</dt> <dt> (PID = 6) </dt></span></span> </dl> | <span data-ttu-id="fcfbd-118">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="fcfbd-118">**VT\_UI4**</span></span><br/> <span data-ttu-id="fcfbd-119">Ein Array von booleschen Werten für einen angegebenen benutzerdefinierten Sensor.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-119">An array of Boolean values for a given custom sensor.</span></span><br/>                  |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE1"></span><span id="sensor_data_type_custom_value1"></span><dl> <span data-ttu-id="fcfbd-120"><dt>**Sensor \_ \_Datentyp \_ Benutzer definiert \_ value1**</dt> <dt> (PID = 7)</dt></span><span class="sxs-lookup"><span data-stu-id="fcfbd-120"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE1**</dt> <dt> (PID = 7) </dt></span></span> </dl>                       | <span data-ttu-id="fcfbd-121">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="fcfbd-121">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="fcfbd-122">Einer von sechs verfügbaren Werten für einen angegebenen benutzerdefinierten Sensor.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-122">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE2"></span><span id="sensor_data_type_custom_value2"></span><dl> <span data-ttu-id="fcfbd-123"><dt>**Sensor \_ \_Datentyp \_ Benutzer definiert \_ value2**</dt> <dt> (PID = 8)</dt></span><span class="sxs-lookup"><span data-stu-id="fcfbd-123"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE2**</dt> <dt> (PID = 8) </dt></span></span> </dl>                       | <span data-ttu-id="fcfbd-124">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="fcfbd-124">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="fcfbd-125">Einer von sechs verfügbaren Werten für einen angegebenen benutzerdefinierten Sensor.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-125">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE3"></span><span id="sensor_data_type_custom_value3"></span><dl> <span data-ttu-id="fcfbd-126"><dt>**Sensor \_ \_Datentyp \_ Benutzer definiert \_ Wert3**</dt> <dt> (PID = 9)</dt></span><span class="sxs-lookup"><span data-stu-id="fcfbd-126"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE3**</dt> <dt> (PID = 9) </dt></span></span> </dl>                       | <span data-ttu-id="fcfbd-127">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="fcfbd-127">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="fcfbd-128">Einer von sechs verfügbaren Werten für einen angegebenen benutzerdefinierten Sensor.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-128">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE4"></span><span id="sensor_data_type_custom_value4"></span><dl> <span data-ttu-id="fcfbd-129"><dt>**Sensor \_ \_Datentyp \_ Benutzer definiert \_ VALUE4**</dt> <dt> (PID = 10)</dt></span><span class="sxs-lookup"><span data-stu-id="fcfbd-129"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE4**</dt> <dt> (PID = 10) </dt></span></span> </dl>                      | <span data-ttu-id="fcfbd-130">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="fcfbd-130">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="fcfbd-131">Einer von sechs verfügbaren Werten für einen angegebenen benutzerdefinierten Sensor.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-131">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE5"></span><span id="sensor_data_type_custom_value5"></span><dl> <span data-ttu-id="fcfbd-132"><dt>**Sensor \_ \_Datentyp \_ Benutzer definiert \_ VALUE5**</dt> <dt> (PID = 11)</dt></span><span class="sxs-lookup"><span data-stu-id="fcfbd-132"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE5**</dt> <dt> (PID = 11) </dt></span></span> </dl>                      | <span data-ttu-id="fcfbd-133">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="fcfbd-133">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="fcfbd-134">Einer von sechs verfügbaren Werten für einen angegebenen benutzerdefinierten Sensor.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-134">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE6"></span><span id="sensor_data_type_custom_value6"></span><dl> <span data-ttu-id="fcfbd-135"><dt>**Sensor \_ \_Datentyp \_ Benutzer definiert \_ VALUE6**</dt> <dt> (PID = 12)</dt></span><span class="sxs-lookup"><span data-stu-id="fcfbd-135"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE6**</dt> <dt> (PID = 12) </dt></span></span> </dl>                      | <span data-ttu-id="fcfbd-136">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="fcfbd-136">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="fcfbd-137">Einer von sechs verfügbaren Werten für einen angegebenen benutzerdefinierten Sensor.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-137">One of six available values for a given custom sensor.</span></span><br/>       |



## <a name="remarks"></a><span data-ttu-id="fcfbd-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fcfbd-138">Remarks</span></span>

<span data-ttu-id="fcfbd-139">Ein Sensor, der die generische Klasse im HID-Klassen Treiber unterstützt, wird einer der anderen definierten Kategorien (biometrische, elektrisch, Umwelt usw.) zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-139">A sensor that supports the Generic class in the HID class driver will map to one of the other defined categories (biometric, electrical, environmental, and so on).</span></span>

## <a name="requirements"></a><span data-ttu-id="fcfbd-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fcfbd-140">Requirements</span></span>



| <span data-ttu-id="fcfbd-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fcfbd-141">Requirement</span></span> | <span data-ttu-id="fcfbd-142">Wert</span><span class="sxs-lookup"><span data-stu-id="fcfbd-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fcfbd-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fcfbd-143">Minimum supported client</span></span><br/> | <span data-ttu-id="fcfbd-144">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fcfbd-144">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fcfbd-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fcfbd-145">Minimum supported server</span></span><br/> | <span data-ttu-id="fcfbd-146">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fcfbd-146">None supported</span></span><br/>                                                            |
| <span data-ttu-id="fcfbd-147">Header</span><span class="sxs-lookup"><span data-stu-id="fcfbd-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcfbd-148"><dt>Sensoren. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcfbd-148"><dt>Sensors.h</dt></span></span> </dl> |



 

 




