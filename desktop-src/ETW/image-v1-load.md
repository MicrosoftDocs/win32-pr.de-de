---
description: 'Image_V1_Load-Klasse: Diese Klasse ist die Ereignistypklasse für Bildladeereignisse. Die folgende Syntax wird aus MOF-Code vereinfacht.'
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
ms.openlocfilehash: 2e8a8c31cee7e45311887c16a1d10545e6a38e41
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106498"
---
# <a name="image_v1_load-class"></a><span data-ttu-id="d0ef0-104">Image \_ V1 \_ Load-Klasse</span><span class="sxs-lookup"><span data-stu-id="d0ef0-104">Image\_V1\_Load class</span></span>

<span data-ttu-id="d0ef0-105">Diese Klasse ist die Ereignistypklasse für Bildladeereignisse.</span><span class="sxs-lookup"><span data-stu-id="d0ef0-105">This class is the event type class for image load events.</span></span>

<span data-ttu-id="d0ef0-106">Die folgende Syntax wird aus MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="d0ef0-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0ef0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0ef0-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="d0ef0-108">Member</span><span class="sxs-lookup"><span data-stu-id="d0ef0-108">Members</span></span>

<span data-ttu-id="d0ef0-109">Die **Image \_ V1 \_ Load-Klasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d0ef0-109">The **Image\_V1\_Load** class has these types of members:</span></span>

-   [<span data-ttu-id="d0ef0-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d0ef0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d0ef0-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d0ef0-111">Properties</span></span>

<span data-ttu-id="d0ef0-112">Die **Image \_ V1 \_ Load-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d0ef0-112">The **Image\_V1\_Load** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d0ef0-113">FileName</span><span class="sxs-lookup"><span data-stu-id="d0ef0-113">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0ef0-114">Datentyp: **String**</span><span class="sxs-lookup"><span data-stu-id="d0ef0-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0ef0-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d0ef0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0ef0-116">Qualifizierer: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span><span class="sxs-lookup"><span data-stu-id="d0ef0-116">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="d0ef0-117">Dateiname und Erweiterung der zu ladende DLL oder des ausführbaren Images.</span><span class="sxs-lookup"><span data-stu-id="d0ef0-117">File name and extension of the DLL or executable image to load.</span></span>

</dd> <dt>

<span data-ttu-id="d0ef0-118">Imagebase</span><span class="sxs-lookup"><span data-stu-id="d0ef0-118">ImageBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0ef0-119">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="d0ef0-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d0ef0-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d0ef0-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0ef0-121">Qualifizierer: WmiDataId(1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="d0ef0-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="d0ef0-122">Basisadresse der Anwendung, in die das Image geladen wird.</span><span class="sxs-lookup"><span data-stu-id="d0ef0-122">Base address of the application in which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="d0ef0-123">Imagesize</span><span class="sxs-lookup"><span data-stu-id="d0ef0-123">ImageSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0ef0-124">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="d0ef0-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d0ef0-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d0ef0-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0ef0-126">Qualifizierer: WmiDataId(2), Zeiger</span><span class="sxs-lookup"><span data-stu-id="d0ef0-126">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="d0ef0-127">Größe des geladenen Images.</span><span class="sxs-lookup"><span data-stu-id="d0ef0-127">Size of the image being loaded.</span></span>

<span data-ttu-id="d0ef0-128">Beim Verwenden dieser Eigenschaft ist der Datentyp für diese Eigenschaft tatsächlich die Größe \_ t.</span><span class="sxs-lookup"><span data-stu-id="d0ef0-128">When consuming this property, the data type for this property is actually size\_t.</span></span> <span data-ttu-id="d0ef0-129">Der Zeigerqualifizierer wird verwendet, um zu bestimmen, ob die Größe \_ t 4 Byte oder 8 Bytes beträgt.</span><span class="sxs-lookup"><span data-stu-id="d0ef0-129">The Pointer qualifier is used to determine if the size\_t is 4-bytes or 8-bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d0ef0-130">ProcessId</span><span class="sxs-lookup"><span data-stu-id="d0ef0-130">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0ef0-131">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="d0ef0-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d0ef0-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d0ef0-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0ef0-133">Qualifizierer: WmiDataId(3)</span><span class="sxs-lookup"><span data-stu-id="d0ef0-133">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="d0ef0-134">Identifiziert den Prozess, in den das Image geladen wird.</span><span class="sxs-lookup"><span data-stu-id="d0ef0-134">Identifies the process into which the image is loaded.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d0ef0-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0ef0-135">Requirements</span></span>



| <span data-ttu-id="d0ef0-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0ef0-136">Requirement</span></span> | <span data-ttu-id="d0ef0-137">Wert</span><span class="sxs-lookup"><span data-stu-id="d0ef0-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d0ef0-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d0ef0-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d0ef0-139">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d0ef0-139">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="d0ef0-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d0ef0-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d0ef0-141">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d0ef0-141">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d0ef0-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d0ef0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0ef0-143">**Image \_ V1**</span><span class="sxs-lookup"><span data-stu-id="d0ef0-143">**Image\_V1**</span></span>](image-v1.md)
</dt> </dl>

 

 




