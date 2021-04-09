---
description: Der benutzerfreundliche Anzeige Pfad für den übergeordneten Ordner eines Elements.
ms.assetid: f60b7465-bca4-4c7b-9caf-9cda1bf6eeeb
title: System. itemfolderpathdisplaynarrow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898927c23aae95b5037919c908a3ae86e020e1fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042333"
---
# <a name="systemitemfolderpathdisplaynarrow"></a><span data-ttu-id="b63b1-103">System. itemfolderpathdisplaynarrow</span><span class="sxs-lookup"><span data-stu-id="b63b1-103">System.ItemFolderPathDisplayNarrow</span></span>

<span data-ttu-id="b63b1-104">Der benutzerfreundliche Anzeige Pfad für den übergeordneten Ordner eines Elements.</span><span class="sxs-lookup"><span data-stu-id="b63b1-104">The user-friendly display path of an item's parent folder.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="b63b1-105">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b63b1-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemFolderPathDisplayNarrow
   shellPKey = PKEY_ItemFolderPathDisplayNarrow
   formatID = DABD30ED-0043-4789-A7F8-D013A4736622
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="b63b1-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b63b1-106">Remarks</span></span>

<span data-ttu-id="b63b1-107">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="b63b1-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="b63b1-108">Das Format der Zeichenfolge sollte angepasst werden, damit der Ordnername zuerst angezeigt wird, um für eine schmale Anzeige Spalte zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="b63b1-108">The format of the string should be tailored so that the folder name comes first, to optimize for a narrow viewing column.</span></span> <span data-ttu-id="b63b1-109">Wenn der Ordner ein Datei Ordner ist, enthält der Wert alle lokalisierten Namen.</span><span class="sxs-lookup"><span data-stu-id="b63b1-109">If the folder is a file folder, the value includes any localized names.</span></span> <span data-ttu-id="b63b1-110">Wenn [System. itemfolderpathdisplay](./props-system-itemfolderpathdisplay.md) den Wert VT \_ empty hat, sollte diese Eigenschaft auch leer sein.</span><span class="sxs-lookup"><span data-stu-id="b63b1-110">If [System.ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) is VT\_EMPTY, then this property should also be empty.</span></span> <span data-ttu-id="b63b1-111">Andernfalls sollte Sie von der Datenquelle aus System. itemfolderpathdisplay ordnungsgemäß abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="b63b1-111">Otherwise, it should be derived appropriately by the data source from System.ItemFolderPathDisplay.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b63b1-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b63b1-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b63b1-113">propertydescription</span><span class="sxs-lookup"><span data-stu-id="b63b1-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="b63b1-114">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="b63b1-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="b63b1-115">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="b63b1-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="b63b1-116">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="b63b1-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="b63b1-117">Display Info</span><span class="sxs-lookup"><span data-stu-id="b63b1-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="b63b1-118">StringFormat</span><span class="sxs-lookup"><span data-stu-id="b63b1-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="b63b1-119">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="b63b1-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="b63b1-120">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="b63b1-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="b63b1-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="b63b1-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="b63b1-122">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="b63b1-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="b63b1-123">DrawControl</span><span class="sxs-lookup"><span data-stu-id="b63b1-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="b63b1-124">editcontrol</span><span class="sxs-lookup"><span data-stu-id="b63b1-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="b63b1-125">FilterControl</span><span class="sxs-lookup"><span data-stu-id="b63b1-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="b63b1-126">querycontrol</span><span class="sxs-lookup"><span data-stu-id="b63b1-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
