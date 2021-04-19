---
description: Die CIM \_ storageerror-Klasse stellt Blöcke von Medien oder Speicherplatz dar, die aufgrund von Fehlern nicht verwendeter Speicher zugeordnet sind. Der Schlüssel der-Klasse ist die StartingAddress-Eigenschaft der Bytes, die fehlerhaft sind.
ms.assetid: e786aa39-4718-416b-b659-bf4b8d3e2851
ms.tgt_platform: multiple
title: CIM_StorageError-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageError
- CIM_StorageError.DeviceCreationClassName
- CIM_StorageError.DeviceID
- CIM_StorageError.EndingAddress
- CIM_StorageError.StartingAddress
- CIM_StorageError.SystemCreationClassName
- CIM_StorageError.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6f5b197a5c82e61e054f5875fad466cac808ec38
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346214"
---
# <a name="cim_storageerror-class"></a><span data-ttu-id="583f1-104">CIM \_ storageerror-Klasse</span><span class="sxs-lookup"><span data-stu-id="583f1-104">CIM\_StorageError class</span></span>

<span data-ttu-id="583f1-105">Die **CIM \_ storageerror** -Klasse stellt Blöcke von Medien oder Speicherplatz dar, die aufgrund von Fehlern nicht verwendeter Speicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="583f1-105">The **CIM\_StorageError** class represents blocks of media or memory space that are mapped out-of-use due to errors.</span></span> <span data-ttu-id="583f1-106">Der Schlüssel der-Klasse ist die **StartingAddress** -Eigenschaft der Bytes, die fehlerhaft sind.</span><span class="sxs-lookup"><span data-stu-id="583f1-106">The key of the class is the **StartingAddress** property of the bytes in error.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="583f1-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="583f1-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="583f1-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="583f1-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="583f1-109">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="583f1-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="583f1-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="583f1-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="583f1-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="583f1-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{71312AB6-DB31-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_StorageError
{
  string DeviceCreationClassName;
  string DeviceID;
  uint64 EndingAddress;
  uint64 StartingAddress;
  string SystemCreationClassName;
  string SystemName;
};
```

## <a name="members"></a><span data-ttu-id="583f1-112">Member</span><span class="sxs-lookup"><span data-stu-id="583f1-112">Members</span></span>

<span data-ttu-id="583f1-113">Die **CIM \_ storageerror** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="583f1-113">The **CIM\_StorageError** class has these types of members:</span></span>

-   [<span data-ttu-id="583f1-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="583f1-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="583f1-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="583f1-115">Properties</span></span>

<span data-ttu-id="583f1-116">Die **CIM \_ storageerror** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="583f1-116">The **CIM\_StorageError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="583f1-117">**Geräteklassen Name**</span><span class="sxs-lookup"><span data-stu-id="583f1-117">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="583f1-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="583f1-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="583f1-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="583f1-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="583f1-120">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ storageblock**](cim-storageextent.md).**"Kreationclassname**")</span><span class="sxs-lookup"><span data-stu-id="583f1-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageExtent**](cim-storageextent.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="583f1-121">Der Name der Erstellungs Klasse des Speicherbereichs.</span><span class="sxs-lookup"><span data-stu-id="583f1-121">Scoping storage extent's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="583f1-122">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="583f1-122">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="583f1-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="583f1-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="583f1-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="583f1-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="583f1-125">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ storageblock**](cim-storageextent.md).\*\*\*\* Geräte-ID ")</span><span class="sxs-lookup"><span data-stu-id="583f1-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageExtent**](cim-storageextent.md).**DeviceID**")</span></span>
</dt> </dl>

<span data-ttu-id="583f1-126">Der Geräte Bezeichner für die Bereichs Definition des Speicherbereichs.</span><span class="sxs-lookup"><span data-stu-id="583f1-126">Scoping storage extent's device identifier.</span></span>

</dd> <dt>

<span data-ttu-id="583f1-127">**"Endadresse"**</span><span class="sxs-lookup"><span data-stu-id="583f1-127">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="583f1-128">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="583f1-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="583f1-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="583f1-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="583f1-130">Die Endadresse der Bytes, die fehlerhaft sind.</span><span class="sxs-lookup"><span data-stu-id="583f1-130">Ending address of the bytes in error.</span></span>

<span data-ttu-id="583f1-131">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="583f1-131">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="583f1-132">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="583f1-132">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="583f1-133">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="583f1-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="583f1-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="583f1-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="583f1-135">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="583f1-135">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="583f1-136">Die Startadresse der Bytes, die fehlerhaft sind.</span><span class="sxs-lookup"><span data-stu-id="583f1-136">Starting address of the bytes in error.</span></span>

<span data-ttu-id="583f1-137">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="583f1-137">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="583f1-138">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="583f1-138">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="583f1-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="583f1-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="583f1-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="583f1-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="583f1-141">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ storageblock**](cim-storageextent.md).**Systemkreationclassname**")</span><span class="sxs-lookup"><span data-stu-id="583f1-141">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageExtent**](cim-storageextent.md).**SystemCreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="583f1-142">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="583f1-142">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="583f1-143">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="583f1-143">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="583f1-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="583f1-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="583f1-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="583f1-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="583f1-146">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ storageblock**](cim-storageextent.md).**Systemname**")</span><span class="sxs-lookup"><span data-stu-id="583f1-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageExtent**](cim-storageextent.md).**SystemName**")</span></span>
</dt> </dl>

<span data-ttu-id="583f1-147">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="583f1-147">Scoping system's name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="583f1-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="583f1-148">Remarks</span></span>

<span data-ttu-id="583f1-149">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="583f1-149">WMI does not implement this class.</span></span>

<span data-ttu-id="583f1-150">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="583f1-150">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="583f1-151">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="583f1-151">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="583f1-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="583f1-152">Requirements</span></span>



| <span data-ttu-id="583f1-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="583f1-153">Requirement</span></span> | <span data-ttu-id="583f1-154">Wert</span><span class="sxs-lookup"><span data-stu-id="583f1-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="583f1-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="583f1-155">Minimum supported client</span></span><br/> | <span data-ttu-id="583f1-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="583f1-156">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="583f1-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="583f1-157">Minimum supported server</span></span><br/> | <span data-ttu-id="583f1-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="583f1-158">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="583f1-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="583f1-159">Namespace</span></span><br/>                | <span data-ttu-id="583f1-160">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="583f1-160">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="583f1-161">MOF</span><span class="sxs-lookup"><span data-stu-id="583f1-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="583f1-162"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="583f1-162"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="583f1-163">DLL</span><span class="sxs-lookup"><span data-stu-id="583f1-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="583f1-164"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="583f1-164"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

