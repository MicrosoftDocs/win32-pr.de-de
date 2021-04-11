---
description: Die CIM \_ logicalidentity-Klasse ist eine abstrakte und generische Zuordnung, die angibt, dass zwei logische Elemente verschiedene Aspekte der gleichen zugrunde liegenden Entität darstellen.
ms.assetid: 624a52bf-001d-4f18-af77-87a5d1cfa1ff
ms.tgt_platform: multiple
title: CIM_LogicalIdentity-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalIdentity
- CIM_LogicalIdentity.SameElement
- CIM_LogicalIdentity.SystemElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 52780144a48cbb424ee037f71a56e238bb864311
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958247"
---
# <a name="cim_logicalidentity-class-cimwin32-wmi-providers"></a><span data-ttu-id="5c883-103">CIM_LogicalIdentity-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="5c883-103">CIM_LogicalIdentity class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="5c883-104">Die **CIM \_ logicalidentity** -Klasse ist eine abstrakte und generische Zuordnung, die angibt, dass zwei logische Elemente verschiedene Aspekte der gleichen zugrunde liegenden Entität darstellen.</span><span class="sxs-lookup"><span data-stu-id="5c883-104">The **CIM\_LogicalIdentity** class is an abstract and generic association that indicates that two logical elements represent different aspects of the same underlying entity.</span></span> <span data-ttu-id="5c883-105">Die Zuordnung stellt dar, was mit Mehrfachvererbung definiert werden kann, und ist auf die logischen Aspekte eines verwalteten System Elements beschränkt.</span><span class="sxs-lookup"><span data-stu-id="5c883-105">The association conveys what can be defined with multiple inheritance and is restricted to the logical aspects of a managed system element.</span></span> <span data-ttu-id="5c883-106">In den meisten Szenarios wird die Identitäts Beziehung durch die Äquivalenz von Schlüsseln oder einige andere identifizierende Eigenschaften der zugehörigen Elemente festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5c883-106">In most scenarios, the identity relationship is determined by the equivalence of keys, or some other identifying properties of the related elements.</span></span>

<span data-ttu-id="5c883-107">Die Zuordnung sollte nur in Szenarios verwendet werden, die gut interpretiert werden und eine konkretere Definition und Klärung in Unterklassen ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="5c883-107">The association should only be used in scenarios that are well understood, allowing more concrete definition and clarification in subclasses.</span></span> <span data-ttu-id="5c883-108">Ein Szenario, in dem die Beziehung vernünftig ist, stellt z. b. ein Gerät dar, das sowohl eine busentität als auch eine funktionale Entität ist, bei der es sich um eine USB-(Bus) und eine Tastatur (funktionale) Einheit handelt</span><span class="sxs-lookup"><span data-stu-id="5c883-108">A scenario where the relationship is reasonable, for example, represents a device that is both a bus entity and a functional entity where the device is a USB (bus) and keyboard (functional) entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5c883-109">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5c883-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5c883-110">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5c883-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5c883-111">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="5c883-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5c883-112">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5c883-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c883-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c883-113">Syntax</span></span>

``` syntax
class CIM_LogicalIdentity
{
  CIM_LogicalElement REF SameElement;
  CIM_LogicalElement REF SystemElement;
};
```

## <a name="members"></a><span data-ttu-id="5c883-114">Member</span><span class="sxs-lookup"><span data-stu-id="5c883-114">Members</span></span>

<span data-ttu-id="5c883-115">Die **CIM \_ logicalidentity** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5c883-115">The **CIM\_LogicalIdentity** class has these types of members:</span></span>

-   [<span data-ttu-id="5c883-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5c883-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5c883-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5c883-117">Properties</span></span>

<span data-ttu-id="5c883-118">Die **CIM \_ logicalidentity** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5c883-118">The **CIM\_LogicalIdentity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5c883-119">**SameElement**</span><span class="sxs-lookup"><span data-stu-id="5c883-119">**SameElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c883-120">Datentyp: **CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="5c883-120">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="5c883-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5c883-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c883-122">Verweis auf einen alternativen Aspekt der System Entität.</span><span class="sxs-lookup"><span data-stu-id="5c883-122">Reference to an alternate aspect of the system entity.</span></span>

</dd> <dt>

<span data-ttu-id="5c883-123">**Systemelement**</span><span class="sxs-lookup"><span data-stu-id="5c883-123">**SystemElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c883-124">Datentyp: **CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="5c883-124">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="5c883-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5c883-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c883-126">Verweis auf einen Aspekt des logischen Elements.</span><span class="sxs-lookup"><span data-stu-id="5c883-126">Reference to one aspect of the logical element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c883-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c883-127">Remarks</span></span>

<span data-ttu-id="5c883-128">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="5c883-128">WMI does not implement this class.</span></span> <span data-ttu-id="5c883-129">Informationen zu Klassen, die von **CIM \_ logicalidentity** abgeleitet sind, finden Sie unter [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5c883-129">For classes derived from **CIM\_LogicalIdentity**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="5c883-130">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="5c883-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5c883-131">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5c883-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c883-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c883-132">Requirements</span></span>



| <span data-ttu-id="5c883-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c883-133">Requirement</span></span> | <span data-ttu-id="5c883-134">Wert</span><span class="sxs-lookup"><span data-stu-id="5c883-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c883-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5c883-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5c883-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c883-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5c883-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5c883-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5c883-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c883-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5c883-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="5c883-139">Namespace</span></span><br/>                | <span data-ttu-id="5c883-140">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5c883-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5c883-141">MOF</span><span class="sxs-lookup"><span data-stu-id="5c883-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c883-142"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5c883-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c883-143">DLL</span><span class="sxs-lookup"><span data-stu-id="5c883-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c883-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c883-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




