---
description: Der benutzerfreundliche Anzeige Pfad für den übergeordneten Ordner eines Elements.
ms.assetid: 16f67edc-ca8a-4c2e-9d9b-be8600446e51
title: System. itemfolderpathdisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c4ae4c9178356d36c644f1bc886d63331155e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359012"
---
# <a name="systemitemfolderpathdisplay"></a><span data-ttu-id="0172c-103">System. itemfolderpathdisplay</span><span class="sxs-lookup"><span data-stu-id="0172c-103">System.ItemFolderPathDisplay</span></span>

<span data-ttu-id="0172c-104">Der benutzerfreundliche Anzeige Pfad für den übergeordneten Ordner eines Elements.</span><span class="sxs-lookup"><span data-stu-id="0172c-104">The user-friendly display path of an item's parent folder.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="0172c-105">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0172c-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemFolderPathDisplay
   shellPKey = PKEY_ItemFolderPathDisplay
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 6
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="0172c-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0172c-106">Remarks</span></span>

<span data-ttu-id="0172c-107">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="0172c-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="0172c-108">Wenn [System. itempathdisplay](./props-system-itempathdisplay.md) den Wert VT \_ empty hat, sollte diese Eigenschaft auch leer sein.</span><span class="sxs-lookup"><span data-stu-id="0172c-108">If [System.ItemPathDisplay](./props-system-itempathdisplay.md) is VT\_EMPTY, then this property should also be empty.</span></span> <span data-ttu-id="0172c-109">Andernfalls sollte Sie von der Datenquelle aus System. itempathdisplay ordnungsgemäß abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="0172c-109">Otherwise, it should be derived appropriately by the data source from System.ItemPathDisplay.</span></span>

<span data-ttu-id="0172c-110">Beispielwerte:</span><span class="sxs-lookup"><span data-stu-id="0172c-110">Example values:</span></span>



| <span data-ttu-id="0172c-111">Pfad</span><span class="sxs-lookup"><span data-stu-id="0172c-111">Path</span></span>                                   | <span data-ttu-id="0172c-112">Itemfolderpathdisplay</span><span class="sxs-lookup"><span data-stu-id="0172c-112">ItemFolderPathDisplay</span></span>    |
|----------------------------------------|--------------------------|
| <span data-ttu-id="0172c-113">c: \\ \\ Eigene Dateien \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="0172c-113">c:\\files\\personal\\hello.txt</span></span>         | <span data-ttu-id="0172c-114">c: \\ \\ persönliche Dateien</span><span class="sxs-lookup"><span data-stu-id="0172c-114">c:\\files\\personal</span></span>      |
| <span data-ttu-id="0172c-115">\\\\Server \\ Freigabe \\ "MyDir" \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="0172c-115">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="0172c-116">\\\\Server \\ Freigabe \\ "MyDir"</span><span class="sxs-lookup"><span data-stu-id="0172c-116">\\\\server\\share\\mydir</span></span> |
| <span data-ttu-id="0172c-117">\\\\Server \\ Freigabe \\numbers.xls</span><span class="sxs-lookup"><span data-stu-id="0172c-117">\\\\server\\share\\numbers.xls</span></span>         | <span data-ttu-id="0172c-118">\\\\Server \\ Freigabe</span><span class="sxs-lookup"><span data-stu-id="0172c-118">\\\\server\\share</span></span>        |
| <span data-ttu-id="0172c-119">c: \\ Nahrungsmittel \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="0172c-119">c:\\food\\MyFolder</span></span>                     | <span data-ttu-id="0172c-120">c: \\ Nahrungsmittel</span><span class="sxs-lookup"><span data-stu-id="0172c-120">c:\\food</span></span>                 |
| <span data-ttu-id="0172c-121">/Mailbox Account/Inbox/"Re: Hello!"</span><span class="sxs-lookup"><span data-stu-id="0172c-121">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="0172c-122">/Mailbox Konto/Eingangsbox</span><span class="sxs-lookup"><span data-stu-id="0172c-122">/Mailbox Account/Inbox</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="0172c-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0172c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0172c-124">propertydescription</span><span class="sxs-lookup"><span data-stu-id="0172c-124">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="0172c-125">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="0172c-125">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="0172c-126">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="0172c-126">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="0172c-127">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="0172c-127">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="0172c-128">Display Info</span><span class="sxs-lookup"><span data-stu-id="0172c-128">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="0172c-129">StringFormat</span><span class="sxs-lookup"><span data-stu-id="0172c-129">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="0172c-130">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="0172c-130">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="0172c-131">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="0172c-131">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="0172c-132">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="0172c-132">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="0172c-133">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="0172c-133">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="0172c-134">DrawControl</span><span class="sxs-lookup"><span data-stu-id="0172c-134">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="0172c-135">editcontrol</span><span class="sxs-lookup"><span data-stu-id="0172c-135">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="0172c-136">FilterControl</span><span class="sxs-lookup"><span data-stu-id="0172c-136">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="0172c-137">querycontrol</span><span class="sxs-lookup"><span data-stu-id="0172c-137">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
