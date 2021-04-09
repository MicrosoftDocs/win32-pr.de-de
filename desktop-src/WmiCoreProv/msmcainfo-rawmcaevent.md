---
description: Enthält ein MCA-Ereignis (Machine Check Architecture). Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.
ms.assetid: d1806b91-43a3-4329-8fe5-de1e4755740f
title: MSMCAInfo_RawMCAEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawMCAEvent
- MSMCAInfo_RawMCAEvent.Active
- MSMCAInfo_RawMCAEvent.Count
- MSMCAInfo_RawMCAEvent.InstanceName
- MSMCAInfo_RawMCAEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: e15af79c67265823e0025849e4c2ef27f690265c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960439"
---
# <a name="msmcainfo_rawmcaevent-class"></a><span data-ttu-id="1447c-104">Msmcainfo \_ rawmcaevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="1447c-104">MSMCAInfo\_RawMCAEvent class</span></span>

<span data-ttu-id="1447c-105">Die **msmcainfo \_ rawmcaevent** -Klasse enthält ein MCA-Ereignis (Machine Check Architecture).</span><span class="sxs-lookup"><span data-stu-id="1447c-105">The **MSMCAInfo\_RawMCAEvent** class contains a Machine Check Architecture (MCA) event.</span></span> <span data-ttu-id="1447c-106">Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1447c-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="1447c-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1447c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="1447c-108">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="1447c-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1447c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1447c-109">Syntax</span></span>

``` syntax
class MSMCAInfo_RawMCAEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a><span data-ttu-id="1447c-110">Member</span><span class="sxs-lookup"><span data-stu-id="1447c-110">Members</span></span>

<span data-ttu-id="1447c-111">Die **msmcainfo \_ rawmcaevent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1447c-111">The **MSMCAInfo\_RawMCAEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="1447c-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1447c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1447c-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1447c-113">Properties</span></span>

<span data-ttu-id="1447c-114">Die **msmcainfo \_ rawmcaevent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1447c-114">The **MSMCAInfo\_RawMCAEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1447c-115">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="1447c-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1447c-116">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1447c-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1447c-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1447c-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1447c-118">TRUE, wenn diese Instanz der-Klasse aktiv ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="1447c-118">TRUE, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1447c-119">**Count**</span><span class="sxs-lookup"><span data-stu-id="1447c-119">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1447c-120">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1447c-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1447c-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1447c-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1447c-122">Anzahl der Fehler Datensätze.</span><span class="sxs-lookup"><span data-stu-id="1447c-122">Number of error records.</span></span>

</dd> <dt>

<span data-ttu-id="1447c-123">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="1447c-123">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1447c-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1447c-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1447c-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1447c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1447c-126">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1447c-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1447c-127">Eine Zeichenfolge, die diese Instanz der **msmcainfo \_ rawmcaevent** -Klasse eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1447c-127">String that uniquely identifies this instance of the **MSMCAInfo\_RawMCAEvent** class.</span></span>

</dd> <dt>

<span data-ttu-id="1447c-128">**Datensätze**</span><span class="sxs-lookup"><span data-stu-id="1447c-128">**Records**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1447c-129">Datentyp: **msmcainfo- \_ Eingabe** Array</span><span class="sxs-lookup"><span data-stu-id="1447c-129">Data type: **MSMCAInfo\_Entry** array</span></span>
</dt> <dt>

<span data-ttu-id="1447c-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1447c-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1447c-131">Array von MCA-Fehler Datensätzen.</span><span class="sxs-lookup"><span data-stu-id="1447c-131">Array of MCA error records.</span></span> <span data-ttu-id="1447c-132">Die Anzahl der MCA-Fehler Datensätze im Array wird durch die **count** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="1447c-132">The number of MCA error records in the array is specified by the **Count** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1447c-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1447c-133">Remarks</span></span>

<span data-ttu-id="1447c-134">Die **msmcainfo \_ rawmcaevent** -Klasse wird von [**wmievent**](wmievent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="1447c-134">The **MSMCAInfo\_RawMCAEvent** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1447c-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1447c-135">Requirements</span></span>



| <span data-ttu-id="1447c-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1447c-136">Requirement</span></span> | <span data-ttu-id="1447c-137">Wert</span><span class="sxs-lookup"><span data-stu-id="1447c-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1447c-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1447c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="1447c-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1447c-139">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="1447c-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1447c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="1447c-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1447c-141">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="1447c-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="1447c-142">Namespace</span></span><br/>                | <span data-ttu-id="1447c-143">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="1447c-143">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="1447c-144">MOF</span><span class="sxs-lookup"><span data-stu-id="1447c-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1447c-145"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1447c-145"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="1447c-146">DLL</span><span class="sxs-lookup"><span data-stu-id="1447c-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1447c-147"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1447c-147"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1447c-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1447c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1447c-149">MSMCA-Klassen</span><span class="sxs-lookup"><span data-stu-id="1447c-149">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="1447c-150">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="1447c-150">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

