---
description: Die CIM \_ productsupport-Klasse stellt eine Zuordnung Zwischenprodukt und Support Zugriff dar, die die Art der Unterstützung für das Produkt übermittelt.
ms.assetid: 61c62556-0cf3-438c-b9c7-152505bf7ed6
ms.tgt_platform: multiple
title: CIM_ProductSupport-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductSupport
- CIM_ProductSupport.Product
- CIM_ProductSupport.Support
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8d1b39e1eef8f9686eee66c629120feaea51c778
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342979"
---
# <a name="cim_productsupport-class"></a><span data-ttu-id="dfb92-103">CIM \_ productsupport-Klasse</span><span class="sxs-lookup"><span data-stu-id="dfb92-103">CIM\_ProductSupport class</span></span>

<span data-ttu-id="dfb92-104">Die **CIM \_ productsupport** -Klasse stellt eine Zuordnung Zwischenprodukt und Support Zugriff dar, die die Art der Unterstützung für das Produkt übermittelt.</span><span class="sxs-lookup"><span data-stu-id="dfb92-104">The **CIM\_ProductSupport** class represents an association between product and support access that conveys how support is obtained for the product.</span></span> <span data-ttu-id="dfb92-105">Für ein Produkt sind verschiedene Support Typen verfügbar. das gleiche Support Objekt bietet Unterstützung für mehrere Produkte.</span><span class="sxs-lookup"><span data-stu-id="dfb92-105">Various types of support are available for a product; the same support object can provide assistance for multiple products.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dfb92-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="dfb92-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dfb92-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="dfb92-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dfb92-108">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dfb92-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="dfb92-109">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="dfb92-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfb92-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfb92-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8D6D6880-DB2B-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ProductSupport
{
  CIM_Product       REF Product;
  CIM_SupportAccess REF Support;
};
```

## <a name="members"></a><span data-ttu-id="dfb92-111">Member</span><span class="sxs-lookup"><span data-stu-id="dfb92-111">Members</span></span>

<span data-ttu-id="dfb92-112">Die **CIM \_ productsupport** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dfb92-112">The **CIM\_ProductSupport** class has these types of members:</span></span>

-   [<span data-ttu-id="dfb92-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dfb92-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dfb92-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dfb92-114">Properties</span></span>

<span data-ttu-id="dfb92-115">Die **CIM \_ productsupport** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dfb92-115">The **CIM\_ProductSupport** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dfb92-116">**Produkt**</span><span class="sxs-lookup"><span data-stu-id="dfb92-116">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfb92-117">Datentyp: **CIM- \_ Produkt**</span><span class="sxs-lookup"><span data-stu-id="dfb92-117">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="dfb92-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dfb92-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dfb92-119">Verweis auf das Produkt.</span><span class="sxs-lookup"><span data-stu-id="dfb92-119">Reference to the product.</span></span>

</dd> <dt>

<span data-ttu-id="dfb92-120">**Unterstützung**</span><span class="sxs-lookup"><span data-stu-id="dfb92-120">**Support**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfb92-121">Datentyp: **CIM \_ supportaccess**</span><span class="sxs-lookup"><span data-stu-id="dfb92-121">Data type: **CIM\_SupportAccess**</span></span>
</dt> <dt>

<span data-ttu-id="dfb92-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dfb92-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dfb92-123">Verweis auf den Produktsupport.</span><span class="sxs-lookup"><span data-stu-id="dfb92-123">Reference to the product support.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dfb92-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dfb92-124">Remarks</span></span>

<span data-ttu-id="dfb92-125">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="dfb92-125">WMI does not implement this class.</span></span>

<span data-ttu-id="dfb92-126">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="dfb92-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dfb92-127">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="dfb92-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfb92-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dfb92-128">Requirements</span></span>



| <span data-ttu-id="dfb92-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dfb92-129">Requirement</span></span> | <span data-ttu-id="dfb92-130">Wert</span><span class="sxs-lookup"><span data-stu-id="dfb92-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfb92-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dfb92-131">Minimum supported client</span></span><br/> | <span data-ttu-id="dfb92-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dfb92-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dfb92-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dfb92-133">Minimum supported server</span></span><br/> | <span data-ttu-id="dfb92-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dfb92-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dfb92-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="dfb92-135">Namespace</span></span><br/>                | <span data-ttu-id="dfb92-136">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dfb92-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dfb92-137">MOF</span><span class="sxs-lookup"><span data-stu-id="dfb92-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dfb92-138"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dfb92-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dfb92-139">DLL</span><span class="sxs-lookup"><span data-stu-id="dfb92-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfb92-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfb92-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




