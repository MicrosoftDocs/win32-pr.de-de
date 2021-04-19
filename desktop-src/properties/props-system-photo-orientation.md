---
description: Die Ausrichtung des Fotos, wenn dieses erstellt wurde, wie in den Informationen zur austauschbaren Bilddatei (EXIF) und in Bezug auf Zeilen und Spalten angegeben.
ms.assetid: d6186248-8944-4bd6-8f04-bab5ea15b169
title: System. Photo. Orientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cac8cec8e199bd8eff52a92c7518a998d805d18d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106373008"
---
# <a name="systemphotoorientation"></a><span data-ttu-id="c85f3-103">System. Photo. Orientation</span><span class="sxs-lookup"><span data-stu-id="c85f3-103">System.Photo.Orientation</span></span>

<span data-ttu-id="c85f3-104">Die Ausrichtung des Fotos, wenn dieses erstellt wurde, wie in den Informationen zur austauschbaren Bilddatei (EXIF) und in Bezug auf Zeilen und Spalten angegeben.</span><span class="sxs-lookup"><span data-stu-id="c85f3-104">The orientation of the photo when it was taken, as specified in the Exchangeable Image File (EXIF) information and in terms of rows and columns.</span></span> <span data-ttu-id="c85f3-105">Dadurch können Anwendungen und die Shell das Bild ordnungsgemäß ausrichten, anstatt die Pixel zu durch sehen und das Bild in der angeforderten Anzeige Ausrichtung beizubehalten, was zu einem Verlust der Treue führen kann.</span><span class="sxs-lookup"><span data-stu-id="c85f3-105">This allows applications and the Shell to properly orient the image, instead of orienting the pixels and persisting the image in the requested display orientation, which can result in a loss of fidelity.</span></span> <span data-ttu-id="c85f3-106">Diese Eigenschaft soll nicht in der Benutzeroberfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c85f3-106">This property is not meant to be displayed in the UI.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="c85f3-107">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="c85f3-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Photo.Orientation
   shellPKey = PKEY_Photo_Orientation
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 274
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Normal
            value = 1
            text = Normal
            defineToken = PHOTO_ORIENTATION_NORMAL
         enum
            name = FlipHorizontal
            value = 2
            text = Flip horizontal
            defineToken = PHOTO_ORIENTATION_FLIPHORIZONTAL
         enum
            name = Rotate180
            value = 3
            text = Rotate 180 degrees
            defineToken = PHOTO_ORIENTATION_ROTATE180
         enum
            name = FlipVertical
            value = 4
            text = Flip vertical
            defineToken = PHOTO_ORIENTATION_FLIPVERTICAL
         enum
            name = Transpose
            value = 5
            text = Transpose
            defineToken = PHOTO_ORIENTATION_TRANSPOSE
         enum
            name = Rotate270
            value = 6
            text = Rotate 270 degrees
            defineToken = PHOTO_ORIENTATION_ROTATE270
         enum
            name = Transverse
            value = 7
            text = Transverse
            defineToken = PHOTO_ORIENTATION_TRANSVERSE
         enum
            name = Rotate90
            value = 8
            text = Rotate 90 degrees
            defineToken = PHOTO_ORIENTATION_ROTATE90
```

## <a name="windows-vista"></a><span data-ttu-id="c85f3-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c85f3-108">Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.Orientation
   shellPKey = PKEY_Photo_Orientation
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 274
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 1
            text = Normal
            defineName = PHOTO_ORIENTATION_NORMAL
         enum
            value = 2
            text = Flip horizontal
            defineName = PHOTO_ORIENTATION_FLIPHORIZONTAL
         enum
            value = 3
            text = Rotate 180 degrees
            defineName = PHOTO_ORIENTATION_ROTATE180
         enum
            value = 4
            text = Flip vertical
            defineName = PHOTO_ORIENTATION_FLIPVERTICAL
         enum
            value = 5
            text = Transpose
            defineName = PHOTO_ORIENTATION_TRANSPOSE
         enum
            value = 6
            text = Rotate 270 degrees
            defineName = PHOTO_ORIENTATION_ROTATE270
         enum
            value = 7
            text = Transverse
            defineName = PHOTO_ORIENTATION_TRANSVERSE
         enum
            value = 8
            text = Rotate 90 degrees
            defineName = PHOTO_ORIENTATION_ROTATE90
```

## <a name="remarks"></a><span data-ttu-id="c85f3-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c85f3-109">Remarks</span></span>

<span data-ttu-id="c85f3-110">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="c85f3-110">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c85f3-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c85f3-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c85f3-112">Exchangeable Image File Format für digitale Kameras: EXIF Version 2,2</span><span class="sxs-lookup"><span data-stu-id="c85f3-112">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="c85f3-113">propertydescription</span><span class="sxs-lookup"><span data-stu-id="c85f3-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="c85f3-114">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="c85f3-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="c85f3-115">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="c85f3-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="c85f3-116">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="c85f3-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="c85f3-117">Display Info</span><span class="sxs-lookup"><span data-stu-id="c85f3-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="c85f3-118">StringFormat</span><span class="sxs-lookup"><span data-stu-id="c85f3-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="c85f3-119">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="c85f3-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="c85f3-120">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="c85f3-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="c85f3-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="c85f3-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="c85f3-122">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="c85f3-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="c85f3-123">DrawControl</span><span class="sxs-lookup"><span data-stu-id="c85f3-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="c85f3-124">editcontrol</span><span class="sxs-lookup"><span data-stu-id="c85f3-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="c85f3-125">FilterControl</span><span class="sxs-lookup"><span data-stu-id="c85f3-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="c85f3-126">querycontrol</span><span class="sxs-lookup"><span data-stu-id="c85f3-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
