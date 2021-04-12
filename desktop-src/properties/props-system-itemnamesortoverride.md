---
description: Diese Zeichenfolge sollte auf die phonetische Version des Anzeige namensfest gelegt werden, wie in "System. itemnamedisplay" in cjk-Gebiets Schemata (CHS Pinyin, JPN Hiragana, Kor Hangul usw.) definiert.
ms.assetid: eb491644-bf59-4439-9e9b-bcafde619d66
title: System. itemnamesoresverride
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d79f9bb07eb15eb5d25fbfa1e95d4c0f80b35611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217212"
---
# <a name="systemitemnamesortoverride"></a><span data-ttu-id="3420b-103">System. itemnamesoresverride</span><span class="sxs-lookup"><span data-stu-id="3420b-103">System.ItemNameSortOverride</span></span>

<span data-ttu-id="3420b-104">Diese Zeichenfolge sollte auf die phonetische Version des Anzeige namensfest gelegt werden, wie in "System. itemnamedisplay" in cjk-Gebiets Schemata (CHS Pinyin, JPN Hiragana, Kor Hangul usw.) definiert.</span><span class="sxs-lookup"><span data-stu-id="3420b-104">This string should be set to the phonetic version of the display name as defined in System.ItemNameDisplay in CJK locales(CHS Pinyin, JPN Hiragana, KOR Hangul, etc.).</span></span> <span data-ttu-id="3420b-105">Das erste Zeichen dieses Felds wird auch zum Gruppieren von Namen nach FirstLetter verwendet.</span><span class="sxs-lookup"><span data-stu-id="3420b-105">The first character of this field is also used for grouping names by firstletter.</span></span> <span data-ttu-id="3420b-106">Bei den meisten nicht-CJK-Sprachen muss dieses Feld nicht festgelegt werden (in diesem Fall wird System. itemnamedisplay verwendet). Wenn es jedoch wünschenswert ist, den Gruppierungs Buchstaben zu überschreiben (z. b. um führende Artikel wie z. b. "a" und "The" zu entfernen), kann hier eine Alternative Zeichenfolge angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3420b-106">For most non-CJK languages, this field does not need to be set (in which case System.ItemNameDisplay will be used).However, if it is desirable to override the grouping letter (for example, to remove leading articles such as "a" and "the"),an alternate string can be provided here.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="3420b-107">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8</span><span class="sxs-lookup"><span data-stu-id="3420b-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.ItemNameSortOverride
   shellPKey = PKEY_ItemNameSortOverride
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 23
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="3420b-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3420b-108">Remarks</span></span>

<span data-ttu-id="3420b-109">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="3420b-109">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3420b-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3420b-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3420b-111">propertydescription</span><span class="sxs-lookup"><span data-stu-id="3420b-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="3420b-112">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="3420b-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="3420b-113">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="3420b-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="3420b-114">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="3420b-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="3420b-115">Display Info</span><span class="sxs-lookup"><span data-stu-id="3420b-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="3420b-116">StringFormat</span><span class="sxs-lookup"><span data-stu-id="3420b-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="3420b-117">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="3420b-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="3420b-118">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="3420b-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="3420b-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="3420b-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="3420b-120">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="3420b-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="3420b-121">DrawControl</span><span class="sxs-lookup"><span data-stu-id="3420b-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="3420b-122">editcontrol</span><span class="sxs-lookup"><span data-stu-id="3420b-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="3420b-123">FilterControl</span><span class="sxs-lookup"><span data-stu-id="3420b-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="3420b-124">querycontrol</span><span class="sxs-lookup"><span data-stu-id="3420b-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
