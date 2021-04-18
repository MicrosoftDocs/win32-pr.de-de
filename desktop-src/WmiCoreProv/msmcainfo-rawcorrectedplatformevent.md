---
description: Enthält ein korrigiertes Platt Form Ereignis (CPE). Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.
ms.assetid: b24a390e-293d-4dd4-b747-33c298a5d45f
title: MSMCAInfo_RawCorrectedPlatformEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawCorrectedPlatformEvent
- MSMCAInfo_RawCorrectedPlatformEvent.Active
- MSMCAInfo_RawCorrectedPlatformEvent.Count
- MSMCAInfo_RawCorrectedPlatformEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 906587ca9ee153eb93542c3e749e8164e6a5ee7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366110"
---
# <a name="msmcainfo_rawcorrectedplatformevent-class"></a><span data-ttu-id="ea8fe-104">Msmcainfo \_ rawcorrectedplatformevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="ea8fe-104">MSMCAInfo\_RawCorrectedPlatformEvent class</span></span>

<span data-ttu-id="ea8fe-105">Die **msmcainfo \_ rawcorrectedplatformevent** -Klasse enthält ein korrigiertes Platt Form Ereignis (CPE).</span><span class="sxs-lookup"><span data-stu-id="ea8fe-105">The **MSMCAInfo\_RawCorrectedPlatformEvent** class contains a Corrected Platform Event (CPE).</span></span> <span data-ttu-id="ea8fe-106">Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ea8fe-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="ea8fe-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ea8fe-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="ea8fe-108">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="ea8fe-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea8fe-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea8fe-109">Syntax</span></span>

``` syntax
class MSMCAInfo_RawCorrectedPlatformEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a><span data-ttu-id="ea8fe-110">Member</span><span class="sxs-lookup"><span data-stu-id="ea8fe-110">Members</span></span>

<span data-ttu-id="ea8fe-111">Die **msmcainfo \_ rawcorrectedplatformevent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ea8fe-111">The **MSMCAInfo\_RawCorrectedPlatformEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="ea8fe-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ea8fe-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ea8fe-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ea8fe-113">Properties</span></span>

<span data-ttu-id="ea8fe-114">Die **msmcainfo \_ rawcorrectedplatformevent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ea8fe-114">The **MSMCAInfo\_RawCorrectedPlatformEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ea8fe-115">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="ea8fe-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8fe-116">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ea8fe-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea8fe-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ea8fe-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8fe-118">TRUE, wenn diese Instanz der-Klasse aktiv ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="ea8fe-118">TRUE, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ea8fe-119">**Count**</span><span class="sxs-lookup"><span data-stu-id="ea8fe-119">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8fe-120">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ea8fe-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ea8fe-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ea8fe-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8fe-122">Anzahl der Fehler Datensätze.</span><span class="sxs-lookup"><span data-stu-id="ea8fe-122">Number of error records.</span></span>

</dd> <dt>

<span data-ttu-id="ea8fe-123">**Datensätze**</span><span class="sxs-lookup"><span data-stu-id="ea8fe-123">**Records**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8fe-124">Datentyp: **msmcainfo- \_ Eingabe** Array</span><span class="sxs-lookup"><span data-stu-id="ea8fe-124">Data type: **MSMCAInfo\_Entry** array</span></span>
</dt> <dt>

<span data-ttu-id="ea8fe-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ea8fe-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8fe-126">Array von MCA-Fehler Datensätzen.</span><span class="sxs-lookup"><span data-stu-id="ea8fe-126">Array of MCA error records.</span></span> <span data-ttu-id="ea8fe-127">Die Anzahl der MCA-Fehler Datensätze im Array wird durch die **count** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="ea8fe-127">The number of MCA error records in the array is specified by the **Count** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ea8fe-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea8fe-128">Remarks</span></span>

<span data-ttu-id="ea8fe-129">Die **msmcainfo \_ rawcorrectedplatformevent** -Klasse wird von [**wmievent**](wmievent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ea8fe-129">The **MSMCAInfo\_RawCorrectedPlatformEvent** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ea8fe-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea8fe-130">Requirements</span></span>



| <span data-ttu-id="ea8fe-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea8fe-131">Requirement</span></span> | <span data-ttu-id="ea8fe-132">Wert</span><span class="sxs-lookup"><span data-stu-id="ea8fe-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea8fe-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea8fe-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ea8fe-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ea8fe-134">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="ea8fe-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ea8fe-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ea8fe-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ea8fe-136">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="ea8fe-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="ea8fe-137">Namespace</span></span><br/>                | <span data-ttu-id="ea8fe-138">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="ea8fe-138">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="ea8fe-139">MOF</span><span class="sxs-lookup"><span data-stu-id="ea8fe-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea8fe-140"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ea8fe-140"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="ea8fe-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ea8fe-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea8fe-142"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea8fe-142"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea8fe-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea8fe-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea8fe-144">MSMCA-Klassen</span><span class="sxs-lookup"><span data-stu-id="ea8fe-144">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="ea8fe-145">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="ea8fe-145">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

 




