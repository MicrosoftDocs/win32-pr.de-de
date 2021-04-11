---
description: Die \_ WMI-Klasse "Win32 comapplicationclasses Abstract Association" verknüpft eine Component Object Model (com)-Komponente und die COM-Anwendung, in der Sie sich befindet.
ms.assetid: 7c188199-86fb-45ba-b318-9d9529b831b8
ms.tgt_platform: multiple
title: Win32_COMApplicationClasses-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMApplicationClasses
- Win32_COMApplicationClasses.PartComponent
- Win32_COMApplicationClasses.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 01413128f7457049a4383c1148938e2136645337
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127348"
---
# <a name="win32_comapplicationclasses-class"></a><span data-ttu-id="75328-103">Win32 \_ comapplicationclasses-Klasse</span><span class="sxs-lookup"><span data-stu-id="75328-103">Win32\_COMApplicationClasses class</span></span>

<span data-ttu-id="75328-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " **Win32 \_ comapplicationclasses** Abstract Association" verknüpft eine Component Object Model (com)-Komponente und die COM-Anwendung, in der Sie sich befindet.</span><span class="sxs-lookup"><span data-stu-id="75328-104">The **Win32\_COMApplicationClasses** abstract association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a Component Object Model (COM) component and the COM application where it resides.</span></span>

<span data-ttu-id="75328-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="75328-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="75328-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="75328-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="75328-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="75328-107">Syntax</span></span>

``` syntax
[abstract, UUID("{0F73ED51-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_COMApplicationClasses : CIM_Component
{
  Win32_COMClass       REF PartComponent;
  Win32_COMApplication REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="75328-108">Member</span><span class="sxs-lookup"><span data-stu-id="75328-108">Members</span></span>

<span data-ttu-id="75328-109">Die **Win32 \_ comapplicationclasses** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="75328-109">The **Win32\_COMApplicationClasses** class has these types of members:</span></span>

-   [<span data-ttu-id="75328-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="75328-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="75328-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="75328-111">Properties</span></span>

<span data-ttu-id="75328-112">Die **Win32 \_ comapplicationclasses** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="75328-112">The **Win32\_COMApplicationClasses** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="75328-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="75328-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75328-114">Datentyp: **Win32 \_ comapplication**</span><span class="sxs-lookup"><span data-stu-id="75328-114">Data type: **Win32\_COMApplication**</span></span>
</dt> <dt>

<span data-ttu-id="75328-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="75328-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75328-116">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ comapplication")</span><span class="sxs-lookup"><span data-stu-id="75328-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_COMApplication")</span></span>
</dt> </dl>

<span data-ttu-id="75328-117">Eine [**Win32- \_ comapplication**](win32-comapplication.md) , die die COM-Anwendung darstellt, die die COM-Komponente enthält.</span><span class="sxs-lookup"><span data-stu-id="75328-117">A [**Win32\_COMApplication**](win32-comapplication.md) that represents the COM application containing the COM component.</span></span>

</dd> <dt>

<span data-ttu-id="75328-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="75328-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75328-119">Datentyp: **Win32 \_ ComClass**</span><span class="sxs-lookup"><span data-stu-id="75328-119">Data type: **Win32\_COMClass**</span></span>
</dt> <dt>

<span data-ttu-id="75328-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="75328-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75328-121">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ComClass")</span><span class="sxs-lookup"><span data-stu-id="75328-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_COMClass")</span></span>
</dt> </dl>

<span data-ttu-id="75328-122">Eine [**Win32- \_ ComClass**](win32-comclass.md) , die die unter der com-Anwendung gruppierte COM-Komponente darstellt.</span><span class="sxs-lookup"><span data-stu-id="75328-122">A [**Win32\_COMClass**](win32-comclass.md) that represents the COM component grouped under the COM application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="75328-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75328-123">Remarks</span></span>

<span data-ttu-id="75328-124">Die **Win32-Klasse \_ comapplicationclasses** wird von der [**CIM- \_ Komponente**](cim-component.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="75328-124">The **Win32\_COMApplicationClasses** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="75328-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75328-125">Requirements</span></span>



| <span data-ttu-id="75328-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75328-126">Requirement</span></span> | <span data-ttu-id="75328-127">Wert</span><span class="sxs-lookup"><span data-stu-id="75328-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75328-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="75328-128">Minimum supported client</span></span><br/> | <span data-ttu-id="75328-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75328-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="75328-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="75328-130">Minimum supported server</span></span><br/> | <span data-ttu-id="75328-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75328-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="75328-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="75328-132">Namespace</span></span><br/>                | <span data-ttu-id="75328-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="75328-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="75328-134">MOF</span><span class="sxs-lookup"><span data-stu-id="75328-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75328-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="75328-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="75328-136">DLL</span><span class="sxs-lookup"><span data-stu-id="75328-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75328-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75328-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75328-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75328-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75328-139">**CIM- \_ Komponente**</span><span class="sxs-lookup"><span data-stu-id="75328-139">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

<span data-ttu-id="75328-140">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="75328-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

