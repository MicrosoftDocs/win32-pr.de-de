---
description: Der ColorSpace, der in das Bild eingebettet ist. Wird aus den Informationen der austauschbaren Bilddatei (EXIF) entnommen.
ms.assetid: 2375e132-e400-419f-a0f9-cbb6f9acdf45
title: System. Image. ColorSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024d99e0f88fd793d0a0f8207b43a52c7be47c30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358866"
---
# <a name="systemimagecolorspace"></a><span data-ttu-id="06e5c-104">System. Image. ColorSpace</span><span class="sxs-lookup"><span data-stu-id="06e5c-104">System.Image.ColorSpace</span></span>

<span data-ttu-id="06e5c-105">Der ColorSpace, der in das Bild eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="06e5c-105">The colorspace embedded in the image.</span></span> <span data-ttu-id="06e5c-106">Wird aus den Informationen der austauschbaren Bilddatei (EXIF) entnommen.</span><span class="sxs-lookup"><span data-stu-id="06e5c-106">Taken from the Exchangeable Image File (EXIF) information.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="06e5c-107">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="06e5c-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Image.ColorSpace
   shellPKey = PKEY_Image_ColorSpace
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 40961
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt16
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = SRGB
            value = 1
            text = sRGB
            defineToken = IMAGE_COLORSPACE_SRGB
         enum
            name = Uncalibrated
            value = 0xFFFF
            text = Uncalibrated
            defineToken = IMAGE_COLORSPACE_UNCALIBRATED
```

## <a name="windows-vista"></a><span data-ttu-id="06e5c-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06e5c-108">Windows Vista</span></span>

```
propertyDescription
   name = System.Image.ColorSpace
   shellPKey = PKEY_Image_ColorSpace
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 40961
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt16
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 1
            text = sRGB
            defineName = IMAGE_COLORSPACE_SRGB
         enum
            value = 0xFFFF
            text = Uncalibrated
            defineName = IMAGE_COLORSPACE_UNCALIBRATED
```

## <a name="remarks"></a><span data-ttu-id="06e5c-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06e5c-109">Remarks</span></span>

<span data-ttu-id="06e5c-110">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="06e5c-110">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06e5c-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="06e5c-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06e5c-112">Exchangeable Image File Format für digitale Kameras: EXIF Version 2,2</span><span class="sxs-lookup"><span data-stu-id="06e5c-112">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="06e5c-113">propertydescription</span><span class="sxs-lookup"><span data-stu-id="06e5c-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="06e5c-114">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="06e5c-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="06e5c-115">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="06e5c-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="06e5c-116">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="06e5c-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="06e5c-117">Display Info</span><span class="sxs-lookup"><span data-stu-id="06e5c-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="06e5c-118">StringFormat</span><span class="sxs-lookup"><span data-stu-id="06e5c-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="06e5c-119">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="06e5c-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="06e5c-120">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="06e5c-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="06e5c-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="06e5c-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="06e5c-122">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="06e5c-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="06e5c-123">DrawControl</span><span class="sxs-lookup"><span data-stu-id="06e5c-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="06e5c-124">editcontrol</span><span class="sxs-lookup"><span data-stu-id="06e5c-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="06e5c-125">FilterControl</span><span class="sxs-lookup"><span data-stu-id="06e5c-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="06e5c-126">querycontrol</span><span class="sxs-lookup"><span data-stu-id="06e5c-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
