---
description: Die folgenden Qualifizierer werden vom WDM-Anbieter in den Gerätetreiber-MOF-Dateien verwendet, wenn Sie Daten aus wnodes extrahieren, um Instanzen von WDM-Treiber Klassen zu generieren.
ms.assetid: 11b0af59-979f-4908-baef-c9ec564b3cfd
ms.tgt_platform: multiple
title: Spezifische Qualifizierer für den WDM-Anbieter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: be2bc4593c19555dd5a851de89a1dc2e5db00596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372905"
---
# <a name="qualifiers-specific-to-the-wdm-provider"></a><span data-ttu-id="1b55a-103">Spezifische Qualifizierer für den WDM-Anbieter</span><span class="sxs-lookup"><span data-stu-id="1b55a-103">Qualifiers Specific to the WDM Provider</span></span>

<span data-ttu-id="1b55a-104">Die folgenden Qualifizierer werden vom [WDM-Anbieter](/windows/desktop/WmiCoreProv/wdm-provider) in den Gerätetreiber-MOF-Dateien verwendet, wenn Sie Daten aus wnodes extrahieren, um Instanzen von WDM-Treiber Klassen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="1b55a-104">The following qualifiers are used by the [WDM Provider](/windows/desktop/WmiCoreProv/wdm-provider) in device driver MOF files when they are extracting data from WNODEs to generate instances of WDM driver classes.</span></span>

<dt>

<span data-ttu-id="1b55a-105"><span id="MissingValue"></span><span id="missingvalue"></span><span id="MISSINGVALUE"></span>**Missingvalue**</span><span class="sxs-lookup"><span data-stu-id="1b55a-105"><span id="MissingValue"></span><span id="missingvalue"></span><span id="MISSINGVALUE"></span>**MissingValue**</span></span>
</dt> <dd>

<span data-ttu-id="1b55a-106">Datentyp: **DWORD, Array, Uint8, UInt16, UInt32, sint8, sint16 oder sint32.**</span><span class="sxs-lookup"><span data-stu-id="1b55a-106">Data type: **DWORD, array, uint8, uint16, uint32, sint8, sint16, or sint32.**</span></span>

<span data-ttu-id="1b55a-107">Gilt für: Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1b55a-107">Applies to: properties</span></span>

<span data-ttu-id="1b55a-108">Ein fehlender Wert für diese Eigenschaft sollte durch **null** anstelle von 0 (null) dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1b55a-108">A missing value for this property should be represented by **NULL** rather than 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="1b55a-109"><span id="WMIDataId"></span><span id="wmidataid"></span><span id="WMIDATAID"></span>**Wmidataid**</span><span class="sxs-lookup"><span data-stu-id="1b55a-109"><span id="WMIDataId"></span><span id="wmidataid"></span><span id="WMIDATAID"></span>**WMIDataId**</span></span>
</dt> <dd>

<span data-ttu-id="1b55a-110">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1b55a-110">Data type: **uint32**</span></span>

<span data-ttu-id="1b55a-111">Gilt für: Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1b55a-111">Applies to: properties</span></span>

<span data-ttu-id="1b55a-112">Index im wnode der Daten für die-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1b55a-112">Index in the WNODE of the data for the property.</span></span> <span data-ttu-id="1b55a-113">Der WDM-Anbieter verwendet diesen Qualifizierer, um zu bestimmen, wie die Daten formatiert werden, während Daten aus dem wnode extrahiert und WMI-Klassen erzeugt werden</span><span class="sxs-lookup"><span data-stu-id="1b55a-113">The WDM provider uses this qualifier to determine how the data is formatted while extracting data from the WNODE and generating WMI classes.</span></span> <span data-ttu-id="1b55a-114">Der Startwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="1b55a-114">The starting value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="1b55a-115"><span id="WMIExpense"></span><span id="wmiexpense"></span><span id="WMIEXPENSE"></span>**WMI-Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="1b55a-115"><span id="WMIExpense"></span><span id="wmiexpense"></span><span id="WMIEXPENSE"></span>**WMIExpense**</span></span>
</dt> <dd>

<span data-ttu-id="1b55a-116">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1b55a-116">Data type: **uint32**</span></span>

<span data-ttu-id="1b55a-117">Gilt für: Klassen</span><span class="sxs-lookup"><span data-stu-id="1b55a-117">Applies to: classes</span></span>

<span data-ttu-id="1b55a-118">Gibt Aufschluss über die Ressourcenkosten für den Zugriff auf den Datenblock.</span><span class="sxs-lookup"><span data-stu-id="1b55a-118">Indication of the resource cost to access the data block.</span></span> <span data-ttu-id="1b55a-119">Beispielsweise sind für Datenträger Geometrie Informationen nicht viele Ressourcen erforderlich, da Sie in der Geräte Erweiterung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="1b55a-119">For example, disk geometry information does not require a lot of resources to obtain because it is available in the device extension.</span></span> <span data-ttu-id="1b55a-120">Die Datenträger-Lese-/Schreibleistung ist ressourcenintensiver, da für jeden Lese-/Schreibvorgang zusätzliche Arbeit erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1b55a-120">Disk read/write performance is more resource-intensive because it requires extra work on each read/write operation.</span></span> <span data-ttu-id="1b55a-121">Daher ist der Wert für den **WMI-Ausgaben** Qualifizierer für die Lese-/Schreibleistung des Datenträgers</span><span class="sxs-lookup"><span data-stu-id="1b55a-121">Therefore, the **WMIExpense** qualifier value is larger for disk read/write performance.</span></span>

</dd> <dt>

<span data-ttu-id="1b55a-122"><span id="WMIMethodId"></span><span id="wmimethodid"></span><span id="WMIMETHODID"></span>**Wmimethodid**</span><span class="sxs-lookup"><span data-stu-id="1b55a-122"><span id="WMIMethodId"></span><span id="wmimethodid"></span><span id="WMIMETHODID"></span>**WMIMethodId**</span></span>
</dt> <dd>

<span data-ttu-id="1b55a-123">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1b55a-123">Data type: **uint32**</span></span>

<span data-ttu-id="1b55a-124">Gilt für: Methoden</span><span class="sxs-lookup"><span data-stu-id="1b55a-124">Applies to: methods</span></span>

<span data-ttu-id="1b55a-125">Index im wnode der Daten für die-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1b55a-125">Index in the WNODE of the data for the property.</span></span> <span data-ttu-id="1b55a-126">Der WDM-Anbieter verwendet diesen Qualifizierer, um zu bestimmen, wie die Daten formatiert werden, während Daten aus dem wnode extrahiert und WMI-Klassen erzeugt werden</span><span class="sxs-lookup"><span data-stu-id="1b55a-126">The WDM provider uses this qualifier to determine how the data is formatted while extracting data from the WNODE and generating WMI classes.</span></span> <span data-ttu-id="1b55a-127">Der Startwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="1b55a-127">The starting value is 1.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1b55a-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b55a-128">Requirements</span></span>



| <span data-ttu-id="1b55a-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b55a-129">Requirement</span></span> | <span data-ttu-id="1b55a-130">Wert</span><span class="sxs-lookup"><span data-stu-id="1b55a-130">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="1b55a-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b55a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1b55a-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1b55a-132">Windows Vista</span></span><br/>       |
| <span data-ttu-id="1b55a-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b55a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1b55a-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b55a-134">Windows Server 2008</span></span><br/> |



 

