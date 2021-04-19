---
description: Die CIM- \_ videosetting-Klasse ordnet das CIM \_ videocontrollerresolution-Einstellungs Objekt dem Controller zu, auf den es angewendet wird.
ms.assetid: 1f6742ad-ab92-4723-b691-0c3e6c0d82fa
ms.tgt_platform: multiple
title: CIM_VideoSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoSetting
- CIM_VideoSetting.Setting
- CIM_VideoSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a37fe8dd03738ae93f391a754caca84564dc6f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343200"
---
# <a name="cim_videosetting-class"></a><span data-ttu-id="90ca5-103">CIM- \_ videosetting-Klasse</span><span class="sxs-lookup"><span data-stu-id="90ca5-103">CIM\_VideoSetting class</span></span>

<span data-ttu-id="90ca5-104">Die **CIM- \_ videosetting** -Klasse ordnet das [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md) -Einstellungs Objekt dem Controller zu, auf den es angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="90ca5-104">The **CIM\_VideoSetting** class associates the [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) setting object with the controller to which it applies.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="90ca5-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="90ca5-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="90ca5-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="90ca5-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="90ca5-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="90ca5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="90ca5-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="90ca5-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="90ca5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="90ca5-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCEB-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_VideoSetting : CIM_ElementSetting
{
  CIM_VideoControllerResolution REF Setting;
  CIM_VideoController           REF Element;
};
```

## <a name="members"></a><span data-ttu-id="90ca5-110">Member</span><span class="sxs-lookup"><span data-stu-id="90ca5-110">Members</span></span>

<span data-ttu-id="90ca5-111">Die **CIM- \_ videosetting** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="90ca5-111">The **CIM\_VideoSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="90ca5-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="90ca5-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="90ca5-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="90ca5-113">Properties</span></span>

<span data-ttu-id="90ca5-114">Die **CIM- \_ videosetting** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="90ca5-114">The **CIM\_VideoSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="90ca5-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="90ca5-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90ca5-116">Datentyp: **CIM \_ Videocontroller**</span><span class="sxs-lookup"><span data-stu-id="90ca5-116">Data type: **CIM\_VideoController**</span></span>
</dt> <dt>

<span data-ttu-id="90ca5-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90ca5-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90ca5-118">Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element")</span><span class="sxs-lookup"><span data-stu-id="90ca5-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element")</span></span>
</dt> </dl>

<span data-ttu-id="90ca5-119">Ein [**CIM- \_ Videocontroller**](cim-videocontroller.md) , der den Videocontroller beschreibt.</span><span class="sxs-lookup"><span data-stu-id="90ca5-119">A [**CIM\_VideoController**](cim-videocontroller.md) that describes the video controller.</span></span>

</dd> <dt>

<span data-ttu-id="90ca5-120">**Einstellung**</span><span class="sxs-lookup"><span data-stu-id="90ca5-120">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90ca5-121">Datentyp: **CIM \_ videocontrollerresolution**</span><span class="sxs-lookup"><span data-stu-id="90ca5-121">Data type: **CIM\_VideoControllerResolution**</span></span>
</dt> <dt>

<span data-ttu-id="90ca5-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90ca5-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90ca5-123">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Setting")</span><span class="sxs-lookup"><span data-stu-id="90ca5-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting")</span></span>
</dt> </dl>

<span data-ttu-id="90ca5-124">Eine [**CIM- \_ videocontrollerresolution**](cim-videocontrollerresolution.md) , in der die Auflösungen, Aktualisierungs Raten, der Überprüfungs Modus und die Anzahl der Farben beschrieben werden, die für den Controller festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="90ca5-124">A [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) that describes the resolutions, refresh rates, scan mode and number of colors that can be set for the Controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90ca5-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90ca5-125">Remarks</span></span>

<span data-ttu-id="90ca5-126">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="90ca5-126">WMI does not implement this class.</span></span> <span data-ttu-id="90ca5-127">Informationen zu WMI-Klassen, die von **CIM \_ videosetting** abgeleitet sind, finden Sie unter [Win32](win32-provider.md)</span><span class="sxs-lookup"><span data-stu-id="90ca5-127">For WMI classes derived from **CIM\_VideoSetting**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="90ca5-128">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="90ca5-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="90ca5-129">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="90ca5-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="90ca5-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90ca5-130">Requirements</span></span>



| <span data-ttu-id="90ca5-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90ca5-131">Requirement</span></span> | <span data-ttu-id="90ca5-132">Wert</span><span class="sxs-lookup"><span data-stu-id="90ca5-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90ca5-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="90ca5-133">Minimum supported client</span></span><br/> | <span data-ttu-id="90ca5-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="90ca5-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="90ca5-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="90ca5-135">Minimum supported server</span></span><br/> | <span data-ttu-id="90ca5-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90ca5-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="90ca5-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="90ca5-137">Namespace</span></span><br/>                | <span data-ttu-id="90ca5-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="90ca5-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="90ca5-139">MOF</span><span class="sxs-lookup"><span data-stu-id="90ca5-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90ca5-140"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="90ca5-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="90ca5-141">DLL</span><span class="sxs-lookup"><span data-stu-id="90ca5-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90ca5-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90ca5-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90ca5-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90ca5-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90ca5-144">**CIM- \_ Element Setting**</span><span class="sxs-lookup"><span data-stu-id="90ca5-144">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> </dl>

 

