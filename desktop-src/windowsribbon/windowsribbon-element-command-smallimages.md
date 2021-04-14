---
title: Command. smallimages (Eigenschaft)
description: Stellt einen Container von Bildern dar. in diesem Fall kleine Bilder.
ms.assetid: 15c00e61-543a-4cc8-b329-516985d02359
keywords:
- Command. smallimages-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- Command.SmallImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b18556cf519c21b01c3e80b63cbfc9cdf9d7d153
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478624"
---
# <a name="commandsmallimages-property"></a><span data-ttu-id="7a8f2-104">Command. smallimages (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7a8f2-104">Command.SmallImages property</span></span>

<span data-ttu-id="7a8f2-105">Stellt einen Container von Bildern dar. in diesem Fall kleine Bilder.</span><span class="sxs-lookup"><span data-stu-id="7a8f2-105">Represents a container of images; in this case, small images.</span></span>

## <a name="usage"></a><span data-ttu-id="7a8f2-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="7a8f2-106">Usage</span></span>

``` syntax
<Command.SmallImages>
  child elements
</Command.SmallImages>
```

## <a name="attributes"></a><span data-ttu-id="7a8f2-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="7a8f2-107">Attributes</span></span>

<span data-ttu-id="7a8f2-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="7a8f2-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="7a8f2-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7a8f2-109">Child elements</span></span>



| <span data-ttu-id="7a8f2-110">Element</span><span class="sxs-lookup"><span data-stu-id="7a8f2-110">Element</span></span>                                                 | <span data-ttu-id="7a8f2-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7a8f2-111">Description</span></span>                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="7a8f2-112">**Image**</span><span class="sxs-lookup"><span data-stu-id="7a8f2-112">**Image**</span></span>](windowsribbon-element-image.md)<br/> | <span data-ttu-id="7a8f2-113">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="7a8f2-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="7a8f2-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7a8f2-114">Parent elements</span></span>



| <span data-ttu-id="7a8f2-115">Element</span><span class="sxs-lookup"><span data-stu-id="7a8f2-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="7a8f2-116">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="7a8f2-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="7a8f2-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a8f2-117">Remarks</span></span>

<span data-ttu-id="7a8f2-118">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="7a8f2-118">Optional.</span></span>

<span data-ttu-id="7a8f2-119">Kann höchstens einmal für jeden [**Befehl**](windowsribbon-element-command.md)auftreten.</span><span class="sxs-lookup"><span data-stu-id="7a8f2-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="7a8f2-120">Bild Ressourcen müssen dem standardmäßigen BMP-Grafikformat (Bitmap) entsprechen, das in Windows verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7a8f2-120">Image resources must conform to the standard bitmap (BMP) graphics format used in Windows.</span></span>

## <a name="examples"></a><span data-ttu-id="7a8f2-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7a8f2-121">Examples</span></span>

<span data-ttu-id="7a8f2-122">Im folgenden Beispiel wird das grundlegende Markup für das [**SplitButton**](windowsribbon-element-splitbutton.md) -Element mit einem [**MenuGroup**](windowsribbon-element-menugroup.md) -Element veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="7a8f2-122">The following example demonstrates the basic markup for the [**SplitButton**](windowsribbon-element-splitbutton.md) with a [**MenuGroup**](windowsribbon-element-menugroup.md) element.</span></span>

<span data-ttu-id="7a8f2-123">In diesem Code Abschnitt werden die Befehls Deklarationen [**SplitButton**](windowsribbon-element-splitbutton.md) und [**MenuGroup**](windowsribbon-element-menugroup.md) mit einer großen und kleinen Bildressource angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7a8f2-123">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and [**MenuGroup**](windowsribbon-element-menugroup.md) Command declarations with a large and a small image resource.</span></span> <span data-ttu-id="7a8f2-124">Eine zugeordnete [**Gruppe**](windowsribbon-element-group.md) , die als übergeordneter Container für das **SplitButton** -Element fungiert, wird ebenfalls deklariert.</span><span class="sxs-lookup"><span data-stu-id="7a8f2-124">An associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **SplitButton** element is also declared.</span></span>


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



## <a name="requirements"></a><span data-ttu-id="7a8f2-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a8f2-125">Requirements</span></span>



| <span data-ttu-id="7a8f2-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a8f2-126">Requirement</span></span> | <span data-ttu-id="7a8f2-127">Wert</span><span class="sxs-lookup"><span data-stu-id="7a8f2-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="7a8f2-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7a8f2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7a8f2-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a8f2-129">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="7a8f2-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7a8f2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7a8f2-131">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a8f2-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7a8f2-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a8f2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a8f2-133">Angeben von Menüband-Bild Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7a8f2-133">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> <dt>

[<span data-ttu-id="7a8f2-134">UI \_ pkey \_ smallImage</span><span class="sxs-lookup"><span data-stu-id="7a8f2-134">UI\_PKEY\_SmallImage</span></span>](windowsribbon-reference-properties-uipkey-smallimage.md)
</dt> </dl>

 

 





