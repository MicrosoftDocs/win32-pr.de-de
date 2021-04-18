---
description: Ein Bewertungssystem, das ganzzahlige Werte zwischen 1 und 99 verwendet. Dies ist das Bewertungssystem, das von der Windows Vista-Shell verwendet wird.
ms.assetid: a6288d29-1ef3-4da1-bd30-577336ab6817
title: System. Rating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e411e313f0fa6042a8cbe3a076a7166928020af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351641"
---
# <a name="systemrating"></a><span data-ttu-id="a52de-104">System. Rating</span><span class="sxs-lookup"><span data-stu-id="a52de-104">System.Rating</span></span>

<span data-ttu-id="a52de-105">Ein Bewertungssystem, das ganzzahlige Werte zwischen 1 und 99 verwendet.</span><span class="sxs-lookup"><span data-stu-id="a52de-105">A rating system that uses integer values between 1 and 99.</span></span> <span data-ttu-id="a52de-106">Dies ist das Bewertungssystem, das von der Windows Vista-Shell verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a52de-106">This is the rating system used by the Windows Vista Shell.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="a52de-107">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="a52de-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Rating
   shellPKey = PKEY_Rating
   formatID = 64440492-4C8B-11D1-8B70-080036B11A03
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = OneStar
            minValue = 1
            setValue = 1
            defineMaxValue = 12
            text = 1 Star
            defineToken = RATING_ONE_STAR
         enumRange
            name = TwoStars
            minValue = 13
            setValue = 25
            defineMaxValue = 37
            text = 2 Stars
            defineToken = RATING_TWO_STARS
         enumRange
            name = ThreeStars
            minValue = 38
            setValue = 50
            defineMaxValue = 62
            text = 3 Stars
            defineToken = RATING_THREE_STARS
         enumRange
            name = FourStars
            minValue = 63
            setValue = 75
            defineMaxValue = 87
            text = 4 Stars
            defineToken = RATING_FOUR_STARS
         enumRange
            name = FiveStars
            minValue = 88
            setValue = 99
            defineMaxValue = 99
            text = 5 Stars
            defineToken = RATING_FIVE_STARS
         enumRange
            name
            minValue = 100
```

## <a name="windows-vista"></a><span data-ttu-id="a52de-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a52de-108">Windows Vista</span></span>

```
propertyDescription
   name = System.Rating
   shellPKey = PKEY_Rating
   formatID = 64440492-4C8B-11D1-8B70-080036B11A03
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            defineMinName = RATING_UNRATED_MIN
            setValue = 0
            defineSetName = RATING_UNRATED_SET
            defineMaxValue = 0
            defineMaxName = RATING_UNRATED_MAX
            text = Unrated
         enumRange
            minValue = 1
            defineMinName = RATING_ONE_STAR_MIN
            setValue = 1
            defineSetName = RATING_ONE_STAR_SET
            defineMaxValue = 12
            defineMaxName = RATING_ONE_STAR_MAX
            text = 1 Star
         enumRange
            minValue = 13
            defineMinName = RATING_TWO_STARS_MIN
            setValue = 25
            defineSetName = RATING_TWO_STARS_SET
            defineMaxValue = 37
            defineMaxName = RATING_TWO_STARS_MAX
            text = 2 Stars
         enumRange
            minValue = 38
            defineMinName = RATING_THREE_STARS_MIN
            setValue = 50
            defineSetName = RATING_THREE_STARS_SET
            defineMaxValue = 62
            defineMaxName = RATING_THREE_STARS_MAX
            text = 3 Stars
         enumRange
            minValue = 63
            defineMinName = RATING_FOUR_STARS_MIN
            setValue = 75
            defineSetName = RATING_FOUR_STARS_SET
            defineMaxValue = 87
            defineMaxName = RATING_FOUR_STARS_MAX
            text = 4 Stars
         enumRange
            minValue = 88
            defineMinName = RATING_FIVE_STARS_MIN
            setValue = 99
            defineSetName = RATING_FIVE_STARS_SET
            defineMaxValue = 99
            defineMaxName = RATING_FIVE_STARS_MAX
            text = 5 Stars
         enumRange
            minValue = 100
```

## <a name="remarks"></a><span data-ttu-id="a52de-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a52de-109">Remarks</span></span>

<span data-ttu-id="a52de-110">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="a52de-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="a52de-111">Informationen zur Kompatibilität mit Bewertungssystemen, die Werte zwischen 1 und 5 verwenden, finden Sie unter Eigenschaften [System. simplerating](./props-system-simplerating.md).</span><span class="sxs-lookup"><span data-stu-id="a52de-111">For compatibility with ratings systems that use values between 1 and 5, see the property [System.SimpleRating](./props-system-simplerating.md).</span></span> <span data-ttu-id="a52de-112">Beachten Sie jedoch, dass System. simplerating in der Windows Vista-Shell nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a52de-112">Note, however, that System.SimpleRating is not used in the Windows Vista Shell.</span></span>

<span data-ttu-id="a52de-113">In der folgenden Tabelle wird beschrieben, was das in der Shell-Benutzeroberfläche verwendete sternbewertungssystem im Hinblick auf den [System. Rating]() -Wert bedeutet.</span><span class="sxs-lookup"><span data-stu-id="a52de-113">The following table describes what the star rating system used in the Shell UI means in terms of the [System.Rating]() value.</span></span>



| <span data-ttu-id="a52de-114">System. Rating</span><span class="sxs-lookup"><span data-stu-id="a52de-114">System.Rating</span></span> | <span data-ttu-id="a52de-115">Bewertung mit Sternen</span><span class="sxs-lookup"><span data-stu-id="a52de-115">Star Rating</span></span> |
|---------------|-------------|
| <span data-ttu-id="a52de-116">1-12</span><span class="sxs-lookup"><span data-stu-id="a52de-116">1-12</span></span>          | <span data-ttu-id="a52de-117">Ein Stern</span><span class="sxs-lookup"><span data-stu-id="a52de-117">1 Star</span></span>      |
| <span data-ttu-id="a52de-118">13-37</span><span class="sxs-lookup"><span data-stu-id="a52de-118">13-37</span></span>         | <span data-ttu-id="a52de-119">Zwei Sterne</span><span class="sxs-lookup"><span data-stu-id="a52de-119">2 Stars</span></span>     |
| <span data-ttu-id="a52de-120">38-62</span><span class="sxs-lookup"><span data-stu-id="a52de-120">38-62</span></span>         | <span data-ttu-id="a52de-121">Drei Sterne</span><span class="sxs-lookup"><span data-stu-id="a52de-121">3 Stars</span></span>     |
| <span data-ttu-id="a52de-122">63-87</span><span class="sxs-lookup"><span data-stu-id="a52de-122">63-87</span></span>         | <span data-ttu-id="a52de-123">Vier Sterne</span><span class="sxs-lookup"><span data-stu-id="a52de-123">4 Stars</span></span>     |
| <span data-ttu-id="a52de-124">88-99</span><span class="sxs-lookup"><span data-stu-id="a52de-124">88-99</span></span>         | <span data-ttu-id="a52de-125">Fünf Sterne</span><span class="sxs-lookup"><span data-stu-id="a52de-125">5 Stars</span></span>     |



 

<span data-ttu-id="a52de-126">Wenn ein Benutzer ein Element durch Auswahl eines Stern Bewertungs Werts in der Benutzeroberfläche bewertet, werden die tatsächlichen [System. Rating]() -Werte wie in der folgenden Tabelle dargestellt zugewiesen:</span><span class="sxs-lookup"><span data-stu-id="a52de-126">When a user rates an item by choosing a star rating value in the UI, actual [System.Rating]() values are assigned as shown in this table:</span></span>



| <span data-ttu-id="a52de-127">Bewertung mit Sternen</span><span class="sxs-lookup"><span data-stu-id="a52de-127">Star Rating</span></span> | <span data-ttu-id="a52de-128">Über die Benutzeroberfläche zugewiesener Wert</span><span class="sxs-lookup"><span data-stu-id="a52de-128">Value Assigned Through UI</span></span> |
|-------------|---------------------------|
| <span data-ttu-id="a52de-129">Ein Stern</span><span class="sxs-lookup"><span data-stu-id="a52de-129">1 Star</span></span>      | <span data-ttu-id="a52de-130">1</span><span class="sxs-lookup"><span data-stu-id="a52de-130">1</span></span>                         |
| <span data-ttu-id="a52de-131">Zwei Sterne</span><span class="sxs-lookup"><span data-stu-id="a52de-131">2 Stars</span></span>     | <span data-ttu-id="a52de-132">25</span><span class="sxs-lookup"><span data-stu-id="a52de-132">25</span></span>                        |
| <span data-ttu-id="a52de-133">Drei Sterne</span><span class="sxs-lookup"><span data-stu-id="a52de-133">3 Stars</span></span>     | <span data-ttu-id="a52de-134">50</span><span class="sxs-lookup"><span data-stu-id="a52de-134">50</span></span>                        |
| <span data-ttu-id="a52de-135">Vier Sterne</span><span class="sxs-lookup"><span data-stu-id="a52de-135">4 Stars</span></span>     | <span data-ttu-id="a52de-136">75</span><span class="sxs-lookup"><span data-stu-id="a52de-136">75</span></span>                        |
| <span data-ttu-id="a52de-137">Fünf Sterne</span><span class="sxs-lookup"><span data-stu-id="a52de-137">5 Stars</span></span>     | <span data-ttu-id="a52de-138">99</span><span class="sxs-lookup"><span data-stu-id="a52de-138">99</span></span>                        |



 

<span data-ttu-id="a52de-139">Wenn die Datei einen [System. simplerating](./props-system-simplerating.md) -Wert anstelle eines [System. Rating]() -Werts aufweist, verwenden Sie die folgende Tabelle, um Werte für System. Rating zu konvertieren und anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a52de-139">If your file has a [System.SimpleRating](./props-system-simplerating.md) value rather than a [System.Rating]() value, use the table below to convert and specify values for System.Rating.</span></span>



| <span data-ttu-id="a52de-140">System. simplerating</span><span class="sxs-lookup"><span data-stu-id="a52de-140">System.SimpleRating</span></span> | <span data-ttu-id="a52de-141">System. Rating</span><span class="sxs-lookup"><span data-stu-id="a52de-141">System.Rating</span></span> |
|---------------------|---------------|
| <span data-ttu-id="a52de-142">1</span><span class="sxs-lookup"><span data-stu-id="a52de-142">1</span></span>                   | <span data-ttu-id="a52de-143">1</span><span class="sxs-lookup"><span data-stu-id="a52de-143">1</span></span>             |
| <span data-ttu-id="a52de-144">2</span><span class="sxs-lookup"><span data-stu-id="a52de-144">2</span></span>                   | <span data-ttu-id="a52de-145">25</span><span class="sxs-lookup"><span data-stu-id="a52de-145">25</span></span>            |
| <span data-ttu-id="a52de-146">3</span><span class="sxs-lookup"><span data-stu-id="a52de-146">3</span></span>                   | <span data-ttu-id="a52de-147">50</span><span class="sxs-lookup"><span data-stu-id="a52de-147">50</span></span>            |
| <span data-ttu-id="a52de-148">4</span><span class="sxs-lookup"><span data-stu-id="a52de-148">4</span></span>                   | <span data-ttu-id="a52de-149">75</span><span class="sxs-lookup"><span data-stu-id="a52de-149">75</span></span>            |
| <span data-ttu-id="a52de-150">5</span><span class="sxs-lookup"><span data-stu-id="a52de-150">5</span></span>                   | <span data-ttu-id="a52de-151">99</span><span class="sxs-lookup"><span data-stu-id="a52de-151">99</span></span>            |



 

<span data-ttu-id="a52de-152">Wenn die Datei sowohl [System. Rating]() als auch [System. simplerating](./props-system-simplerating.md) persistent ist, verwenden Sie immer den Wert System. Rating, wenn Sie direkt angefordert wird, ohne dass auf System. simplerating verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="a52de-152">If your file has both [System.Rating]() and [System.SimpleRating](./props-system-simplerating.md) persisted values, always use the System.Rating value when it is directly requested, without reference to System.SimpleRating.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a52de-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a52de-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a52de-154">propertydescription</span><span class="sxs-lookup"><span data-stu-id="a52de-154">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="a52de-155">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="a52de-155">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="a52de-156">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="a52de-156">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="a52de-157">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="a52de-157">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="a52de-158">Display Info</span><span class="sxs-lookup"><span data-stu-id="a52de-158">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="a52de-159">StringFormat</span><span class="sxs-lookup"><span data-stu-id="a52de-159">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="a52de-160">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="a52de-160">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="a52de-161">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="a52de-161">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="a52de-162">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="a52de-162">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="a52de-163">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="a52de-163">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="a52de-164">DrawControl</span><span class="sxs-lookup"><span data-stu-id="a52de-164">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="a52de-165">editcontrol</span><span class="sxs-lookup"><span data-stu-id="a52de-165">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="a52de-166">FilterControl</span><span class="sxs-lookup"><span data-stu-id="a52de-166">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="a52de-167">querycontrol</span><span class="sxs-lookup"><span data-stu-id="a52de-167">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
