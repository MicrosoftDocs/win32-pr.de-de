---
title: Image-Element (Windows Ribbon Framework)
description: Stellt ein Bild dar.
ms.assetid: 2c71bb16-93ac-484f-b81b-1b95842472b3
keywords:
- Bildelement Windows-Menüband
topic_type:
- apiref
api_name:
- Image
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe0b9afb51697d50de9cb80886cf829b90c81262
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442891"
---
# <a name="image-element"></a><span data-ttu-id="0b6ac-104">Image-Element</span><span class="sxs-lookup"><span data-stu-id="0b6ac-104">Image element</span></span>

<span data-ttu-id="0b6ac-105">Stellt ein Bild dar.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-105">Represents an image.</span></span>

## <a name="usage"></a><span data-ttu-id="0b6ac-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="0b6ac-106">Usage</span></span>

``` syntax
<Image
  Source = "xs:anyURI"
  MinDPI = "xs:positiveInteger"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string">
  child elements
</Image>
```

## <a name="attributes"></a><span data-ttu-id="0b6ac-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="0b6ac-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0b6ac-108">attribute</span><span class="sxs-lookup"><span data-stu-id="0b6ac-108">Attribute</span></span></th>
<th><span data-ttu-id="0b6ac-109">Typ</span><span class="sxs-lookup"><span data-stu-id="0b6ac-109">Type</span></span></th>
<th><span data-ttu-id="0b6ac-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0b6ac-110">Required</span></span></th>
<th><span data-ttu-id="0b6ac-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b6ac-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0b6ac-112"><strong>Id</strong></span><span class="sxs-lookup"><span data-stu-id="0b6ac-112"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="0b6ac-113">xs:positiveInteger union xs:string</span><span class="sxs-lookup"><span data-stu-id="0b6ac-113">xs:positiveInteger union xs:string</span></span><br/></td>
<td><span data-ttu-id="0b6ac-114">Nein</span><span class="sxs-lookup"><span data-stu-id="0b6ac-114">No</span></span><br/></td>
<td><span data-ttu-id="0b6ac-115">Die eindeutige Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-115">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="0b6ac-116">
<dt><span></span><span></span><strong></strong> (Die Vereinigung von xs:positiveInteger und xs:string)</span><span class="sxs-lookup"><span data-stu-id="0b6ac-116">
<dt><span></span><span></span><strong></strong> (The union of xs:positiveInteger and xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="0b6ac-117">Ein ganzzahliger Wert zwischen 2 und 59999, einschließlich oder 0x2 und 0xea5f hexadezimal, einschließlich.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-117">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="0b6ac-118">Die maximale Länge beträgt 10 Zeichen, einschließlich optionaler führender Nullen.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-118">The maximum length is 10 characters including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b6ac-119"><strong>MinDPI</strong></span><span class="sxs-lookup"><span data-stu-id="0b6ac-119"><strong>MinDPI</strong></span></span><br/></td>
<td><span data-ttu-id="0b6ac-120">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="0b6ac-120">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="0b6ac-121">Nein</span><span class="sxs-lookup"><span data-stu-id="0b6ac-121">No</span></span><br/></td>
<td><span data-ttu-id="0b6ac-122"><dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="0b6ac-122"><dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="0b6ac-123">Eine beliebige Sequenz von Ziffern mit einem Mindestwert von 96.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-123">Any sequence of digits with a minimum value of 96.</span></span> <br/> <span data-ttu-id="0b6ac-124">Wenn MinDPI weggelassen wird, ist der Standardwert 96.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-124">If MinDPI is omitted, the default value is 96.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0b6ac-125"><strong>Quelle</strong></span><span class="sxs-lookup"><span data-stu-id="0b6ac-125"><strong>Source</strong></span></span><br/></td>
<td><span data-ttu-id="0b6ac-126">xs:anyURI</span><span class="sxs-lookup"><span data-stu-id="0b6ac-126">xs:anyURI</span></span><br/></td>
<td><span data-ttu-id="0b6ac-127">Nein</span><span class="sxs-lookup"><span data-stu-id="0b6ac-127">No</span></span><br/></td>
<td><span data-ttu-id="0b6ac-128"><dt><span></span><span></span><strong></strong> (xs:anyURI)</span><span class="sxs-lookup"><span data-stu-id="0b6ac-128"><dt><span></span><span></span><strong></strong> (xs:anyURI)</span></span><br/> </dt> <dd> <span data-ttu-id="0b6ac-129">Jede Sequenz von Zeichen, die einen URI darstellt.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-129">Any sequence of characters that represents a URI.</span></span> <span data-ttu-id="0b6ac-130">Der URI-Wert ist ein absoluter oder relativer Pfad (zur Menübandmarkupdatei) zu einer Bildressource vom Typ BMP.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-130">The URI value is an absolute or relative (to the Ribbon markup file) path to an image resource of type BMP.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b6ac-131"><strong>Symbol</strong></span><span class="sxs-lookup"><span data-stu-id="0b6ac-131"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="0b6ac-132">xs:string</span><span class="sxs-lookup"><span data-stu-id="0b6ac-132">xs:string</span></span><br/></td>
<td><span data-ttu-id="0b6ac-133">Nein</span><span class="sxs-lookup"><span data-stu-id="0b6ac-133">No</span></span><br/></td>
<td><span data-ttu-id="0b6ac-134">Das Ressourcensymbol für das Bild.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-134">The resource symbol for the image.</span></span><br/> <br/><span data-ttu-id="0b6ac-135">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="0b6ac-135">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="0b6ac-136">Eine Zeichenfolge, die aus einem Buchstaben oder Unterstrich gefolgt von einer beliebigen Folge von Buchstaben, Ziffern oder Unterstrichen bis zu maximal 100 Zeichen besteht.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-136">A string composed of a letter or underscore followed by any sequence of letters, digits, or underscores up to a maximum of 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="0b6ac-137">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0b6ac-137">Child elements</span></span>



| <span data-ttu-id="0b6ac-138">Element</span><span class="sxs-lookup"><span data-stu-id="0b6ac-138">Element</span></span>                                                               | <span data-ttu-id="0b6ac-139">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b6ac-139">Description</span></span>                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="0b6ac-140">**Image.Source**</span><span class="sxs-lookup"><span data-stu-id="0b6ac-140">**Image.Source**</span></span>](windowsribbon-element-image-source.md)<br/> | <span data-ttu-id="0b6ac-141">Kann nur einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-141">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="0b6ac-142">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0b6ac-142">Parent elements</span></span>



| <span data-ttu-id="0b6ac-143">Element</span><span class="sxs-lookup"><span data-stu-id="0b6ac-143">Element</span></span>                                                                                                     |
|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b6ac-144">**Command.LargeHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="0b6ac-144">**Command.LargeHighContrastImages**</span></span>](windowsribbon-element-command-largehighcontrastimages.md)<br/> |
| [<span data-ttu-id="0b6ac-145">**Command.LargeImages**</span><span class="sxs-lookup"><span data-stu-id="0b6ac-145">**Command.LargeImages**</span></span>](windowsribbon-element-command-largeimages.md)<br/>                         |
| [<span data-ttu-id="0b6ac-146">**Command.SmallHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="0b6ac-146">**Command.SmallHighContrastImages**</span></span>](windowsribbon-element-command-smallhighcontrastimages.md)<br/> |
| [<span data-ttu-id="0b6ac-147">**Command.SmallImages**</span><span class="sxs-lookup"><span data-stu-id="0b6ac-147">**Command.SmallImages**</span></span>](windowsribbon-element-command-smallimages.md)<br/>                         |



## <a name="remarks"></a><span data-ttu-id="0b6ac-148">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0b6ac-148">Remarks</span></span>

<span data-ttu-id="0b6ac-149">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-149">Optional.</span></span>

<span data-ttu-id="0b6ac-150">Kann ein oder mehrere Male für jedes [**Command.SmallImages-,**](windowsribbon-element-command-smallimages.md) [**Command.SmallHighContrastImages-,**](windowsribbon-element-command-smallhighcontrastimages.md) [**Command.LargeImages-**](windowsribbon-element-command-largeimages.md)oder [**Command.LargeHighContrastImages-Element**](windowsribbon-element-command-largehighcontrastimages.md) auftreten.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-150">May occur one or more times for each [**Command.SmallImages**](windowsribbon-element-command-smallimages.md), [**Command.SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md), [**Command.LargeImages**](windowsribbon-element-command-largeimages.md), or [**Command.LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md) element.</span></span>

<span data-ttu-id="0b6ac-151">Wenn eine Sammlung von Bildressourcen, die für die Unterstützung bestimmter DPI-Einstellungen (Screen Dots per Inch) entworfen  wurden, für das Menübandframework über eine Reihe von **Image-Elementen** bereitgestellt wird, verwendet das Framework das Image mit einem *MinDPI-Attributwert,* der der aktuellen DPI-Einstellung des Bildschirms entspricht.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-151">When a collection of image resources that are designed to support specific screen dots per inch (dpi) settings is supplied to the Ribbon framework through a set of **Image** elements, the framework uses the **Image** with a *MinDPI* attribute value that matches the current screen dpi setting.</span></span>

<span data-ttu-id="0b6ac-152">Wenn kein **Image-Element** mit einem *MinDPI-Wert* deklariert wird, der der  aktuellen DPI-Einstellung des Bildschirms entspricht, wählt das Framework das Bild aus, das den nächstgelegenen *MinDPI-Wert* kleiner als die aktuelle DPI-Einstellung des Bildschirms hat, und skaliert die Bildressource hoch.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-152">If no **Image** element is declared with a *MinDPI* value that matches the current screen dpi setting, the framework picks the **Image** that has the nearest *MinDPI* value less than the current screen dpi setting and scales the image resource up.</span></span> <span data-ttu-id="0b6ac-153">Wenn andernfalls kein **Image-Element** mit einem *MinDPI-Attributwert* deklariert wird, der kleiner als die aktuelle DPI-Einstellung des Bildschirms ist, wählt das Framework den nächsten *MinDPI-Wert* aus, der größer als die aktuelle DPI-Einstellung des Bildschirms ist, und skaliert die Bildressource herunter.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-153">Otherwise, if no **Image** element is declared with a *MinDPI* attribute value less than the current screen dpi setting, the framework picks the nearest *MinDPI* value greater than the current screen dpi setting and scales the image resource down.</span></span>

## <a name="examples"></a><span data-ttu-id="0b6ac-154">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b6ac-154">Examples</span></span>

<span data-ttu-id="0b6ac-155">Das folgende Codebeispiel zeigt das Markup, das erforderlich ist, um über einen Satz von **Image-Elementen** eine Sammlung von Bildressourcen zu deklarieren, die zur Unterstützung von vier spezifischen DPI-Bildschirmeinstellungen entwickelt wurden.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-155">The following code example shows the markup required to declare, through a set of **Image** elements, a collection of image resources that are designed to support four specific screen dpi settings.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="0b6ac-156">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0b6ac-156">Element information</span></span>

* <span data-ttu-id="0b6ac-157">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="0b6ac-157">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="0b6ac-158">**Kann leer sein:** Nein</span><span class="sxs-lookup"><span data-stu-id="0b6ac-158">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="0b6ac-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b6ac-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b6ac-160">Angeben von Menübandbildressourcen</span><span class="sxs-lookup"><span data-stu-id="0b6ac-160">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> </dl>

 

 





