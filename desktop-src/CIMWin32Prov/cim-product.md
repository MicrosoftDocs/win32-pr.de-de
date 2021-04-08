---
description: Die CIM- \_ Produktklasse ist eine konkrete Klasse, die eine Auflistung physischer Elemente, Software Features und anderer Produkte darstellt, die als Einheit erworben wurden.
ms.assetid: beb20f61-de39-4221-8d29-4727104518d5
ms.tgt_platform: multiple
title: CIM_Product-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Product
- CIM_Product.Caption
- CIM_Product.Description
- CIM_Product.IdentifyingNumber
- CIM_Product.Name
- CIM_Product.SKUNumber
- CIM_Product.Vendor
- CIM_Product.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 16c8541a18185d721bbdcbf23acaeb67adf508c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748008"
---
# <a name="cim_product-class"></a><span data-ttu-id="95970-103">CIM- \_ Produktklasse</span><span class="sxs-lookup"><span data-stu-id="95970-103">CIM\_Product class</span></span>

<span data-ttu-id="95970-104">Die **CIM- \_ Produkt** Klasse ist eine konkrete Klasse, die eine Auflistung physischer Elemente, Software Features und anderer Produkte darstellt, die als Einheit erworben wurden.</span><span class="sxs-lookup"><span data-stu-id="95970-104">The **CIM\_Product** class is a concrete class that represents a collection of physical elements, software features and, other products, acquired as a unit.</span></span> <span data-ttu-id="95970-105">Der Erwerb impliziert eine Vereinbarung zwischen dem Lieferanten und dem Consumer, die Auswirkungen auf die Produkt Lizenzierung, den Support und die Gewährleistung haben kann.</span><span class="sxs-lookup"><span data-stu-id="95970-105">Acquisition implies an agreement between the supplier and consumer, which can have implications on product licensing, support, and warranty.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="95970-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="95970-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="95970-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="95970-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="95970-108">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="95970-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="95970-109">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="95970-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="95970-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="95970-110">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B63-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Product
{
  string Caption;
  string Description;
  string IdentifyingNumber;
  string Name;
  string SKUNumber;
  string Vendor;
  string Version;
};
```

## <a name="members"></a><span data-ttu-id="95970-111">Member</span><span class="sxs-lookup"><span data-stu-id="95970-111">Members</span></span>

<span data-ttu-id="95970-112">Die **CIM- \_ Produkt** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="95970-112">The **CIM\_Product** class has these types of members:</span></span>

-   [<span data-ttu-id="95970-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="95970-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="95970-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="95970-114">Properties</span></span>

<span data-ttu-id="95970-115">Die **CIM- \_ Produkt** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="95970-115">The **CIM\_Product** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="95970-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="95970-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95970-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="95970-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95970-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="95970-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95970-119">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="95970-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="95970-120">Kurze Textbeschreibung für das Produkt.</span><span class="sxs-lookup"><span data-stu-id="95970-120">Short textual description for the product.</span></span>

</dd> <dt>

<span data-ttu-id="95970-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="95970-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95970-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="95970-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95970-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="95970-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95970-124">Die Textbeschreibung des Produkts.</span><span class="sxs-lookup"><span data-stu-id="95970-124">Textual description of the product.</span></span>

</dd> <dt>

<span data-ttu-id="95970-125">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="95970-125">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95970-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="95970-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95970-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="95970-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95970-128">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="95970-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="95970-129">Produktidentifizierung, z. b. Seriennummer auf Software, eine Nummer auf einem Hardware Chip oder (bei nicht kommerziellen Produkten) eine Projekt Nummer.</span><span class="sxs-lookup"><span data-stu-id="95970-129">Product identification, such as a serial number on software, a die number on a hardware chip, or (for noncommercial products) a project number.</span></span>

</dd> <dt>

<span data-ttu-id="95970-130">**Name**</span><span class="sxs-lookup"><span data-stu-id="95970-130">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95970-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="95970-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95970-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="95970-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95970-133">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="95970-133">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="95970-134">Häufig verwendeter Produktname.</span><span class="sxs-lookup"><span data-stu-id="95970-134">Commonly used product name.</span></span>

</dd> <dt>

<span data-ttu-id="95970-135">**SKUNumber**</span><span class="sxs-lookup"><span data-stu-id="95970-135">**SKUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95970-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="95970-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95970-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="95970-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95970-138">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="95970-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="95970-139">SKU-Informationen (Stock-Keeping Unit) des Produkts.</span><span class="sxs-lookup"><span data-stu-id="95970-139">Product's stock-keeping unit (SKU) information.</span></span>

</dd> <dt>

<span data-ttu-id="95970-140">**Hersteller**</span><span class="sxs-lookup"><span data-stu-id="95970-140">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95970-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="95970-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95970-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="95970-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95970-143">Qualifizierer: [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="95970-143">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="95970-144">Der Name des Lieferanten des Produkts oder die Entität, die das Produkt verkauft (Hersteller, Reseller, OEM usw.).</span><span class="sxs-lookup"><span data-stu-id="95970-144">Name of the product's supplier, or the entity selling the product (the manufacturer, reseller, OEM, and so on).</span></span>

</dd> <dt>

<span data-ttu-id="95970-145">**Version**</span><span class="sxs-lookup"><span data-stu-id="95970-145">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95970-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="95970-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95970-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="95970-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95970-148">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="95970-148">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="95970-149">Informationen zur Produktversion.</span><span class="sxs-lookup"><span data-stu-id="95970-149">Product version information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95970-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95970-150">Remarks</span></span>

<span data-ttu-id="95970-151">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="95970-151">WMI does not implement this class.</span></span> <span data-ttu-id="95970-152">Informationen zu WMI-Klassen, die vom **CIM- \_ Produkt** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="95970-152">For WMI classes that are derived from **CIM\_Product**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="95970-153">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="95970-153">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="95970-154">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="95970-154">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="95970-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95970-155">Requirements</span></span>



| <span data-ttu-id="95970-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95970-156">Requirement</span></span> | <span data-ttu-id="95970-157">Wert</span><span class="sxs-lookup"><span data-stu-id="95970-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95970-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95970-158">Minimum supported client</span></span><br/> | <span data-ttu-id="95970-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95970-159">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="95970-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95970-160">Minimum supported server</span></span><br/> | <span data-ttu-id="95970-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95970-161">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="95970-162">Namespace</span><span class="sxs-lookup"><span data-stu-id="95970-162">Namespace</span></span><br/>                | <span data-ttu-id="95970-163">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="95970-163">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="95970-164">MOF</span><span class="sxs-lookup"><span data-stu-id="95970-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95970-165"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="95970-165"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="95970-166">DLL</span><span class="sxs-lookup"><span data-stu-id="95970-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95970-167"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95970-167"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

