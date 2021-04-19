---
description: Der Dateiname, einschließlich der Erweiterung.
ms.assetid: 40940026-6c67-4196-aff6-5f846dc94f27
title: System. filename
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8f535eff4625178b3c32a04ea6d325505266a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367902"
---
# <a name="systemfilename"></a><span data-ttu-id="5fbda-103">System. filename</span><span class="sxs-lookup"><span data-stu-id="5fbda-103">System.FileName</span></span>

<span data-ttu-id="5fbda-104">Der Dateiname, einschließlich der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="5fbda-104">The file name, including its extension.</span></span> <span data-ttu-id="5fbda-105">System. File Extension wird von dieser Eigenschaft abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="5fbda-105">System.FileExtension is derived from this property.</span></span>

<span data-ttu-id="5fbda-106">Es ist möglich, dass das Element in einem Dateisystem nicht vorhanden ist (d. h., es kann nicht mithilfe von "deatefile" geöffnet werden).</span><span class="sxs-lookup"><span data-stu-id="5fbda-106">It is possible that the item might not exist on a filesystem (that is, it may not be opened using CreateFile).</span></span> <span data-ttu-id="5fbda-107">Wenn das Element jedoch als Datei dargestellt wird und der Name der standardmäßigen Win32-Dateibenennungs Syntax folgt, sollte die Datenquelle diese Eigenschaft ausgeben.</span><span class="sxs-lookup"><span data-stu-id="5fbda-107">Nonetheless, if the item is represented as a file and its name follows standard Win32 file-naming syntax, then the data source should emit this property.</span></span> <span data-ttu-id="5fbda-108">Wenn es sich bei dem Element nicht um eine Datei handelt, sollte die Datenquelle diese Eigenschaft als VT \_ empty ausgeben.</span><span class="sxs-lookup"><span data-stu-id="5fbda-108">If the item is not a file, then the data source should emit this property as VT\_EMPTY.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="5fbda-109">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="5fbda-109">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.FileName
   shellPKey = PKEY_FileName
   formatID = 41CF5AE0-F75A-4806-BD87-59C7D9248EB9
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="windows-vista"></a><span data-ttu-id="5fbda-110">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5fbda-110">Windows Vista</span></span>

```
propertyDescription
   name = System.FileName
   shellPKey = PKEY_FileName
   formatID = 41CF5AE0-F75A-4806-BD87-59C7D9248EB9
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            setValue = 0
            text = 0-9
         enumRange
            minValue = A
            setValue = A
            text = A-H
         enumRange
            minValue = I
            setValue = I
            text = I-P
         enumRange
            minValue = Q
            setValue = Q
            text = Q-Z
```

## <a name="remarks"></a><span data-ttu-id="5fbda-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5fbda-111">Remarks</span></span>

<span data-ttu-id="5fbda-112">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="5fbda-112">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="5fbda-113">Das Element ist möglicherweise nicht in einem Dateisystem vorhanden (d. h. es kann nicht mithilfe von "anatefile" geöffnet werden). wenn das Element jedoch als Datei aus dem logischen Sinne dargestellt wird und der Name der standardmäßigen Win32-Datei namens Syntax folgt, sollte die Datenquelle diese Eigenschaft ausgeben.</span><span class="sxs-lookup"><span data-stu-id="5fbda-113">The item might not exist on a filesystem (that is, it may not be opened using CreateFile), but if the item is represented as a file from the logical sense and its name follows standard Win32 file-naming syntax, then the data source should emit this property.</span></span> <span data-ttu-id="5fbda-114">Wenn es sich bei einem Element nicht um eine Datei handelt, ist der Wert für diese Eigenschaft VT \_ empty.</span><span class="sxs-lookup"><span data-stu-id="5fbda-114">If an item is not a file, then the value for this property is VT\_EMPTY.</span></span> <span data-ttu-id="5fbda-115">Weitere Informationen finden Sie unter System. itemnamedisplay.</span><span class="sxs-lookup"><span data-stu-id="5fbda-115">See System.ItemNameDisplay.</span></span> <span data-ttu-id="5fbda-116">Dies hat den gleichen Wert wie System. Parser Name für Elemente, die vom Datei Ordner der Shell bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5fbda-116">This has the same value as System.ParsingName for items that are provided by the Shell's file folder.</span></span>

<span data-ttu-id="5fbda-117">In der folgenden Tabelle sind Beispiele für Pfad-und Dateinamen Eigenschaftswerte aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="5fbda-117">The following table lists examples of path and filename property values:</span></span>



| <span data-ttu-id="5fbda-118">Pfad</span><span class="sxs-lookup"><span data-stu-id="5fbda-118">Path</span></span>                               | <span data-ttu-id="5fbda-119">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5fbda-119">Property Value</span></span> |
|------------------------------------|----------------|
| <span data-ttu-id="5fbda-120">c: \\ \\ Eigene Dateien \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="5fbda-120">c:\\files\\personal\\hello.txt</span></span>     | <span data-ttu-id="5fbda-121">hello.txt</span><span class="sxs-lookup"><span data-stu-id="5fbda-121">hello.txt</span></span>      |
| <span data-ttu-id="5fbda-122">\\\\Server \\ Freigabe \\ "MyDir" \\news.doc</span><span class="sxs-lookup"><span data-stu-id="5fbda-122">\\\\server\\share\\mydir\\news.doc</span></span> | <span data-ttu-id="5fbda-123">news.doc</span><span class="sxs-lookup"><span data-stu-id="5fbda-123">news.doc</span></span>       |
| <span data-ttu-id="5fbda-124">\\\\Server \\ Freigabe \\numbers.xls</span><span class="sxs-lookup"><span data-stu-id="5fbda-124">\\\\server\\share\\numbers.xls</span></span>     | <span data-ttu-id="5fbda-125">numbers.xls</span><span class="sxs-lookup"><span data-stu-id="5fbda-125">numbers.xls</span></span>    |
| <span data-ttu-id="5fbda-126">c: \\ Material \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="5fbda-126">c:\\Stuff\\MyFolder</span></span>                | <span data-ttu-id="5fbda-127">MyFolder</span><span class="sxs-lookup"><span data-stu-id="5fbda-127">MyFolder</span></span>       |
| <span data-ttu-id="5fbda-128">\[e-Mail senden\]</span><span class="sxs-lookup"><span data-stu-id="5fbda-128">\[email message\]</span></span>                  | <span data-ttu-id="5fbda-129">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="5fbda-129">VT\_EMPTY</span></span>      |
| <span data-ttu-id="5fbda-130">\["Song. wma" auf einem tragbaren Gerät\]</span><span class="sxs-lookup"><span data-stu-id="5fbda-130">\[song.wma on portable device\]</span></span>    | <span data-ttu-id="5fbda-131">"Song. wma"</span><span class="sxs-lookup"><span data-stu-id="5fbda-131">song.wma</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="5fbda-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5fbda-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fbda-133">propertydescription</span><span class="sxs-lookup"><span data-stu-id="5fbda-133">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="5fbda-134">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="5fbda-134">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="5fbda-135">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="5fbda-135">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="5fbda-136">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="5fbda-136">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="5fbda-137">Display Info</span><span class="sxs-lookup"><span data-stu-id="5fbda-137">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="5fbda-138">StringFormat</span><span class="sxs-lookup"><span data-stu-id="5fbda-138">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="5fbda-139">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="5fbda-139">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="5fbda-140">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="5fbda-140">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="5fbda-141">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="5fbda-141">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="5fbda-142">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="5fbda-142">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="5fbda-143">DrawControl</span><span class="sxs-lookup"><span data-stu-id="5fbda-143">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="5fbda-144">editcontrol</span><span class="sxs-lookup"><span data-stu-id="5fbda-144">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="5fbda-145">FilterControl</span><span class="sxs-lookup"><span data-stu-id="5fbda-145">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="5fbda-146">querycontrol</span><span class="sxs-lookup"><span data-stu-id="5fbda-146">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
