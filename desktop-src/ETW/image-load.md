---
description: Diese Klasse ist die Ereignistyp Klasse für Bild Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 70ec0542-16d3-4186-a346-7f3c44dedf67
title: Image_Load-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_Load
- Image_Load.ImageBase
- Image_Load.ImageSize
- Image_Load.ProcessId
- Image_Load.ImageCheckSum
- Image_Load.TimeDateStamp
- Image_Load.Reserved0
- Image_Load.DefaultBase
- Image_Load.Reserved1
- Image_Load.Reserved2
- Image_Load.Reserved3
- Image_Load.Reserved4
- Image_Load.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 647879b972c7cff2c086f656f76fa8decedb49a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528652"
---
# <a name="image_load-class"></a><span data-ttu-id="e8355-104">Image- \_ Lade Klasse</span><span class="sxs-lookup"><span data-stu-id="e8355-104">Image\_Load class</span></span>

<span data-ttu-id="e8355-105">Diese Klasse ist die Ereignistyp Klasse für Bild Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="e8355-105">This class is the event type class for image events.</span></span>

<span data-ttu-id="e8355-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="e8355-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8355-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8355-107">Syntax</span></span>

``` syntax
[EventType(10, 2, 3, 4), EventTypeName("Load", "Unload", "DCStart", "DCEnd")]
class Image_Load : Image
{
  uint32 ImageBase;
  uint32 ImageSize;
  uint32 ProcessId;
  uint32 ImageCheckSum;
  uint32 TimeDateStamp;
  uint32 Reserved0;
  uint32 DefaultBase;
  uint32 Reserved1;
  uint32 Reserved2;
  uint32 Reserved3;
  uint32 Reserved4;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="e8355-108">Member</span><span class="sxs-lookup"><span data-stu-id="e8355-108">Members</span></span>

<span data-ttu-id="e8355-109">Die **Bild \_ Lade** Klasse verfügt über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e8355-109">The **Image\_Load** class has these types of members:</span></span>

-   [<span data-ttu-id="e8355-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e8355-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e8355-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e8355-111">Properties</span></span>

<span data-ttu-id="e8355-112">Die **Bild \_ Lade** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e8355-112">The **Image\_Load** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e8355-113">DEFAULTBASE</span><span class="sxs-lookup"><span data-stu-id="e8355-113">DefaultBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8355-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e8355-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e8355-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e8355-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8355-116">Qualifizierer: wmidataid (7), Zeiger</span><span class="sxs-lookup"><span data-stu-id="e8355-116">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="e8355-117">Standardbasis Adresse.</span><span class="sxs-lookup"><span data-stu-id="e8355-117">Default base address.</span></span>

</dd> <dt>

<span data-ttu-id="e8355-118">FileName</span><span class="sxs-lookup"><span data-stu-id="e8355-118">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8355-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e8355-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8355-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e8355-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8355-121">Qualifizierer: wmidataid (12), stringbeendigung ("nullterminiert"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="e8355-121">Qualifiers: WmiDataId(12), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="e8355-122">Dateiname und Erweiterung der DLL oder des ausführbaren Images.</span><span class="sxs-lookup"><span data-stu-id="e8355-122">File name and extension of the DLL or executable image.</span></span>

</dd> <dt>

<span data-ttu-id="e8355-123">ImageBase</span><span class="sxs-lookup"><span data-stu-id="e8355-123">ImageBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8355-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e8355-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e8355-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e8355-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8355-126">Qualifizierer: wmidataid (1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="e8355-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="e8355-127">Die Basisadresse der Anwendung, in der das Image geladen wird.</span><span class="sxs-lookup"><span data-stu-id="e8355-127">Base address of the application in which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="e8355-128">Imagechecksum</span><span class="sxs-lookup"><span data-stu-id="e8355-128">ImageCheckSum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8355-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e8355-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e8355-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e8355-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8355-131">Qualifizierer: wmidataid (4)</span><span class="sxs-lookup"><span data-stu-id="e8355-131">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="e8355-132">Abbild-Prüfsumme.</span><span class="sxs-lookup"><span data-stu-id="e8355-132">Image check sum.</span></span>

</dd> <dt>

<span data-ttu-id="e8355-133">ImageSize</span><span class="sxs-lookup"><span data-stu-id="e8355-133">ImageSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8355-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e8355-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e8355-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e8355-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8355-136">Qualifizierer: wmidataid (2), Zeiger</span><span class="sxs-lookup"><span data-stu-id="e8355-136">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="e8355-137">Größe des geladenen Bilds.</span><span class="sxs-lookup"><span data-stu-id="e8355-137">Size of the image being loaded.</span></span>

<span data-ttu-id="e8355-138">Wenn diese Eigenschaft genutzt wird, ist die Größe des Datentyps für diese Eigenschaft tatsächlich " \_ t".</span><span class="sxs-lookup"><span data-stu-id="e8355-138">When consuming this property, the data type for this property is actually size\_t.</span></span> <span data-ttu-id="e8355-139">Der Zeiger Qualifizierer wird verwendet, um zu bestimmen, ob die Größe \_ t 4 Bytes oder 8 Bytes beträgt.</span><span class="sxs-lookup"><span data-stu-id="e8355-139">The Pointer qualifier is used to determine if the size\_t is 4-bytes or 8-bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e8355-140">ProcessId</span><span class="sxs-lookup"><span data-stu-id="e8355-140">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8355-141">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e8355-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e8355-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e8355-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8355-143">Qualifizierer: wmidataid (3)</span><span class="sxs-lookup"><span data-stu-id="e8355-143">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="e8355-144">Identifiziert den Prozess, in den das Bild geladen wird.</span><span class="sxs-lookup"><span data-stu-id="e8355-144">Identifies the process into which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="e8355-145">Reserved0</span><span class="sxs-lookup"><span data-stu-id="e8355-145">Reserved0</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8355-146">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e8355-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e8355-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e8355-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8355-148">Qualifizierer: wmidataid (6)</span><span class="sxs-lookup"><span data-stu-id="e8355-148">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="e8355-149">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="e8355-149">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="e8355-150">Reserved1</span><span class="sxs-lookup"><span data-stu-id="e8355-150">Reserved1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8355-151">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e8355-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e8355-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e8355-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8355-153">Qualifizierer: wmidataid (8)</span><span class="sxs-lookup"><span data-stu-id="e8355-153">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="e8355-154">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="e8355-154">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="e8355-155">Reserved2</span><span class="sxs-lookup"><span data-stu-id="e8355-155">Reserved2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8355-156">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e8355-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e8355-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e8355-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8355-158">Qualifizierer: wmidataid (9)</span><span class="sxs-lookup"><span data-stu-id="e8355-158">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="e8355-159">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="e8355-159">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="e8355-160">"Reserved3"</span><span class="sxs-lookup"><span data-stu-id="e8355-160">Reserved3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8355-161">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e8355-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e8355-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e8355-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8355-163">Qualifizierer: wmidataid (10)</span><span class="sxs-lookup"><span data-stu-id="e8355-163">Qualifiers: WmiDataId(10)</span></span>
</dt> </dl>

<span data-ttu-id="e8355-164">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="e8355-164">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="e8355-165">"Reserved4"</span><span class="sxs-lookup"><span data-stu-id="e8355-165">Reserved4</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8355-166">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e8355-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e8355-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e8355-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8355-168">Qualifizierer: wmidataid (11)</span><span class="sxs-lookup"><span data-stu-id="e8355-168">Qualifiers: WmiDataId(11)</span></span>
</dt> </dl>

<span data-ttu-id="e8355-169">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="e8355-169">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="e8355-170">TimeDateStamp</span><span class="sxs-lookup"><span data-stu-id="e8355-170">TimeDateStamp</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8355-171">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e8355-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e8355-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e8355-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8355-173">Qualifizierer: wmidataid (5)</span><span class="sxs-lookup"><span data-stu-id="e8355-173">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="e8355-174">Uhrzeit und Datum, zu der das Bild geladen oder entladen wurde.</span><span class="sxs-lookup"><span data-stu-id="e8355-174">Time and date that the image was loaded or unloaded.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e8355-175">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8355-175">Remarks</span></span>

<span data-ttu-id="e8355-176">Mit den Ereignissen DCStart und DCEnd werden alle geladenen Bilder am Anfang bzw. Ende der Ablauf Verfolgung aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e8355-176">The DCStart and DCEnd events enumerate all loaded images at the beginning and end of the trace, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8355-177">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e8355-177">Requirements</span></span>



| <span data-ttu-id="e8355-178">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8355-178">Requirement</span></span> | <span data-ttu-id="e8355-179">Wert</span><span class="sxs-lookup"><span data-stu-id="e8355-179">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e8355-180">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e8355-180">Minimum supported client</span></span><br/> | <span data-ttu-id="e8355-181">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8355-181">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e8355-182">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e8355-182">Minimum supported server</span></span><br/> | <span data-ttu-id="e8355-183">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8355-183">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e8355-184">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e8355-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8355-185">**Image**</span><span class="sxs-lookup"><span data-stu-id="e8355-185">**Image**</span></span>](image.md)
</dt> <dt>

[<span data-ttu-id="e8355-186">**Bild \_ v0**</span><span class="sxs-lookup"><span data-stu-id="e8355-186">**Image\_V0**</span></span>](image-v0.md)
</dt> <dt>

[<span data-ttu-id="e8355-187">**Bild \_ v1**</span><span class="sxs-lookup"><span data-stu-id="e8355-187">**Image\_V1**</span></span>](image-v1.md)
</dt> </dl>

 

 




