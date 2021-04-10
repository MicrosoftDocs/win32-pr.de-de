---
description: Stellt ein Produkt dar. Dies schließt Software und Hardware ein, die auf diesem Computersystem verwendet wird.
ms.assetid: 6241e703-4ce9-435f-bf36-4388e38a3ea5
ms.tgt_platform: multiple
title: Win32_ComputerSystemProduct-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystemProduct
- Win32_ComputerSystemProduct.Caption
- Win32_ComputerSystemProduct.Description
- Win32_ComputerSystemProduct.IdentifyingNumber
- Win32_ComputerSystemProduct.Name
- Win32_ComputerSystemProduct.SKUNumber
- Win32_ComputerSystemProduct.Vendor
- Win32_ComputerSystemProduct.Version
- Win32_ComputerSystemProduct.UUID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8cab3dc8679c606076eca2f5cf704867aa9833c9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126260"
---
# <a name="win32_computersystemproduct-class"></a><span data-ttu-id="62ab5-104">Win32 \_ computersystemproduct-Klasse</span><span class="sxs-lookup"><span data-stu-id="62ab5-104">Win32\_ComputerSystemProduct class</span></span>

<span data-ttu-id="62ab5-105">Die **Win32 \_ computersystemproduct** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) stellt ein Produkt dar.</span><span class="sxs-lookup"><span data-stu-id="62ab5-105">The **Win32\_ComputerSystemProduct** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a product.</span></span> <span data-ttu-id="62ab5-106">Dies schließt Software und Hardware ein, die auf diesem Computersystem verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="62ab5-106">This includes software and hardware used on this computer system.</span></span>

<span data-ttu-id="62ab5-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="62ab5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="62ab5-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="62ab5-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="62ab5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="62ab5-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B96-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_ComputerSystemProduct : CIM_Product
{
  string Caption;
  string Description;
  string IdentifyingNumber;
  string Name;
  string SKUNumber;
  string Vendor;
  string Version;
  string UUID;
};
```

## <a name="members"></a><span data-ttu-id="62ab5-110">Member</span><span class="sxs-lookup"><span data-stu-id="62ab5-110">Members</span></span>

<span data-ttu-id="62ab5-111">Die **Win32 \_ Computersystem Product** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="62ab5-111">The **Win32\_ComputerSystemProduct** class has these types of members:</span></span>

-   [<span data-ttu-id="62ab5-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="62ab5-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="62ab5-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="62ab5-113">Properties</span></span>

<span data-ttu-id="62ab5-114">Die **Win32 \_ Computersystem Product** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="62ab5-114">The **Win32\_ComputerSystemProduct** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="62ab5-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="62ab5-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62ab5-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62ab5-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62ab5-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62ab5-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62ab5-118">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="62ab5-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="62ab5-119">Kurze Textbeschreibung für das Produkt.</span><span class="sxs-lookup"><span data-stu-id="62ab5-119">Short textual description for the product.</span></span>

<span data-ttu-id="62ab5-120">Diese Eigenschaft wird vom [**CIM- \_ Produkt**](cim-product.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62ab5-120">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="62ab5-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="62ab5-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62ab5-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62ab5-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62ab5-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62ab5-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62ab5-124">Die Textbeschreibung des Produkts.</span><span class="sxs-lookup"><span data-stu-id="62ab5-124">Textual description of the product.</span></span>

<span data-ttu-id="62ab5-125">Diese Eigenschaft wird vom [**CIM- \_ Produkt**](cim-product.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62ab5-125">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="62ab5-126">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="62ab5-126">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62ab5-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62ab5-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62ab5-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62ab5-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62ab5-129">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="62ab5-129">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="62ab5-130">Produktidentifizierung, z. b. Seriennummer auf Software, eine Nummer auf einem Hardware Chip oder (bei nicht kommerziellen Produkten) eine Projekt Nummer.</span><span class="sxs-lookup"><span data-stu-id="62ab5-130">Product identification, such as a serial number on software, a die number on a hardware chip, or (for noncommercial products) a project number.</span></span>

<span data-ttu-id="62ab5-131">Diese Eigenschaft wird vom [**CIM- \_ Produkt**](cim-product.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62ab5-131">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="62ab5-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="62ab5-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62ab5-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62ab5-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62ab5-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62ab5-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62ab5-135">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="62ab5-135">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="62ab5-136">Häufig verwendeter Produktname.</span><span class="sxs-lookup"><span data-stu-id="62ab5-136">Commonly used product name.</span></span>

<span data-ttu-id="62ab5-137">Diese Eigenschaft wird vom [**CIM- \_ Produkt**](cim-product.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62ab5-137">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="62ab5-138">**SKUNumber**</span><span class="sxs-lookup"><span data-stu-id="62ab5-138">**SKUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62ab5-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62ab5-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62ab5-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62ab5-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62ab5-141">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="62ab5-141">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="62ab5-142">SKU-Informationen (Stock-Keeping Unit) des Produkts.</span><span class="sxs-lookup"><span data-stu-id="62ab5-142">Product's stock-keeping unit (SKU) information.</span></span>

<span data-ttu-id="62ab5-143">Diese Eigenschaft wird vom [**CIM- \_ Produkt**](cim-product.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62ab5-143">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="62ab5-144">**UUID**</span><span class="sxs-lookup"><span data-stu-id="62ab5-144">**UUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62ab5-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62ab5-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62ab5-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62ab5-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62ab5-147">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 1 \| UUID")</span><span class="sxs-lookup"><span data-stu-id="62ab5-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|UUID")</span></span>
</dt> </dl>

<span data-ttu-id="62ab5-148">Universelle eindeutige Kennung (UUID) für dieses Produkt.</span><span class="sxs-lookup"><span data-stu-id="62ab5-148">Universally unique identifier (UUID) for this product.</span></span> <span data-ttu-id="62ab5-149">Eine UUID ist ein 128-Bit-Bezeichner, der sich garantiert von anderen generierten UUIDs unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="62ab5-149">A UUID is a 128-bit identifier that is guaranteed to be different from other generated UUIDs.</span></span> <span data-ttu-id="62ab5-150">Wenn eine UUID nicht verfügbar ist, wird eine UUID aller Nullen verwendet.</span><span class="sxs-lookup"><span data-stu-id="62ab5-150">If a UUID is not available, a UUID of all zeros is used.</span></span>

<span data-ttu-id="62ab5-151">Dieser Wert stammt aus dem **UUID** -Member der **System Informations** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="62ab5-151">This value comes from the **UUID** member of the **System Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="62ab5-152">**Hersteller**</span><span class="sxs-lookup"><span data-stu-id="62ab5-152">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62ab5-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62ab5-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62ab5-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62ab5-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62ab5-155">Qualifizierer: [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="62ab5-155">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="62ab5-156">Der Name des Lieferanten des Produkts oder die Entität, die das Produkt verkauft (Hersteller, Reseller, OEM usw.).</span><span class="sxs-lookup"><span data-stu-id="62ab5-156">Name of the product's supplier, or the entity selling the product (the manufacturer, reseller, OEM, and so on).</span></span>

<span data-ttu-id="62ab5-157">Diese Eigenschaft wird vom [**CIM- \_ Produkt**](cim-product.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62ab5-157">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="62ab5-158">**Version**</span><span class="sxs-lookup"><span data-stu-id="62ab5-158">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62ab5-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62ab5-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62ab5-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62ab5-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62ab5-161">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="62ab5-161">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="62ab5-162">Informationen zur Produktversion.</span><span class="sxs-lookup"><span data-stu-id="62ab5-162">Product version information.</span></span>

<span data-ttu-id="62ab5-163">Diese Eigenschaft wird vom [**CIM- \_ Produkt**](cim-product.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62ab5-163">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62ab5-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62ab5-164">Remarks</span></span>

<span data-ttu-id="62ab5-165">Die **Win32- \_ computersystemproduct** -Klasse wird vom [**CIM- \_ Produkt**](cim-product.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="62ab5-165">The **Win32\_ComputerSystemProduct** class is derived from [**CIM\_Product**](cim-product.md).</span></span>

## <a name="examples"></a><span data-ttu-id="62ab5-166">Beispiele</span><span class="sxs-lookup"><span data-stu-id="62ab5-166">Examples</span></span>

<span data-ttu-id="62ab5-167">Das [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell-Beispiel in der TechNet Gallery verwendet zum **Win32 \_ computersystemproduct** , um eine Liste der nicht funktionierenden Hardware mithilfe von WMI abzurufen.</span><span class="sxs-lookup"><span data-stu-id="62ab5-167">The [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell sample on TechNet Gallery uses to **Win32\_ComputerSystemProduct** to retrieve a list of non-working hardware using WMI.</span></span>

## <a name="requirements"></a><span data-ttu-id="62ab5-168">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62ab5-168">Requirements</span></span>



| <span data-ttu-id="62ab5-169">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62ab5-169">Requirement</span></span> | <span data-ttu-id="62ab5-170">Wert</span><span class="sxs-lookup"><span data-stu-id="62ab5-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62ab5-171">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="62ab5-171">Minimum supported client</span></span><br/> | <span data-ttu-id="62ab5-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62ab5-172">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="62ab5-173">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="62ab5-173">Minimum supported server</span></span><br/> | <span data-ttu-id="62ab5-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62ab5-174">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="62ab5-175">Namespace</span><span class="sxs-lookup"><span data-stu-id="62ab5-175">Namespace</span></span><br/>                | <span data-ttu-id="62ab5-176">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="62ab5-176">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="62ab5-177">MOF</span><span class="sxs-lookup"><span data-stu-id="62ab5-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62ab5-178"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="62ab5-178"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="62ab5-179">DLL</span><span class="sxs-lookup"><span data-stu-id="62ab5-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62ab5-180"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62ab5-180"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62ab5-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62ab5-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62ab5-182">**CIM- \_ Produkt**</span><span class="sxs-lookup"><span data-stu-id="62ab5-182">**CIM\_Product**</span></span>](cim-product.md)
</dt> <dt>

<span data-ttu-id="62ab5-183">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="62ab5-183">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

