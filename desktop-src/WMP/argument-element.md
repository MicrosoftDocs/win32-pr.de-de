---
title: Argument-Element
description: Das Argument-Element enthält einen Teil einer Bedingungs Zeichenfolge.
ms.assetid: 7e4744ce-e9e2-4a70-a2cc-d33ae1ad2f99
keywords:
- Argument Element Windows Media Player
topic_type:
- apiref
api_name:
- argument Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c4adc0b853054d448bc9955f3bd8c64115ac2ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371187"
---
# <a name="argument-element"></a><span data-ttu-id="d4dfc-104">Argument-Element</span><span class="sxs-lookup"><span data-stu-id="d4dfc-104">argument Element</span></span>

<span data-ttu-id="d4dfc-105">Das **Argument** -Element enthält einen Teil einer Bedingungs Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d4dfc-105">The **argument** element contains one portion of a condition string.</span></span> <span data-ttu-id="d4dfc-106">Eine Bedingungs Zeichenfolge weist in der Regel einen Bedingungs Teil und einen Wertanteil auf.</span><span class="sxs-lookup"><span data-stu-id="d4dfc-106">A condition string typically has a condition portion and a value portion.</span></span> <span data-ttu-id="d4dfc-107">In der Bedingungs Zeichenfolge "Artist ist beispielsweise Joe" ist der Bedingungs Teil "ist" und der Wert Teil "Joe".</span><span class="sxs-lookup"><span data-stu-id="d4dfc-107">For example, in the condition string "Artist Equals Joe", the condition portion is "Equals" and the value portion is "Joe".</span></span>

``` syntax
<argument
   name = "string"
>
   string
</argument>
        
```

## <a name="attributes"></a><span data-ttu-id="d4dfc-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d4dfc-108">Attributes</span></span>

<span data-ttu-id="d4dfc-109">**Name** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="d4dfc-109">**name** (required)</span></span>

<span data-ttu-id="d4dfc-110">Der Name eines Teils der Bedingungs Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d4dfc-110">The name of one portion of the condition string.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="d4dfc-111">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="d4dfc-111">Parent/Child Elements</span></span>



| <span data-ttu-id="d4dfc-112">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="d4dfc-112">Hierarchy</span></span> | <span data-ttu-id="d4dfc-113">Elemente</span><span class="sxs-lookup"><span data-stu-id="d4dfc-113">Elements</span></span>                         |
|-----------|----------------------------------|
| <span data-ttu-id="d4dfc-114">Parent</span><span class="sxs-lookup"><span data-stu-id="d4dfc-114">Parent</span></span>    | [<span data-ttu-id="d4dfc-115">Bruch</span><span class="sxs-lookup"><span data-stu-id="d4dfc-115">fragment</span></span>](fragment-element.md) |
| <span data-ttu-id="d4dfc-116">Untergeordnet</span><span class="sxs-lookup"><span data-stu-id="d4dfc-116">Child</span></span>     | <span data-ttu-id="d4dfc-117">Keine</span><span class="sxs-lookup"><span data-stu-id="d4dfc-117">None</span></span>                             |



 

## <a name="remarks"></a><span data-ttu-id="d4dfc-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4dfc-118">Remarks</span></span>

<span data-ttu-id="d4dfc-119">Wenn das **Name** -Attribut eines **Fragment** -Elements ein Medien Element Merkmal ist, z. b. ein Album-Maler oder Genre, muss das **Fragment** -Element zwei **Argument** Elemente enthalten: eines, das eine Bedingung angibt, und ein anderes, das einen Wert angibt.</span><span class="sxs-lookup"><span data-stu-id="d4dfc-119">When the **name** attribute of a **fragment** element is a media item characteristic such as Album Artist, or Genre, the **fragment** element must contain two **argument** elements: one that specifies a condition and another that specifies a value.</span></span> <span data-ttu-id="d4dfc-120">In der folgenden Tabelle werden zwei mögliche Werte für das **Name** -Attribut und die Verwendung von **Argument** Elementen zum Angeben von Bedingungen und Werten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d4dfc-120">The following table shows two possible values for the **name** attribute and how **argument** elements are used to specify conditions and values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d4dfc-121">Attributwert</span><span class="sxs-lookup"><span data-stu-id="d4dfc-121">Attribute value</span></span></th>
<th><span data-ttu-id="d4dfc-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4dfc-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d4dfc-123">Bedingung</span><span class="sxs-lookup"><span data-stu-id="d4dfc-123">Condition</span></span></td>
<td><span data-ttu-id="d4dfc-124">Der Inhalt des <strong>Argument</strong> -Elements ist der Bedingungs Teil einer Bedingungs Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d4dfc-124">The content of the <strong>argument</strong> element is the condition portion of a condition string.</span></span> <span data-ttu-id="d4dfc-125">Beispielsweise ist im Bedingungs zeichenfolgenmaler " &quot; Joe" &quot; der Bedingungs &quot; Teil &quot; .</span><span class="sxs-lookup"><span data-stu-id="d4dfc-125">For example, in the condition string &quot;Artist Equals Joe&quot;, the condition portion is &quot;Equals&quot;.</span></span> <span data-ttu-id="d4dfc-126">Der Bedingungs Teil einer Bedingungs Zeichenfolge muss einer der folgenden sein: ist gleich, ist nicht gleich, enthält, enthält nicht, ist kleiner als, ist größer als, ist, ist nicht, ist vor, ist höher als, ist aktueller als, oberhalb, aufsteigend, aufsteigend, zufällig, ist mindestens, ist nicht größer als.</span><span class="sxs-lookup"><span data-stu-id="d4dfc-126">The condition portion of a condition string must be one of the following: Equals, Does Not Equal, Contains, Does Not Contain, Is Less Than, Is Greater Than, Is, Is Not, Is Before, Is Later Than, Is More Recent Than, Above, Below, Ascending, Descending, Random, Is At Least, Is No More Than.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4dfc-127">Wert</span><span class="sxs-lookup"><span data-stu-id="d4dfc-127">Value</span></span></td>
<td><span data-ttu-id="d4dfc-128">Der Inhalt des <strong>Argument</strong> -Elements ist der Wertteil einer Bedingungs Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d4dfc-128">The content of the <strong>argument</strong> element is the value portion of a condition string.</span></span> <span data-ttu-id="d4dfc-129">Beispielsweise ist im Bedingungs zeichenfolgenmaler " &quot; Joe" &quot; der Wert Teil Joe &quot; &quot; . Beispiel</span><span class="sxs-lookup"><span data-stu-id="d4dfc-129">For example, in the condition string &quot;Artist Equals Joe&quot;, the value portion is &quot;Joe&quot;.Example:</span></span><br/>
<pre data-space="preserve"><code><fragment name = &quot;Artist&quot;>
  <argument name = &quot;Condition&quot;>Equals</argument>
  <argument name = &quot;Value&quot;>Joe</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d4dfc-130">Wenn das Attribut " **Name** " eines **fragmentelements** "Gesamtgröße begrenzen auf" oder "gesamte Dauer begrenzen auf" festgelegt ist, muss das **Fragment** -Element zwei **Argument** Elemente enthalten: eine, die ein Format angibt, und eine, die eine Zahl angibt.</span><span class="sxs-lookup"><span data-stu-id="d4dfc-130">When the **name** attribute of a **fragment** element is "Limit Total Size To" or "Limit Total Duration To", the **fragment** element must contain two **argument** elements: one that specifies a format and one that specifies a number.</span></span> <span data-ttu-id="d4dfc-131">In der folgenden Tabelle werden zwei mögliche Werte für das **Name** -Attribut und die Verwendung von **Argument** Elementen zum Begrenzen der Größe oder Dauer einer Wiedergabeliste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d4dfc-131">The following table shows two possible values for the **name** attribute and how **argument** elements are used to limit the size or duration of a playlist.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d4dfc-132">Attributwert</span><span class="sxs-lookup"><span data-stu-id="d4dfc-132">Attribute value</span></span></th>
<th><span data-ttu-id="d4dfc-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d4dfc-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d4dfc-134">Format</span><span class="sxs-lookup"><span data-stu-id="d4dfc-134">Format</span></span></td>
<td><span data-ttu-id="d4dfc-135">Wenn für das Attribut " <strong>Name</strong> " des <strong>fragmentelements</strong> die &quot; Gesamtgröße auf begrenzt ist &quot; , muss der Inhalt des <strong>Argument</strong> -Elements eines der folgenden sein: Kilobytes, Megabyte oder Gigabyte. Wenn für das <strong>Name</strong> -Attribut des <strong>Fragment</strong> -Elements die &quot; Gesamtdauer der Beschränkung auf begrenzt ist &quot; , muss der Inhalt des <strong>Argument</strong> -Elements eines der folgenden sein: Sekunden, Minuten, Stunden oder Tage.</span><span class="sxs-lookup"><span data-stu-id="d4dfc-135">When the <strong>name</strong> attribute of the <strong>fragment</strong> element is &quot;Limit Total Size To&quot;, the content of the <strong>argument</strong> element must be one of the following: Kilobytes, Megabytes, or Gigabytes.When the <strong>name</strong> attribute of the <strong>fragment</strong> element is &quot;Limit Total Duration To&quot;, the content of the <strong>argument</strong> element must be one of the following: Seconds, Minutes, Hours, or Days.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4dfc-136">Number</span><span class="sxs-lookup"><span data-stu-id="d4dfc-136">Number</span></span></td>
<td><span data-ttu-id="d4dfc-137">Der Inhalt des <strong>Argument</strong> -Elements ist eine Zahl, die die Größe oder Dauer der Wiedergabeliste einschränkt. Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4dfc-137">The content of the <strong>argument</strong> element is a number that limits the size or duration of the playlist.Examples:</span></span><br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Total Size To&quot;>
  <argument name = &quot;Format&quot;>Megabytes</argument>
  <argument name = &quot;Number&quot;>5</argument>
</fragment>

<fragment name = &quot;Limit Total Duration To&quot;>
  <argument name = &quot;Format&quot;>Minutes</argument>
  <argument name = &quot;Number&quot;>20</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d4dfc-138">Wenn das **Name** -Attribut eines **Fragment** -Elements "Limit number of Items" lautet, muss das **Fragment** -Element ein **Argument** Element enthalten, das die Anzahl der Elemente angibt.</span><span class="sxs-lookup"><span data-stu-id="d4dfc-138">When the **name** attribute of a **fragment** element is "Limit Number of Items", the **fragment** element must contain one **argument** element that specifies the number of items.</span></span> <span data-ttu-id="d4dfc-139">In der folgenden Tabelle wird gezeigt, wie Sie den Number-Wert des **Name** -Attributs verwenden.</span><span class="sxs-lookup"><span data-stu-id="d4dfc-139">The following table shows how to use the Number value of the **name** attribute.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d4dfc-140">Attributwert</span><span class="sxs-lookup"><span data-stu-id="d4dfc-140">Attribute value</span></span></th>
<th><span data-ttu-id="d4dfc-141">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d4dfc-141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d4dfc-142">Number</span><span class="sxs-lookup"><span data-stu-id="d4dfc-142">Number</span></span></td>
<td><span data-ttu-id="d4dfc-143">Der Inhalt des <strong>Argument</strong> -Elements ist eine Zahl, die die Anzahl der Elemente in einer Wiedergabeliste einschränkt. Beispiel</span><span class="sxs-lookup"><span data-stu-id="d4dfc-143">The content of the <strong>argument</strong> element is a number that limits the number of items in a playlist.Example:</span></span><br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Number of Items&quot;>
  <argument name = &quot;Number&quot;>15</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="d4dfc-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4dfc-144">Requirements</span></span>



| <span data-ttu-id="d4dfc-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4dfc-145">Requirement</span></span> | <span data-ttu-id="d4dfc-146">Wert</span><span class="sxs-lookup"><span data-stu-id="d4dfc-146">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="d4dfc-147">Version</span><span class="sxs-lookup"><span data-stu-id="d4dfc-147">Version</span></span><br/> | <span data-ttu-id="d4dfc-148">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="d4dfc-148">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d4dfc-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4dfc-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4dfc-150">**Fragment-Element**</span><span class="sxs-lookup"><span data-stu-id="d4dfc-150">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="d4dfc-151">**Referenz zu Windows Media-Wiedergabelisten Elementen**</span><span class="sxs-lookup"><span data-stu-id="d4dfc-151">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





