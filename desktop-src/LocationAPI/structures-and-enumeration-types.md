---
description: Die Location-API definiert die folgenden Enumerationstypen.
ms.assetid: a1d9d274-2861-4818-8fa1-d8d66edf27b3
title: Strukturen und Enumerationstypen (Location-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a73c27cb2ad6dc0dcd0c2b92f4e9ba52e98fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359158"
---
# <a name="structures-and-enumeration-types-location-api"></a><span data-ttu-id="b4115-103">Strukturen und Enumerationstypen (Location-API)</span><span class="sxs-lookup"><span data-stu-id="b4115-103">Structures and Enumeration Types (Location API)</span></span>

<span data-ttu-id="b4115-104">\[Die Win32-Location-API ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="b4115-104">\[The Win32 Location API is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b4115-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="b4115-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b4115-106">Verwenden Sie stattdessen die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API.</span><span class="sxs-lookup"><span data-stu-id="b4115-106">Instead, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.</span></span> <span data-ttu-id="b4115-107">\]</span><span class="sxs-lookup"><span data-stu-id="b4115-107">\]</span></span>

<span data-ttu-id="b4115-108">Die Location-API definiert die folgenden Enumerationstypen.</span><span class="sxs-lookup"><span data-stu-id="b4115-108">The Location API defines the following enumeration types.</span></span>



| <span data-ttu-id="b4115-109">Enumeration</span><span class="sxs-lookup"><span data-stu-id="b4115-109">Enumeration</span></span>                                                                       | <span data-ttu-id="b4115-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4115-110">Description</span></span>                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="b4115-111">[**\_gewünschte \_ Genauigkeit für Speicherort**](/previous-versions/windows/desktop/legacy/dd756639(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b4115-111">[**LOCATION\_DESIRED\_ACCURACY**](/previous-versions/windows/desktop/legacy/dd756639(v=vs.85))</span></span>                  | <span data-ttu-id="b4115-112">Definiert die möglichen gewünschten Genauigkeits Typen.</span><span class="sxs-lookup"><span data-stu-id="b4115-112">Defines the possible desired accuracy types.</span></span>                         |
| [<span data-ttu-id="b4115-113">**Standort \_ \_ Status Bericht**</span><span class="sxs-lookup"><span data-stu-id="b4115-113">**LOCATION\_REPORT\_STATUS**</span></span>](/windows/win32/api/locationapi/ne-locationapi-location_report_status) | <span data-ttu-id="b4115-114">Definiert den möglichen Status für neue Berichte eines bestimmten Berichts Typs.</span><span class="sxs-lookup"><span data-stu-id="b4115-114">Defines possible status for new reports of a particular report type.</span></span> |



 

## <a name="location-constants-from-the-sensor-api"></a><span data-ttu-id="b4115-115">Location-Konstanten von der Sensor-API</span><span class="sxs-lookup"><span data-stu-id="b4115-115">Location Constants from the Sensor API</span></span>

<span data-ttu-id="b4115-116">Die Sensor-API definiert auch standortbezogene Eigenschaften Schlüssel und-Konstanten.</span><span class="sxs-lookup"><span data-stu-id="b4115-116">The Sensor API also defines location-related property keys and constants.</span></span> <span data-ttu-id="b4115-117">Die in "Sensors. h" definierten Eigenschafts Schlüssel können zum Abrufen von Standortdaten aus einem Bericht durch Aufrufen von " [**ilocationreport:: GetValue**](/windows/win32/api/locationapi/nf-locationapi-ilocationreport-getvalue)" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4115-117">The property keys defined in sensors.h can be used to retrieve location data from a report by calling [**ILocationReport::GetValue**](/windows/win32/api/locationapi/nf-locationapi-ilocationreport-getvalue).</span></span>

 

 
