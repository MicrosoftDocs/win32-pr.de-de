---
title: Image-Element (Windows-Menüband-Framework)
description: Stellt ein Bild dar.
ms.assetid: 2c71bb16-93ac-484f-b81b-1b95842472b3
keywords:
- Windows-Menüband für Bildelement
topic_type:
- apiref
api_name:
- Image
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1d33f6710da2261a359aa7fd0a3b493871155cf4
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/12/2019
ms.locfileid: "104101050"
---
# <a name="image-element"></a><span data-ttu-id="9b8ba-104">Image-Element</span><span class="sxs-lookup"><span data-stu-id="9b8ba-104">Image element</span></span>

<span data-ttu-id="9b8ba-105">Stellt ein Bild dar.</span><span class="sxs-lookup"><span data-stu-id="9b8ba-105">Represents an image.</span></span>

## <a name="usage"></a><span data-ttu-id="9b8ba-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="9b8ba-106">Usage</span></span>

``` syntax
<Image
  Source = "xs:anyURI"
  MinDPI = "xs:positiveInteger"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string">
  child elements
</Image>
```

## <a name="attributes"></a><span data-ttu-id="9b8ba-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="9b8ba-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b8ba-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="9b8ba-108">Attribute</span></span></th>
<th><span data-ttu-id="9b8ba-109">type</span><span class="sxs-lookup"><span data-stu-id="9b8ba-109">Type</span></span></th>
<th><span data-ttu-id="9b8ba-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="9b8ba-110">Required</span></span></th>
<th><span data-ttu-id="9b8ba-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b8ba-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b8ba-112"><strong>Id</strong></span><span class="sxs-lookup"><span data-stu-id="9b8ba-112"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="9b8ba-113">xs: positivan teger Union xs: String</span><span class="sxs-lookup"><span data-stu-id="9b8ba-113">xs:positiveInteger union xs:string</span></span><br/></td>
<td><span data-ttu-id="9b8ba-114">Nein</span><span class="sxs-lookup"><span data-stu-id="9b8ba-114">No</span></span><br/></td>
<td><span data-ttu-id="9b8ba-115">Die eindeutige Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="9b8ba-115">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="9b8ba-116">
<dt><span></span><span></span><strong></strong> (Die Vereinigung von xs: positiveingeteger und xs: String)</span><span class="sxs-lookup"><span data-stu-id="9b8ba-116">
<dt><span></span><span></span><strong></strong> (The union of xs:positiveInteger and xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="9b8ba-117">Ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder 0x2 und 0xea5f in Hexadezimal (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="9b8ba-117">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="9b8ba-118">Die maximale Länge beträgt 10 Zeichen, einschließlich optionaler führender Nullen.</span><span class="sxs-lookup"><span data-stu-id="9b8ba-118">The maximum length is 10 characters including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b8ba-119"><strong>Mindpi</strong></span><span class="sxs-lookup"><span data-stu-id="9b8ba-119"><strong>MinDPI</strong></span></span><br/></td>
<td><span data-ttu-id="9b8ba-120">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="9b8ba-120">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="9b8ba-121">Nein</span><span class="sxs-lookup"><span data-stu-id="9b8ba-121">No</span></span><br/></td>
<td><span data-ttu-id="9b8ba-122"><dt><span></span><span></span><strong></strong> (xs: positivin teger)</span><span class="sxs-lookup"><span data-stu-id="9b8ba-122"><dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="9b8ba-123">Eine beliebige Sequenz von Ziffern mit einem Minimalwert von 96.</span><span class="sxs-lookup"><span data-stu-id="9b8ba-123">Any sequence of digits with a minimum value of 96.</span></span> <br/> <span data-ttu-id="9b8ba-124">Wenn mindpi weggelassen wird, ist der Standardwert 96.</span><span class="sxs-lookup"><span data-stu-id="9b8ba-124">If MinDPI is omitted, the default value is 96.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b8ba-125"><strong>Quelle</strong></span><span class="sxs-lookup"><span data-stu-id="9b8ba-125"><strong>Source</strong></span></span><br/></td>
<td><span data-ttu-id="9b8ba-126">xs:anyURI</span><span class="sxs-lookup"><span data-stu-id="9b8ba-126">xs:anyURI</span></span><br/></td>
<td><span data-ttu-id="9b8ba-127">Nein</span><span class="sxs-lookup"><span data-stu-id="9b8ba-127">No</span></span><br/></td>
<td><span data-ttu-id="9b8ba-128"><dt><span></span><span></span><strong></strong> (xs: anyURI)</span><span class="sxs-lookup"><span data-stu-id="9b8ba-128"><dt><span></span><span></span><strong></strong> (xs:anyURI)</span></span><br/> </dt> <dd> <span data-ttu-id="9b8ba-129">Eine beliebige Sequenz von Zeichen, die einen URI darstellt.</span><span class="sxs-lookup"><span data-stu-id="9b8ba-129">Any sequence of characters that represents a URI.</span></span> <span data-ttu-id="9b8ba-130">Der URI-Wert ist eine absolute oder relative (für den Menüband-Markup Datei) Pfad zu einer Bildressource des Typs BMP.</span><span class="sxs-lookup"><span data-stu-id="9b8ba-130">The URI value is an absolute or relative (to the Ribbon markup file) path to an image resource of type BMP.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b8ba-131"><strong>Symbol</strong></span><span class="sxs-lookup"><span data-stu-id="9b8ba-131"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="9b8ba-132">xs:string</span><span class="sxs-lookup"><span data-stu-id="9b8ba-132">xs:string</span></span><br/></td>
<td><span data-ttu-id="9b8ba-133">Nein</span><span class="sxs-lookup"><span data-stu-id="9b8ba-133">No</span></span><br/></td>
<td><span data-ttu-id="9b8ba-134">Das Ressourcen Symbol für das Bild.</span><span class="sxs-lookup"><span data-stu-id="9b8ba-134">The resource symbol for the image.</span></span><br/> <br/><span data-ttu-id="9b8ba-135">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="9b8ba-135">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="9b8ba-136">Eine Zeichenfolge, die aus einem Buchstaben oder einem Unterstrich gefolgt von einer beliebigen Folge von Buchstaben, Ziffern oder unterstrichen mit maximal 100 Zeichen besteht.</span><span class="sxs-lookup"><span data-stu-id="9b8ba-136">A string composed of a letter or underscore followed by any sequence of letters, digits, or underscores up to a maximum of 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="9b8ba-137">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9b8ba-137">Child elements</span></span>



| <span data-ttu-id="9b8ba-138">Element</span><span class="sxs-lookup"><span data-stu-id="9b8ba-138">Element</span></span>                                                               | <span data-ttu-id="9b8ba-139">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b8ba-139">Description</span></span>                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="9b8ba-140">**Image. Source**</span><span class="sxs-lookup"><span data-stu-id="9b8ba-140">**Image.Source**</span></span>](windowsribbon-element-image-source.md)<br/> | <span data-ttu-id="9b8ba-141">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="9b8ba-141">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="9b8ba-142">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9b8ba-142">Parent elements</span></span>



| <span data-ttu-id="9b8ba-143">Element</span><span class="sxs-lookup"><span data-stu-id="9b8ba-143">Element</span></span>                                                                                                     |
|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9b8ba-144">**Command. largehighkontra stimages**</span><span class="sxs-lookup"><span data-stu-id="9b8ba-144">**Command.LargeHighContrastImages**</span></span>](windowsribbon-element-command-largehighcontrastimages.md)<br/> |
| [<span data-ttu-id="9b8ba-145">**Command. largeimages**</span><span class="sxs-lookup"><span data-stu-id="9b8ba-145">**Command.LargeImages**</span></span>](windowsribbon-element-command-largeimages.md)<br/>                         |
| [<span data-ttu-id="9b8ba-146">**Command. smallhighkontra stimages**</span><span class="sxs-lookup"><span data-stu-id="9b8ba-146">**Command.SmallHighContrastImages**</span></span>](windowsribbon-element-command-smallhighcontrastimages.md)<br/> |
| [<span data-ttu-id="9b8ba-147">**Command. smallimages**</span><span class="sxs-lookup"><span data-stu-id="9b8ba-147">**Command.SmallImages**</span></span>](windowsribbon-element-command-smallimages.md)<br/>                         |



## <a name="remarks"></a><span data-ttu-id="9b8ba-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b8ba-148">Remarks</span></span>

<span data-ttu-id="9b8ba-149">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="9b8ba-149">Optional.</span></span>

<span data-ttu-id="9b8ba-150">Kann für jeden Befehl einmal oder mehrmals vorkommen [**. smallimages**](windowsribbon-element-command-smallimages.md), [**Command. smallhighkontra stimages**](windowsribbon-element-command-smallhighcontrastimages.md), [**Command. largeimages**](windowsribbon-element-command-largeimages.md)oder [**Command. largehighkontra stimages**](windowsribbon-element-command-largehighcontrastimages.md) .</span><span class="sxs-lookup"><span data-stu-id="9b8ba-150">May occur one or more times for each [**Command.SmallImages**](windowsribbon-element-command-smallimages.md), [**Command.SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md), [**Command.LargeImages**](windowsribbon-element-command-largeimages.md), or [**Command.LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md) element.</span></span>

<span data-ttu-id="9b8ba-151">Wenn eine Auflistung von Bild Ressourcen, die für die Unterstützung bestimmter Bildschirmpunkte pro Zoll (dpi) entwickelt wurden, über einen Satz von **Bild** Elementen an das Menüband-Framework übergeben wird, verwendet das Framework das **Bild** mit einem *mindpi* -Attribut Wert, der mit der aktuellen Bildschirm-dpi-Einstellung übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="9b8ba-151">When a collection of image resources that are designed to support specific screen dots per inch (dpi) settings is supplied to the Ribbon framework through a set of **Image** elements, the framework uses the **Image** with a *MinDPI* attribute value that matches the current screen dpi setting.</span></span>

<span data-ttu-id="9b8ba-152">Wenn kein **Bild** Element mit einem *mindpi* -Wert deklariert wird, der mit der aktuellen Bildschirm dpi-Einstellung übereinstimmt, wählt das Framework das **Bild** aus, das den nächstgelegenen *mindpi* -Wert aufweist, der kleiner ist als die aktuelle Bildschirm dpi-Einstellung, und skaliert die Bildressource</span><span class="sxs-lookup"><span data-stu-id="9b8ba-152">If no **Image** element is declared with a *MinDPI* value that matches the current screen dpi setting, the framework picks the **Image** that has the nearest *MinDPI* value less than the current screen dpi setting and scales the image resource up.</span></span> <span data-ttu-id="9b8ba-153">Wenn kein **Bild** Element mit einem *mindpi* -Attribut Wert, der kleiner als die aktuelle Bildschirm dpi-Einstellung ist, deklariert ist, wählt das Framework den nächsten *mindpi* -Wert aus, der größer als die aktuelle Bildschirm dpi-Einstellung ist, und skaliert die Bildressource nach unten.</span><span class="sxs-lookup"><span data-stu-id="9b8ba-153">Otherwise, if no **Image** element is declared with a *MinDPI* attribute value less than the current screen dpi setting, the framework picks the nearest *MinDPI* value greater than the current screen dpi setting and scales the image resource down.</span></span>

## <a name="examples"></a><span data-ttu-id="9b8ba-154">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9b8ba-154">Examples</span></span>

<span data-ttu-id="9b8ba-155">Das folgende Codebeispiel zeigt das Markup, das zum Deklarieren von über einen Satz von **Bild** Elementen erforderlich ist, eine Auflistung von Bild Ressourcen, die für die Unterstützung von vier bestimmten Bildschirm DPI-Einstellungen entworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="9b8ba-155">The following code example shows the markup required to declare, through a set of **Image** elements, a collection of image resources that are designed to support four specific screen dpi settings.</span></span>


```XML
<Command Name="cmdSizeAndColor" Symbol="IDR_CMD_SIZEANDCOLOR">
  <Command.LabelTitle>
    <String Id="250">Size and Color</String>
  </Command.LabelTitle>
  <Command.LargeImages>
    <Image Id="251" MinDPI="96">res/sizeAndColor_96.bmp</Image>
    <Image Id="252" MinDPI="120">res/sizeAndColor_120.bmp</Image>
    <Image Id="253" MinDPI="144">res/sizeAndColor_144.bmp</Image>
    <Image Id="254" MinDPI="192">res/sizeAndColor_192.bmp</Image>
  </Command.LargeImages>
</Command>
```



## <a name="element-information"></a><span data-ttu-id="9b8ba-156">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="9b8ba-156">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="9b8ba-157">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="9b8ba-157">Minimum supported system</span></span><br/> | <span data-ttu-id="9b8ba-158">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9b8ba-158">Windows 7</span></span> |
| <span data-ttu-id="9b8ba-159">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="9b8ba-159">Can be empty</span></span>                        | <span data-ttu-id="9b8ba-160">Nein</span><span class="sxs-lookup"><span data-stu-id="9b8ba-160">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="9b8ba-161">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9b8ba-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b8ba-162">Angeben von Menüband-Bild Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9b8ba-162">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> </dl>

 

 





