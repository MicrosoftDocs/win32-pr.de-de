---
title: Image. Source (Eigenschaft)
description: Stellt den Verzeichnispfad eines Bilds dar.
ms.assetid: 174a518a-e9a3-4461-a9a3-d61b62d2b718
keywords:
- Bild. Quell Eigenschaft (Windows-Menüband)
topic_type:
- apiref
api_name:
- Image.Source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ace2a907280a11c54452b54bfb6172539980e38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741000"
---
# <a name="imagesource-property"></a><span data-ttu-id="34126-104">Image. Source (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="34126-104">Image.Source property</span></span>

<span data-ttu-id="34126-105">Stellt den Verzeichnispfad eines Bilds dar.</span><span class="sxs-lookup"><span data-stu-id="34126-105">Represents the directory path of an image.</span></span>

## <a name="usage"></a><span data-ttu-id="34126-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="34126-106">Usage</span></span>

``` syntax
<Image.Source/>
```

## <a name="attributes"></a><span data-ttu-id="34126-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="34126-107">Attributes</span></span>

<span data-ttu-id="34126-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="34126-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="34126-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="34126-109">Child elements</span></span>

<span data-ttu-id="34126-110">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="34126-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="34126-111">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="34126-111">Parent elements</span></span>



| <span data-ttu-id="34126-112">Element</span><span class="sxs-lookup"><span data-stu-id="34126-112">Element</span></span>                                                 |
|---------------------------------------------------------|
| [<span data-ttu-id="34126-113">**Image**</span><span class="sxs-lookup"><span data-stu-id="34126-113">**Image**</span></span>](windowsribbon-element-image.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="34126-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34126-114">Remarks</span></span>

<span data-ttu-id="34126-115">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="34126-115">Optional.</span></span>

<span data-ttu-id="34126-116">Kann höchstens einmal für jedes [**Image**](windowsribbon-element-image.md)auftreten.</span><span class="sxs-lookup"><span data-stu-id="34126-116">May occur at most once for each [**Image**](windowsribbon-element-image.md).</span></span>

<span data-ttu-id="34126-117">Dieses Element enthält einen Wert vom Typ *xs: anyURI* oder eine beliebige Sequenz von Zeichen, die einen Uniform Resource Identifier (URI) darstellt.</span><span class="sxs-lookup"><span data-stu-id="34126-117">This element contains a value of type *xs:anyURI* or any sequence of characters that represents a Uniform Resource Identifier (URI).</span></span> <span data-ttu-id="34126-118">Der URI-Wert ist eine absolute oder relative (für den Menü Band Markup Datei) Verzeichnispfad einer Bildressource des Typs Bitmap (BMP).</span><span class="sxs-lookup"><span data-stu-id="34126-118">The URI value is an absolute or relative (to the Ribbon markup file) directory path of an image resource of type bitmap (BMP).</span></span>

## <a name="examples"></a><span data-ttu-id="34126-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="34126-119">Examples</span></span>

<span data-ttu-id="34126-120">Das folgende Codebeispiel zeigt das Markup, das zum Deklarieren von über einen Satz von [**Bild**](windowsribbon-element-image.md) Elementen erforderlich ist, eine Auflistung von Bild Ressourcen, die für die Unterstützung von vier bestimmten Bildschirm DPI-Einstellungen entworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="34126-120">The following code example shows the markup required to declare, through a set of [**Image**](windowsribbon-element-image.md) elements, a collection of image resources that are designed to support four specific screen dpi settings.</span></span> <span data-ttu-id="34126-121">Die **Image. Source** -Eigenschaft wird verwendet, um den Pfad zur Bildressource anzugeben.</span><span class="sxs-lookup"><span data-stu-id="34126-121">The **Image.Source** property is used to specify the path to the image resource.</span></span>


```C++
<Command Name="cmdSizeAndColor" Symbol="IDR_CMD_SIZEANDCOLOR">
  <Command.LabelTitle>
    <String Id="250">Size and Color</String>
  </Command.LabelTitle>
  <Command.LargeImages>
    <Image Id="251" MinDPI="96">
      <Image.Source>res/sizeAndColor_96.bmp</Image.Source>
    </Image>
    <Image Id="252" MinDPI="120">
      <Image.Source>res/sizeAndColor_120.bmp</Image.Source>
    </Image>
    <Image Id="253" MinDPI="144">
      <Image.Source>res/sizeAndColor_144.bmp</Image.Source>
    </Image>
    <Image Id="254" MinDPI="192">
      <Image.Source>res/sizeAndColor_192.bmp</Image.Source>
    </Image>
  </Command.LargeImages>
</Command>
```



## <a name="requirements"></a><span data-ttu-id="34126-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34126-122">Requirements</span></span>



| <span data-ttu-id="34126-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34126-123">Requirement</span></span> | <span data-ttu-id="34126-124">Wert</span><span class="sxs-lookup"><span data-stu-id="34126-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="34126-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="34126-125">Minimum supported client</span></span><br/> | <span data-ttu-id="34126-126">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="34126-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="34126-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="34126-127">Minimum supported server</span></span><br/> | <span data-ttu-id="34126-128">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="34126-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





