---
description: 'Das Präfix eines Elements, das für e-Mail-Nachrichten verwendet wird, bei denen der Betreff mit dem Präfix &\# 0034 Re: &\# 0034;.'
ms.assetid: 3c257edc-b7f7-498d-8347-0be4fca41023
title: System. itemnameprefix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf669dd867c8cf60046f226e33dae18f46060cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959130"
---
# <a name="systemitemnameprefix"></a><span data-ttu-id="f7cae-103">System. itemnameprefix</span><span class="sxs-lookup"><span data-stu-id="f7cae-103">System.ItemNamePrefix</span></span>

<span data-ttu-id="f7cae-104">Das Präfix eines Elements, das für e-Mail-Nachrichten verwendet wird, wobei der Betreff mit dem Präfix "Re:" beginnt.</span><span class="sxs-lookup"><span data-stu-id="f7cae-104">The prefix of an item, used for e-mail messages where the subject begins with the prefix "Re:".</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="f7cae-105">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7cae-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemNamePrefix
   shellPKey = PKEY_ItemNamePrefix
   formatID = D7313FF1-A77A-401C-8C99-3DBDD68ADD36
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="f7cae-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7cae-106">Remarks</span></span>

<span data-ttu-id="f7cae-107">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="f7cae-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="f7cae-108">Wenn es sich bei dem Element um eine Datei handelt, ist der Wert dieser Eigenschaft VT \_ empty.</span><span class="sxs-lookup"><span data-stu-id="f7cae-108">If the item is a file, then the value of this property is VT\_EMPTY.</span></span> <span data-ttu-id="f7cae-109">Wenn es sich bei dem Element um eine Nachricht handelt, ist der Wert dieser Eigenschaft die Weiterleitungs-oder Antwort Präfixe (einschließlich des Trenn Zeichens, aber ohne Leerzeichen), oder VT \_ empty, wenn kein Präfix vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f7cae-109">If the item is a message, then the value of this property is the forwarding or reply prefixes (including the delimiting colon, but no whitespace), or VT\_EMPTY if there is no prefix.</span></span>

<span data-ttu-id="f7cae-110">Beispielwerte:</span><span class="sxs-lookup"><span data-stu-id="f7cae-110">Example values:</span></span>



| <span data-ttu-id="f7cae-111">System. itemnameprefix</span><span class="sxs-lookup"><span data-stu-id="f7cae-111">System.ItemNamePrefix</span></span> | <span data-ttu-id="f7cae-112">System. ItemName</span><span class="sxs-lookup"><span data-stu-id="f7cae-112">System.ItemName</span></span>  | <span data-ttu-id="f7cae-113">System.ItemNameDisplay</span><span class="sxs-lookup"><span data-stu-id="f7cae-113">System.ItemNameDisplay</span></span> |
|-----------------------|------------------|------------------------|
| <span data-ttu-id="f7cae-114">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="f7cae-114">VT\_EMPTY</span></span>             | <span data-ttu-id="f7cae-115">"Toller Tag"</span><span class="sxs-lookup"><span data-stu-id="f7cae-115">"Great day"</span></span>      | <span data-ttu-id="f7cae-116">"Toller Tag"</span><span class="sxs-lookup"><span data-stu-id="f7cae-116">"Great day"</span></span>            |
| <span data-ttu-id="f7cae-117">"Re:"</span><span class="sxs-lookup"><span data-stu-id="f7cae-117">"Re:"</span></span>                 | <span data-ttu-id="f7cae-118">"Toller Tag"</span><span class="sxs-lookup"><span data-stu-id="f7cae-118">"Great day"</span></span>      | <span data-ttu-id="f7cae-119">"Re: tolle Tage"</span><span class="sxs-lookup"><span data-stu-id="f7cae-119">"Re: Great day"</span></span>        |
| <span data-ttu-id="f7cae-120">"F":</span><span class="sxs-lookup"><span data-stu-id="f7cae-120">"Fwd: "</span></span>               | <span data-ttu-id="f7cae-121">"Monatliches Budget"</span><span class="sxs-lookup"><span data-stu-id="f7cae-121">"Monthly budget"</span></span> | <span data-ttu-id="f7cae-122">"F: Monatliches Budget"</span><span class="sxs-lookup"><span data-stu-id="f7cae-122">"Fwd: Monthly budget"</span></span>  |
| <span data-ttu-id="f7cae-123">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="f7cae-123">VT\_EMPTY</span></span>             | <span data-ttu-id="f7cae-124">accounts.xls</span><span class="sxs-lookup"><span data-stu-id="f7cae-124">accounts.xls</span></span>     | <span data-ttu-id="f7cae-125">accounts.xls</span><span class="sxs-lookup"><span data-stu-id="f7cae-125">accounts.xls</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="f7cae-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f7cae-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7cae-127">propertydescription</span><span class="sxs-lookup"><span data-stu-id="f7cae-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="f7cae-128">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="f7cae-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="f7cae-129">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="f7cae-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="f7cae-130">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="f7cae-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="f7cae-131">Display Info</span><span class="sxs-lookup"><span data-stu-id="f7cae-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="f7cae-132">StringFormat</span><span class="sxs-lookup"><span data-stu-id="f7cae-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="f7cae-133">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="f7cae-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="f7cae-134">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="f7cae-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="f7cae-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="f7cae-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="f7cae-136">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="f7cae-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="f7cae-137">DrawControl</span><span class="sxs-lookup"><span data-stu-id="f7cae-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="f7cae-138">editcontrol</span><span class="sxs-lookup"><span data-stu-id="f7cae-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="f7cae-139">FilterControl</span><span class="sxs-lookup"><span data-stu-id="f7cae-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="f7cae-140">querycontrol</span><span class="sxs-lookup"><span data-stu-id="f7cae-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
