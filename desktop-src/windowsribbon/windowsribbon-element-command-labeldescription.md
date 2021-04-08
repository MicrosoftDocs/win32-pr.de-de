---
title: Command. labeldescription (Eigenschaft)
description: Stellt eine Bezeichnungs Beschreibung dar.
ms.assetid: 6c683e9e-0742-466e-9fdd-3d29f8ccb9ff
keywords:
- Command. labeldescription-Eigenschaft (Windows-Menüband)
topic_type:
- apiref
api_name:
- Command.LabelDescription
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f748425b4c8363feee737d18c750b3a1d91121b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957017"
---
# <a name="commandlabeldescription-property"></a><span data-ttu-id="aa212-104">Command. labeldescription (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="aa212-104">Command.LabelDescription property</span></span>

<span data-ttu-id="aa212-105">Stellt eine Bezeichnungs Beschreibung dar.</span><span class="sxs-lookup"><span data-stu-id="aa212-105">Represents a label description.</span></span>

## <a name="usage"></a><span data-ttu-id="aa212-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="aa212-106">Usage</span></span>

``` syntax
<Command.LabelDescription>
  child elements
</Command.LabelDescription>
```

## <a name="attributes"></a><span data-ttu-id="aa212-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="aa212-107">Attributes</span></span>

<span data-ttu-id="aa212-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="aa212-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="aa212-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aa212-109">Child elements</span></span>



| <span data-ttu-id="aa212-110">Element</span><span class="sxs-lookup"><span data-stu-id="aa212-110">Element</span></span>                                                   | <span data-ttu-id="aa212-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aa212-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="aa212-112">**Schnür**</span><span class="sxs-lookup"><span data-stu-id="aa212-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="aa212-113">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="aa212-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="aa212-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aa212-114">Parent elements</span></span>



| <span data-ttu-id="aa212-115">Element</span><span class="sxs-lookup"><span data-stu-id="aa212-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="aa212-116">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="aa212-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="aa212-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa212-117">Remarks</span></span>

<span data-ttu-id="aa212-118">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="aa212-118">Optional.</span></span>

<span data-ttu-id="aa212-119">Kann höchstens einmal für jeden [**Befehl**](windowsribbon-element-command.md)auftreten.</span><span class="sxs-lookup"><span data-stu-id="aa212-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="aa212-120">**Command. labeldescription** kann einen Wert vom *Typ xs: String* enthalten, der auf eine beliebige Sequenz von Zeichen beschränkt ist, einschließlich Leerzeichen und Zeilenumbruch Zeichen.</span><span class="sxs-lookup"><span data-stu-id="aa212-120">**Command.LabelDescription** can contain a value of *type xs:string* constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="aa212-121">Verwenden Sie den XML-Zeichen Verweis Universal Character Set (UCS) `&#xA;` , um einen Zeilenumbruch anzugeben.</span><span class="sxs-lookup"><span data-stu-id="aa212-121">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="aa212-122">Die maximale Länge ist unbegrenzt.</span><span class="sxs-lookup"><span data-stu-id="aa212-122">The maximum length is unbounded.</span></span>

<span data-ttu-id="aa212-123">Wenn für **Command. labeldescription** kein Wert angegeben wird, ist das untergeordnete [**Zeichen**](windowsribbon-element-string.md) folgen Element erforderlich.</span><span class="sxs-lookup"><span data-stu-id="aa212-123">If no value is supplied for **Command.LabelDescription**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="aa212-124">Wenn **Command. labeldescription** sowohl einen Wert als auch ein untergeordnetes [**Zeichen**](windowsribbon-element-string.md) folgen Element enthält, hat die **Zeichenfolge** Vorrang.</span><span class="sxs-lookup"><span data-stu-id="aa212-124">If **Command.LabelDescription** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="aa212-125">**Command. labeldescription** unterstützt nur die linke Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="aa212-125">**Command.LabelDescription** only supports left alignment.</span></span>

## <a name="examples"></a><span data-ttu-id="aa212-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aa212-126">Examples</span></span>

<span data-ttu-id="aa212-127">Das folgende Beispiel zeigt ein Manifest von Zwischenablage Befehlen mit verschiedenen **Command. labeldescription** -Deklarationen.</span><span class="sxs-lookup"><span data-stu-id="aa212-127">The following example shows a manifest of clipboard Commands with various **Command.LabelDescription** declarations.</span></span>


```XML
<Command Name="cmdHomeTab"
         LabelTitle="Home"
         Keytip="H" />
<Command Name="cmdClipboardGroup"
         Symbol="IDR_CMD_CLIPBOARD"
         Id="10000"
         Comment="Command definition for clipboard group"
         LabelTitle="Clipboard"
         Keytip="CB" />
<Command Name="cmdCopy"
         Symbol="IDR_CMD_COPY"
         LabelTitle="Copy"
         LabelDescription="Copy"
         Keytip="C"
         TooltipTitle="Copy"
         TooltipDescription="Click to copy">
  <Command.SmallImages>
    <Image>res/copyS_16.bmp</Image>
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/copyL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdPaste"
         Symbol="IDR_CMD_PASTE" >
  <Command.LabelTitle>Paste</Command.LabelTitle>
  <Command.LabelDescription>
    <String Content="Paste contents of clipboard"
            Id="10001"
            Symbol="IDR_RES_LABELDESC_PASTE" />
  </Command.LabelDescription>
  <Command.Keytip>P</Command.Keytip>
  <Command.TooltipTitle>
    <String Content="Paste contents of clipboard"
            Id="10002"
            Symbol="IDR_RES_TOOLTIP_PASTE"/>
  </Command.TooltipTitle>
  <Command.TooltipDescription>
    <String Content="Click to paste contents of clipboard"/>
  </Command.TooltipDescription>
  <Command.SmallImages>
    <Image
      Id="10010"
      MinDPI="96"
      Symbol="IDR_RES_SMALL_IMAGE96">
      <Image.Source>res/pasteS_96bpp.bmp</Image.Source>
    </Image>
    <Image Source="res/pasteS_120bpp.bmp"
           Id="10011"
           MinDPI="120"
           Symbol="IDR_RES_SMALL_IMAGE120" />
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/pasteL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdMinimize"
         Symbol="IDR_CMD_MINIMIZE"
         Id="10001"
         LabelTitle="Minimize" />
```



## <a name="requirements"></a><span data-ttu-id="aa212-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa212-128">Requirements</span></span>



| <span data-ttu-id="aa212-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa212-129">Requirement</span></span> | <span data-ttu-id="aa212-130">Wert</span><span class="sxs-lookup"><span data-stu-id="aa212-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="aa212-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aa212-131">Minimum supported client</span></span><br/> | <span data-ttu-id="aa212-132">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa212-132">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="aa212-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aa212-133">Minimum supported server</span></span><br/> | <span data-ttu-id="aa212-134">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa212-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aa212-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa212-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa212-136">UI \_ pkey \_ labeldescription</span><span class="sxs-lookup"><span data-stu-id="aa212-136">UI\_PKEY\_LabelDescription</span></span>](windowsribbon-reference-properties-uipkey-labeldescription.md)
</dt> </dl>

 

 





