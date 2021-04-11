---
description: Die CIM- \_ Location-Klasse stellt die Position und die Adresse eines physischen Elements dar.
ms.assetid: c1ec467c-a338-4beb-a8fe-1ebc5b05c754
ms.tgt_platform: multiple
title: CIM_Location-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Location
- CIM_Location.Address
- CIM_Location.Name
- CIM_Location.PhysicalPosition
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd5a1c1c23d07020b45c1c5979a941f01baff0d0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214183"
---
# <a name="cim_location-class"></a><span data-ttu-id="91dac-103">CIM- \_ Location-Klasse</span><span class="sxs-lookup"><span data-stu-id="91dac-103">CIM\_Location class</span></span>

<span data-ttu-id="91dac-104">Die **CIM- \_ Location** -Klasse stellt die Position und die Adresse eines physischen Elements dar.</span><span class="sxs-lookup"><span data-stu-id="91dac-104">The **CIM\_Location** class represents the position and address of a physical element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="91dac-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="91dac-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="91dac-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="91dac-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="91dac-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="91dac-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="91dac-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="91dac-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="91dac-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="91dac-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B67-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Location
{
  string Address;
  string Name;
  string PhysicalPosition;
};
```

## <a name="members"></a><span data-ttu-id="91dac-110">Member</span><span class="sxs-lookup"><span data-stu-id="91dac-110">Members</span></span>

<span data-ttu-id="91dac-111">Die **CIM- \_ Location** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="91dac-111">The **CIM\_Location** class has these types of members:</span></span>

-   [<span data-ttu-id="91dac-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="91dac-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="91dac-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="91dac-113">Properties</span></span>

<span data-ttu-id="91dac-114">Die **CIM- \_ Location** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="91dac-114">The **CIM\_Location** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="91dac-115">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="91dac-115">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91dac-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91dac-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91dac-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91dac-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91dac-118">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="91dac-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="91dac-119">Eine frei Form Zeichenfolge, die eine Straße oder einen anderen Adresstyp für den Speicherort des physischen Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="91dac-119">Free-form string that indicates a street or other type of address for the physical element's location.</span></span>

</dd> <dt>

<span data-ttu-id="91dac-120">**Name**</span><span class="sxs-lookup"><span data-stu-id="91dac-120">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91dac-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91dac-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91dac-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91dac-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91dac-123">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="91dac-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="91dac-124">Eine frei Form Zeichenfolge, die eine Bezeichnung für den Speicherort definiert und Teil des Schlüssels für das Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="91dac-124">Free-form string that defines a label for the location and is part of the key for the object.</span></span>

</dd> <dt>

<span data-ttu-id="91dac-125">**Physicalposition**</span><span class="sxs-lookup"><span data-stu-id="91dac-125">**PhysicalPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91dac-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91dac-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91dac-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91dac-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91dac-128">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="91dac-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="91dac-129">Eine frei Form Zeichenfolge, die die Platzierung eines physischen Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="91dac-129">Free-form string that indicates the placement of a physical element.</span></span> <span data-ttu-id="91dac-130">Es können Slot-Informationen auf einem hostingboard, eine Montage Site in einer CAB-Datei oder Informationen zu breiten-und Längengrad angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="91dac-130">It can specify slot information on a hosting board, mounting site in a cabinet, or latitude and longitude information.</span></span> <span data-ttu-id="91dac-131">Sie ist Teil des Schlüssels des CIM- **\_ Speicherort** Objekts.</span><span class="sxs-lookup"><span data-stu-id="91dac-131">It is part of the key of the **CIM\_Location** object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91dac-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91dac-132">Remarks</span></span>

<span data-ttu-id="91dac-133">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="91dac-133">WMI does not implement this class.</span></span> <span data-ttu-id="91dac-134">Informationen zu Klassen, die vom **CIM- \_ Speicherort** abgeleitet sind [, finden Sie](win32-provider.md)unter</span><span class="sxs-lookup"><span data-stu-id="91dac-134">For classes derived from **CIM\_Location**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="91dac-135">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="91dac-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="91dac-136">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="91dac-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="91dac-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91dac-137">Requirements</span></span>



| <span data-ttu-id="91dac-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91dac-138">Requirement</span></span> | <span data-ttu-id="91dac-139">Wert</span><span class="sxs-lookup"><span data-stu-id="91dac-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91dac-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="91dac-140">Minimum supported client</span></span><br/> | <span data-ttu-id="91dac-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91dac-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="91dac-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="91dac-142">Minimum supported server</span></span><br/> | <span data-ttu-id="91dac-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91dac-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="91dac-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="91dac-144">Namespace</span></span><br/>                | <span data-ttu-id="91dac-145">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="91dac-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="91dac-146">MOF</span><span class="sxs-lookup"><span data-stu-id="91dac-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="91dac-147"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="91dac-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="91dac-148">DLL</span><span class="sxs-lookup"><span data-stu-id="91dac-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91dac-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91dac-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

