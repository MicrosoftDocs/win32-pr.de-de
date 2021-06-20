---
description: Erfahren Sie mehr über die System.ItemFolderPathDisplayNarrow-Eigenschaft, die den benutzerfreundlichen Anzeigepfad des übergeordneten Ordners eines Elements darstellt.
ms.assetid: f60b7465-bca4-4c7b-9caf-9cda1bf6eeeb
title: System.ItemFolderPathDisplayNarrow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbee8a45eb6ea557e99c854464c7dc09ec5613d2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403913"
---
# <a name="systemitemfolderpathdisplaynarrow"></a><span data-ttu-id="294c4-103">System.ItemFolderPathDisplayNarrow</span><span class="sxs-lookup"><span data-stu-id="294c4-103">System.ItemFolderPathDisplayNarrow</span></span>

<span data-ttu-id="294c4-104">Der benutzerfreundliche Anzeigepfad des übergeordneten Ordners eines Elements.</span><span class="sxs-lookup"><span data-stu-id="294c4-104">The user-friendly display path of an item's parent folder.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="294c4-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="294c4-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

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

## <a name="remarks"></a><span data-ttu-id="294c4-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="294c4-106">Remarks</span></span>

<span data-ttu-id="294c4-107">PKEY-Werte werden in Propkey.h definiert.</span><span class="sxs-lookup"><span data-stu-id="294c4-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="294c4-108">Das Format der Zeichenfolge sollte so angepasst werden, dass der Ordnername an erster Stelle steht, um eine Schmalansichtsspalte zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="294c4-108">The format of the string should be tailored so that the folder name comes first, to optimize for a narrow viewing column.</span></span> <span data-ttu-id="294c4-109">Wenn der Ordner ein Dateiordner ist, enthält der Wert alle lokalisierten Namen.</span><span class="sxs-lookup"><span data-stu-id="294c4-109">If the folder is a file folder, the value includes any localized names.</span></span> <span data-ttu-id="294c4-110">Wenn [System.ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) VT \_ EMPTY ist, sollte diese Eigenschaft ebenfalls leer sein.</span><span class="sxs-lookup"><span data-stu-id="294c4-110">If [System.ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) is VT\_EMPTY, then this property should also be empty.</span></span> <span data-ttu-id="294c4-111">Andernfalls sollte sie von der Datenquelle von System.ItemFolderPathDisplay entsprechend abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="294c4-111">Otherwise, it should be derived appropriately by the data source from System.ItemFolderPathDisplay.</span></span>

## <a name="related-topics"></a><span data-ttu-id="294c4-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="294c4-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="294c4-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="294c4-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="294c4-114">searchInfo</span><span class="sxs-lookup"><span data-stu-id="294c4-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="294c4-115">labelInfo</span><span class="sxs-lookup"><span data-stu-id="294c4-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="294c4-116">Typeinfo</span><span class="sxs-lookup"><span data-stu-id="294c4-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="294c4-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="294c4-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="294c4-118">Stringformat</span><span class="sxs-lookup"><span data-stu-id="294c4-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="294c4-119">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="294c4-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="294c4-120">Numberformat</span><span class="sxs-lookup"><span data-stu-id="294c4-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="294c4-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="294c4-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="294c4-122">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="294c4-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="294c4-123">drawControl</span><span class="sxs-lookup"><span data-stu-id="294c4-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="294c4-124">editControl</span><span class="sxs-lookup"><span data-stu-id="294c4-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="294c4-125">Filtercontrol</span><span class="sxs-lookup"><span data-stu-id="294c4-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="294c4-126">queryControl</span><span class="sxs-lookup"><span data-stu-id="294c4-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
