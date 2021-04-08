---
description: Die CIM \_ FRU-Klasse stellt eine Hersteller definierte Auflistung von Produkten und physischen Elementen dar, die einer von einem Feld ersetzbaren Einheit (FRU) zugeordnet sind, um ein Produkt am Standort des Kunden zu unterstützen, zu warten oder zu aktualisieren.
ms.assetid: 4464ec3a-5509-4e15-9020-4abb2edd2570
ms.tgt_platform: multiple
title: CIM_FRU-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FRU
- CIM_FRU.Caption
- CIM_FRU.Description
- CIM_FRU.FRUNumber
- CIM_FRU.IdentifyingNumber
- CIM_FRU.Name
- CIM_FRU.RevisionLevel
- CIM_FRU.Vendor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d163c3c223159ad8e09aa6e36d63187ff0aa97f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748465"
---
# <a name="cim_fru-class"></a><span data-ttu-id="127bf-103">CIM \_ FRU-Klasse</span><span class="sxs-lookup"><span data-stu-id="127bf-103">CIM\_FRU class</span></span>

<span data-ttu-id="127bf-104">Die **CIM \_ FRU** -Klasse stellt eine Hersteller definierte Auflistung von Produkten und physischen Elementen dar, die einer von einem Feld ersetzbaren Einheit (FRU) zugeordnet sind, um ein Produkt am Standort des Kunden zu unterstützen, zu warten oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="127bf-104">The **CIM\_FRU** class represents a vendor-defined collection of products and physical elements that are associated with a field replaceable unit (FRU) to support, maintain, or upgrade a product at the customer's location.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="127bf-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="127bf-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="127bf-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="127bf-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="127bf-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="127bf-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="127bf-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="127bf-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="127bf-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="127bf-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{778C74EE-DB2A-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_FRU
{
  string Caption;
  string Description;
  string FRUNumber;
  string IdentifyingNumber;
  string Name;
  string RevisionLevel;
  string Vendor;
};
```

## <a name="members"></a><span data-ttu-id="127bf-110">Member</span><span class="sxs-lookup"><span data-stu-id="127bf-110">Members</span></span>

<span data-ttu-id="127bf-111">Die **CIM \_ FRU** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="127bf-111">The **CIM\_FRU** class has these types of members:</span></span>

-   [<span data-ttu-id="127bf-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="127bf-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="127bf-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="127bf-113">Properties</span></span>

<span data-ttu-id="127bf-114">Die **CIM \_ FRU** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="127bf-114">The **CIM\_FRU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="127bf-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="127bf-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="127bf-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="127bf-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="127bf-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="127bf-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="127bf-118">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="127bf-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="127bf-119">Kurze Textbeschreibung für den FRU.</span><span class="sxs-lookup"><span data-stu-id="127bf-119">Short textual description for the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="127bf-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="127bf-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="127bf-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="127bf-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="127bf-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="127bf-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="127bf-123">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| FRU \| 002,3 ")</span><span class="sxs-lookup"><span data-stu-id="127bf-123">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.3")</span></span>
</dt> </dl>

<span data-ttu-id="127bf-124">Die Beschreibung der FRU.</span><span class="sxs-lookup"><span data-stu-id="127bf-124">Description of the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="127bf-125">**FRUNumber**</span><span class="sxs-lookup"><span data-stu-id="127bf-125">**FRUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="127bf-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="127bf-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="127bf-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="127bf-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="127bf-128">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| FRU \| 002,6 "), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="127bf-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.6"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="127bf-129">FRU-Bestellinformationen.</span><span class="sxs-lookup"><span data-stu-id="127bf-129">FRU ordering information.</span></span>

</dd> <dt>

<span data-ttu-id="127bf-130">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="127bf-130">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="127bf-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="127bf-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="127bf-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="127bf-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="127bf-133">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| FRU \| 002,7 "), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="127bf-133">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.7"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="127bf-134">Identifizierung von Software, z. b. eine Seriennummer oder eine Zahl auf einem Hardware Chip.</span><span class="sxs-lookup"><span data-stu-id="127bf-134">Identification on software, such as a serial number, or a die number on a hardware chip.</span></span>

</dd> <dt>

<span data-ttu-id="127bf-135">**Name**</span><span class="sxs-lookup"><span data-stu-id="127bf-135">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="127bf-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="127bf-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="127bf-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="127bf-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="127bf-138">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="127bf-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="127bf-139">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="127bf-139">Label by which the object is known.</span></span>

</dd> <dt>

<span data-ttu-id="127bf-140">**Revisions Ebene**</span><span class="sxs-lookup"><span data-stu-id="127bf-140">**RevisionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="127bf-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="127bf-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="127bf-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="127bf-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="127bf-143">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| FRU \| 002,8 "), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="127bf-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.8"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="127bf-144">Revisions Ebene der FRU.</span><span class="sxs-lookup"><span data-stu-id="127bf-144">Revision level of the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="127bf-145">**Hersteller**</span><span class="sxs-lookup"><span data-stu-id="127bf-145">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="127bf-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="127bf-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="127bf-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="127bf-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="127bf-148">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| FRU \| 002,4 "), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="127bf-148">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.4"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="127bf-149">Der Name des Lieferanten.</span><span class="sxs-lookup"><span data-stu-id="127bf-149">Name of the supplier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="127bf-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="127bf-150">Remarks</span></span>

<span data-ttu-id="127bf-151">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="127bf-151">WMI does not implement this class.</span></span>

<span data-ttu-id="127bf-152">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="127bf-152">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="127bf-153">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="127bf-153">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="127bf-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="127bf-154">Requirements</span></span>



| <span data-ttu-id="127bf-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="127bf-155">Requirement</span></span> | <span data-ttu-id="127bf-156">Wert</span><span class="sxs-lookup"><span data-stu-id="127bf-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="127bf-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="127bf-157">Minimum supported client</span></span><br/> | <span data-ttu-id="127bf-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="127bf-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="127bf-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="127bf-159">Minimum supported server</span></span><br/> | <span data-ttu-id="127bf-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="127bf-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="127bf-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="127bf-161">Namespace</span></span><br/>                | <span data-ttu-id="127bf-162">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="127bf-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="127bf-163">MOF</span><span class="sxs-lookup"><span data-stu-id="127bf-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="127bf-164"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="127bf-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="127bf-165">DLL</span><span class="sxs-lookup"><span data-stu-id="127bf-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="127bf-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="127bf-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

