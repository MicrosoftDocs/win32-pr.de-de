---
title: Command. ToolTipTitle (Eigenschaft)
description: Stellt einen QuickInfo-Titel dar.
ms.assetid: b06a7a6a-fbdd-464b-b804-e62912d6e176
keywords:
- Command. ToolTipTitle-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- Command.TooltipTitle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c60f4ddea77fbf88a15d5d27e90ca5660bc0edb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478618"
---
# <a name="commandtooltiptitle-property"></a><span data-ttu-id="a9a7d-104">Command. ToolTipTitle (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a9a7d-104">Command.TooltipTitle property</span></span>

<span data-ttu-id="a9a7d-105">Stellt einen QuickInfo-Titel dar.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-105">Represents a tooltip title.</span></span>

## <a name="usage"></a><span data-ttu-id="a9a7d-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="a9a7d-106">Usage</span></span>

``` syntax
<Command.TooltipTitle>
  child elements
</Command.TooltipTitle>
```

## <a name="attributes"></a><span data-ttu-id="a9a7d-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="a9a7d-107">Attributes</span></span>

<span data-ttu-id="a9a7d-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a9a7d-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a9a7d-109">Child elements</span></span>



| <span data-ttu-id="a9a7d-110">Element</span><span class="sxs-lookup"><span data-stu-id="a9a7d-110">Element</span></span>                                                   | <span data-ttu-id="a9a7d-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a9a7d-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="a9a7d-112">**Schnür**</span><span class="sxs-lookup"><span data-stu-id="a9a7d-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="a9a7d-113">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="a9a7d-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="a9a7d-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a9a7d-114">Parent elements</span></span>



| <span data-ttu-id="a9a7d-115">Element</span><span class="sxs-lookup"><span data-stu-id="a9a7d-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="a9a7d-116">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="a9a7d-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a9a7d-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9a7d-117">Remarks</span></span>

<span data-ttu-id="a9a7d-118">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-118">Optional.</span></span>

<span data-ttu-id="a9a7d-119">Kann höchstens einmal für jeden [**Befehl**](windowsribbon-element-command.md)auftreten.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="a9a7d-120">**Command. ToolTipTitle** kann einen Wert vom Typ *xs: String* enthalten, der auf eine beliebige Sequenz von Zeichen beschränkt ist, einschließlich Leerzeichen und Zeilenumbruch Zeichen.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-120">**Command.TooltipTitle** can contain a value of type *xs:string* constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="a9a7d-121">Verwenden Sie den XML-Zeichen Verweis Universal Character Set (UCS) `&#xA;` , um einen Zeilenumbruch anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-121">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="a9a7d-122">Die maximale Länge ist unbegrenzt.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-122">The maximum length is unbounded.</span></span>

<span data-ttu-id="a9a7d-123">Wenn für **Command. ToolTipTitle** kein Wert angegeben wird, ist das untergeordnete [**Zeichen**](windowsribbon-element-string.md) folgen Element erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-123">If no value is supplied for **Command.TooltipTitle**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="a9a7d-124">Wenn **Command. ToolTipTitle** sowohl einen Wert als auch ein untergeordnetes [**Zeichen**](windowsribbon-element-string.md) folgen Element enthält, hat die **Zeichenfolge** Vorrang.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-124">If **Command.TooltipTitle** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="a9a7d-125">**Command. ToolTipTitle** unterstützt nur die linke Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-125">**Command.TooltipTitle** only supports left alignment.</span></span>

## <a name="examples"></a><span data-ttu-id="a9a7d-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9a7d-126">Examples</span></span>

<span data-ttu-id="a9a7d-127">Im folgenden Beispiel wird das Markup für ein [**Command**](windowsribbon-element-command.md) -Element mit der **Command. ToolTipTitle** -Deklaration veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-127">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.TooltipTitle** declaration.</span></span>


```XML
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
```



## <a name="requirements"></a><span data-ttu-id="a9a7d-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9a7d-128">Requirements</span></span>



| <span data-ttu-id="a9a7d-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9a7d-129">Requirement</span></span> | <span data-ttu-id="a9a7d-130">Wert</span><span class="sxs-lookup"><span data-stu-id="a9a7d-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="a9a7d-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a9a7d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a9a7d-132">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9a7d-132">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="a9a7d-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a9a7d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a9a7d-134">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9a7d-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a9a7d-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9a7d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9a7d-136">UI- \_ pkey- \_ ToolTipTitle</span><span class="sxs-lookup"><span data-stu-id="a9a7d-136">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)
</dt> </dl>

 

 





