---
description: Die CIM \_ -ElementSetting-Klasse stellt die Zuordnung zwischen verwalteten Systemelementen und der Einstellungs Klasse dar, die für Sie definiert ist.
ms.assetid: e9b7c43f-7539-48c3-8679-568fb4b036bb
ms.tgt_platform: multiple
title: CIM_ElementSetting-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementSetting
- CIM_ElementSetting.Element
- CIM_ElementSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2c1ea52648728397e811cfae35e7a83e272ab8d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342600"
---
# <a name="cim_elementsetting-class-cimwin32-wmi-providers"></a><span data-ttu-id="aefb4-103">CIM_ElementSetting-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="aefb4-103">CIM_ElementSetting class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="aefb4-104">Die **CIM- \_ ElementSetting** -Klasse stellt die Zuordnung zwischen verwalteten Systemelementen und der Einstellungs Klasse dar, die für Sie definiert ist.</span><span class="sxs-lookup"><span data-stu-id="aefb4-104">The **CIM\_ElementSetting** class represents the association between managed system elements and the setting class defined for them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aefb4-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="aefb4-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="aefb4-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="aefb4-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="aefb4-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="aefb4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="aefb4-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="aefb4-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="aefb4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="aefb4-109">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{8502C577-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ElementSetting
{
  CIM_ManagedSystemElement REF Element;
  CIM_Setting              REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="aefb4-110">Member</span><span class="sxs-lookup"><span data-stu-id="aefb4-110">Members</span></span>

<span data-ttu-id="aefb4-111">Die **CIM- \_ ElementSetting** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="aefb4-111">The **CIM\_ElementSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="aefb4-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aefb4-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aefb4-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aefb4-113">Properties</span></span>

<span data-ttu-id="aefb4-114">Die **CIM- \_ ElementSetting** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="aefb4-114">The **CIM\_ElementSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aefb4-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="aefb4-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aefb4-116">Datentyp: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="aefb4-116">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="aefb4-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aefb4-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aefb4-118">Verweis auf die Rolle des [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) -Objekts der **CIM \_ Element Setting** -Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="aefb4-118">Reference to the role of the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) object of the **CIM\_ElementSetting** association.</span></span> <span data-ttu-id="aefb4-119">Das zugeordnete verwaltete System Element stellt das Element bereit, das die-Element Einstellung implementiert.</span><span class="sxs-lookup"><span data-stu-id="aefb4-119">The associated managed system element provides the element that implements the element setting.</span></span>

</dd> <dt>

<span data-ttu-id="aefb4-120">**Einstellung**</span><span class="sxs-lookup"><span data-stu-id="aefb4-120">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aefb4-121">Datentyp: **CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="aefb4-121">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="aefb4-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aefb4-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aefb4-123">Verweis auf die Rolle des [**CIM- \_ Einstellungs**](cim-setting.md) Objekts der **CIM- \_ ElementSetting** -Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="aefb4-123">Reference to the role of the [**CIM\_Setting**](cim-setting.md) object of the **CIM\_ElementSetting** association.</span></span> <span data-ttu-id="aefb4-124">Die zugehörige Einstellung gibt die Einstellung an, die die-Element Einstellung implementiert.</span><span class="sxs-lookup"><span data-stu-id="aefb4-124">The associated setting provides the setting that implements the element setting.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aefb4-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aefb4-125">Remarks</span></span>

<span data-ttu-id="aefb4-126">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="aefb4-126">WMI does not implement this class.</span></span> <span data-ttu-id="aefb4-127">Informationen zu Klassen, die von **CIM \_ Element Setting** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md)</span><span class="sxs-lookup"><span data-stu-id="aefb4-127">For classes derived from **CIM\_ElementSetting**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="aefb4-128">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="aefb4-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="aefb4-129">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="aefb4-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="aefb4-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aefb4-130">Requirements</span></span>



| <span data-ttu-id="aefb4-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aefb4-131">Requirement</span></span> | <span data-ttu-id="aefb4-132">Wert</span><span class="sxs-lookup"><span data-stu-id="aefb4-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aefb4-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aefb4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="aefb4-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aefb4-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aefb4-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aefb4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="aefb4-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aefb4-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aefb4-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="aefb4-137">Namespace</span></span><br/>                | <span data-ttu-id="aefb4-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="aefb4-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aefb4-139">MOF</span><span class="sxs-lookup"><span data-stu-id="aefb4-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aefb4-140"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="aefb4-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aefb4-141">DLL</span><span class="sxs-lookup"><span data-stu-id="aefb4-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aefb4-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aefb4-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




