---
description: Der benutzerfreundliche Anzeige Pfad zum Element.
ms.assetid: 27e4490b-7914-4b38-9799-e9d5dc407f13
title: System. itempathdisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb76a4218e7e7580ec70cb57dd16c635ca024ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131573"
---
# <a name="systemitempathdisplay"></a><span data-ttu-id="b8a0c-103">System. itempathdisplay</span><span class="sxs-lookup"><span data-stu-id="b8a0c-103">System.ItemPathDisplay</span></span>

<span data-ttu-id="b8a0c-104">Der benutzerfreundliche Anzeige Pfad zum Element.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-104">The user-friendly display path to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="b8a0c-105">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8a0c-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

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

## <a name="remarks"></a><span data-ttu-id="b8a0c-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8a0c-106">Remarks</span></span>

<span data-ttu-id="b8a0c-107">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="b8a0c-108">Wenn es sich bei dem Element um eine Datei oder einen Ordner handelt, enthält diese Eigenschaft in allen Fällen die Erweiterung und wird lokalisiert, wenn ein lokalisierter Name verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-108">If the item is a file or folder, this property includes the extension in all cases, and is localized if a localized name is available.</span></span> <span data-ttu-id="b8a0c-109">Bei anderen Elementen ist dies die benutzerfreundliche Entsprechung, wobei angenommen wird, dass das Element im hierarchischen Speicher vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-109">For other items, this is the user-friendly equivalent, assuming that the item exists in hierarchical storage.</span></span>

<span data-ttu-id="b8a0c-110">Im Gegensatz zu [System. itemurl](./props-system-itemurl.md)enthält dieser Eigenschafts Wert nicht das URL-Schema.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-110">Unlike [System.ItemUrl](./props-system-itemurl.md), this property value does not include the URL scheme.</span></span> <span data-ttu-id="b8a0c-111">Um einen Element Pfad zu analysieren, verwenden Sie "System. itemurl" oder " [System. Parser Path](./props-system-parsingpath.md)".</span><span class="sxs-lookup"><span data-stu-id="b8a0c-111">To parse an item path, use System.ItemUrl or [System.ParsingPath](./props-system-parsingpath.md).</span></span> <span data-ttu-id="b8a0c-112">Verwenden Sie zum Verweisen auf Shell-Namespace Elemente mithilfe von Shell-APIs System. Parser Path.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-112">To reference Shell namespace items using Shell APIs, use System.ParsingPath.</span></span>

<span data-ttu-id="b8a0c-113">Beispielwerte:</span><span class="sxs-lookup"><span data-stu-id="b8a0c-113">Example values:</span></span>



| <span data-ttu-id="b8a0c-114">Pfad</span><span class="sxs-lookup"><span data-stu-id="b8a0c-114">Path</span></span>                                   | <span data-ttu-id="b8a0c-115">Itempathdisplay</span><span class="sxs-lookup"><span data-stu-id="b8a0c-115">ItemPathDisplay</span></span>                        |
|----------------------------------------|----------------------------------------|
| <span data-ttu-id="b8a0c-116">c: \\ "MyDir"- \\ Leiste \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="b8a0c-116">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="b8a0c-117">c: \\ "MyDir"- \\ Leiste \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="b8a0c-117">c:\\mydir\\bar\\hello.txt</span></span>              |
| <span data-ttu-id="b8a0c-118">\\\\Server \\ Freigabe \\ "MyDir" \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="b8a0c-118">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="b8a0c-119">\\\\Server \\ Freigabe \\ "MyDir" \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="b8a0c-119">\\\\server\\share\\mydir\\goodnews.doc</span></span> |
| <span data-ttu-id="b8a0c-120">\\\\Server \\ Freigabe \\numbers.xls</span><span class="sxs-lookup"><span data-stu-id="b8a0c-120">\\\\server\\share\\numbers.xls</span></span>         | <span data-ttu-id="b8a0c-121">\\\\Server \\ Freigabe \\numbers.xls</span><span class="sxs-lookup"><span data-stu-id="b8a0c-121">\\\\server\\share\\numbers.xls</span></span>         |
| <span data-ttu-id="b8a0c-122">c: \\ "MyDir" \\ meinOrdner</span><span class="sxs-lookup"><span data-stu-id="b8a0c-122">c:\\mydir\\MyFolder</span></span>                    | <span data-ttu-id="b8a0c-123">c: \\ "MyDir" \\ meinOrdner</span><span class="sxs-lookup"><span data-stu-id="b8a0c-123">c:\\mydir\\MyFolder</span></span>                    |
| <span data-ttu-id="b8a0c-124">/Mailbox Account/Inbox/"Re: Hello!"</span><span class="sxs-lookup"><span data-stu-id="b8a0c-124">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="b8a0c-125">/Mailbox Account/Inbox/"Re: Hello!"</span><span class="sxs-lookup"><span data-stu-id="b8a0c-125">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="b8a0c-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b8a0c-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8a0c-127">propertydescription</span><span class="sxs-lookup"><span data-stu-id="b8a0c-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="b8a0c-128">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="b8a0c-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="b8a0c-129">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="b8a0c-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="b8a0c-130">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="b8a0c-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="b8a0c-131">Display Info</span><span class="sxs-lookup"><span data-stu-id="b8a0c-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="b8a0c-132">StringFormat</span><span class="sxs-lookup"><span data-stu-id="b8a0c-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="b8a0c-133">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="b8a0c-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="b8a0c-134">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="b8a0c-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="b8a0c-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="b8a0c-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="b8a0c-136">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="b8a0c-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="b8a0c-137">DrawControl</span><span class="sxs-lookup"><span data-stu-id="b8a0c-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="b8a0c-138">editcontrol</span><span class="sxs-lookup"><span data-stu-id="b8a0c-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="b8a0c-139">FilterControl</span><span class="sxs-lookup"><span data-stu-id="b8a0c-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="b8a0c-140">querycontrol</span><span class="sxs-lookup"><span data-stu-id="b8a0c-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
