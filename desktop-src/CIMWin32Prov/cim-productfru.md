---
description: Die CIM \_ productfru-Klasse stellt eine Zuordnung zwischen dem Produkt und einer ersetzbaren (Feld) Einheit (FRU) dar, die Informationen zu Produktkomponenten bereitstellt, die bereits waren oder ersetzt werden.
ms.assetid: 15d682e5-cd90-4fc4-8fff-e3fe1d2a0ac4
ms.tgt_platform: multiple
title: CIM_ProductFRU-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductFRU
- CIM_ProductFRU.FRU
- CIM_ProductFRU.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b141d16adb50c5bc3f8d6be682a90aa4921061ef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126307"
---
# <a name="cim_productfru-class"></a><span data-ttu-id="7e066-103">CIM \_ productfru-Klasse</span><span class="sxs-lookup"><span data-stu-id="7e066-103">CIM\_ProductFRU class</span></span>

<span data-ttu-id="7e066-104">Die **CIM \_ productfru** -Klasse stellt eine Zuordnung zwischen dem Produkt und einer ersetzbaren (Feld) Einheit (FRU) dar, die Informationen zu Produktkomponenten bereitstellt, die bereits waren oder ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="7e066-104">The **CIM\_ProductFRU** class represents an association between the product and a field replaceable unit (FRU), which provides information about product components that have been, or are being replaced.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7e066-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7e066-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7e066-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7e066-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7e066-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7e066-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="7e066-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7e066-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e066-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e066-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{EB98A1B2-DB36-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ProductFRU
{
  CIM_FRU     REF FRU;
  CIM_Product REF Product;
};
```

## <a name="members"></a><span data-ttu-id="7e066-110">Member</span><span class="sxs-lookup"><span data-stu-id="7e066-110">Members</span></span>

<span data-ttu-id="7e066-111">Die **CIM \_ productfru** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7e066-111">The **CIM\_ProductFRU** class has these types of members:</span></span>

-   [<span data-ttu-id="7e066-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7e066-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7e066-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7e066-113">Properties</span></span>

<span data-ttu-id="7e066-114">Die **CIM \_ productfru** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7e066-114">The **CIM\_ProductFRU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7e066-115">**FRU**</span><span class="sxs-lookup"><span data-stu-id="7e066-115">**FRU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e066-116">Datentyp: **CIM \_ FRU**</span><span class="sxs-lookup"><span data-stu-id="7e066-116">Data type: **CIM\_FRU**</span></span>
</dt> <dt>

<span data-ttu-id="7e066-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e066-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e066-118">Verweis auf das FRU-.</span><span class="sxs-lookup"><span data-stu-id="7e066-118">Reference to the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="7e066-119">**Produkt**</span><span class="sxs-lookup"><span data-stu-id="7e066-119">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e066-120">Datentyp: **CIM- \_ Produkt**</span><span class="sxs-lookup"><span data-stu-id="7e066-120">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="7e066-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e066-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e066-122">Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="7e066-122">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="7e066-123">Verweis auf das Produkt, auf das die FRU angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="7e066-123">Reference to the product to which the FRU is applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e066-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e066-124">Remarks</span></span>

<span data-ttu-id="7e066-125">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="7e066-125">WMI does not implement this class.</span></span>

<span data-ttu-id="7e066-126">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="7e066-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7e066-127">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7e066-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e066-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e066-128">Requirements</span></span>



| <span data-ttu-id="7e066-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e066-129">Requirement</span></span> | <span data-ttu-id="7e066-130">Wert</span><span class="sxs-lookup"><span data-stu-id="7e066-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e066-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7e066-131">Minimum supported client</span></span><br/> | <span data-ttu-id="7e066-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7e066-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7e066-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7e066-133">Minimum supported server</span></span><br/> | <span data-ttu-id="7e066-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e066-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7e066-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="7e066-135">Namespace</span></span><br/>                | <span data-ttu-id="7e066-136">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7e066-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7e066-137">MOF</span><span class="sxs-lookup"><span data-stu-id="7e066-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e066-138"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7e066-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e066-139">DLL</span><span class="sxs-lookup"><span data-stu-id="7e066-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e066-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e066-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

