---
description: Der WDM-Klassen Anbieter definiert die wmibinarymufresource-Klasse \\ im \\ WMI-Stamm Namespace, um die Aufgabe zu unterstützen, den Status der Daten im WMI-Repository zu verfolgen.
ms.assetid: 57416a36-5b3a-4d04-808c-09adc597c47a
title: Wmibinarymufresource-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WMIBinaryMofResource
- WMIBinaryMofResource.HighDateTime
- WMIBinaryMofResource.LowDateTime
- WMIBinaryMofResource.MofProcessed
- WMIBinaryMofResource.Name
api_type:
- Schema
api_location:
- Root\WMI
ms.openlocfilehash: 715436ef19308c811e5486926b3cd7e59ee9de0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863331"
---
# <a name="wmibinarymofresource-class"></a><span data-ttu-id="01703-103">Wmibinarymufresource-Klasse</span><span class="sxs-lookup"><span data-stu-id="01703-103">WMIBinaryMofResource class</span></span>

<span data-ttu-id="01703-104">Der WDM-Klassen Anbieter definiert die **wmibinarymufresource** -Klasse \\ im \\ WMI-Stamm Namespace, um die Aufgabe zu unterstützen, den Status der Daten im WMI-Repository zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="01703-104">The WDM class provider defines the **WMIBinaryMofResource** class in the \\root\\wmi namespace to support the task of keeping track of the status of data in the WMI repository.</span></span>

## <a name="syntax"></a><span data-ttu-id="01703-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="01703-105">Syntax</span></span>

``` syntax
class WMIBinaryMofResource
{
  uint32  HighDateTime;
  uint32  LowDateTime;
  boolean MofProcessed;
  string  Name;
};
```

## <a name="members"></a><span data-ttu-id="01703-106">Member</span><span class="sxs-lookup"><span data-stu-id="01703-106">Members</span></span>

<span data-ttu-id="01703-107">Die **wmibinarymufresource** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="01703-107">The **WMIBinaryMofResource** class has these types of members:</span></span>

-   [<span data-ttu-id="01703-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="01703-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="01703-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="01703-109">Properties</span></span>

<span data-ttu-id="01703-110">Die **wmibinarymufresource** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="01703-110">The **WMIBinaryMofResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="01703-111">**Highdatetime**</span><span class="sxs-lookup"><span data-stu-id="01703-111">**HighDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01703-112">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="01703-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="01703-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="01703-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01703-114">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="01703-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="01703-115">Hohe Hälfte des Datums-/Uhrzeitstempels.</span><span class="sxs-lookup"><span data-stu-id="01703-115">High half of the date-time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="01703-116">**Lowdatetime**</span><span class="sxs-lookup"><span data-stu-id="01703-116">**LowDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01703-117">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="01703-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="01703-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="01703-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01703-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="01703-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="01703-120">Niedrige Hälfte des Datums-/Uhrzeitstempels.</span><span class="sxs-lookup"><span data-stu-id="01703-120">Low half of the date-time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="01703-121">**Durch die Verarbeitung**</span><span class="sxs-lookup"><span data-stu-id="01703-121">**MofProcessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01703-122">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="01703-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="01703-123">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="01703-123">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="01703-124">Flag, das angibt, ob die MOF-Datei vollständig verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="01703-124">Flag indicating whether the .mof file was fully processed.</span></span>

</dd> <dt>

<span data-ttu-id="01703-125">**Name**</span><span class="sxs-lookup"><span data-stu-id="01703-125">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01703-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="01703-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01703-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="01703-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01703-128">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="01703-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="01703-129">Der Name des WDM-fähigen Treibers, der über eine binäre MOF-Datei verfügt, die im WMI-Repository erfolgreich kompiliert wurde.</span><span class="sxs-lookup"><span data-stu-id="01703-129">Name of the WDM enabled driver that has a binary MOF file successfully compiled in the WMI repository.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01703-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01703-130">Remarks</span></span>

<span data-ttu-id="01703-131">Der WDM-Klassen Anbieter erstellt eine Instanz von **wmibinarymufresource** für jeden WDM-Treiber, der eine binäre MOF-Datei bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="01703-131">The WDM class provider creates an instance of **WMIBinaryMofResource** for each WDM driver that supplies a binary MOF file.</span></span>

<span data-ttu-id="01703-132">Wenn WMI den Anbieter initialisiert, vergleicht der Anbieter den Zeitstempel mit dem Zeitstempel der Treiber Image Datei.</span><span class="sxs-lookup"><span data-stu-id="01703-132">Whenever WMI initializes the provider, the provider compares the timestamp with the timestamp of the driver image file.</span></span> <span data-ttu-id="01703-133">Wenn sich die Zeitstempel unterscheiden, kompiliert WMI die MOF-Datei erneut.</span><span class="sxs-lookup"><span data-stu-id="01703-133">If the timestamps differ, WMI re-compiles the MOF file.</span></span>

## <a name="requirements"></a><span data-ttu-id="01703-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01703-134">Requirements</span></span>



| <span data-ttu-id="01703-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01703-135">Requirement</span></span> | <span data-ttu-id="01703-136">Wert</span><span class="sxs-lookup"><span data-stu-id="01703-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="01703-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="01703-137">Minimum supported client</span></span><br/> | <span data-ttu-id="01703-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="01703-138">Windows XP</span></span><br/>                                                              |
| <span data-ttu-id="01703-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="01703-139">Minimum supported server</span></span><br/> | <span data-ttu-id="01703-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="01703-140">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="01703-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="01703-141">Namespace</span></span><br/>                | <span data-ttu-id="01703-142">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="01703-142">Root\\WMI</span></span><br/>                                                               |
| <span data-ttu-id="01703-143">MOF</span><span class="sxs-lookup"><span data-stu-id="01703-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01703-144"><dt>WMI. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="01703-144"><dt>Wmi.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01703-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01703-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01703-146">WDM-Anbieter</span><span class="sxs-lookup"><span data-stu-id="01703-146">WDM Provider</span></span>](wdm-provider.md)
</dt> </dl>

 

