---
description: Die Win32 \_ -Klasse implementedcategory Association WMI verknüpft eine Komponenten Kategorie und die Component Object Model (com)-Klasse mithilfe ihrer Schnittstellen.
ms.assetid: 7cf32b50-9ae6-44e5-b364-bc74dea3dc17
ms.tgt_platform: multiple
title: Win32_ImplementedCategory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ImplementedCategory
- Win32_ImplementedCategory.Category
- Win32_ImplementedCategory.Component
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1d885c8c8e92ea661e06b46f338924355438ff9a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749016"
---
# <a name="win32_implementedcategory-class"></a><span data-ttu-id="18ebb-103">Win32 \_ implementedcategory-Klasse</span><span class="sxs-lookup"><span data-stu-id="18ebb-103">Win32\_ImplementedCategory class</span></span>

<span data-ttu-id="18ebb-104">Die **Win32-Klasse \_ implementedcategory** Association [WMI](/windows/desktop/WmiSdk/retrieving-a-class) verknüpft eine Komponenten Kategorie und die Component Object Model (com)-Klasse mithilfe ihrer Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="18ebb-104">The **Win32\_ImplementedCategory** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a component category and the Component Object Model (COM) class using its interfaces.</span></span>

<span data-ttu-id="18ebb-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="18ebb-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="18ebb-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="18ebb-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="18ebb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="18ebb-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5B-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ImplementedCategory
{
  Win32_ComponentCategory REF Category;
  Win32_ClassicCOMClass   REF Component;
};
```

## <a name="members"></a><span data-ttu-id="18ebb-108">Member</span><span class="sxs-lookup"><span data-stu-id="18ebb-108">Members</span></span>

<span data-ttu-id="18ebb-109">Die **Win32 \_ implementedcategory** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="18ebb-109">The **Win32\_ImplementedCategory** class has these types of members:</span></span>

-   [<span data-ttu-id="18ebb-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18ebb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18ebb-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18ebb-111">Properties</span></span>

<span data-ttu-id="18ebb-112">Die **Win32 \_ implementedcategory** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="18ebb-112">The **Win32\_ImplementedCategory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18ebb-113">**Kategorie**</span><span class="sxs-lookup"><span data-stu-id="18ebb-113">**Category**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18ebb-114">Datentyp: **Win32 \_ componentcategory**</span><span class="sxs-lookup"><span data-stu-id="18ebb-114">Data type: **Win32\_ComponentCategory**</span></span>
</dt> <dt>

<span data-ttu-id="18ebb-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18ebb-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18ebb-116">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ componentcategory")</span><span class="sxs-lookup"><span data-stu-id="18ebb-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ComponentCategory")</span></span>
</dt> </dl>

<span data-ttu-id="18ebb-117">Verweis auf die-Instanz, die die von der com-Klasse verwendete Komponenten Kategorie darstellt.</span><span class="sxs-lookup"><span data-stu-id="18ebb-117">Reference to the instance representing the component category being used by the COM class.</span></span>

</dd> <dt>

<span data-ttu-id="18ebb-118">**Komponente**</span><span class="sxs-lookup"><span data-stu-id="18ebb-118">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18ebb-119">Datentyp: **Win32 \_ classiccomclass**</span><span class="sxs-lookup"><span data-stu-id="18ebb-119">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="18ebb-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18ebb-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18ebb-121">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ classiccomclass")</span><span class="sxs-lookup"><span data-stu-id="18ebb-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="18ebb-122">Verweis auf die-Instanz, die die com-Klasse unter Verwendung der zugeordneten Kategorie darstellt.</span><span class="sxs-lookup"><span data-stu-id="18ebb-122">Reference to the instance representing the COM class using the associated category.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18ebb-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18ebb-123">Requirements</span></span>



| <span data-ttu-id="18ebb-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18ebb-124">Requirement</span></span> | <span data-ttu-id="18ebb-125">Wert</span><span class="sxs-lookup"><span data-stu-id="18ebb-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18ebb-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="18ebb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="18ebb-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18ebb-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="18ebb-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="18ebb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="18ebb-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18ebb-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="18ebb-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="18ebb-130">Namespace</span></span><br/>                | <span data-ttu-id="18ebb-131">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="18ebb-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="18ebb-132">MOF</span><span class="sxs-lookup"><span data-stu-id="18ebb-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18ebb-133"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="18ebb-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="18ebb-134">DLL</span><span class="sxs-lookup"><span data-stu-id="18ebb-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18ebb-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18ebb-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18ebb-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18ebb-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="18ebb-137">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="18ebb-137">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

