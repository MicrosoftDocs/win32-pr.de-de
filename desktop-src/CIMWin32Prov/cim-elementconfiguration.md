---
description: Die CIM-ElementConfiguration-Zuordnung verknüpft \_ ein CIM- \_ Konfigurationsobjekt mit einem oder mehreren verwalteten Systemelementen. Das CIM- \_ Konfigurationsobjekt stellt ein bestimmtes Verhalten oder einen gewünschten funktionalen Zustand für das zugeordnete CIM \_ ManagedSystemElement dar.
ms.assetid: 4d2af009-7466-4394-af42-72c8d96e0786
ms.tgt_platform: multiple
title: CIM_ElementConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementConfiguration
- CIM_ElementConfiguration.Configuration
- CIM_ElementConfiguration.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7707338a3c2268cba51146aa8462b3b244b149ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041452"
---
# <a name="cim_elementconfiguration-class"></a><span data-ttu-id="c613d-104">CIM \_ ElementConfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="c613d-104">CIM\_ElementConfiguration class</span></span>

<span data-ttu-id="c613d-105">Die **CIM- \_ ElementConfiguration** -Zuordnung verknüpft ein [**CIM- \_ Konfigurations**](cim-configuration.md) Objekt mit einem oder mehreren verwalteten Systemelementen.</span><span class="sxs-lookup"><span data-stu-id="c613d-105">The **CIM\_ElementConfiguration** association relates a [**CIM\_Configuration**](cim-configuration.md) object to one or more managed system elements.</span></span> <span data-ttu-id="c613d-106">Das **CIM- \_ Konfigurations** Objekt stellt ein bestimmtes Verhalten oder einen gewünschten funktionalen Zustand für das zugeordnete [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)dar.</span><span class="sxs-lookup"><span data-stu-id="c613d-106">The **CIM\_Configuration** object represents a certain behavior, or a desired functional state for the associated [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c613d-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c613d-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c613d-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c613d-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c613d-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="c613d-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c613d-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c613d-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c613d-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c613d-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FC049DCE-DB29-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ElementConfiguration
{
  CIM_Configuration        REF Configuration;
  CIM_ManagedSystemElement REF Element;
};
```

## <a name="members"></a><span data-ttu-id="c613d-112">Member</span><span class="sxs-lookup"><span data-stu-id="c613d-112">Members</span></span>

<span data-ttu-id="c613d-113">Die **CIM \_ ElementConfiguration** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c613d-113">The **CIM\_ElementConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="c613d-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c613d-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c613d-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c613d-115">Properties</span></span>

<span data-ttu-id="c613d-116">Die **CIM \_ ElementConfiguration** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c613d-116">The **CIM\_ElementConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c613d-117">**Configuration**</span><span class="sxs-lookup"><span data-stu-id="c613d-117">**Configuration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c613d-118">Datentyp: **CIM- \_ Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="c613d-118">Data type: **CIM\_Configuration**</span></span>
</dt> <dt>

<span data-ttu-id="c613d-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c613d-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c613d-120">Verweis auf das [**CIM- \_ Konfigurations**](cim-configuration.md) Objekt, das die dem verwalteten System Element zugeordneten Einstellungen und Abhängigkeiten gruppiert.</span><span class="sxs-lookup"><span data-stu-id="c613d-120">Reference to the [**CIM\_Configuration**](cim-configuration.md) object that groups the settings and dependencies associated with the managed system element.</span></span>

</dd> <dt>

<span data-ttu-id="c613d-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="c613d-121">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c613d-122">Datentyp: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="c613d-122">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="c613d-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c613d-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c613d-124">Verweis auf das verwaltete System Element.</span><span class="sxs-lookup"><span data-stu-id="c613d-124">Reference to the managed system element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c613d-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c613d-125">Remarks</span></span>

<span data-ttu-id="c613d-126">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="c613d-126">WMI does not implement this class.</span></span>

<span data-ttu-id="c613d-127">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c613d-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c613d-128">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c613d-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c613d-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c613d-129">Requirements</span></span>



| <span data-ttu-id="c613d-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c613d-130">Requirement</span></span> | <span data-ttu-id="c613d-131">Wert</span><span class="sxs-lookup"><span data-stu-id="c613d-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c613d-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c613d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c613d-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c613d-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c613d-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c613d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c613d-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c613d-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c613d-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="c613d-136">Namespace</span></span><br/>                | <span data-ttu-id="c613d-137">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c613d-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c613d-138">MOF</span><span class="sxs-lookup"><span data-stu-id="c613d-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c613d-139"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c613d-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c613d-140">DLL</span><span class="sxs-lookup"><span data-stu-id="c613d-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c613d-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c613d-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




