---
description: Die Windows-Sensor-und-Location-Plattform definiert Konstanten für Treiber Ereignisse. Sensor manfuactureres können auch Ihre eigenen Konstanten definieren.
ms.assetid: ca61c912-bce5-4e41-ab48-40615d5b93ba
title: Ereignis Konstanten (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc9fb3ced92c1fe263538f2ce27c3fc65fdd7676
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364090"
---
# <a name="event-constants-sensorsh"></a><span data-ttu-id="5d5de-104">Ereignis Konstanten (Sensors. h)</span><span class="sxs-lookup"><span data-stu-id="5d5de-104">Event Constants (Sensors.h)</span></span>

<span data-ttu-id="5d5de-105">Die Windows-Sensor-und-Location-Plattform definiert Konstanten für Treiber Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="5d5de-105">The Windows Sensor and Location platform defines constants for driver events.</span></span> <span data-ttu-id="5d5de-106">Sensor manfuactureres können auch Ihre eigenen Konstanten definieren.</span><span class="sxs-lookup"><span data-stu-id="5d5de-106">Sensor manfuactureres can also define their own constants.</span></span>

<span data-ttu-id="5d5de-107">**Sensor Ereignis Typen**</span><span class="sxs-lookup"><span data-stu-id="5d5de-107">**Sensor Event Types**</span></span>

<span data-ttu-id="5d5de-108">Die Plattform definiert die folgenden Typen von Sensor Ereignis Typen.</span><span class="sxs-lookup"><span data-stu-id="5d5de-108">The platform defines the following sensor event type identifiers.</span></span>



| <span data-ttu-id="5d5de-109">Sensor Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="5d5de-109">Sensor event type</span></span>                                                                                                                                                                                                                                                                                                    | <span data-ttu-id="5d5de-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d5de-110">Description</span></span>                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_ACCELEROMETER_SHAKE"></span><span id="sensor_event_accelerometer_shake"></span><dl> <span data-ttu-id="5d5de-111"><dt>**Sensor \_ Ereignis \_ Beschleunigungsmesser- \_ Shake**</dt> <dt>{825 f 94-0 ecb5c99d915}</dt></span><span class="sxs-lookup"><span data-stu-id="5d5de-111"><dt>**SENSOR\_EVENT\_ACCELEROMETER\_SHAKE**</dt> <dt>{825F5A94-0F48-4396-9CA0-6ECB5C99D915}</dt></span></span> </dl> | <span data-ttu-id="5d5de-112">Gibt an, dass das Gerät geschüttelt wurde.</span><span class="sxs-lookup"><span data-stu-id="5d5de-112">Indicates that the device was shaken.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_DATA_UPDATED"></span><span id="sensor_event_data_updated"></span><dl> <span data-ttu-id="5d5de-113"><dt>**Sensor \_ Ereignis \_ Daten \_ aktualisiert**</dt> <dt>{2ed0f 2a4-0087-41d3-87dB-6773370b3c88}</dt></span><span class="sxs-lookup"><span data-stu-id="5d5de-113"><dt>**SENSOR\_EVENT\_DATA\_UPDATED**</dt> <dt>{2ED0F2A4-0087-41D3-87DB-6773370B3C88}</dt></span></span> </dl>                      | <span data-ttu-id="5d5de-114">Gibt an, dass neue Daten verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="5d5de-114">Indicates that new data is available.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_PROPERTY_CHANGED"></span><span id="sensor_event_property_changed"></span><dl> <span data-ttu-id="5d5de-115"><dt>**Sensor \_ Ereignis \_ Eigenschaft \_ geändert**</dt> <dt>{2358f 099-84c9-4d3d-90df-c2421e2b2045}</dt></span><span class="sxs-lookup"><span data-stu-id="5d5de-115"><dt>**SENSOR\_EVENT\_PROPERTY\_CHANGED**</dt> <dt>{2358F099-84C9-4D3D-90DF-C2421E2B2045}</dt></span></span> </dl>          | <span data-ttu-id="5d5de-116">Gibt an, dass sich ein Eigenschafts Wert geändert hat.</span><span class="sxs-lookup"><span data-stu-id="5d5de-116">Indicates that a property value changed.</span></span> <span data-ttu-id="5d5de-117">Überprüfen Sie die Schnittstelle [iportablewavicevalues](/previous-versions//ms740012(v=vs.85)) , die über den Parameter " *Peer Event Data* " an [**OnEvent**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onevent)übergeben wird, um zu bestimmen, welche Eigenschaft geändert wurde, und den neuen Wert.</span><span class="sxs-lookup"><span data-stu-id="5d5de-117">Check the [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) interface, passed through the *pEventData* parameter to [**OnEvent**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onevent), to determine which property changed and its new value.</span></span><br/> |
| <span id="SENSOR_EVENT_STATE_CHANGED"></span><span id="sensor_event_state_changed"></span><dl> <span data-ttu-id="5d5de-118"><dt>**Sensor \_ Ereignis \_ Status \_ geändert**</dt> <dt>{BFD96016-6BD7-4560-AD34-F2F6607E8F81}</dt></span><span class="sxs-lookup"><span data-stu-id="5d5de-118"><dt>**SENSOR\_EVENT\_STATE\_CHANGED**</dt> <dt>{BFD96016-6BD7-4560-AD34-F2F6607E8F81}</dt></span></span> </dl>                   | <span data-ttu-id="5d5de-119">Gibt eine Änderung des Betriebsstatus an, z. b. vom Sensor \_ Status \_ Initialisierung in den Sensor \_ Zustand \_ bereit.</span><span class="sxs-lookup"><span data-stu-id="5d5de-119">Indicates a change of operational state, for example, from SENSOR\_STATE\_INITIALIZING to SENSOR\_STATE\_READY.</span></span><br/>                                                                                                                                                                                            |



<span data-ttu-id="5d5de-120">**PropertyKeys des Sensor Ereignisses**</span><span class="sxs-lookup"><span data-stu-id="5d5de-120">**Sensor Event PROPERTYKEYs**</span></span>

<span data-ttu-id="5d5de-121">Platt Form definierte Eigenschafts Schlüssel für Ereignisse basieren auf der folgenden GUID:</span><span class="sxs-lookup"><span data-stu-id="5d5de-121">Platform-defined property keys for events are based on the following GUID:</span></span>

<span data-ttu-id="5d5de-122">{64346e30-8728-4b34-bdf6-4l52442c5c28}</span><span class="sxs-lookup"><span data-stu-id="5d5de-122">{64346E30-8728-4B34-BDF6-4F52442C5C28}</span></span>

<span data-ttu-id="5d5de-123">Die Sensorplattform definiert die folgenden **PropertyKeys**, die Sensor Ereignis Parameter identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5d5de-123">The sensor platform defines the following **PROPERTYKEY** s that identify sensor event parameters.</span></span>



| <span data-ttu-id="5d5de-124">PropertyKey und PID des Sensor Ereignisses</span><span class="sxs-lookup"><span data-stu-id="5d5de-124">Sensor event PROPERTYKEY and PID</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="5d5de-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d5de-125">Description</span></span>                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_PARAMETER_EVENT_ID"></span><span id="sensor_event_parameter_event_id"></span><dl> <span data-ttu-id="5d5de-126"><dt>**Sensor \_ Ereignis \_ Parameter \_ Ereignis- \_ ID**</dt> <dt>(PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="5d5de-126"><dt>**SENSOR\_EVENT\_PARAMETER\_EVENT\_ID**</dt> <dt>(PID = 2)</dt></span></span> </dl> | <span data-ttu-id="5d5de-127">Gibt an, dass der **GUID** -Wert in [iportabledevicevalues](/previous-versions//ms740012(v=vs.85)) eine Ereignistyp-ID ist, z \_ . b \_ . aktualisierte Sensor Ereignisdaten \_ .</span><span class="sxs-lookup"><span data-stu-id="5d5de-127">Indicates that the **GUID** value in [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) is an event type ID, such as SENSOR\_EVENT\_DATA\_UPDATED.</span></span><br/> |
| <span id="SENSOR_EVENT_PARAMETER_STATE"></span><span id="sensor_event_parameter_state"></span><dl> <span data-ttu-id="5d5de-128"><dt>**Sensor \_ \_ \_ Status des Ereignis Parameters**</dt> <dt>(PID = 3)</dt></span><span class="sxs-lookup"><span data-stu-id="5d5de-128"><dt>**SENSOR\_EVENT\_PARAMETER\_STATE**</dt> <dt>(PID = 3)</dt></span></span> </dl>           | <span data-ttu-id="5d5de-129">Gibt an, dass der Wert einer Ganzzahl ohne Vorzeichen in **iportableendvicevalues** ein Sensor Zustand ist, z. b. der Sensor \_ Status \_ Ready.</span><span class="sxs-lookup"><span data-stu-id="5d5de-129">Indicates that the unsigned integer value in **IPortableDeviceValues** is a sensor state, such as SENSOR\_STATE\_READY.</span></span><br/>                                                  |



<span data-ttu-id="5d5de-130">**PropertyKeys des Sensor Fehlers**</span><span class="sxs-lookup"><span data-stu-id="5d5de-130">**Sensor Error PROPERTYKEYs**</span></span>

<span data-ttu-id="5d5de-131">Platt Form definierte Eigenschafts Schlüssel für Fehler basieren auf der folgenden GUID:</span><span class="sxs-lookup"><span data-stu-id="5d5de-131">Platform-defined property keys for errors will be based on the following GUID:</span></span>

<span data-ttu-id="5d5de-132">{77112bcd-oce1-4f 43-b8b8-a88256adb4b3}</span><span class="sxs-lookup"><span data-stu-id="5d5de-132">{77112BCD-FCE1-4f43-B8B8-A88256ADB4B3}</span></span>

<span data-ttu-id="5d5de-133">Die Sensorplattform reserviert diese GUID für die zukünftige Verwendung.</span><span class="sxs-lookup"><span data-stu-id="5d5de-133">The sensor platform reserves this GUID for future use.</span></span>

<dl></dl>

## <a name="requirements"></a><span data-ttu-id="5d5de-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d5de-134">Requirements</span></span>



| <span data-ttu-id="5d5de-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d5de-135">Requirement</span></span> | <span data-ttu-id="5d5de-136">Wert</span><span class="sxs-lookup"><span data-stu-id="5d5de-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5d5de-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5d5de-137">Minimum supported client</span></span><br/> | <span data-ttu-id="5d5de-138">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d5de-138">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5d5de-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5d5de-139">Minimum supported server</span></span><br/> | <span data-ttu-id="5d5de-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5d5de-140">None supported</span></span><br/>                                                            |
| <span data-ttu-id="5d5de-141">Header</span><span class="sxs-lookup"><span data-stu-id="5d5de-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d5de-142"><dt>Sensoren. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d5de-142"><dt>Sensors.h</dt></span></span> </dl> |



 

