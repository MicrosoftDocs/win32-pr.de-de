---
description: Gibt die MCA-Protokolle (RAW Machine Check Architecture) an. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.
ms.assetid: d465ba8d-14b2-4911-ae19-19ebeb32126e
title: MSMCAInfo_RawMCAData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawMCAData
- MSMCAInfo_RawMCAData.Active
- MSMCAInfo_RawMCAData.Count
- MSMCAInfo_RawMCAData.InstanceName
- MSMCAInfo_RawMCAData.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 6cafc16ddbc91181cc2114def07a193941988228
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526102"
---
# <a name="msmcainfo_rawmcadata-class"></a><span data-ttu-id="fab16-104">Msmcainfo \_ rawmcadata-Klasse</span><span class="sxs-lookup"><span data-stu-id="fab16-104">MSMCAInfo\_RawMCAData class</span></span>

<span data-ttu-id="fab16-105">**Msmcainfo \_ rawmcadata** gibt die MCA-Protokolle (RAW Machine Check Architecture) an.</span><span class="sxs-lookup"><span data-stu-id="fab16-105">The **MSMCAInfo\_RawMCAData** specifies the raw Machine Check Architecture (MCA) logs.</span></span> <span data-ttu-id="fab16-106">Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fab16-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="fab16-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fab16-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="fab16-108">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="fab16-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fab16-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fab16-109">Syntax</span></span>

``` syntax
class MSMCAInfo_RawMCAData : MSMCAInfo
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a><span data-ttu-id="fab16-110">Member</span><span class="sxs-lookup"><span data-stu-id="fab16-110">Members</span></span>

<span data-ttu-id="fab16-111">Die **msmcainfo \_ rawmcadata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fab16-111">The **MSMCAInfo\_RawMCAData** class has these types of members:</span></span>

-   [<span data-ttu-id="fab16-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fab16-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fab16-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fab16-113">Properties</span></span>

<span data-ttu-id="fab16-114">Die **msmcainfo \_ rawmcadata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fab16-114">The **MSMCAInfo\_RawMCAData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fab16-115">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="fab16-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab16-116">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fab16-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fab16-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fab16-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab16-118">TRUE, wenn diese Instanz der-Klasse aktiv ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="fab16-118">TRUE, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="fab16-119">**Count**</span><span class="sxs-lookup"><span data-stu-id="fab16-119">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab16-120">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fab16-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fab16-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fab16-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab16-122">Anzahl der Fehler Datensätze.</span><span class="sxs-lookup"><span data-stu-id="fab16-122">Number of error records.</span></span>

</dd> <dt>

<span data-ttu-id="fab16-123">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="fab16-123">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab16-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fab16-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fab16-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fab16-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fab16-126">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fab16-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fab16-127">Eindeutiger Bezeichner dieser Instanz der Klasse.</span><span class="sxs-lookup"><span data-stu-id="fab16-127">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="fab16-128">**Datensätze**</span><span class="sxs-lookup"><span data-stu-id="fab16-128">**Records**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab16-129">Datentyp: **msmcainfo- \_ Eingabe** Array</span><span class="sxs-lookup"><span data-stu-id="fab16-129">Data type: **MSMCAInfo\_Entry** array</span></span>
</dt> <dt>

<span data-ttu-id="fab16-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fab16-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab16-131">Array von MCA-Fehler Datensätzen.</span><span class="sxs-lookup"><span data-stu-id="fab16-131">Array of MCA error records.</span></span> <span data-ttu-id="fab16-132">Die Anzahl der MCA-Fehler Datensätze im Array wird durch die **count** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="fab16-132">The number of MCA error records in the array is specified by the **Count** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fab16-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fab16-133">Remarks</span></span>

<span data-ttu-id="fab16-134">Die **msmcainfo \_ rawmcadata** -Klasse wird von [**msmcainfo**](msmcainfo.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="fab16-134">The **MSMCAInfo\_RawMCAData** class is derived from [**MSMCAInfo**](msmcainfo.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fab16-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fab16-135">Requirements</span></span>



| <span data-ttu-id="fab16-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fab16-136">Requirement</span></span> | <span data-ttu-id="fab16-137">Wert</span><span class="sxs-lookup"><span data-stu-id="fab16-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fab16-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fab16-138">Minimum supported client</span></span><br/> | <span data-ttu-id="fab16-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fab16-139">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="fab16-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fab16-140">Minimum supported server</span></span><br/> | <span data-ttu-id="fab16-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fab16-141">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="fab16-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="fab16-142">Namespace</span></span><br/>                | <span data-ttu-id="fab16-143">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="fab16-143">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="fab16-144">MOF</span><span class="sxs-lookup"><span data-stu-id="fab16-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fab16-145"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fab16-145"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="fab16-146">DLL</span><span class="sxs-lookup"><span data-stu-id="fab16-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fab16-147"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fab16-147"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fab16-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fab16-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fab16-149">MSMCA-Klassen</span><span class="sxs-lookup"><span data-stu-id="fab16-149">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="fab16-150">**Msmcainfo**</span><span class="sxs-lookup"><span data-stu-id="fab16-150">**MSMCAInfo**</span></span>](msmcainfo.md)
</dt> </dl>

 

