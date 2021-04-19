---
description: Stellt ein DVD-Laufwerk dar.
ms.assetid: 6127b58d-c70f-47c7-9eeb-6aff819f672e
title: CIM_DVDDrive-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DVDDrive
- CIM_DVDDrive.FormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 44c69cfe537257076623e472f4bb1406f8bf7665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348457"
---
# <a name="cim_dvddrive-class"></a><span data-ttu-id="050aa-103">CIM \_ dvddrive-Klasse</span><span class="sxs-lookup"><span data-stu-id="050aa-103">CIM\_DVDDrive class</span></span>

<span data-ttu-id="050aa-104">Stellt ein DVD-Laufwerk dar.</span><span class="sxs-lookup"><span data-stu-id="050aa-104">Represents a DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="050aa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="050aa-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageDevices"), AMENDMENT]
class CIM_DVDDrive : CIM_MediaAccessDevice
{
  uint16 FormatsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="050aa-106">Member</span><span class="sxs-lookup"><span data-stu-id="050aa-106">Members</span></span>

<span data-ttu-id="050aa-107">Die **CIM- \_ dvddrive** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="050aa-107">The **CIM\_DVDDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="050aa-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="050aa-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="050aa-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="050aa-109">Properties</span></span>

<span data-ttu-id="050aa-110">Die **CIM- \_ dvddrive** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="050aa-110">The **CIM\_DVDDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="050aa-111">**Formatssupported**</span><span class="sxs-lookup"><span data-stu-id="050aa-111">**FormatsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="050aa-112">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="050aa-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="050aa-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="050aa-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="050aa-114">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ physicalmedia**](/windows/desktop/CIMWin32Prov/cim-physicalmedia)".**MediaType**")</span><span class="sxs-lookup"><span data-stu-id="050aa-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalMedia**](/windows/desktop/CIMWin32Prov/cim-physicalmedia).**MediaType**")</span></span>
</dt> </dl>

<span data-ttu-id="050aa-115">Die vom Gerät unterstützten CD-und DVD-Formate.</span><span class="sxs-lookup"><span data-stu-id="050aa-115">The CD and DVD formats that are supported by the device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="050aa-116">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="050aa-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="050aa-117">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="050aa-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span data-ttu-id="050aa-118">**CD-ROM** (16)</span><span class="sxs-lookup"><span data-stu-id="050aa-118">**CD-ROM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>

<span data-ttu-id="050aa-119">**CD-ROM/XA** (17)</span><span class="sxs-lookup"><span data-stu-id="050aa-119">**CD-ROM/XA** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-I"></span><span id="cd-i"></span>

<span data-ttu-id="050aa-120">**CD-I** (18)</span><span class="sxs-lookup"><span data-stu-id="050aa-120">**CD-I** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>

<span data-ttu-id="050aa-121">**CD-Recordable** (19)</span><span class="sxs-lookup"><span data-stu-id="050aa-121">**CD Recordable** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD"></span><span id="dvd"></span>

<span data-ttu-id="050aa-122">**DVD** (22)</span><span class="sxs-lookup"><span data-stu-id="050aa-122">**DVD** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-RW_"></span><span id="dvd-rw_"></span>

<span data-ttu-id="050aa-123">**DVD-RW +** (23)</span><span class="sxs-lookup"><span data-stu-id="050aa-123">**DVD-RW+** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-RAM"></span><span id="dvd-ram"></span>

<span data-ttu-id="050aa-124">**DVD-RAM** (24)</span><span class="sxs-lookup"><span data-stu-id="050aa-124">**DVD-RAM** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-ROM"></span><span id="dvd-rom"></span>

<span data-ttu-id="050aa-125">**DVD-ROM** (25)</span><span class="sxs-lookup"><span data-stu-id="050aa-125">**DVD-ROM** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>

<span data-ttu-id="050aa-126">**DVD-Video** (26)</span><span class="sxs-lookup"><span data-stu-id="050aa-126">**DVD-Video** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>

<span data-ttu-id="050aa-127">**MPEG** (27)</span><span class="sxs-lookup"><span data-stu-id="050aa-127">**Divx** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-RW"></span><span id="cd-rw"></span>

<span data-ttu-id="050aa-128">**CD-RW** (33)</span><span class="sxs-lookup"><span data-stu-id="050aa-128">**CD-RW** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-DA"></span><span id="cd-da"></span>

<span data-ttu-id="050aa-129">**CD-da** (34)</span><span class="sxs-lookup"><span data-stu-id="050aa-129">**CD-DA** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_"></span><span id="cd_"></span>

<span data-ttu-id="050aa-130">**CD +** (35)</span><span class="sxs-lookup"><span data-stu-id="050aa-130">**CD+** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>

<span data-ttu-id="050aa-131">**DVD-Recordable** (36)</span><span class="sxs-lookup"><span data-stu-id="050aa-131">**DVD Recordable** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-RW"></span><span id="dvd-rw"></span>

<span data-ttu-id="050aa-132">**DVD-RW** (37)</span><span class="sxs-lookup"><span data-stu-id="050aa-132">**DVD-RW** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>

<span data-ttu-id="050aa-133">**DVD-Audiodaten** (38)</span><span class="sxs-lookup"><span data-stu-id="050aa-133">**DVD-Audio** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-5"></span><span id="dvd-5"></span>

<span data-ttu-id="050aa-134">**DVD-5** (39)</span><span class="sxs-lookup"><span data-stu-id="050aa-134">**DVD-5** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-9"></span><span id="dvd-9"></span>

<span data-ttu-id="050aa-135">**DVD-9** (40)</span><span class="sxs-lookup"><span data-stu-id="050aa-135">**DVD-9** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-10"></span><span id="dvd-10"></span>

<span data-ttu-id="050aa-136">**DVD-10** (41)</span><span class="sxs-lookup"><span data-stu-id="050aa-136">**DVD-10** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-18"></span><span id="dvd-18"></span>

<span data-ttu-id="050aa-137">**DVD-18** (42)</span><span class="sxs-lookup"><span data-stu-id="050aa-137">**DVD-18** (42)</span></span>


<span data-ttu-id="050aa-138"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="050aa-138"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="050aa-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="050aa-139">Requirements</span></span>



| <span data-ttu-id="050aa-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="050aa-140">Requirement</span></span> | <span data-ttu-id="050aa-141">Wert</span><span class="sxs-lookup"><span data-stu-id="050aa-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="050aa-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="050aa-142">Minimum supported client</span></span><br/> | <span data-ttu-id="050aa-143">Windows 8</span><span class="sxs-lookup"><span data-stu-id="050aa-143">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="050aa-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="050aa-144">Minimum supported server</span></span><br/> | <span data-ttu-id="050aa-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="050aa-145">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="050aa-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="050aa-146">Namespace</span></span><br/>                | <span data-ttu-id="050aa-147">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="050aa-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="050aa-148">MOF</span><span class="sxs-lookup"><span data-stu-id="050aa-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="050aa-149"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="050aa-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="050aa-150">DLL</span><span class="sxs-lookup"><span data-stu-id="050aa-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="050aa-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="050aa-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="050aa-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="050aa-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="050aa-153">**CIM \_ mediaaccessdevice**</span><span class="sxs-lookup"><span data-stu-id="050aa-153">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

