---
description: Gibt Zusammenfassungs Informationen für virtuelle Computer zurück.
ms.assetid: CDDC2B5A-8172-4E6D-A206-CEAB9E54C69A
title: Getsummaryinformation-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetSummaryInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1399acd40f768fdb857d6a4a26e80a52d29111b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342799"
---
# <a name="getsummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="f8a09-103">Getsummaryinformation-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="f8a09-103">GetSummaryInformation method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="f8a09-104">Gibt Zusammenfassungs Informationen für virtuelle Computer zurück.</span><span class="sxs-lookup"><span data-stu-id="f8a09-104">Returns virtual machine summary information.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8a09-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8a09-105">Syntax</span></span>


```mof
uint32 GetSummaryInformation(
  [in]  CIM_VirtualSystemSettingData REF SettingData[],
  [in]  uint32                           RequestedInformation[],
  [out] Msvm_SummaryInformationBase      SummaryInformation[]
);
```



## <a name="parameters"></a><span data-ttu-id="f8a09-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8a09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8a09-107">*SettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f8a09-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8a09-108">Typ: **CIM \_ virtualsystemsettingdata \[ \]**</span><span class="sxs-lookup"><span data-stu-id="f8a09-108">Type: **CIM\_VirtualSystemSettingData\[\]**</span></span>

<span data-ttu-id="f8a09-109">Ein Array von [**CIM- \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85)) -Instanzen, die die virtuellen Computer oder Momentaufnahmen angeben, für die Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f8a09-109">An array of [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instances that specify the virtual machines or snapshots for which information is to be retrieved.</span></span> <span data-ttu-id="f8a09-110">Wenn dieser Parameter **null** ist, werden Informationen für alle virtuellen Computer abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f8a09-110">If this parameter is **Null**, information for all virtual machines is retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="f8a09-111">*Requestedinformation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f8a09-111">*RequestedInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8a09-112">Typ: **UInt32 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="f8a09-112">Type: **uint32\[\]**</span></span>

<span data-ttu-id="f8a09-113">Ein Array von Enumerationswerten, die den Eigenschaften in der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse entsprechen, die die Daten angeben, die für die im *SettingData* -Array angegebenen virtuellen Maschinen und Momentaufnahmen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f8a09-113">An array of enumeration values, which correspond to the properties in the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class, that specify the data to retrieve for the virtual machines and snapshots specified in the *SettingData* array.</span></span>

<dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>

<span data-ttu-id="f8a09-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name** (0)</span><span class="sxs-lookup"><span data-stu-id="f8a09-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-115">Dies entspricht der **Name** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="f8a09-115">This corresponds to the **Name** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>

<span data-ttu-id="f8a09-116"><span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>**Element Name** (1)</span><span class="sxs-lookup"><span data-stu-id="f8a09-116"><span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>**Element Name** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-117">Dies entspricht der **ElementName** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="f8a09-117">This corresponds to the **ElementName** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>

<span data-ttu-id="f8a09-118"><span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>**Erstellungszeit** (2)</span><span class="sxs-lookup"><span data-stu-id="f8a09-118"><span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>**Creation Time** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-119">Dies entspricht der Eigenschaft " **kreationtime** " der Klasse " [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) ".</span><span class="sxs-lookup"><span data-stu-id="f8a09-119">This corresponds to the **CreationTime** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>

<span data-ttu-id="f8a09-120"><span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>**Hinweise** (3)</span><span class="sxs-lookup"><span data-stu-id="f8a09-120"><span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>**Notes** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-121">Dies entspricht der **Notes** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="f8a09-121">This corresponds to the **Notes** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>

<span data-ttu-id="f8a09-122"><span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>**Anzahl der Prozessoren** (4)</span><span class="sxs-lookup"><span data-stu-id="f8a09-122"><span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>**Number of Processors** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-123">Dies entspricht der Eigenschaft " **numofprocessor** " der [**MSVM-Klasse " \_ SummaryInformation**](msvm-summaryinformation.md) ".</span><span class="sxs-lookup"><span data-stu-id="f8a09-123">This corresponds to the **NumberOfProcessors** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>

<span data-ttu-id="f8a09-124"><span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>**Kleines Miniaturbild (80X 60)** (5)</span><span class="sxs-lookup"><span data-stu-id="f8a09-124"><span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>**Small Thumbnail Image (80x60)** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-125">Dies entspricht der **thumbnailimage** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="f8a09-125">This corresponds to the **ThumbnailImage** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span> <span data-ttu-id="f8a09-126">Ein Miniaturbild mit den Abmessungen 80 60 wird abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f8a09-126">A thumbnail image with the dimensions of 80 60 will be retrieved.</span></span>

</dd> <dt>

<span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>

<span data-ttu-id="f8a09-127"><span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>**Bild für mittlere Miniaturansicht (160 x 120)** (6)</span><span class="sxs-lookup"><span data-stu-id="f8a09-127"><span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>**Medium Thumbnail Image (160x120)** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-128">Dies entspricht der **thumbnailimage** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="f8a09-128">This corresponds to the **ThumbnailImage** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span> <span data-ttu-id="f8a09-129">Ein Miniaturbild mit den Abmessungen 160 120 wird abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f8a09-129">A thumbnail image with the dimensions of 160 120 will be retrieved.</span></span>

</dd> <dt>

<span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>

<span data-ttu-id="f8a09-130"><span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>**Großes Miniaturbild (320 x 240)** (7)</span><span class="sxs-lookup"><span data-stu-id="f8a09-130"><span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>**Large Thumbnail Image (320x240)** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-131">Dies entspricht der **thumbnailimage** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="f8a09-131">This corresponds to the **ThumbnailImage** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span> <span data-ttu-id="f8a09-132">Ein Miniaturbild mit den Abmessungen 320 240 wird abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f8a09-132">A thumbnail image with the dimensions of 320 240 will be retrieved.</span></span>

</dd> <dt>

<span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>

<span data-ttu-id="f8a09-133"><span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>**Zugedgpu** (8)</span><span class="sxs-lookup"><span data-stu-id="f8a09-133"><span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>**AllocatedGPU** (8)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-134">Dies entspricht der Eigenschaft " **zugseredgpu** " der [**MSVM-Klasse " \_ SummaryInformation**](msvm-summaryinformation.md) ".</span><span class="sxs-lookup"><span data-stu-id="f8a09-134">This corresponds to the **AllocatedGPU** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>

<span data-ttu-id="f8a09-135"><span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>**Virtualswitchnames** (9)</span><span class="sxs-lookup"><span data-stu-id="f8a09-135"><span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>**VirtualSwitchNames** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>

<span data-ttu-id="f8a09-136"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version** (10)</span><span class="sxs-lookup"><span data-stu-id="f8a09-136"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version** (10)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="f8a09-137">In Windows 10 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f8a09-137">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span data-ttu-id="f8a09-138"><span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Abgeschirmt** (11)</span><span class="sxs-lookup"><span data-stu-id="f8a09-138"><span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Shielded** (11)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="f8a09-139">In Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f8a09-139">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>

<span data-ttu-id="f8a09-140"><span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>**Enabledstate** (100)</span><span class="sxs-lookup"><span data-stu-id="f8a09-140"><span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>**EnabledState** (100)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-141">Dies entspricht der **enabledstate** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="f8a09-141">This corresponds to the **EnabledState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>

<span data-ttu-id="f8a09-142"><span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>**Processorload** (101)</span><span class="sxs-lookup"><span data-stu-id="f8a09-142"><span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>**ProcessorLoad** (101)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-143">Dies entspricht der **processorload** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="f8a09-143">This corresponds to the **ProcessorLoad** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>

<span data-ttu-id="f8a09-144"><span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>**Processorloadhistory** (102)</span><span class="sxs-lookup"><span data-stu-id="f8a09-144"><span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>**ProcessorLoadHistory** (102)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-145">Dies entspricht der **processorloadhistory** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="f8a09-145">This corresponds to the **ProcessorLoadHistory** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>

<span data-ttu-id="f8a09-146"><span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>**Memoryusage** (103)</span><span class="sxs-lookup"><span data-stu-id="f8a09-146"><span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>**MemoryUsage** (103)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-147">Dies entspricht der **memoryusage** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="f8a09-147">This corresponds to the **MemoryUsage** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>

<span data-ttu-id="f8a09-148"><span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>Takt **(104** )</span><span class="sxs-lookup"><span data-stu-id="f8a09-148"><span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>**Heartbeat** (104)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-149">Dies entspricht der **Heartbeat** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="f8a09-149">This corresponds to the **Heartbeat** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>

<span data-ttu-id="f8a09-150"><span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>**Betriebszeit** (105)</span><span class="sxs-lookup"><span data-stu-id="f8a09-150"><span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>**Uptime** (105)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-151">Dies entspricht der Eigenschaft " **Uptime** " der Klasse " [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) ".</span><span class="sxs-lookup"><span data-stu-id="f8a09-151">This corresponds to the **UpTime** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>

<span data-ttu-id="f8a09-152"><span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>**Guestoperatingsystem** (106)</span><span class="sxs-lookup"><span data-stu-id="f8a09-152"><span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>**GuestOperatingSystem** (106)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-153">Dies entspricht der **guestoperatingsystem** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="f8a09-153">This corresponds to the **GuestOperatingSystem** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>

<span data-ttu-id="f8a09-154"><span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>**Momentaufnahmen** (107)</span><span class="sxs-lookup"><span data-stu-id="f8a09-154"><span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>**Snapshots** (107)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-155">Dies entspricht der **Momentaufnahmen** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="f8a09-155">This corresponds to the **Snapshots** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>

<span data-ttu-id="f8a09-156"><span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>**Asynchronoustasks** (108)</span><span class="sxs-lookup"><span data-stu-id="f8a09-156"><span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>**AsynchronousTasks** (108)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-157">Dies entspricht der **asynchronoustasks** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="f8a09-157">This corresponds to the **AsynchronousTasks** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>

<span data-ttu-id="f8a09-158"><span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>**Healthstate** (109)</span><span class="sxs-lookup"><span data-stu-id="f8a09-158"><span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>**HealthState** (109)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-159">Dies entspricht der **healthstate** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="f8a09-159">This corresponds to the **HealthState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>

<span data-ttu-id="f8a09-160"><span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>**OperationalStatus** (110)</span><span class="sxs-lookup"><span data-stu-id="f8a09-160"><span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>**OperationalStatus** (110)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-161">Dies entspricht der **OperationalStatus** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="f8a09-161">This corresponds to the **OperationalStatus** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>

<span data-ttu-id="f8a09-162"><span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>**Status Beschreibungen** (111)</span><span class="sxs-lookup"><span data-stu-id="f8a09-162"><span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>**StatusDescriptions** (111)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-163">Dies entspricht der Eigenschaft " **Status Beschreibungen** " der [**MSVM-Klasse " \_ SummaryInformation**](msvm-summaryinformation.md) ".</span><span class="sxs-lookup"><span data-stu-id="f8a09-163">This corresponds to the **StatusDescriptions** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>

<span data-ttu-id="f8a09-164"><span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>Speicher **verfügbar** (112)</span><span class="sxs-lookup"><span data-stu-id="f8a09-164"><span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>**MemoryAvailable** (112)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-165">Dies entspricht der **memoryavailable** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="f8a09-165">This corresponds to the **MemoryAvailable** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>

<span data-ttu-id="f8a09-166"><span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>**Availablememorybuffer** (113)</span><span class="sxs-lookup"><span data-stu-id="f8a09-166"><span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>**AvailableMemoryBuffer** (113)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-167">Dies entspricht der **availablememorybuffer** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="f8a09-167">This corresponds to the **AvailableMemoryBuffer** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>

<span data-ttu-id="f8a09-168"><span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>**Replikations Modus** (114)</span><span class="sxs-lookup"><span data-stu-id="f8a09-168"><span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>**Replication Mode** (114)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-169">Dies entspricht der **replicationmode** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="f8a09-169">This corresponds to the **ReplicationMode** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>

<span data-ttu-id="f8a09-170"><span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>**Replikations Status** (115)</span><span class="sxs-lookup"><span data-stu-id="f8a09-170"><span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>**Replication State** (115)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-171">Dies entspricht der **replicationstate** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="f8a09-171">This corresponds to the **ReplicationState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>

<span data-ttu-id="f8a09-172"><span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>**Replikation healthtest Replica System** (116)</span><span class="sxs-lookup"><span data-stu-id="f8a09-172"><span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>**Replication HealthTest Replica System** (116)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-173">Dies entspricht der **ReplicationHealth** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="f8a09-173">This corresponds to the **ReplicationHealth** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>

<span data-ttu-id="f8a09-174"><span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>**Anwendungs** Integrität (117)</span><span class="sxs-lookup"><span data-stu-id="f8a09-174"><span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>**Application Health** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>

<span data-ttu-id="f8a09-175"><span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>**Replicationstateex** (118)</span><span class="sxs-lookup"><span data-stu-id="f8a09-175"><span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>**ReplicationStateEx** (118)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-176">Dies entspricht der **replicationstate** -Eigenschaft der [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="f8a09-176">This corresponds to the **ReplicationState** property of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class.</span></span> <span data-ttu-id="f8a09-177">Dies ist ein Array für alle Replikations Zustands Werte über die primäre und erweiterte Beziehung hinweg.</span><span class="sxs-lookup"><span data-stu-id="f8a09-177">This is array for all replication state values across primary and extended relationship.</span></span> <span data-ttu-id="f8a09-178">0 der Indexwert ist für die primäre Beziehung immer, und wenn die erweiterte Replikation aktiviert ist, wird Sie in Index 1 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f8a09-178">0 index value is always for primary relationship, and if extended replication is enabled, it is returned in index 1.</span></span>

</dd> <dt>

<span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>

<span data-ttu-id="f8a09-179"><span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>**Replicationhealthex** (119)</span><span class="sxs-lookup"><span data-stu-id="f8a09-179"><span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>**ReplicationHealthEx** (119)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-180">Dies entspricht der **ReplicationHealth** -Eigenschaft der [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="f8a09-180">This corresponds to the **ReplicationHealth** property of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class.</span></span> <span data-ttu-id="f8a09-181">Dies ist ein Array für alle Replikations Integritäts Werte über die primäre und erweiterte Beziehung hinweg.</span><span class="sxs-lookup"><span data-stu-id="f8a09-181">This is array for all replication health values across primary and extended relationship.</span></span> <span data-ttu-id="f8a09-182">0 der Indexwert ist für die primäre Beziehung immer, und wenn die erweiterte Replikation aktiviert ist, wird Sie in Index 1 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f8a09-182">0 index value is always for primary relationship, and if extended replication is enabled, it is returned in index 1.</span></span>

</dd> <dt>

<span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>

<span data-ttu-id="f8a09-183"><span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>" **Swap-FilesInUse** " (120)</span><span class="sxs-lookup"><span data-stu-id="f8a09-183"><span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>**SwapFilesInUse** (120)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-184">Dies entspricht der Eigenschaft " **shiapfilesinuse** " der Klasse " [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) ".</span><span class="sxs-lookup"><span data-stu-id="f8a09-184">This corresponds to the **SwapFilesInUse** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span data-ttu-id="f8a09-185"><span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**Integrationservicesversionstate** (121)</span><span class="sxs-lookup"><span data-stu-id="f8a09-185"><span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>

<span data-ttu-id="f8a09-186"><span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>**Replicationproviderid** (122)</span><span class="sxs-lookup"><span data-stu-id="f8a09-186"><span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>**ReplicationProviderId** (122)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-187">Dies entspricht der **Name** -Eigenschaft der [**MSVM \_ replicationprovider**](msvm-replicationprovider.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="f8a09-187">This corresponds to the **Name** property of the [**Msvm\_ReplicationProvider**](msvm-replicationprovider.md) class.</span></span>

</dd> <dt>

<span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>

<span data-ttu-id="f8a09-188"><span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>**Memoryspansphysicalnumanodes** (123)</span><span class="sxs-lookup"><span data-stu-id="f8a09-188"><span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>**MemorySpansPhysicalNumaNodes** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span data-ttu-id="f8a09-189"><span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**Integrationservicesversionstate** (132)</span><span class="sxs-lookup"><span data-stu-id="f8a09-189"><span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (132)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-190">Dies entspricht der **integrationservicesversionstate** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="f8a09-190">This corresponds to the **IntegrationServicesVersionState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>

<span data-ttu-id="f8a09-191"><span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>**Otherenabledstate** (132)</span><span class="sxs-lookup"><span data-stu-id="f8a09-191"><span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>**OtherEnabledState** (132)</span></span>


</dt> <dd>

<span data-ttu-id="f8a09-192">Dies entspricht der **otherenabledstate** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="f8a09-192">This corresponds to the **OtherEnabledState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>



 <span data-ttu-id="f8a09-193">(133)</span><span class="sxs-lookup"><span data-stu-id="f8a09-193">(133)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="f8a09-194">*SummaryInformation* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f8a09-194">*SummaryInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8a09-195">Typ: **[ **MSVM \_ summaryinformationbase**](msvm-summaryinformationbase.md)\[\]**</span><span class="sxs-lookup"><span data-stu-id="f8a09-195">Type: **[**Msvm\_SummaryInformationBase**](msvm-summaryinformationbase.md)\[\]**</span></span>

<span data-ttu-id="f8a09-196">Ein Array von [**MSVM- \_ summaryinformationbase**](msvm-summaryinformationbase.md) -Instanzen, die die angeforderten Informationen für die virtuellen Computer und/oder Momentaufnahmen enthalten, die im *SettingData* -Array angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="f8a09-196">An array of [**Msvm\_SummaryInformationBase**](msvm-summaryinformationbase.md) instances containing the requested information for the virtual machines and/or snapshots specified in the *SettingData* array.</span></span> <span data-ttu-id="f8a09-197">Dieses Array verfügt über die gleiche Anzahl von Elementen wie das *SettingData* -Array.</span><span class="sxs-lookup"><span data-stu-id="f8a09-197">This array will have the same number of elements as the *SettingData* array.</span></span> <span data-ttu-id="f8a09-198">Jeder dieser Einträge enthält die **Name** -Eigenschaft, auch wenn diese Eigenschaft nicht angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="f8a09-198">Each of these entries will contain the **Name** property, even if this property was not requested.</span></span> <span data-ttu-id="f8a09-199">Wenn der virtuelle Computer oder die Momentaufnahme nicht gefunden werden kann oder nicht verfügbar ist, ist die **Name** -Eigenschaft des entsprechenden zusammenfassenden Informations Eintrags leer.</span><span class="sxs-lookup"><span data-stu-id="f8a09-199">If the virtual machine or snapshot cannot be found or is unavailable, the **Name** property of the corresponding summary information entry will be empty.</span></span>

<span data-ttu-id="f8a09-200">Eigenschaften, die nicht im *requestedinformation* -Parameter angegeben sind, haben einen **null** -Wert.</span><span class="sxs-lookup"><span data-stu-id="f8a09-200">Properties not specified in the *RequestedInformation* parameter will have a **Null** value.</span></span>

> [!Note]  
> <span data-ttu-id="f8a09-201">Der Datentyp wurde in Windows 10, Version 1703, von [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md)aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f8a09-201">Datatype updated from in Windows 10, version 1703 from [**Msvm\_SummaryInformation**](msvm-summaryinformation.md).</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8a09-202">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8a09-202">Return value</span></span>

<span data-ttu-id="f8a09-203">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f8a09-203">Type: **uint32**</span></span>

<span data-ttu-id="f8a09-204">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="f8a09-204">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f8a09-205">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="f8a09-205">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f8a09-206">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="f8a09-206">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f8a09-207">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="f8a09-207">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f8a09-208">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="f8a09-208">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f8a09-209">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="f8a09-209">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f8a09-210">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="f8a09-210">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f8a09-211">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="f8a09-211">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f8a09-212">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="f8a09-212">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f8a09-213">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="f8a09-213">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f8a09-214">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="f8a09-214">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f8a09-215">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="f8a09-215">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f8a09-216">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="f8a09-216">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f8a09-217">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="f8a09-217">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="f8a09-218">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8a09-218">Remarks</span></span>

<span data-ttu-id="f8a09-219">Der Zugriff auf die [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="f8a09-219">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f8a09-220">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f8a09-220">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="f8a09-221">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8a09-221">Examples</span></span>

<span data-ttu-id="f8a09-222">Im folgenden c#-Beispiel werden Zusammenfassungs Informationen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f8a09-222">The following C# sample displays summary information.</span></span> <span data-ttu-id="f8a09-223">Die Dienstprogramme, auf die verwiesen wird, finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="f8a09-223">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f8a09-224">Der folgende Code muss auf dem Host Server des virtuellen Computers ausgeführt werden, und er muss mit Administrator Rechten ausgeführt werden, um ordnungsgemäß zu funktionieren.</span><span class="sxs-lookup"><span data-stu-id="f8a09-224">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
public class GetSummaryInformationClassV2
{
    public static void GetSummaryInformation(string[] vmNames)
    {
        ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
        ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");
        ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("GetSummaryInformation");

        ManagementObject[] virtualSystemSettings = new ManagementObject[vmNames.Length];

        for (int i = 0; i < vmNames.Length; i++)
        {
            virtualSystemSettings[i] = GetVirtualSystemSetting(vmNames[i], scope);
        }

        UInt32[] requestedInformation = new UInt32[4];
        requestedInformation[0] = 1;    // ElementName
        requestedInformation[2] = 103;  // MemoryUsage
        requestedInformation[3] = 112;  // MemoryAvailable

        inParams["SettingData"] = virtualSystemSettings;
        inParams["RequestedInformation"] = requestedInformation;

        ManagementBaseObject outParams = virtualSystemService.InvokeMethod("GetSummaryInformation", inParams, null);

        if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
        {
            Console.WriteLine("Summary information was retrieved successfully.");

            ManagementBaseObject[] summaryInformationArray = 
                (ManagementBaseObject[])outParams["SummaryInformation"];

            foreach (ManagementBaseObject summaryInformation in summaryInformationArray)
            {
                Console.WriteLine("\nVirtual System Summary Information:");
                if ((null == summaryInformation["Name"]) || 
                    (summaryInformation["Name"].ToString().Length == 0))
                {
                    Console.WriteLine("\tThe VM or snapshot could not be found.");
                }
                else
                {
                    Console.WriteLine("\tName: {0}", summaryInformation["Name"].ToString());
                    foreach (UInt32 requested in requestedInformation)
                    {
                        switch (requested)
                        {
                            case 1:
                                Console.WriteLine("\tElementName: {0}", summaryInformation["ElementName"].ToString());
                                break;

                            case 103:
                                Console.WriteLine("\tMemoryUsage: {0}", summaryInformation["MemoryUsage"].ToString());
                                break;

                            case 112:
                                Console.WriteLine("\tMemoryAvailable: {0}", summaryInformation["MemoryAvailable"].ToString());
                                break;
                        }
                    }
                }
            }
        }
        else
        {
            Console.WriteLine("Failed to retrieve virtual system summary information");
        }

        inParams.Dispose();
        outParams.Dispose();
        virtualSystemService.Dispose();
    }

    public static ManagementObject GetVirtualSystemSetting(string vmName, ManagementScope scope)
    {
        ManagementObject virtualSystem = Utility.GetTargetComputer(vmName, scope);

        ManagementObjectCollection virtualSystemSettings = virtualSystem.GetRelated
         (
             "Msvm_VirtualSystemSettingData",
             "Msvm_SettingsDefineState",
             null,
             null,
             "SettingData",
             "ManagedElement",
             false,
             null
         );

        ManagementObject virtualSystemSetting = null;

        foreach (ManagementObject instance in virtualSystemSettings)
        {
            virtualSystemSetting = instance;
            break;
        }

        return virtualSystemSetting;

    }
}
```



## <a name="requirements"></a><span data-ttu-id="f8a09-225">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8a09-225">Requirements</span></span>



| <span data-ttu-id="f8a09-226">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8a09-226">Requirement</span></span> | <span data-ttu-id="f8a09-227">Wert</span><span class="sxs-lookup"><span data-stu-id="f8a09-227">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8a09-228">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f8a09-228">Minimum supported client</span></span><br/> | <span data-ttu-id="f8a09-229">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8a09-229">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f8a09-230">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f8a09-230">Minimum supported server</span></span><br/> | <span data-ttu-id="f8a09-231">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8a09-231">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f8a09-232">Namespace</span><span class="sxs-lookup"><span data-stu-id="f8a09-232">Namespace</span></span><br/>                | <span data-ttu-id="f8a09-233">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="f8a09-233">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f8a09-234">MOF</span><span class="sxs-lookup"><span data-stu-id="f8a09-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8a09-235"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f8a09-235"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8a09-236">DLL</span><span class="sxs-lookup"><span data-stu-id="f8a09-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8a09-237"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f8a09-237"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f8a09-238">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8a09-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8a09-239">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="f8a09-239">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="f8a09-240">[**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f8a09-240">[**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f8a09-241">**MSVM- \_ SummaryInformation**</span><span class="sxs-lookup"><span data-stu-id="f8a09-241">**Msvm\_SummaryInformation**</span></span>](msvm-summaryinformation.md)
</dt> </dl>

 

