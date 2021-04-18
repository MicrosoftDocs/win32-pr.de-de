---
description: Diese Eigenschaft ähnelt System. itemnamedisplay, mit der Ausnahme, dass Sie nur für Ordner festgelegt wird, wenn Sie leer ist.
ms.assetid: 4517a4bf-3cc1-4835-b21b-03de5b33db0c
title: System. foldernamedisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60922054e80a6589bcb04c3962a4527ee62eaf7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347651"
---
# <a name="systemfoldernamedisplay"></a><span data-ttu-id="1aa1e-103">System. foldernamedisplay</span><span class="sxs-lookup"><span data-stu-id="1aa1e-103">System.FolderNameDisplay</span></span>

<span data-ttu-id="1aa1e-104">Diese Eigenschaft ähnelt System. itemnamedisplay, mit der Ausnahme, dass Sie nur für Ordner festgelegt wird, wenn Sie leer ist.</span><span class="sxs-lookup"><span data-stu-id="1aa1e-104">This property is similar to System.ItemNameDisplay except it is only set for folders, for files it will be empty.</span></span> <span data-ttu-id="1aa1e-105">Dies ist hilfreich, um Dateien und Ordner zu trennen, indem Sie diese als ersten Sortierschlüssel verwenden.</span><span class="sxs-lookup"><span data-stu-id="1aa1e-105">This is useful to segregate files and folders by using this as the first sort key.</span></span> <span data-ttu-id="1aa1e-106">Wenn System. itemdate als zweiter Sortierschlüssel verwendet wird, werden Ergebnisse mit zuerst nach Namen sortierter Ordner erstellt, danach werden die Dateien nach Datum sortiert.</span><span class="sxs-lookup"><span data-stu-id="1aa1e-106">When System.ItemDate is used as a second sort key it produces results with folders first ordered by name, then files ordered by date.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a><span data-ttu-id="1aa1e-107">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1aa1e-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1</span></span>

```
propertyDescription
   name = System.FolderNameDisplay
   shellPKey = PKEY_FolderNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 25
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="1aa1e-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1aa1e-108">Remarks</span></span>

<span data-ttu-id="1aa1e-109">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="1aa1e-109">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1aa1e-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1aa1e-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1aa1e-111">propertydescription</span><span class="sxs-lookup"><span data-stu-id="1aa1e-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="1aa1e-112">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="1aa1e-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="1aa1e-113">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="1aa1e-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="1aa1e-114">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="1aa1e-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="1aa1e-115">Display Info</span><span class="sxs-lookup"><span data-stu-id="1aa1e-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="1aa1e-116">StringFormat</span><span class="sxs-lookup"><span data-stu-id="1aa1e-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="1aa1e-117">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="1aa1e-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="1aa1e-118">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="1aa1e-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="1aa1e-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="1aa1e-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="1aa1e-120">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="1aa1e-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="1aa1e-121">DrawControl</span><span class="sxs-lookup"><span data-stu-id="1aa1e-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="1aa1e-122">editcontrol</span><span class="sxs-lookup"><span data-stu-id="1aa1e-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="1aa1e-123">FilterControl</span><span class="sxs-lookup"><span data-stu-id="1aa1e-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="1aa1e-124">querycontrol</span><span class="sxs-lookup"><span data-stu-id="1aa1e-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
