---
description: Enthält ein korrigiertes Computer Überprüfung-Ereignis (CMC). Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.
ms.assetid: e12efbf7-7d53-415a-bc48-90d33e4ce16d
title: MSMCAInfo_RawCMCEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawCMCEvent
- MSMCAInfo_RawCMCEvent.Active
- MSMCAInfo_RawCMCEvent.Count
- MSMCAInfo_RawCMCEvent.InstanceName
- MSMCAInfo_RawCMCEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 1bb60d5fbcf004b924a91e640d8cd8a8c5ad3c25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352254"
---
# <a name="msmcainfo_rawcmcevent-class"></a><span data-ttu-id="de9ad-104">Msmcainfo \_ rawcmcevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="de9ad-104">MSMCAInfo\_RawCMCEvent class</span></span>

<span data-ttu-id="de9ad-105">Die **msmcainfo \_ rawcmcevent** -Klasse enthält ein "korrigiertes Computer Überprüfung (CMC)"-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="de9ad-105">The **MSMCAInfo\_RawCMCEvent** class contains a Corrected Machine Check (CMC) event.</span></span> <span data-ttu-id="de9ad-106">Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="de9ad-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="de9ad-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="de9ad-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="de9ad-108">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="de9ad-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="de9ad-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="de9ad-109">Syntax</span></span>

``` syntax
class MSMCAInfo_RawCMCEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a><span data-ttu-id="de9ad-110">Member</span><span class="sxs-lookup"><span data-stu-id="de9ad-110">Members</span></span>

<span data-ttu-id="de9ad-111">Die **msmcainfo \_ rawcmcevent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="de9ad-111">The **MSMCAInfo\_RawCMCEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="de9ad-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="de9ad-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="de9ad-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="de9ad-113">Properties</span></span>

<span data-ttu-id="de9ad-114">Die **msmcainfo \_ rawcmcevent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="de9ad-114">The **MSMCAInfo\_RawCMCEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="de9ad-115">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="de9ad-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de9ad-116">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="de9ad-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="de9ad-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="de9ad-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de9ad-118">TRUE, wenn diese Instanz der-Klasse aktiv ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="de9ad-118">TRUE, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="de9ad-119">**Count**</span><span class="sxs-lookup"><span data-stu-id="de9ad-119">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de9ad-120">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="de9ad-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="de9ad-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="de9ad-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de9ad-122">Anzahl der Fehler Datensätze.</span><span class="sxs-lookup"><span data-stu-id="de9ad-122">Number of error records.</span></span>

</dd> <dt>

<span data-ttu-id="de9ad-123">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="de9ad-123">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de9ad-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="de9ad-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de9ad-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="de9ad-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de9ad-126">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="de9ad-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="de9ad-127">Eindeutiger Bezeichner dieser Instanz der Klasse.</span><span class="sxs-lookup"><span data-stu-id="de9ad-127">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="de9ad-128">**Datensätze**</span><span class="sxs-lookup"><span data-stu-id="de9ad-128">**Records**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de9ad-129">Datentyp: **msmcainfo- \_ Eingabe** Array</span><span class="sxs-lookup"><span data-stu-id="de9ad-129">Data type: **MSMCAInfo\_Entry** array</span></span>
</dt> <dt>

<span data-ttu-id="de9ad-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="de9ad-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de9ad-131">Array von MCA-Fehler Datensätzen (Machine Check Architecture).</span><span class="sxs-lookup"><span data-stu-id="de9ad-131">Array of Machine Check Architecture (MCA) error records.</span></span> <span data-ttu-id="de9ad-132">Die Anzahl der MCA-Fehler Datensätze im Array wird durch die **count** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="de9ad-132">The number of MCA error records in the array is specified by the **Count** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de9ad-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de9ad-133">Remarks</span></span>

<span data-ttu-id="de9ad-134">Die **msmcainfo \_ rawcmcevent** -Klasse wird von [**wmievent**](wmievent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="de9ad-134">The **MSMCAInfo\_RawCMCEvent** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="de9ad-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de9ad-135">Requirements</span></span>



| <span data-ttu-id="de9ad-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de9ad-136">Requirement</span></span> | <span data-ttu-id="de9ad-137">Wert</span><span class="sxs-lookup"><span data-stu-id="de9ad-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="de9ad-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de9ad-138">Minimum supported client</span></span><br/> | <span data-ttu-id="de9ad-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="de9ad-139">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="de9ad-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de9ad-140">Minimum supported server</span></span><br/> | <span data-ttu-id="de9ad-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="de9ad-141">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="de9ad-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="de9ad-142">Namespace</span></span><br/>                | <span data-ttu-id="de9ad-143">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="de9ad-143">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="de9ad-144">MOF</span><span class="sxs-lookup"><span data-stu-id="de9ad-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de9ad-145"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="de9ad-145"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="de9ad-146">DLL</span><span class="sxs-lookup"><span data-stu-id="de9ad-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de9ad-147"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de9ad-147"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de9ad-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de9ad-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de9ad-149">MSMCA-Klassen</span><span class="sxs-lookup"><span data-stu-id="de9ad-149">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="de9ad-150">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="de9ad-150">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

