---
description: 'Image_V0_Load Klasse: Diese Klasse ist die Ereignistypklasse für Bildladeereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
ms.assetid: e2836153-8e4f-4c7f-9542-9402ed9e4356
title: Image_V0_Load-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_V0_Load
- Image_V0_Load.BaseAddress
- Image_V0_Load.ModuleSize
- Image_V0_Load.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: ed15254ac509334c802ba4c6165c73e681a2c7b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106512"
---
# <a name="image_v0_load-class"></a><span data-ttu-id="c9dae-104">Image \_ V0 \_ Load-Klasse</span><span class="sxs-lookup"><span data-stu-id="c9dae-104">Image\_V0\_Load class</span></span>

<span data-ttu-id="c9dae-105">Diese Klasse ist die Ereignistypklasse für Bildladeereignisse.</span><span class="sxs-lookup"><span data-stu-id="c9dae-105">This class is the event type class for image load events.</span></span>

<span data-ttu-id="c9dae-106">Die folgende Syntax wird durch MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="c9dae-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9dae-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9dae-107">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V0_Load
{
  uint32 BaseAddress;
  uint32 ModuleSize;
  string ImageFileName;
};
```

## <a name="members"></a><span data-ttu-id="c9dae-108">Member</span><span class="sxs-lookup"><span data-stu-id="c9dae-108">Members</span></span>

<span data-ttu-id="c9dae-109">Die **Image \_ V0 \_ Load-Klasse** verfügt über die folgenden Membertypen:</span><span class="sxs-lookup"><span data-stu-id="c9dae-109">The **Image\_V0\_Load** class has these types of members:</span></span>

-   [<span data-ttu-id="c9dae-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c9dae-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c9dae-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c9dae-111">Properties</span></span>

<span data-ttu-id="c9dae-112">Die **Image \_ V0 \_ Load-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c9dae-112">The **Image\_V0\_Load** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c9dae-113">BaseAddress</span><span class="sxs-lookup"><span data-stu-id="c9dae-113">BaseAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9dae-114">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="c9dae-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9dae-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c9dae-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9dae-116">Qualifizierer: WmiDataId(1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="c9dae-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c9dae-117">Basisadresse der Anwendung, in die das Image geladen wird.</span><span class="sxs-lookup"><span data-stu-id="c9dae-117">Base address of the application in which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="c9dae-118">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="c9dae-118">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9dae-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c9dae-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9dae-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c9dae-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9dae-121">Qualifizierer: WmiDataId(3), StringTermination("NullTerminated"), Format("w")</span><span class="sxs-lookup"><span data-stu-id="c9dae-121">Qualifiers: WmiDataId(3), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="c9dae-122">Dateiname und Erweiterung der zu ladenden DLL oder des ausführbaren Images.</span><span class="sxs-lookup"><span data-stu-id="c9dae-122">File name and extension of the DLL or executable image to load.</span></span>

</dd> <dt>

<span data-ttu-id="c9dae-123">ModuleSize</span><span class="sxs-lookup"><span data-stu-id="c9dae-123">ModuleSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9dae-124">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="c9dae-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9dae-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c9dae-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9dae-126">Qualifizierer: WmiDataId(2)</span><span class="sxs-lookup"><span data-stu-id="c9dae-126">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="c9dae-127">Größe des Bilds.</span><span class="sxs-lookup"><span data-stu-id="c9dae-127">Size of the image.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9dae-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9dae-128">Requirements</span></span>



| <span data-ttu-id="c9dae-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9dae-129">Requirement</span></span> | <span data-ttu-id="c9dae-130">Wert</span><span class="sxs-lookup"><span data-stu-id="c9dae-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c9dae-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c9dae-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c9dae-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9dae-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c9dae-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c9dae-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c9dae-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9dae-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c9dae-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c9dae-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9dae-136">**Image \_ V0**</span><span class="sxs-lookup"><span data-stu-id="c9dae-136">**Image\_V0**</span></span>](image-v0.md)
</dt> </dl>

 

 




