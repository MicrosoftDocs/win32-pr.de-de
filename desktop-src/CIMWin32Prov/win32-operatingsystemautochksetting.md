---
description: Diese Klasse stellt die Zuordnung zwischen einem Betriebssystem und den AUTOCHK-Einstellungen dar, die auf die Datenträger auf dem Computer angewendet werden. Beachten Sie, dass die Einstellung dem Betriebssystem und nicht dem Computersystem zugeordnet ist, da ein oder mehrere Betriebssysteme auf dem Computer installiert sein können, die jeweils über eigene automatische chk-Einstellungen verfügen.
ms.assetid: 11178459-85c2-41c0-83b3-5b967e3311cf
ms.tgt_platform: multiple
title: Win32_OperatingSystemAutochkSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 905ffc92273b46bb36b7b3e2909afea32e6baeff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127465"
---
# <a name="win32_operatingsystemautochksetting-class"></a><span data-ttu-id="e64e6-103">Win32 \_ operatingsystemautochksetting-Klasse</span><span class="sxs-lookup"><span data-stu-id="e64e6-103">Win32\_OperatingSystemAutochkSetting class</span></span>

<span data-ttu-id="e64e6-104">Diese Klasse stellt die Zuordnung zwischen einem Betriebssystem und den AUTOCHK-Einstellungen dar, die auf die Datenträger auf dem Computer angewendet werden. Beachten Sie, dass die Einstellung dem Betriebssystem und nicht dem Computersystem zugeordnet ist, da ein oder mehrere Betriebssysteme auf dem Computer installiert sein können, die jeweils über eigene automatische chk-Einstellungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="e64e6-104">This class represents the association between an operating system and the autochk settings that apply to the disks on the machine.Note that the setting is associated to operating system rather than computer system since there can be one or more operating systems installed on the machine, each with its own autochk settings.</span></span>

<span data-ttu-id="e64e6-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e64e6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e64e6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e64e6-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32a"), AMENDMENT]
class Win32_OperatingSystemAutochkSetting : CIM_ElementSetting
{
  Win32_OperatingSystem REF Element;
  Win32_AutochkSetting  REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="e64e6-107">Member</span><span class="sxs-lookup"><span data-stu-id="e64e6-107">Members</span></span>

<span data-ttu-id="e64e6-108">Die **Win32 \_ operatingsystemautochksetting** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e64e6-108">The **Win32\_OperatingSystemAutochkSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="e64e6-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e64e6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e64e6-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e64e6-110">Properties</span></span>

<span data-ttu-id="e64e6-111">Die **Win32 \_ operatingsystemautochksetting** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e64e6-111">The **Win32\_OperatingSystemAutochkSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e64e6-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="e64e6-112">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e64e6-113">Datentyp: **Win32- \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="e64e6-113">Data type: **Win32\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="e64e6-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e64e6-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e64e6-115">Qualifizierer: [**override**](../wmisdk/standard-qualifiers.md) ("Element"), [**Schlüssel**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="e64e6-115">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="e64e6-116">TBD</span><span class="sxs-lookup"><span data-stu-id="e64e6-116">TBD</span></span>

</dd> <dt>

<span data-ttu-id="e64e6-117">**Einstellung**</span><span class="sxs-lookup"><span data-stu-id="e64e6-117">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e64e6-118">Datentyp: **Win32 \_ autochksetting**</span><span class="sxs-lookup"><span data-stu-id="e64e6-118">Data type: **Win32\_AutochkSetting**</span></span>
</dt> <dt>

<span data-ttu-id="e64e6-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e64e6-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e64e6-120">Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("Setting"), [**Key**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="e64e6-120">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="e64e6-121">TBD</span><span class="sxs-lookup"><span data-stu-id="e64e6-121">TBD</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e64e6-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e64e6-122">Requirements</span></span>



| <span data-ttu-id="e64e6-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e64e6-123">Requirement</span></span> | <span data-ttu-id="e64e6-124">Wert</span><span class="sxs-lookup"><span data-stu-id="e64e6-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e64e6-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e64e6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e64e6-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e64e6-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e64e6-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e64e6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e64e6-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e64e6-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e64e6-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="e64e6-129">Namespace</span></span><br/>                | <span data-ttu-id="e64e6-130">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e64e6-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e64e6-131">MOF</span><span class="sxs-lookup"><span data-stu-id="e64e6-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e64e6-132"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e64e6-132"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e64e6-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e64e6-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e64e6-134"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e64e6-134"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e64e6-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e64e6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e64e6-136">**CIM- \_ Element Setting**</span><span class="sxs-lookup"><span data-stu-id="e64e6-136">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> </dl>

 

 
