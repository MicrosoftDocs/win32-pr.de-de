---
description: Die CIM \_ productproductdepen-Klasse stellt eine Zuordnung zwischen zwei Produkten dar, die angibt, dass eine für die andere installiert werden muss oder nicht. Dies entspricht konzeptionell der CIM \_ serviceserviceabhängigkeiten-Zuordnung.
ms.assetid: 898b9993-3bdc-4a7c-98c1-ed960014ace8
ms.tgt_platform: multiple
title: CIM_ProductProductDependency-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductProductDependency
- CIM_ProductProductDependency.DependentProduct
- CIM_ProductProductDependency.RequiredProduct
- CIM_ProductProductDependency.TypeOfDependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 094800b3a2d50d7be4039d5850f9ac1d3f236a40
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041377"
---
# <a name="cim_productproductdependency-class"></a><span data-ttu-id="23f9b-104">CIM \_ productproductdepensklasse</span><span class="sxs-lookup"><span data-stu-id="23f9b-104">CIM\_ProductProductDependency class</span></span>

<span data-ttu-id="23f9b-105">Die **CIM \_ productproductdepen-Klasse** stellt eine Zuordnung zwischen zwei Produkten dar, die angibt, dass eine für die andere installiert werden muss oder nicht.</span><span class="sxs-lookup"><span data-stu-id="23f9b-105">The **CIM\_ProductProductDependency** class represents an association between two products, which indicates that one must be installed or absent for the other to function.</span></span> <span data-ttu-id="23f9b-106">Dies entspricht konzeptionell der [**CIM \_ serviceserviceabhängigkeiten**](cim-serviceservicedependency.md) -Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="23f9b-106">This is conceptually equivalent to the [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md) association.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="23f9b-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="23f9b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="23f9b-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="23f9b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="23f9b-109">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="23f9b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="23f9b-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="23f9b-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="23f9b-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="23f9b-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{65878E68-DB2B-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ProductProductDependency
{
  CIM_Product REF DependentProduct;
  CIM_Product REF RequiredProduct;
  uint16          TypeOfDependency;
};
```

## <a name="members"></a><span data-ttu-id="23f9b-112">Member</span><span class="sxs-lookup"><span data-stu-id="23f9b-112">Members</span></span>

<span data-ttu-id="23f9b-113">Die **CIM \_ productproductdepensklasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="23f9b-113">The **CIM\_ProductProductDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="23f9b-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="23f9b-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="23f9b-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="23f9b-115">Properties</span></span>

<span data-ttu-id="23f9b-116">Die **CIM \_ productproductdepensklasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="23f9b-116">The **CIM\_ProductProductDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="23f9b-117">**Dependentproduct**</span><span class="sxs-lookup"><span data-stu-id="23f9b-117">**DependentProduct**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f9b-118">Datentyp: **CIM- \_ Produkt**</span><span class="sxs-lookup"><span data-stu-id="23f9b-118">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="23f9b-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23f9b-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f9b-120">Verweis auf das Produkt, das von einem anderen Produkt abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="23f9b-120">Reference to the product that is dependent on another product.</span></span>

</dd> <dt>

<span data-ttu-id="23f9b-121">**Requirements DProduct**</span><span class="sxs-lookup"><span data-stu-id="23f9b-121">**RequiredProduct**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f9b-122">Datentyp: **CIM- \_ Produkt**</span><span class="sxs-lookup"><span data-stu-id="23f9b-122">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="23f9b-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23f9b-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f9b-124">Verweis auf das erforderliche Produkt.</span><span class="sxs-lookup"><span data-stu-id="23f9b-124">Reference to the required product.</span></span>

</dd> <dt>

<span data-ttu-id="23f9b-125">**Typeofabhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="23f9b-125">**TypeOfDependency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f9b-126">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23f9b-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23f9b-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23f9b-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f9b-128">Die Art der Produkt Abhängigkeit.</span><span class="sxs-lookup"><span data-stu-id="23f9b-128">Nature of the product dependency.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="23f9b-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="23f9b-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="23f9b-130">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="23f9b-130">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="23f9b-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="23f9b-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="23f9b-132">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="23f9b-132">Other.</span></span>

</dd> <dt>

<span id="Product_Must_Be_Installed"></span><span id="product_must_be_installed"></span><span id="PRODUCT_MUST_BE_INSTALLED"></span>

<span data-ttu-id="23f9b-133"><span id="Product_Must_Be_Installed"></span><span id="product_must_be_installed"></span><span id="PRODUCT_MUST_BE_INSTALLED"></span>Das **Produkt muss installiert sein** (2).</span><span class="sxs-lookup"><span data-stu-id="23f9b-133"><span id="Product_Must_Be_Installed"></span><span id="product_must_be_installed"></span><span id="PRODUCT_MUST_BE_INSTALLED"></span>**Product Must Be Installed** (2)</span></span>


</dt> <dd>

<span data-ttu-id="23f9b-134">Das Produkt muss installiert sein.</span><span class="sxs-lookup"><span data-stu-id="23f9b-134">Product must be installed.</span></span>

</dd> <dt>

<span id="Product_Must_Not_Be_Installed"></span><span id="product_must_not_be_installed"></span><span id="PRODUCT_MUST_NOT_BE_INSTALLED"></span>

<span data-ttu-id="23f9b-135"><span id="Product_Must_Not_Be_Installed"></span><span id="product_must_not_be_installed"></span><span id="PRODUCT_MUST_NOT_BE_INSTALLED"></span>Das **Produkt darf nicht installiert sein** (3).</span><span class="sxs-lookup"><span data-stu-id="23f9b-135"><span id="Product_Must_Not_Be_Installed"></span><span id="product_must_not_be_installed"></span><span id="PRODUCT_MUST_NOT_BE_INSTALLED"></span>**Product Must Not Be Installed** (3)</span></span>


</dt> <dd>

<span data-ttu-id="23f9b-136">Das Produkt darf nicht installiert sein.</span><span class="sxs-lookup"><span data-stu-id="23f9b-136">Product must not be installed.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23f9b-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23f9b-137">Remarks</span></span>

<span data-ttu-id="23f9b-138">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="23f9b-138">WMI does not implement this class.</span></span>

<span data-ttu-id="23f9b-139">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="23f9b-139">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="23f9b-140">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="23f9b-140">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="23f9b-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23f9b-141">Requirements</span></span>



| <span data-ttu-id="23f9b-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="23f9b-142">Requirement</span></span> | <span data-ttu-id="23f9b-143">Wert</span><span class="sxs-lookup"><span data-stu-id="23f9b-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23f9b-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="23f9b-144">Minimum supported client</span></span><br/> | <span data-ttu-id="23f9b-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="23f9b-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="23f9b-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="23f9b-146">Minimum supported server</span></span><br/> | <span data-ttu-id="23f9b-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="23f9b-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="23f9b-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="23f9b-148">Namespace</span></span><br/>                | <span data-ttu-id="23f9b-149">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="23f9b-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="23f9b-150">MOF</span><span class="sxs-lookup"><span data-stu-id="23f9b-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23f9b-151"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="23f9b-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="23f9b-152">DLL</span><span class="sxs-lookup"><span data-stu-id="23f9b-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23f9b-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23f9b-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




