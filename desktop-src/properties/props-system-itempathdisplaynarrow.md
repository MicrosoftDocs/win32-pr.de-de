---
description: Der benutzerfreundliche Anzeige Pfad zum Element.
ms.assetid: 5dd44e13-bc5c-4e32-b5eb-2c7c40e10dfb
title: System. itempathdisplaynarrow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ef7b9d03a78a23e955c20f52e32062a8bcabd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217520"
---
# <a name="systemitempathdisplaynarrow"></a><span data-ttu-id="995c4-103">System. itempathdisplaynarrow</span><span class="sxs-lookup"><span data-stu-id="995c4-103">System.ItemPathDisplayNarrow</span></span>

<span data-ttu-id="995c4-104">Der benutzerfreundliche Anzeige Pfad zum Element.</span><span class="sxs-lookup"><span data-stu-id="995c4-104">The user-friendly display path to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="995c4-105">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="995c4-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemPathDisplayNarrow
   shellPKey = PKEY_ItemPathDisplayNarrow
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 8
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="995c4-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="995c4-106">Remarks</span></span>

<span data-ttu-id="995c4-107">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="995c4-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="995c4-108">Um für eine schmale Anzeige Spalte zu optimieren, sollte das Format der Zeichenfolge so angepasst werden, dass der Name zuerst angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="995c4-108">To optimize for a narrow viewing column, the format of the string should be tailored so that the name comes first.</span></span>

<span data-ttu-id="995c4-109">Wenn es sich bei dem Element um eine Datei handelt, schließt der Eigenschafts Wert die Dateierweiterung aus, enthält jedoch lokalisierte Namen, sofern diese vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="995c4-109">If the item is a file, the property value excludes the file extension, but includes localized names if they are present.</span></span> <span data-ttu-id="995c4-110">Wenn das Element eine Meldung ist, enthält der Wert " [System. itemnameprefix](./props-system-itemnameprefix.md)".</span><span class="sxs-lookup"><span data-stu-id="995c4-110">If the item is a message, the value includes the [System.ItemNamePrefix](./props-system-itemnameprefix.md).</span></span> <span data-ttu-id="995c4-111">Um einen Element Pfad zu analysieren, verwenden Sie " [System. itemurl](./props-system-itemurl.md) " oder " [System. Parser Path](./props-system-parsingpath.md)".</span><span class="sxs-lookup"><span data-stu-id="995c4-111">To parse an item path, use [System.ItemUrl](./props-system-itemurl.md) or [System.ParsingPath](./props-system-parsingpath.md).</span></span>

<span data-ttu-id="995c4-112">Beispielwerte:</span><span class="sxs-lookup"><span data-stu-id="995c4-112">Example values:</span></span>



| <span data-ttu-id="995c4-113">Pfad</span><span class="sxs-lookup"><span data-stu-id="995c4-113">Path</span></span>                                   | <span data-ttu-id="995c4-114">Itempathdisplayname</span><span class="sxs-lookup"><span data-stu-id="995c4-114">ItemPathDisplayName</span></span>                 |
|----------------------------------------|-------------------------------------|
| <span data-ttu-id="995c4-115">c: \\ "MyDir"- \\ Leiste \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="995c4-115">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="995c4-116">Hello (c: \\ "MyDir"- \\ Leiste)</span><span class="sxs-lookup"><span data-stu-id="995c4-116">hello (c:\\mydir\\bar)</span></span>              |
| <span data-ttu-id="995c4-117">\\\\Server \\ Freigabe \\ "MyDir" \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="995c4-117">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="995c4-118">goodnews ( \\ \\ Server \\ Freigabe \\ mydir)</span><span class="sxs-lookup"><span data-stu-id="995c4-118">goodnews (\\\\server\\share\\mydir)</span></span> |
| <span data-ttu-id="995c4-119">\\\\Server \\ Freigabe \\ Ordner</span><span class="sxs-lookup"><span data-stu-id="995c4-119">\\\\server\\share\\folder</span></span>              | <span data-ttu-id="995c4-120">Ordner ( \\ \\ Server \\ Freigabe)</span><span class="sxs-lookup"><span data-stu-id="995c4-120">folder (\\\\server\\share)</span></span>          |
| <span data-ttu-id="995c4-121">c: \\ mydir \\ meinOrdner</span><span class="sxs-lookup"><span data-stu-id="995c4-121">c:\\MyDir\\MyFolder</span></span>                    | <span data-ttu-id="995c4-122">MyFolder (c: \\ mydir)</span><span class="sxs-lookup"><span data-stu-id="995c4-122">MyFolder (c:\\mydir)</span></span>                |
| <span data-ttu-id="995c4-123">/Mailbox Account/Inbox/"Re: Hello!"</span><span class="sxs-lookup"><span data-stu-id="995c4-123">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="995c4-124">Neu: Hallo!</span><span class="sxs-lookup"><span data-stu-id="995c4-124">Re: Hello!</span></span> <span data-ttu-id="995c4-125">(/Mailbox Account/Inbox)</span><span class="sxs-lookup"><span data-stu-id="995c4-125">(/Mailbox Account/Inbox)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="995c4-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="995c4-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="995c4-127">propertydescription</span><span class="sxs-lookup"><span data-stu-id="995c4-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="995c4-128">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="995c4-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="995c4-129">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="995c4-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="995c4-130">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="995c4-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="995c4-131">Display Info</span><span class="sxs-lookup"><span data-stu-id="995c4-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="995c4-132">StringFormat</span><span class="sxs-lookup"><span data-stu-id="995c4-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="995c4-133">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="995c4-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="995c4-134">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="995c4-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="995c4-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="995c4-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="995c4-136">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="995c4-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="995c4-137">DrawControl</span><span class="sxs-lookup"><span data-stu-id="995c4-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="995c4-138">editcontrol</span><span class="sxs-lookup"><span data-stu-id="995c4-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="995c4-139">FilterControl</span><span class="sxs-lookup"><span data-stu-id="995c4-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="995c4-140">querycontrol</span><span class="sxs-lookup"><span data-stu-id="995c4-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
