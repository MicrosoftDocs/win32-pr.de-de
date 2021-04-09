---
description: Die \_ WMI-Klasse Win32 userdesktop Association verknüpft ein bestimmtes Benutzerkonto und eigene Desktop Einstellungen.
ms.assetid: 5ea83ad6-bd0a-4c16-85b2-e3e61ef05903
ms.tgt_platform: multiple
title: Win32_UserDesktop-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserDesktop
- Win32_UserDesktop.Element
- Win32_UserDesktop.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 39b45ee7859fea9f1068123041a87309cf40c2d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860823"
---
# <a name="win32_userdesktop-class"></a><span data-ttu-id="6b611-103">Win32 \_ userdesktop-Klasse</span><span class="sxs-lookup"><span data-stu-id="6b611-103">Win32\_UserDesktop class</span></span>

<span data-ttu-id="6b611-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) **Win32 \_ userdesktop** Association verknüpft ein bestimmtes Benutzerkonto und eigene Desktop Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="6b611-104">The **Win32\_UserDesktop** association [WMI class](../wmisdk/retrieving-a-class.md) relates a user account and desktop settings that are specific to it.</span></span>

<span data-ttu-id="6b611-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6b611-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6b611-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="6b611-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b611-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b611-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_UserDesktop : CIM_ElementSetting
{
  Win32_UserAccount REF Element;
  Win32_Desktop     REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="6b611-108">Member</span><span class="sxs-lookup"><span data-stu-id="6b611-108">Members</span></span>

<span data-ttu-id="6b611-109">Die **Win32 \_ userdesktop-** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6b611-109">The **Win32\_UserDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="6b611-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6b611-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6b611-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6b611-111">Properties</span></span>

<span data-ttu-id="6b611-112">Die **Win32 \_ userdesktop-** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6b611-112">The **Win32\_UserDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6b611-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6b611-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b611-114">Datentyp: **Win32- \_ Benutzerkonto**</span><span class="sxs-lookup"><span data-stu-id="6b611-114">Data type: **Win32\_UserAccount**</span></span>
</dt> <dt>

<span data-ttu-id="6b611-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b611-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b611-116">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Element"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ User Account")</span><span class="sxs-lookup"><span data-stu-id="6b611-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_UserAccount")</span></span>
</dt> </dl>

<span data-ttu-id="6b611-117">Verweis auf die-Instanz, die das Benutzerkonto darstellt, dessen Desktop mithilfe der **Settings** -Eigenschaft dieser Klasse angepasst werden kann.</span><span class="sxs-lookup"><span data-stu-id="6b611-117">Reference to the instance representing the user account whose desktop can be customized by the **Settings** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="6b611-118">**Einstellung**</span><span class="sxs-lookup"><span data-stu-id="6b611-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b611-119">Datentyp: **Win32 \_ -Desktop**</span><span class="sxs-lookup"><span data-stu-id="6b611-119">Data type: **Win32\_Desktop**</span></span>
</dt> <dt>

<span data-ttu-id="6b611-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b611-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b611-121">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Desktop")</span><span class="sxs-lookup"><span data-stu-id="6b611-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="6b611-122">Verweis auf die-Instanz, die die Desktop Einstellungen darstellt, die zum Anpassen eines bestimmten Benutzerkonto Desktops dienen.</span><span class="sxs-lookup"><span data-stu-id="6b611-122">Reference to the instance representing the desktop settings that serve to customize a specific user account desktop.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b611-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b611-123">Remarks</span></span>

<span data-ttu-id="6b611-124">Die **Win32 \_ userdesktop-** Klasse wird von [**CIM \_ Element Setting**](cim-elementsetting.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="6b611-124">The **Win32\_UserDesktop** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b611-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b611-125">Requirements</span></span>



| <span data-ttu-id="6b611-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b611-126">Requirement</span></span> | <span data-ttu-id="6b611-127">Wert</span><span class="sxs-lookup"><span data-stu-id="6b611-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b611-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b611-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6b611-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b611-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6b611-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b611-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6b611-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b611-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6b611-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="6b611-132">Namespace</span></span><br/>                | <span data-ttu-id="6b611-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6b611-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6b611-134">MOF</span><span class="sxs-lookup"><span data-stu-id="6b611-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b611-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6b611-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b611-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6b611-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b611-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b611-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b611-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b611-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b611-139">**CIM- \_ Element Setting**</span><span class="sxs-lookup"><span data-stu-id="6b611-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="6b611-140">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="6b611-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
