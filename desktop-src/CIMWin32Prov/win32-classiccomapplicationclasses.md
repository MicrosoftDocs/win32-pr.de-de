---
description: Die Win32 \_ -WMI-Klasse classiccomapplicationclasses verknüpft eine COM-Anwendung und eine gruppierte COM-Komponente.
ms.assetid: 77f24461-9ca0-4fc3-8728-4a4b9a1edbc3
ms.tgt_platform: multiple
title: Win32_ClassicCOMApplicationClasses-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMApplicationClasses
- Win32_ClassicCOMApplicationClasses.PartComponent
- Win32_ClassicCOMApplicationClasses.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dfd451c1c5d4819f1ec1d21f890b207a06d6fb82
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861519"
---
# <a name="win32_classiccomapplicationclasses-class"></a><span data-ttu-id="b65b5-103">Win32 \_ classiccomapplicationclasses-Klasse</span><span class="sxs-lookup"><span data-stu-id="b65b5-103">Win32\_ClassicCOMApplicationClasses class</span></span>

<span data-ttu-id="b65b5-104">Die Win32- [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) **\_ classiccomapplicationclasses** verknüpft eine COM-Anwendung und eine gruppierte COM-Komponente.</span><span class="sxs-lookup"><span data-stu-id="b65b5-104">The **Win32\_ClassicCOMApplicationClasses** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a COM application and a COM component grouped under it.</span></span>

<span data-ttu-id="b65b5-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b65b5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b65b5-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b65b5-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b65b5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b65b5-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED54-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMApplicationClasses : Win32_COMApplicationClasses
{
  Win32_ClassicCOMClass REF PartComponent;
  Win32_DCOMApplication REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="b65b5-108">Member</span><span class="sxs-lookup"><span data-stu-id="b65b5-108">Members</span></span>

<span data-ttu-id="b65b5-109">Die Klasse " **Win32 \_ classiccomapplicationclasses** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b65b5-109">The **Win32\_ClassicCOMApplicationClasses** class has these types of members:</span></span>

-   [<span data-ttu-id="b65b5-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b65b5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b65b5-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b65b5-111">Properties</span></span>

<span data-ttu-id="b65b5-112">Die Klasse " **Win32 \_ classiccomapplicationclasses** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b65b5-112">The **Win32\_ClassicCOMApplicationClasses** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b65b5-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="b65b5-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b65b5-114">Datentyp: **Win32 \_ dcomapplication**</span><span class="sxs-lookup"><span data-stu-id="b65b5-114">Data type: **Win32\_DCOMApplication**</span></span>
</dt> <dt>

<span data-ttu-id="b65b5-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b65b5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b65b5-116">Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ dcomapplication")</span><span class="sxs-lookup"><span data-stu-id="b65b5-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DCOMApplication")</span></span>
</dt> </dl>

<span data-ttu-id="b65b5-117">Eine [**Win32 \_ dcomapplication**](win32-dcomapplication.md) , die eine DCOM-Anwendung darstellt, die die COM-Komponente enthält oder verwendet.</span><span class="sxs-lookup"><span data-stu-id="b65b5-117">A [**Win32\_DCOMApplication**](win32-dcomapplication.md) that represents a DCOM application containing or using the COM component.</span></span>

</dd> <dt>

<span data-ttu-id="b65b5-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="b65b5-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b65b5-119">Datentyp: **Win32 \_ classiccomclass**</span><span class="sxs-lookup"><span data-stu-id="b65b5-119">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="b65b5-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b65b5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b65b5-121">Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ classiccomclass")</span><span class="sxs-lookup"><span data-stu-id="b65b5-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="b65b5-122">Eine [**Win32 \_ classiccomclass**](win32-classiccomclass.md) , die die COM-Komponente darstellt, die in der DCOM-Anwendung vorhanden ist oder von dieser verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b65b5-122">A [**Win32\_ClassicCOMClass**](win32-classiccomclass.md) that represents the COM component existing in or used by the DCOM application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b65b5-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b65b5-123">Remarks</span></span>

<span data-ttu-id="b65b5-124">Die Klasse " **Win32 \_ classiccomapplicationclasses** " wird von [**Win32 \_ comapplicationclasses**](win32-comapplicationclasses.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b65b5-124">The **Win32\_ClassicCOMApplicationClasses** class is derived from [**Win32\_COMApplicationClasses**](win32-comapplicationclasses.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b65b5-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b65b5-125">Requirements</span></span>



| <span data-ttu-id="b65b5-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b65b5-126">Requirement</span></span> | <span data-ttu-id="b65b5-127">Wert</span><span class="sxs-lookup"><span data-stu-id="b65b5-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b65b5-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b65b5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b65b5-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b65b5-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b65b5-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b65b5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b65b5-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b65b5-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b65b5-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="b65b5-132">Namespace</span></span><br/>                | <span data-ttu-id="b65b5-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b65b5-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b65b5-134">MOF</span><span class="sxs-lookup"><span data-stu-id="b65b5-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b65b5-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b65b5-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b65b5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b65b5-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b65b5-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b65b5-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b65b5-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b65b5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b65b5-139">**Win32- \_ comapplicationclasses**</span><span class="sxs-lookup"><span data-stu-id="b65b5-139">**Win32\_COMApplicationClasses**</span></span>](win32-comapplicationclasses.md)
</dt> <dt>

<span data-ttu-id="b65b5-140">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b65b5-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

