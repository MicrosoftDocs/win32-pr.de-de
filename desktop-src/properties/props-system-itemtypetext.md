---
description: Der benutzerfreundliche Typname des Elements.
ms.assetid: 5d4c86da-6317-4a34-88d6-caf794aaa165
title: System. itemtypetext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699a953392054cb2344c5f3b3d652e64a9a2c1f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215779"
---
# <a name="systemitemtypetext"></a><span data-ttu-id="d5870-103">System. itemtypetext</span><span class="sxs-lookup"><span data-stu-id="d5870-103">System.ItemTypeText</span></span>

<span data-ttu-id="d5870-104">Der benutzerfreundliche Typname des Elements.</span><span class="sxs-lookup"><span data-stu-id="d5870-104">The user-friendly type name of the item.</span></span> <span data-ttu-id="d5870-105">Dieser Wert sollte nicht Programm gesteuert analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="d5870-105">This value is not intended to be programmatically parsed.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="d5870-106">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d5870-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemTypeText
   shellPKey = PKEY_ItemTypeText
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 4
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="d5870-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5870-107">Remarks</span></span>

<span data-ttu-id="d5870-108">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="d5870-108">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="d5870-109">Wenn [System. ItemType](./props-system-itemtype.md) \_ den Wert VT Empty hat, ist der Wert dieser Eigenschaft ebenfalls VT \_ empty.</span><span class="sxs-lookup"><span data-stu-id="d5870-109">If [System.ItemType](./props-system-itemtype.md) is VT\_EMPTY, the value of this property is also VT\_EMPTY.</span></span> <span data-ttu-id="d5870-110">Wenn es sich bei dem Element um eine Datei handelt, ist der Wert dieser Eigenschaft mit dem Wert identisch, wenn Sie den System. ItemType-Wert der Datei an [**psformatfordisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay)übergeben haben.</span><span class="sxs-lookup"><span data-stu-id="d5870-110">If the item is a file, the value of this property is the same as if you passed the file's System.ItemType value to [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay).</span></span>

<span data-ttu-id="d5870-111">Diese Eigenschaft sollte nicht mit [System. Kind](./props-system-kind.md)verwechselt werden. Dies ist ein allgemeiner, benutzerfreundlicher Name der Art.</span><span class="sxs-lookup"><span data-stu-id="d5870-111">This property should not be confused with [System.Kind](./props-system-kind.md), which is a high-level, user-friendly kind name.</span></span> <span data-ttu-id="d5870-112">Für eine doc-Dokument Datei werden z. b. die verschiedenen Eigenschaften wie hier gezeigt angezeigt:</span><span class="sxs-lookup"><span data-stu-id="d5870-112">For example, for a .doc document file, the various properties are as shown here:</span></span>



| <span data-ttu-id="d5870-113">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d5870-113">Property</span></span>                                               | <span data-ttu-id="d5870-114">Wert</span><span class="sxs-lookup"><span data-stu-id="d5870-114">Value</span></span>                   |
|--------------------------------------------------------|-------------------------|
| [<span data-ttu-id="d5870-115">System. Kind</span><span class="sxs-lookup"><span data-stu-id="d5870-115">System.Kind</span></span>](./props-system-kind.md)                 | <span data-ttu-id="d5870-116">Dokument</span><span class="sxs-lookup"><span data-stu-id="d5870-116">Document</span></span>                |
| [<span data-ttu-id="d5870-117">System. ItemType</span><span class="sxs-lookup"><span data-stu-id="d5870-117">System.ItemType</span></span>](./props-system-itemtype.md)         | <span data-ttu-id="d5870-118">.doc</span><span class="sxs-lookup"><span data-stu-id="d5870-118">.doc</span></span>                    |
| [<span data-ttu-id="d5870-119">System. itemtypetext</span><span class="sxs-lookup"><span data-stu-id="d5870-119">System.ItemTypeText</span></span>]() | <span data-ttu-id="d5870-120">Microsoft Word-Dokument</span><span class="sxs-lookup"><span data-stu-id="d5870-120">Microsoft Word Document</span></span> |



 

<span data-ttu-id="d5870-121">Beispielwerte:</span><span class="sxs-lookup"><span data-stu-id="d5870-121">Example values:</span></span>



| <span data-ttu-id="d5870-122">Pfad</span><span class="sxs-lookup"><span data-stu-id="d5870-122">Path</span></span>                                   | <span data-ttu-id="d5870-123">Itemtypetext</span><span class="sxs-lookup"><span data-stu-id="d5870-123">ItemTypeText</span></span>            |
|----------------------------------------|-------------------------|
| <span data-ttu-id="d5870-124">c: \\ "MyDir"- \\ Leiste \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="d5870-124">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="d5870-125">Textdatei</span><span class="sxs-lookup"><span data-stu-id="d5870-125">Text File</span></span>               |
| <span data-ttu-id="d5870-126">\\\\Server \\ Freigabe \\ "MyDir" \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="d5870-126">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="d5870-127">Microsoft Word-Dokument</span><span class="sxs-lookup"><span data-stu-id="d5870-127">Microsoft Word Document</span></span> |
| <span data-ttu-id="d5870-128">\\\\Server \\ Freigabe \\ Ordner</span><span class="sxs-lookup"><span data-stu-id="d5870-128">\\\\server\\share\\folder</span></span>              | <span data-ttu-id="d5870-129">Datei Ordner</span><span class="sxs-lookup"><span data-stu-id="d5870-129">File Folder</span></span>             |
| <span data-ttu-id="d5870-130">c: \\ mydir \\ meinOrdner</span><span class="sxs-lookup"><span data-stu-id="d5870-130">c:\\MyDir\\MyFolder</span></span>                    | <span data-ttu-id="d5870-131">Datei Ordner</span><span class="sxs-lookup"><span data-stu-id="d5870-131">File Folder</span></span>             |
| <span data-ttu-id="d5870-132">/Mailbox Account/Inbox/"Re: Hello!"</span><span class="sxs-lookup"><span data-stu-id="d5870-132">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="d5870-133">Outlook-e-Mail</span><span class="sxs-lookup"><span data-stu-id="d5870-133">Outlook E-Mail Message</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="d5870-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d5870-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5870-135">propertydescription</span><span class="sxs-lookup"><span data-stu-id="d5870-135">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="d5870-136">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="d5870-136">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="d5870-137">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="d5870-137">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="d5870-138">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="d5870-138">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="d5870-139">Display Info</span><span class="sxs-lookup"><span data-stu-id="d5870-139">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="d5870-140">StringFormat</span><span class="sxs-lookup"><span data-stu-id="d5870-140">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="d5870-141">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="d5870-141">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="d5870-142">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="d5870-142">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="d5870-143">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="d5870-143">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="d5870-144">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="d5870-144">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="d5870-145">DrawControl</span><span class="sxs-lookup"><span data-stu-id="d5870-145">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="d5870-146">editcontrol</span><span class="sxs-lookup"><span data-stu-id="d5870-146">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="d5870-147">FilterControl</span><span class="sxs-lookup"><span data-stu-id="d5870-147">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="d5870-148">querycontrol</span><span class="sxs-lookup"><span data-stu-id="d5870-148">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
