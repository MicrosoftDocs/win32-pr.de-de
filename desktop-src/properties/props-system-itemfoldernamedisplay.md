---
description: Der benutzerfreundliche Anzeige Name des übergeordneten Ordners eines Elements.
ms.assetid: 4049b6cb-41a1-4df6-89d1-a2022d3a285d
title: System. itemfoldernamedisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d637412b02345b52fee2e1c13e8f499314af4c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216996"
---
# <a name="systemitemfoldernamedisplay"></a><span data-ttu-id="1702f-103">System. itemfoldernamedisplay</span><span class="sxs-lookup"><span data-stu-id="1702f-103">System.ItemFolderNameDisplay</span></span>

<span data-ttu-id="1702f-104">Der benutzerfreundliche Anzeige Name des übergeordneten Ordners eines Elements.</span><span class="sxs-lookup"><span data-stu-id="1702f-104">The user-friendly display name of an item's parent folder.</span></span>

<span data-ttu-id="1702f-105">Dies wird von [System. itemfolderpathdisplay](./props-system-itemfolderpathdisplay.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="1702f-105">This is derived from [System.ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md).</span></span> <span data-ttu-id="1702f-106">Wenn diese Eigenschaft den Wert VT \_ empty hat, sollte diese Eigenschaft ebenfalls sein.</span><span class="sxs-lookup"><span data-stu-id="1702f-106">If that property is VT\_EMPTY, then this property should be too.</span></span>

<span data-ttu-id="1702f-107">Wenn es sich bei dem Ordner um einen Datei Ordner handelt, wird der Wert lokalisiert, wenn ein lokalisierter Name verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="1702f-107">If the folder is a file folder, the value will be localized if a localized name is available.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="1702f-108">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1702f-108">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemFolderNameDisplay
   shellPKey = PKEY_ItemFolderNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 2
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="1702f-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1702f-109">Remarks</span></span>

<span data-ttu-id="1702f-110">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="1702f-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="1702f-111">Wenn [System. itemfolderpathdisplay](./props-system-itemfolderpathdisplay.md) den Wert VT \_ empty hat, sollte diese Eigenschaft auch leer sein.</span><span class="sxs-lookup"><span data-stu-id="1702f-111">If [System.ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) is VT\_EMPTY, then this property should also be empty.</span></span> <span data-ttu-id="1702f-112">Andernfalls sollte Sie von der Datenquelle aus System. itemfolderpathdisplay ordnungsgemäß abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="1702f-112">Otherwise, it should be derived appropriately by the data source from System.ItemFolderPathDisplay.</span></span>

<span data-ttu-id="1702f-113">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="1702f-113">Examples:</span></span>



| <span data-ttu-id="1702f-114">Gegebener Pfad</span><span class="sxs-lookup"><span data-stu-id="1702f-114">Given path</span></span>                             | <span data-ttu-id="1702f-115">Anzeige Name des Ordners</span><span class="sxs-lookup"><span data-stu-id="1702f-115">Folder Display Name</span></span> |
|----------------------------------------|---------------------|
| <span data-ttu-id="1702f-116">c: \\ myfiles- \\ Text \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="1702f-116">c:\\MyFiles\\Text\\hello.txt</span></span>           | <span data-ttu-id="1702f-117">Text</span><span class="sxs-lookup"><span data-stu-id="1702f-117">Text</span></span>                |
| <span data-ttu-id="1702f-118">\\\\Server \\ Freigabe \\ "MyDir" \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="1702f-118">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="1702f-119">"MyDir"</span><span class="sxs-lookup"><span data-stu-id="1702f-119">mydir</span></span>               |
| <span data-ttu-id="1702f-120">\\\\Server \\ Freigabe \\numbers.xls</span><span class="sxs-lookup"><span data-stu-id="1702f-120">\\\\server\\share\\numbers.xls</span></span>         | <span data-ttu-id="1702f-121">Freigeben</span><span class="sxs-lookup"><span data-stu-id="1702f-121">share</span></span>               |
| <span data-ttu-id="1702f-122">c: \\ Ordner \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="1702f-122">c:\\Folders\\MyFolder</span></span>                  | <span data-ttu-id="1702f-123">Ordner</span><span class="sxs-lookup"><span data-stu-id="1702f-123">Folders</span></span>             |
| <span data-ttu-id="1702f-124">/Mailbox Account/Inbox/"Re: Hello!"</span><span class="sxs-lookup"><span data-stu-id="1702f-124">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="1702f-125">Posteingang</span><span class="sxs-lookup"><span data-stu-id="1702f-125">Inbox</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="1702f-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1702f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1702f-127">propertydescription</span><span class="sxs-lookup"><span data-stu-id="1702f-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="1702f-128">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="1702f-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="1702f-129">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="1702f-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="1702f-130">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="1702f-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="1702f-131">Display Info</span><span class="sxs-lookup"><span data-stu-id="1702f-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="1702f-132">StringFormat</span><span class="sxs-lookup"><span data-stu-id="1702f-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="1702f-133">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="1702f-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="1702f-134">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="1702f-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="1702f-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="1702f-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="1702f-136">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="1702f-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="1702f-137">DrawControl</span><span class="sxs-lookup"><span data-stu-id="1702f-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="1702f-138">editcontrol</span><span class="sxs-lookup"><span data-stu-id="1702f-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="1702f-139">FilterControl</span><span class="sxs-lookup"><span data-stu-id="1702f-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="1702f-140">querycontrol</span><span class="sxs-lookup"><span data-stu-id="1702f-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
