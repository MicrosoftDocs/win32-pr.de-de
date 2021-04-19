---
description: Der Titel des Elements.
ms.assetid: 8fb948d6-2677-4e5d-b283-8757c3df574d
title: System.Title
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eee57037a35c08fd3a6be4f4a0ce7a8475f82cf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352717"
---
# <a name="systemtitle"></a><span data-ttu-id="5d92d-103">System.Title</span><span class="sxs-lookup"><span data-stu-id="5d92d-103">System.Title</span></span>

<span data-ttu-id="5d92d-104">Der Titel des Elements.</span><span class="sxs-lookup"><span data-stu-id="5d92d-104">The title of the item.</span></span> <span data-ttu-id="5d92d-105">Dabei kann es sich z. B. um den Titel eines Dokuments, den Betreff einer Nachricht, die Beschriftung eines Fotos oder den Namen eines Musiktitels handeln.</span><span class="sxs-lookup"><span data-stu-id="5d92d-105">For example, the title of a document, the subject of a message, the caption of a photo, or the name of a music track.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="5d92d-106">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d92d-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Title
   shellPKey = PKEY_Title
   formatID = F29F85E0-4FF9-1068-AB91-08002B27B3D9
   propID = 2
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
```

## <a name="remarks"></a><span data-ttu-id="5d92d-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d92d-107">Remarks</span></span>

<span data-ttu-id="5d92d-108">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="5d92d-108">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="5d92d-109">Diese Eigenschaft wird dem *Titel* der OLE-Dokument Eigenschaft zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="5d92d-109">This property maps to the OLE document property *Title*.</span></span> <span data-ttu-id="5d92d-110">[System. Title]() ist eine häufig verwendete Eigenschaft, insbesondere in heterogenen Listen von Elementen, bei denen die Elemente viele verschiedene Typen aufweisen können.</span><span class="sxs-lookup"><span data-stu-id="5d92d-110">[System.Title]() is a commonly used property, particularly in heterogeneous lists of items where the items can be of many different types.</span></span> <span data-ttu-id="5d92d-111">Daher wird empfohlen, dass Eigenschafts Handler diese Eigenschaft auffüllen, auch wenn Sie redundant ist. beispielsweise eine e-Mail, die sowohl System. Title als auch [System. Subject](./props-system-subject.md) mit dem gleichen Wert Auffüllen würde.</span><span class="sxs-lookup"><span data-stu-id="5d92d-111">Therefore, it is recommended that property handlers populate this property even if it is redundant; for example, an e-mail, which would populate both System.Title and [System.Subject](./props-system-subject.md) with the same value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d92d-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5d92d-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d92d-113">propertydescription</span><span class="sxs-lookup"><span data-stu-id="5d92d-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="5d92d-114">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="5d92d-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="5d92d-115">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="5d92d-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="5d92d-116">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="5d92d-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="5d92d-117">Display Info</span><span class="sxs-lookup"><span data-stu-id="5d92d-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="5d92d-118">StringFormat</span><span class="sxs-lookup"><span data-stu-id="5d92d-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="5d92d-119">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="5d92d-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="5d92d-120">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="5d92d-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="5d92d-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="5d92d-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="5d92d-122">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="5d92d-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="5d92d-123">DrawControl</span><span class="sxs-lookup"><span data-stu-id="5d92d-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="5d92d-124">editcontrol</span><span class="sxs-lookup"><span data-stu-id="5d92d-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="5d92d-125">FilterControl</span><span class="sxs-lookup"><span data-stu-id="5d92d-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="5d92d-126">querycontrol</span><span class="sxs-lookup"><span data-stu-id="5d92d-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
