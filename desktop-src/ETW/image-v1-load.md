---
description: Diese Klasse ist die Ereignistyp Klasse für Bild Lade Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 43bf0b2b-3ab4-4561-b48c-65fbace38a79
title: Image_V1_Load-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_V1_Load
- Image_V1_Load.ImageBase
- Image_V1_Load.ImageSize
- Image_V1_Load.ProcessId
- Image_V1_Load.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: bd0a2a61b263ce78c2cf28cdf1cd5df4b702140d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977120"
---
# <a name="image_v1_load-class"></a><span data-ttu-id="e181d-104">Image \_ v1- \_ Lade Klasse</span><span class="sxs-lookup"><span data-stu-id="e181d-104">Image\_V1\_Load class</span></span>

<span data-ttu-id="e181d-105">Diese Klasse ist die Ereignistyp Klasse für Bild Lade Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="e181d-105">This class is the event type class for image load events.</span></span>

<span data-ttu-id="e181d-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="e181d-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e181d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e181d-107">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V1_Load : Image_V1
{
  uint32 ImageBase;
  uint32 ImageSize;
  uint32 ProcessId;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="e181d-108">Member</span><span class="sxs-lookup"><span data-stu-id="e181d-108">Members</span></span>

<span data-ttu-id="e181d-109">Die **\_ \_ Load** -Klasse von Image v1 verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e181d-109">The **Image\_V1\_Load** class has these types of members:</span></span>

-   [<span data-ttu-id="e181d-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e181d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e181d-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e181d-111">Properties</span></span>

<span data-ttu-id="e181d-112">Die **\_ \_ Load** -Klasse von Image v1 verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e181d-112">The **Image\_V1\_Load** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e181d-113">FileName</span><span class="sxs-lookup"><span data-stu-id="e181d-113">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e181d-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e181d-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e181d-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e181d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e181d-116">Qualifizierer: wmidataid (4), stringbeendigung ("nullterminiert"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="e181d-116">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="e181d-117">Dateiname und Erweiterung der zu ladenden DLL oder des zu ladenden ausführbaren Images.</span><span class="sxs-lookup"><span data-stu-id="e181d-117">File name and extension of the DLL or executable image to load.</span></span>

</dd> <dt>

<span data-ttu-id="e181d-118">ImageBase</span><span class="sxs-lookup"><span data-stu-id="e181d-118">ImageBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e181d-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e181d-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e181d-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e181d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e181d-121">Qualifizierer: wmidataid (1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="e181d-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="e181d-122">Die Basisadresse der Anwendung, in der das Image geladen wird.</span><span class="sxs-lookup"><span data-stu-id="e181d-122">Base address of the application in which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="e181d-123">ImageSize</span><span class="sxs-lookup"><span data-stu-id="e181d-123">ImageSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e181d-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e181d-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e181d-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e181d-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e181d-126">Qualifizierer: wmidataid (2), Zeiger</span><span class="sxs-lookup"><span data-stu-id="e181d-126">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="e181d-127">Größe des geladenen Bilds.</span><span class="sxs-lookup"><span data-stu-id="e181d-127">Size of the image being loaded.</span></span>

<span data-ttu-id="e181d-128">Wenn diese Eigenschaft genutzt wird, ist die Größe des Datentyps für diese Eigenschaft tatsächlich " \_ t".</span><span class="sxs-lookup"><span data-stu-id="e181d-128">When consuming this property, the data type for this property is actually size\_t.</span></span> <span data-ttu-id="e181d-129">Der Zeiger Qualifizierer wird verwendet, um zu bestimmen, ob die Größe \_ t 4 Bytes oder 8 Bytes beträgt.</span><span class="sxs-lookup"><span data-stu-id="e181d-129">The Pointer qualifier is used to determine if the size\_t is 4-bytes or 8-bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e181d-130">ProcessId</span><span class="sxs-lookup"><span data-stu-id="e181d-130">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e181d-131">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e181d-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e181d-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e181d-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e181d-133">Qualifizierer: wmidataid (3)</span><span class="sxs-lookup"><span data-stu-id="e181d-133">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="e181d-134">Identifiziert den Prozess, in den das Bild geladen wird.</span><span class="sxs-lookup"><span data-stu-id="e181d-134">Identifies the process into which the image is loaded.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e181d-135">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e181d-135">Requirements</span></span>



| <span data-ttu-id="e181d-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e181d-136">Requirement</span></span> | <span data-ttu-id="e181d-137">Wert</span><span class="sxs-lookup"><span data-stu-id="e181d-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e181d-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e181d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e181d-139">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e181d-139">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="e181d-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e181d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e181d-141">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e181d-141">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e181d-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e181d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e181d-143">**Bild \_ v1**</span><span class="sxs-lookup"><span data-stu-id="e181d-143">**Image\_V1**</span></span>](image-v1.md)
</dt> </dl>

 

 




