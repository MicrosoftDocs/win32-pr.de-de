---
description: Erfahren Sie mehr über die System.ItemPathDisplay-Eigenschaft, die den benutzerfreundlichen Anzeigepfad zum Element darstellt.
ms.assetid: 27e4490b-7914-4b38-9799-e9d5dc407f13
title: System.ItemPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ddad0edbc1a77a3de1fab7956d8ce6e6f906f06
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403903"
---
# <a name="systemitempathdisplay"></a><span data-ttu-id="9de5b-103">System.ItemPathDisplay</span><span class="sxs-lookup"><span data-stu-id="9de5b-103">System.ItemPathDisplay</span></span>

<span data-ttu-id="9de5b-104">Der benutzerfreundliche Anzeigepfad zum Element.</span><span class="sxs-lookup"><span data-stu-id="9de5b-104">The user-friendly display path to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="9de5b-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9de5b-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemPathDisplay
   shellPKey = PKEY_ItemPathDisplay
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 7
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="9de5b-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9de5b-106">Remarks</span></span>

<span data-ttu-id="9de5b-107">PKEY-Werte werden in Propkey.h definiert.</span><span class="sxs-lookup"><span data-stu-id="9de5b-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="9de5b-108">Wenn es sich bei dem Element um eine Datei oder einen Ordner handelt, enthält diese Eigenschaft in allen Fällen die Erweiterung und wird lokalisiert, wenn ein lokalisierter Name verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="9de5b-108">If the item is a file or folder, this property includes the extension in all cases, and is localized if a localized name is available.</span></span> <span data-ttu-id="9de5b-109">Für andere Elemente ist dies die benutzerfreundliche Entsprechung, vorausgesetzt, dass das Element im hierarchischen Speicher vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9de5b-109">For other items, this is the user-friendly equivalent, assuming that the item exists in hierarchical storage.</span></span>

<span data-ttu-id="9de5b-110">Im [Gegensatz zu System.ItemUrl](./props-system-itemurl.md)enthält dieser Eigenschaftswert nicht das URL-Schema.</span><span class="sxs-lookup"><span data-stu-id="9de5b-110">Unlike [System.ItemUrl](./props-system-itemurl.md), this property value does not include the URL scheme.</span></span> <span data-ttu-id="9de5b-111">Um einen Elementpfad zu analysieren, verwenden Sie System.ItemUrl oder [System.ParsingPath](./props-system-parsingpath.md).</span><span class="sxs-lookup"><span data-stu-id="9de5b-111">To parse an item path, use System.ItemUrl or [System.ParsingPath](./props-system-parsingpath.md).</span></span> <span data-ttu-id="9de5b-112">Verwenden Sie System.ParsingPath, um mithilfe von Shell-APIs auf Shellnamespaceelemente zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="9de5b-112">To reference Shell namespace items using Shell APIs, use System.ParsingPath.</span></span>

<span data-ttu-id="9de5b-113">Beispielwerte:</span><span class="sxs-lookup"><span data-stu-id="9de5b-113">Example values:</span></span>



| <span data-ttu-id="9de5b-114">Pfad</span><span class="sxs-lookup"><span data-stu-id="9de5b-114">Path</span></span>                                   | <span data-ttu-id="9de5b-115">ItemPathDisplay</span><span class="sxs-lookup"><span data-stu-id="9de5b-115">ItemPathDisplay</span></span>                        |
|----------------------------------------|----------------------------------------|
| <span data-ttu-id="9de5b-116">c: \\ mydir \\ bar \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="9de5b-116">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="9de5b-117">c: \\ mydir \\ bar \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="9de5b-117">c:\\mydir\\bar\\hello.txt</span></span>              |
| <span data-ttu-id="9de5b-118">\\\\server \\ share \\ mydir \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="9de5b-118">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="9de5b-119">\\\\server \\ share \\ mydir \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="9de5b-119">\\\\server\\share\\mydir\\goodnews.doc</span></span> |
| <span data-ttu-id="9de5b-120">\\\\Serverfreigabe \\ \\numbers.xls</span><span class="sxs-lookup"><span data-stu-id="9de5b-120">\\\\server\\share\\numbers.xls</span></span>         | <span data-ttu-id="9de5b-121">\\\\Serverfreigabe \\ \\numbers.xls</span><span class="sxs-lookup"><span data-stu-id="9de5b-121">\\\\server\\share\\numbers.xls</span></span>         |
| <span data-ttu-id="9de5b-122">c: \\ mydir \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="9de5b-122">c:\\mydir\\MyFolder</span></span>                    | <span data-ttu-id="9de5b-123">c: \\ mydir \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="9de5b-123">c:\\mydir\\MyFolder</span></span>                    |
| <span data-ttu-id="9de5b-124">/Postfachkonto/Posteingang/'Re: Hello!'</span><span class="sxs-lookup"><span data-stu-id="9de5b-124">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="9de5b-125">/Postfachkonto/Posteingang/'Re: Hello!'</span><span class="sxs-lookup"><span data-stu-id="9de5b-125">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="9de5b-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9de5b-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9de5b-127">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="9de5b-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="9de5b-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="9de5b-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="9de5b-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="9de5b-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="9de5b-130">Typeinfo</span><span class="sxs-lookup"><span data-stu-id="9de5b-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="9de5b-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="9de5b-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="9de5b-132">Stringformat</span><span class="sxs-lookup"><span data-stu-id="9de5b-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="9de5b-133">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="9de5b-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="9de5b-134">Numberformat</span><span class="sxs-lookup"><span data-stu-id="9de5b-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="9de5b-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="9de5b-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="9de5b-136">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="9de5b-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="9de5b-137">drawControl</span><span class="sxs-lookup"><span data-stu-id="9de5b-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="9de5b-138">editControl</span><span class="sxs-lookup"><span data-stu-id="9de5b-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="9de5b-139">Filtercontrol</span><span class="sxs-lookup"><span data-stu-id="9de5b-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="9de5b-140">queryControl</span><span class="sxs-lookup"><span data-stu-id="9de5b-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
