---
description: Diese Klasse ist die Ereignistyp Klasse für das Laden von Bildern in Auslagerungs Datei Ereignissen. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 7d2f08e8-ec1f-4630-922a-548b55eadfda
title: PageFault_ImageLoadBacked-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_ImageLoadBacked
- PageFault_ImageLoadBacked.FileObject
- PageFault_ImageLoadBacked.DeviceChar
- PageFault_ImageLoadBacked.FileChar
- PageFault_ImageLoadBacked.LoadFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1644db74c5c7c361acda796219ae1415ecc262bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980088"
---
# <a name="pagefault_imageloadbacked-class"></a><span data-ttu-id="14496-104">Pagefault \_ imageloadbackup-Klasse</span><span class="sxs-lookup"><span data-stu-id="14496-104">PageFault\_ImageLoadBacked class</span></span>

<span data-ttu-id="14496-105">Diese Klasse ist die Ereignistyp Klasse für das Laden von Bildern in Auslagerungs Datei Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="14496-105">This class is the event type class for image load in page file events.</span></span>

<span data-ttu-id="14496-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="14496-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="14496-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="14496-107">Syntax</span></span>

``` syntax
[EventType{105}, EventTypeName{"ImageLoadBacked"}]
class PageFault_ImageLoadBacked : PageFault_V2
{
  uint32 FileObject;
  uint32 DeviceChar;
  uint16 FileChar;
  uint16 LoadFlags;
};
```

## <a name="members"></a><span data-ttu-id="14496-108">Member</span><span class="sxs-lookup"><span data-stu-id="14496-108">Members</span></span>

<span data-ttu-id="14496-109">Die **Pagefault \_ imageloadbackup** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="14496-109">The **PageFault\_ImageLoadBacked** class has these types of members:</span></span>

-   [<span data-ttu-id="14496-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="14496-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="14496-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="14496-111">Properties</span></span>

<span data-ttu-id="14496-112">Die **Pagefault \_ imageloadbackup** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="14496-112">The **PageFault\_ImageLoadBacked** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="14496-113">**Devicechar**</span><span class="sxs-lookup"><span data-stu-id="14496-113">**DeviceChar**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14496-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14496-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14496-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="14496-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14496-116">Qualifizierer: wmidataid (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="14496-116">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="14496-117">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="14496-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="14496-118">**Filechar**</span><span class="sxs-lookup"><span data-stu-id="14496-118">**FileChar**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14496-119">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="14496-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="14496-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="14496-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14496-121">Qualifizierer: wmidataid (3), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="14496-121">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="14496-122">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="14496-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="14496-123">**File Object**</span><span class="sxs-lookup"><span data-stu-id="14496-123">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14496-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14496-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14496-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="14496-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14496-126">Qualifizierer: wmidataid (1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="14496-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="14496-127">Vergleichen Sie den Wert dieses Zeigers mit dem **FileObject** -Zeiger Wert in einem [**FileIO- \_ namens**](fileio-name.md) Ereignis, um den Namen der Datei zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="14496-127">Match the value of this pointer to the **FileObject** pointer value in a [**FileIo\_Name**](fileio-name.md) event to determine the name of the file.</span></span>

</dd> <dt>

<span data-ttu-id="14496-128">**Loadflags**</span><span class="sxs-lookup"><span data-stu-id="14496-128">**LoadFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14496-129">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="14496-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="14496-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="14496-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14496-131">Qualifizierer: wmidataid (4), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="14496-131">Qualifiers: WmiDataId(4), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="14496-132">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="14496-132">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="14496-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14496-133">Remarks</span></span>

<span data-ttu-id="14496-134">Das Ereignis wird während der Erstellung eines Bild Abschnitts (z. b. beim Laden einer DLL) protokolliert, wenn der Speicher-Manager feststellt, dass das Image in die Auslagerungs Datei kopiert und aus dieser ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="14496-134">The event is logged during an image section creation (for example, a DLL load) when the memory manager determines that the image needs to be copied into and run from the page file.</span></span> <span data-ttu-id="14496-135">In der Regel werden Bilder aus der Quelldatei ausgeführt, aber eine Auslagerungs Datei kann auftreten, wenn der Speicher-Manager feststellt, dass die Quelldatei asynchron durch vorhandene Writer geändert werden kann oder wenn sich die Quelldatei auf einem Wechselmedium oder einem Remote Gerät befindet.</span><span class="sxs-lookup"><span data-stu-id="14496-135">Typically, images are run from the source file but pagefile-backing can occur when the memory manager determines that the source file may be modified asynchronously by existing writers or when the source file is on a removable media or a remote device.</span></span>

## <a name="requirements"></a><span data-ttu-id="14496-136">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="14496-136">Requirements</span></span>



| <span data-ttu-id="14496-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14496-137">Requirement</span></span> | <span data-ttu-id="14496-138">Wert</span><span class="sxs-lookup"><span data-stu-id="14496-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="14496-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="14496-139">Minimum supported client</span></span><br/> | <span data-ttu-id="14496-140">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="14496-140">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="14496-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="14496-141">Minimum supported server</span></span><br/> | <span data-ttu-id="14496-142">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="14496-142">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="14496-143">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="14496-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14496-144">**Pagefault \_ v2**</span><span class="sxs-lookup"><span data-stu-id="14496-144">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




