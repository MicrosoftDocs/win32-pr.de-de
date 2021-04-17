---
title: Command. labeltitle (Eigenschaft)
description: Stellt einen Bezeichnungs Titel dar.
ms.assetid: 97378ec3-7988-4e39-9cf5-c382b246c5c9
keywords:
- Command. labeltitle-Eigenschaft (Windows-Menüband)
topic_type:
- apiref
api_name:
- Command.LabelTitle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed6d6c72ddd60cca63834fdcf21cf8f8b726ad22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518689"
---
# <a name="commandlabeltitle-property"></a><span data-ttu-id="b02a2-104">Command. labeltitle (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b02a2-104">Command.LabelTitle property</span></span>

<span data-ttu-id="b02a2-105">Stellt einen Bezeichnungs Titel dar.</span><span class="sxs-lookup"><span data-stu-id="b02a2-105">Represents a label title.</span></span>

## <a name="usage"></a><span data-ttu-id="b02a2-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="b02a2-106">Usage</span></span>

``` syntax
<Command.LabelTitle>
  child elements
</Command.LabelTitle>
```

## <a name="attributes"></a><span data-ttu-id="b02a2-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="b02a2-107">Attributes</span></span>

<span data-ttu-id="b02a2-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="b02a2-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b02a2-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b02a2-109">Child elements</span></span>



| <span data-ttu-id="b02a2-110">Element</span><span class="sxs-lookup"><span data-stu-id="b02a2-110">Element</span></span>                                                   | <span data-ttu-id="b02a2-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b02a2-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="b02a2-112">**Schnür**</span><span class="sxs-lookup"><span data-stu-id="b02a2-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="b02a2-113">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="b02a2-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="b02a2-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b02a2-114">Parent elements</span></span>



| <span data-ttu-id="b02a2-115">Element</span><span class="sxs-lookup"><span data-stu-id="b02a2-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="b02a2-116">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="b02a2-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="b02a2-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b02a2-117">Remarks</span></span>

<span data-ttu-id="b02a2-118">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="b02a2-118">Optional.</span></span>

<span data-ttu-id="b02a2-119">Kann höchstens einmal für jeden [**Befehl**](windowsribbon-element-command.md)auftreten.</span><span class="sxs-lookup"><span data-stu-id="b02a2-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="b02a2-120">**Command. labeltitle** kann einen Wert vom Typ *xs: String* enthalten, der auf eine beliebige Sequenz von Zeichen beschränkt ist, einschließlich Leerzeichen und Zeilenumbruch Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b02a2-120">**Command.LabelTitle** can contain a value of type *xs:string* constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="b02a2-121">Verwenden Sie den XML-Zeichen Verweis Universal Character Set (UCS) `&#xA;` , um einen Zeilenumbruch anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b02a2-121">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="b02a2-122">Die maximale Länge ist unbegrenzt.</span><span class="sxs-lookup"><span data-stu-id="b02a2-122">The maximum length is unbounded.</span></span>

<span data-ttu-id="b02a2-123">Wenn für **Command. labeltitle** kein Wert angegeben wird, ist das untergeordnete [**Zeichen**](windowsribbon-element-string.md) folgen Element erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b02a2-123">If no value is supplied for **Command.LabelTitle**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="b02a2-124">Wenn **Command. labeltitle** sowohl einen Wert als auch ein untergeordnetes [**Zeichen**](windowsribbon-element-string.md) folgen Element enthält, hat die **Zeichenfolge** Vorrang.</span><span class="sxs-lookup"><span data-stu-id="b02a2-124">If **Command.LabelTitle** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="b02a2-125">**Command. labeltitle** unterstützt nur die linke Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="b02a2-125">**Command.LabelTitle** only supports left alignment.</span></span>

<span data-ttu-id="b02a2-126">Wenn ein Befehl über ein Menü Element verfügbar gemacht wird und der Wert von **Command. labeltitle** oder [UI \_ pkey \_ Label](windowsribbon-reference-properties-uipkey-label.md) einen Buchstaben enthält, dem ein kaufmännisches und vorangestellt ist, wie im folgenden Beispiel gezeigt, wird dieser Buchstabe sowohl als KeyTip als auch als Tastaturbeschleuniger für diesen Befehl durch das Multifunktionsleisten-Framework behandelt.</span><span class="sxs-lookup"><span data-stu-id="b02a2-126">If a Command is exposed through a menu item and the value of **Command.LabelTitle** or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md) contains a letter preceded by an ampersand, as shown in the following example, this letter is treated as both a keytip and a keyboard accelerator for that Command by the Ribbon framework.</span></span>


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



<span data-ttu-id="b02a2-127">Um ein kaufmännisches und-Zeichen in einer Bezeichnung anzuzeigen, versehen Sie die Bezeichnung für Sonderzeichen mit einem doppelten kaufmännisches und-Zeichen ( `&&` ), wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="b02a2-127">To display an ampersand in a label, escape the special character designation with a double ampersand (`&&`) as shown in the following example.</span></span>


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="examples"></a><span data-ttu-id="b02a2-128">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b02a2-128">Examples</span></span>

<span data-ttu-id="b02a2-129">Im folgenden Beispiel wird das Markup für ein [**Command**](windowsribbon-element-command.md) -Element mit der **Command. labeltitle** -Deklaration veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="b02a2-129">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.LabelTitle** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="b02a2-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b02a2-130">Requirements</span></span>



| <span data-ttu-id="b02a2-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b02a2-131">Requirement</span></span> | <span data-ttu-id="b02a2-132">Wert</span><span class="sxs-lookup"><span data-stu-id="b02a2-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="b02a2-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b02a2-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b02a2-134">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b02a2-134">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="b02a2-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b02a2-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b02a2-136">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b02a2-136">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b02a2-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b02a2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b02a2-138">UI- \_ pkey- \_ Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="b02a2-138">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)
</dt> </dl>

 

 





