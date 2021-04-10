---
description: Die CIM \_ CollectionSetting-Klasse stellt die Zuordnung zwischen einem CIM \_ CollectionOfMSEs und der Einstellungs Klasse dar, die für Sie definiert ist.
ms.assetid: f09bd656-5fdd-4ab1-8ef9-52d431a5117d
ms.tgt_platform: multiple
title: CIM_CollectionSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionSetting
- CIM_CollectionSetting.Collection
- CIM_CollectionSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c290225ee38008f0345b695af794e57f311f2998
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861340"
---
# <a name="cim_collectionsetting-class"></a><span data-ttu-id="2bc92-103">CIM \_ CollectionSetting-Klasse</span><span class="sxs-lookup"><span data-stu-id="2bc92-103">CIM\_CollectionSetting class</span></span>

<span data-ttu-id="2bc92-104">Die **CIM \_ CollectionSetting** -Klasse stellt die Zuordnung zwischen einem [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) und der Einstellungs Klasse dar, die für Sie definiert ist.</span><span class="sxs-lookup"><span data-stu-id="2bc92-104">The **CIM\_CollectionSetting** class represents the association between a [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) and the setting class defined for them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2bc92-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2bc92-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2bc92-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2bc92-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2bc92-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="2bc92-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2bc92-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="2bc92-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bc92-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bc92-109">Syntax</span></span>

``` syntax
class CIM_CollectionSetting
{
  CIM_CollectionOfMSEs REF Collection;
  CIM_Setting          REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="2bc92-110">Member</span><span class="sxs-lookup"><span data-stu-id="2bc92-110">Members</span></span>

<span data-ttu-id="2bc92-111">Die **CIM \_ CollectionSetting** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2bc92-111">The **CIM\_CollectionSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="2bc92-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2bc92-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2bc92-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2bc92-113">Properties</span></span>

<span data-ttu-id="2bc92-114">Die **CIM \_ CollectionSetting** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2bc92-114">The **CIM\_CollectionSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2bc92-115">**Sammlung**</span><span class="sxs-lookup"><span data-stu-id="2bc92-115">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bc92-116">Datentyp: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="2bc92-116">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="2bc92-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bc92-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bc92-118">Verweis auf die [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="2bc92-118">Reference to the [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="2bc92-119">**Einstellung**</span><span class="sxs-lookup"><span data-stu-id="2bc92-119">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bc92-120">Datentyp: **CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="2bc92-120">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="2bc92-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bc92-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bc92-122">Verweis auf das **Einstellungs** Objekt, das der Auflistungs **Eigenschaft zugeordnet** ist.</span><span class="sxs-lookup"><span data-stu-id="2bc92-122">Reference to the **Setting** object associated with the **Collection** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2bc92-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2bc92-123">Remarks</span></span>

<span data-ttu-id="2bc92-124">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="2bc92-124">WMI does not implement this class.</span></span> <span data-ttu-id="2bc92-125">Weitere Informationen zu WMI-Klassen, die von **CIM \_ CollectionSetting** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2bc92-125">For more information about WMI classes derived from **CIM\_CollectionSetting**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="2bc92-126">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="2bc92-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2bc92-127">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="2bc92-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bc92-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2bc92-128">Requirements</span></span>



| <span data-ttu-id="2bc92-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2bc92-129">Requirement</span></span> | <span data-ttu-id="2bc92-130">Wert</span><span class="sxs-lookup"><span data-stu-id="2bc92-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2bc92-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2bc92-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2bc92-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2bc92-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2bc92-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2bc92-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2bc92-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2bc92-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2bc92-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="2bc92-135">Namespace</span></span><br/>                | <span data-ttu-id="2bc92-136">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2bc92-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2bc92-137">MOF</span><span class="sxs-lookup"><span data-stu-id="2bc92-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2bc92-138"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2bc92-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2bc92-139">DLL</span><span class="sxs-lookup"><span data-stu-id="2bc92-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2bc92-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bc92-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




