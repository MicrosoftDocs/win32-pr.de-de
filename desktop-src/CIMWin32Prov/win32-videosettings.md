---
description: Die \_ WMI-Klasse "Win32 videosettings Association" bezieht sich auf einen Videocontroller und Videoeinstellungen, die darauf angewendet werden können.
ms.assetid: 0cc42352-0a89-434d-a8b6-230c677de49c
ms.tgt_platform: multiple
title: Win32_VideoSettings-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoSettings
- Win32_VideoSettings.Setting
- Win32_VideoSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 38e949b6b6501dc51b39448d72e6bf61f37fbecb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343588"
---
# <a name="win32_videosettings-class"></a><span data-ttu-id="6c1cc-103">Win32 \_ videosettings-Klasse</span><span class="sxs-lookup"><span data-stu-id="6c1cc-103">Win32\_VideoSettings class</span></span>

<span data-ttu-id="6c1cc-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ videosettings** Association" bezieht sich auf einen Videocontroller und Videoeinstellungen, die darauf angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="6c1cc-104">The **Win32\_VideoSettings** association [WMI class](../wmisdk/retrieving-a-class.md) relates a video controller and video settings that can be applied to it.</span></span>

<span data-ttu-id="6c1cc-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6c1cc-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6c1cc-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6c1cc-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c1cc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c1cc-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCEE-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class Win32_VideoSettings : CIM_VideoSetting
{
  CIM_VideoControllerResolution REF Setting;
  Win32_VideoController         REF Element;
};
```

## <a name="members"></a><span data-ttu-id="6c1cc-108">Member</span><span class="sxs-lookup"><span data-stu-id="6c1cc-108">Members</span></span>

<span data-ttu-id="6c1cc-109">Die **Win32- \_ videosettings** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6c1cc-109">The **Win32\_VideoSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="6c1cc-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6c1cc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6c1cc-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6c1cc-111">Properties</span></span>

<span data-ttu-id="6c1cc-112">Die **Win32 \_ Video Settings** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6c1cc-112">The **Win32\_VideoSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6c1cc-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6c1cc-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c1cc-114">Datentyp: **Win32 \_ Videocontroller**</span><span class="sxs-lookup"><span data-stu-id="6c1cc-114">Data type: **Win32\_VideoController**</span></span>
</dt> <dt>

<span data-ttu-id="6c1cc-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c1cc-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c1cc-116">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Element"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Videocontroller")</span><span class="sxs-lookup"><span data-stu-id="6c1cc-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_VideoController")</span></span>
</dt> </dl>

<span data-ttu-id="6c1cc-117">Ein [**Win32- \_ Videocontroller**](win32-videocontroller.md) , der die Eigenschaften des Video Controllers enthält, in dem eine Video Einstellung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6c1cc-117">A [**Win32\_VideoController**](win32-videocontroller.md) containing the properties of the video controller that a video setting can be used on.</span></span>

</dd> <dt>

<span data-ttu-id="6c1cc-118">**Einstellung**</span><span class="sxs-lookup"><span data-stu-id="6c1cc-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c1cc-119">Datentyp: **CIM \_ videocontrollerresolution**</span><span class="sxs-lookup"><span data-stu-id="6c1cc-119">Data type: **CIM\_VideoControllerResolution**</span></span>
</dt> <dt>

<span data-ttu-id="6c1cc-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c1cc-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c1cc-121">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ videocontrollerresolution")</span><span class="sxs-lookup"><span data-stu-id="6c1cc-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_VideoControllerResolution")</span></span>
</dt> </dl>

<span data-ttu-id="6c1cc-122">Eine [**CIM- \_ videocontrollerresolution**](cim-videocontrollerresolution.md) mit Einstellungen, die auf den Videocontroller angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="6c1cc-122">A [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) containing settings that can be applied to the video controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c1cc-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c1cc-123">Remarks</span></span>

<span data-ttu-id="6c1cc-124">Die **Win32 \_ Video Settings** -Klasse wird von [**CIM \_ videosetting**](cim-videosetting.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="6c1cc-124">The **Win32\_VideoSettings** class is derived from [**CIM\_VideoSetting**](cim-videosetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6c1cc-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c1cc-125">Requirements</span></span>



| <span data-ttu-id="6c1cc-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c1cc-126">Requirement</span></span> | <span data-ttu-id="6c1cc-127">Wert</span><span class="sxs-lookup"><span data-stu-id="6c1cc-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c1cc-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c1cc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6c1cc-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c1cc-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6c1cc-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c1cc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6c1cc-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c1cc-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6c1cc-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="6c1cc-132">Namespace</span></span><br/>                | <span data-ttu-id="6c1cc-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6c1cc-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6c1cc-134">MOF</span><span class="sxs-lookup"><span data-stu-id="6c1cc-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c1cc-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6c1cc-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c1cc-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6c1cc-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c1cc-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c1cc-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c1cc-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c1cc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c1cc-139">**CIM- \_ videosetting**</span><span class="sxs-lookup"><span data-stu-id="6c1cc-139">**CIM\_VideoSetting**</span></span>](cim-videosetting.md)
</dt> <dt>

[<span data-ttu-id="6c1cc-140">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="6c1cc-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
