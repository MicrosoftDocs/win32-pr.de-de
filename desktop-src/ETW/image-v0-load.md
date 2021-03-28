---
description: Diese Klasse ist die Ereignistyp Klasse für Bild Lade Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: b2486e6918884e51a57f077dc9c569f926dc902e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977121"
---
# <a name="image_v0_load-class"></a><span data-ttu-id="d49c9-104">Image \_ v0- \_ Lade Klasse</span><span class="sxs-lookup"><span data-stu-id="d49c9-104">Image\_V0\_Load class</span></span>

<span data-ttu-id="d49c9-105">Diese Klasse ist die Ereignistyp Klasse für Bild Lade Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="d49c9-105">This class is the event type class for image load events.</span></span>

<span data-ttu-id="d49c9-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="d49c9-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d49c9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d49c9-107">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V0_Load
{
  uint32 BaseAddress;
  uint32 ModuleSize;
  string ImageFileName;
};
```

## <a name="members"></a><span data-ttu-id="d49c9-108">Member</span><span class="sxs-lookup"><span data-stu-id="d49c9-108">Members</span></span>

<span data-ttu-id="d49c9-109">Die **\_ \_ Load** -Klasse von Image v0 verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d49c9-109">The **Image\_V0\_Load** class has these types of members:</span></span>

-   [<span data-ttu-id="d49c9-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d49c9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d49c9-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d49c9-111">Properties</span></span>

<span data-ttu-id="d49c9-112">Die **\_ \_ Load** -Klasse von Image v0 verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d49c9-112">The **Image\_V0\_Load** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d49c9-113">BaseAddress</span><span class="sxs-lookup"><span data-stu-id="d49c9-113">BaseAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d49c9-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d49c9-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d49c9-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d49c9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d49c9-116">Qualifizierer: wmidataid (1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="d49c9-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="d49c9-117">Die Basisadresse der Anwendung, in der das Image geladen wird.</span><span class="sxs-lookup"><span data-stu-id="d49c9-117">Base address of the application in which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="d49c9-118">Imagefilename</span><span class="sxs-lookup"><span data-stu-id="d49c9-118">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d49c9-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d49c9-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d49c9-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d49c9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d49c9-121">Qualifizierer: wmidataid (3), stringbeendigung ("nullterminiert"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="d49c9-121">Qualifiers: WmiDataId(3), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="d49c9-122">Dateiname und Erweiterung der zu ladenden DLL oder des zu ladenden ausführbaren Images.</span><span class="sxs-lookup"><span data-stu-id="d49c9-122">File name and extension of the DLL or executable image to load.</span></span>

</dd> <dt>

<span data-ttu-id="d49c9-123">Modulesize</span><span class="sxs-lookup"><span data-stu-id="d49c9-123">ModuleSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d49c9-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d49c9-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d49c9-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d49c9-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d49c9-126">Qualifizierer: wmidataid (2)</span><span class="sxs-lookup"><span data-stu-id="d49c9-126">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="d49c9-127">Größe des Bilds.</span><span class="sxs-lookup"><span data-stu-id="d49c9-127">Size of the image.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d49c9-128">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d49c9-128">Requirements</span></span>



| <span data-ttu-id="d49c9-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d49c9-129">Requirement</span></span> | <span data-ttu-id="d49c9-130">Wert</span><span class="sxs-lookup"><span data-stu-id="d49c9-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d49c9-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d49c9-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d49c9-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d49c9-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d49c9-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d49c9-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d49c9-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d49c9-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d49c9-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d49c9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d49c9-136">**Bild \_ v0**</span><span class="sxs-lookup"><span data-stu-id="d49c9-136">**Image\_V0**</span></span>](image-v0.md)
</dt> </dl>

 

 




