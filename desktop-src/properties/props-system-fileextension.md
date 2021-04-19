---
description: Identifiziert die Dateierweiterung des dateibasierten Elements, einschließlich des führenden Zeitraums.
ms.assetid: b72c695e-bdbd-471d-b902-9e30a62facd4
title: System. File Extension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf8792a3965c394a1944985515df527e41e3a159
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360506"
---
# <a name="systemfileextension"></a><span data-ttu-id="6f8a5-103">System. File Extension</span><span class="sxs-lookup"><span data-stu-id="6f8a5-103">System.FileExtension</span></span>

<span data-ttu-id="6f8a5-104">Identifiziert die Dateierweiterung des dateibasierten Elements, einschließlich des führenden Zeitraums.</span><span class="sxs-lookup"><span data-stu-id="6f8a5-104">Identifies the file extension of the file-based item, including the leading period.</span></span> <span data-ttu-id="6f8a5-105">Diese Eigenschaft wird von System. filename abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="6f8a5-105">This property is derived from System.FileName.</span></span> <span data-ttu-id="6f8a5-106">Wenn System. filename entweder keine Dateierweiterung hat oder VT \_ leer ist, sollte der Wert für diese Eigenschaft "VT Empty" lauten \_ .</span><span class="sxs-lookup"><span data-stu-id="6f8a5-106">If System.FileName either does not have a file extension or is VT\_EMPTY, the value for this property should be VT\_EMPTY.</span></span>

<span data-ttu-id="6f8a5-107">Zum Abrufen des Typs eines beliebigen Elements (einschließlich eines Elements, das keine Datei ist), verwenden Sie System. ItemType.</span><span class="sxs-lookup"><span data-stu-id="6f8a5-107">To obtain the type of any item (including an item that is not a file), use System.ItemType.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="6f8a5-108">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f8a5-108">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.FileExtension
   shellPKey = PKEY_FileExtension
   formatID = E4F10A3C-49E6-405D-8288-A23BD4EEAA6C
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="6f8a5-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f8a5-109">Remarks</span></span>

<span data-ttu-id="6f8a5-110">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="6f8a5-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="6f8a5-111">Wenn [System. filename](./props-system-filename.md) den Wert VT \_ empty hat, sollte diese Eigenschaft auch leer sein.</span><span class="sxs-lookup"><span data-stu-id="6f8a5-111">If [System.FileName](./props-system-filename.md) is VT\_EMPTY, this property should also be empty.</span></span> <span data-ttu-id="6f8a5-112">Andernfalls sollte diese Eigenschaft von der Datenquelle aus System. filename abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="6f8a5-112">Otherwise, this property should be derived appropriately by the data source from System.FileName.</span></span> <span data-ttu-id="6f8a5-113">Wenn "System. filename" keine Dateierweiterung enthält, muss " [System. FileExtension]() " "VT Empty" lauten \_ .</span><span class="sxs-lookup"><span data-stu-id="6f8a5-113">If System.FileName does not include a file extension, [System.FileExtension]() should be VT\_EMPTY.</span></span> <span data-ttu-id="6f8a5-114">Zum Abrufen des Typs eines beliebigen Elements (einschließlich eines Elements, das keine Datei ist), verwenden Sie [System. ItemType](./props-system-itemtype.md).</span><span class="sxs-lookup"><span data-stu-id="6f8a5-114">To obtain the type of any item (including an item that is not a file), use [System.ItemType](./props-system-itemtype.md).</span></span>

<span data-ttu-id="6f8a5-115">Beispiele für Pfad-und Datei Erweiterungs Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6f8a5-115">Path and file extension property examples.</span></span> 

| <span data-ttu-id="6f8a5-116">Pfad</span><span class="sxs-lookup"><span data-stu-id="6f8a5-116">Path</span></span>                               | <span data-ttu-id="6f8a5-117">Dateierweiterung</span><span class="sxs-lookup"><span data-stu-id="6f8a5-117">File Extension</span></span> |
|------------------------------------|----------------|
| <span data-ttu-id="6f8a5-118">c: \\ \\ Eigene Dateien \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="6f8a5-118">c:\\files\\personal\\hello.txt</span></span>     | <span data-ttu-id="6f8a5-119">.txt</span><span class="sxs-lookup"><span data-stu-id="6f8a5-119">.txt</span></span>           |
| <span data-ttu-id="6f8a5-120">\\\\Server \\ Freigabe \\ "MyDir" \\news.doc</span><span class="sxs-lookup"><span data-stu-id="6f8a5-120">\\\\server\\share\\mydir\\news.doc</span></span> | <span data-ttu-id="6f8a5-121">.doc</span><span class="sxs-lookup"><span data-stu-id="6f8a5-121">.doc</span></span>           |
| <span data-ttu-id="6f8a5-122">\\\\Server \\ Freigabe \\numbers.xls</span><span class="sxs-lookup"><span data-stu-id="6f8a5-122">\\\\server\\share\\numbers.xls</span></span>     | <span data-ttu-id="6f8a5-123">.xls</span><span class="sxs-lookup"><span data-stu-id="6f8a5-123">.xls</span></span>           |
| <span data-ttu-id="6f8a5-124">\\\\Server \\ Freigabe \\ Ordner</span><span class="sxs-lookup"><span data-stu-id="6f8a5-124">\\\\server\\share\\folder</span></span>          | <span data-ttu-id="6f8a5-125">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="6f8a5-125">VT\_EMPTY</span></span>      |
| <span data-ttu-id="6f8a5-126">c: \\ Material \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="6f8a5-126">c:\\Stuff\\MyFolder</span></span>                | <span data-ttu-id="6f8a5-127">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="6f8a5-127">VT\_EMPTY</span></span>      |
| <span data-ttu-id="6f8a5-128">\[desktop\]</span><span class="sxs-lookup"><span data-stu-id="6f8a5-128">\[desktop\]</span></span>                        | <span data-ttu-id="6f8a5-129">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="6f8a5-129">VT\_EMPTY</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="6f8a5-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6f8a5-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f8a5-131">propertydescription</span><span class="sxs-lookup"><span data-stu-id="6f8a5-131">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="6f8a5-132">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="6f8a5-132">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="6f8a5-133">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="6f8a5-133">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="6f8a5-134">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="6f8a5-134">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="6f8a5-135">Display Info</span><span class="sxs-lookup"><span data-stu-id="6f8a5-135">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="6f8a5-136">StringFormat</span><span class="sxs-lookup"><span data-stu-id="6f8a5-136">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="6f8a5-137">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="6f8a5-137">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="6f8a5-138">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="6f8a5-138">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="6f8a5-139">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="6f8a5-139">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="6f8a5-140">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="6f8a5-140">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="6f8a5-141">DrawControl</span><span class="sxs-lookup"><span data-stu-id="6f8a5-141">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="6f8a5-142">editcontrol</span><span class="sxs-lookup"><span data-stu-id="6f8a5-142">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="6f8a5-143">FilterControl</span><span class="sxs-lookup"><span data-stu-id="6f8a5-143">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="6f8a5-144">querycontrol</span><span class="sxs-lookup"><span data-stu-id="6f8a5-144">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
