---
title: Command. Symbol-Eigenschaft
description: Stellt den Namen eines Befehls dar, auf den extern verwiesen werden kann.
ms.assetid: affa5f3f-f641-4bec-9165-6102509cf355
keywords:
- Command. Symbol-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- Command.Symbol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88dccb71a90feca7348ca9731ca5966b012c9c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341020"
---
# <a name="commandsymbol-property"></a><span data-ttu-id="15c69-104">Command. Symbol-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="15c69-104">Command.Symbol property</span></span>

<span data-ttu-id="15c69-105">Stellt den Namen eines [**Befehls**](windowsribbon-element-command.md) dar, auf den extern verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="15c69-105">Represents the name of a [**Command**](windowsribbon-element-command.md) that can be referenced externally.</span></span>

## <a name="usage"></a><span data-ttu-id="15c69-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="15c69-106">Usage</span></span>

``` syntax
<Command.Symbol/>
```

## <a name="attributes"></a><span data-ttu-id="15c69-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="15c69-107">Attributes</span></span>

<span data-ttu-id="15c69-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="15c69-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="15c69-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="15c69-109">Child elements</span></span>

<span data-ttu-id="15c69-110">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="15c69-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="15c69-111">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="15c69-111">Parent elements</span></span>



| <span data-ttu-id="15c69-112">Element</span><span class="sxs-lookup"><span data-stu-id="15c69-112">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="15c69-113">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="15c69-113">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="15c69-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15c69-114">Remarks</span></span>

<span data-ttu-id="15c69-115">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="15c69-115">Optional.</span></span>

<span data-ttu-id="15c69-116">Kann höchstens einmal für jeden [**Befehl**](windowsribbon-element-command.md)auftreten.</span><span class="sxs-lookup"><span data-stu-id="15c69-116">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="15c69-117">Das Symbol ist einer Befehls Definition in der Menüband-Header Datei zugeordnet, z `#define cmdSave 25003 /* Save */` . b..</span><span class="sxs-lookup"><span data-stu-id="15c69-117">The symbol is associated with a Command definition in the Ribbon header file, for example, `#define cmdSave 25003 /* Save */`.</span></span>

<span data-ttu-id="15c69-118">Dieses Element enthält einen Wert vom Typ *xs: String*.</span><span class="sxs-lookup"><span data-stu-id="15c69-118">This element contains a value of type *xs:string*.</span></span>

<span data-ttu-id="15c69-119">Der Wert ist auf eine Zeichenfolge beschränkt, die aus einem Buchstaben oder Unterstrich besteht, gefolgt von einer beliebigen Folge von Buchstaben, Ziffern und unterstrichen.</span><span class="sxs-lookup"><span data-stu-id="15c69-119">The value is constrained to a string that consists of a letter or underscore followed by any sequence of letters, digits, and underscores.</span></span>

<span data-ttu-id="15c69-120">Die maximale Länge beträgt 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="15c69-120">The maximum length is 100 characters.</span></span>

## <a name="examples"></a><span data-ttu-id="15c69-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="15c69-121">Examples</span></span>

<span data-ttu-id="15c69-122">Im folgenden Beispiel wird das Markup für ein [**Command**](windowsribbon-element-command.md) -Element mit der **Command. Symbol** -Deklaration veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="15c69-122">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Symbol** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="15c69-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15c69-123">Requirements</span></span>



| <span data-ttu-id="15c69-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15c69-124">Requirement</span></span> | <span data-ttu-id="15c69-125">Wert</span><span class="sxs-lookup"><span data-stu-id="15c69-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="15c69-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="15c69-126">Minimum supported client</span></span><br/> | <span data-ttu-id="15c69-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15c69-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="15c69-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="15c69-128">Minimum supported server</span></span><br/> | <span data-ttu-id="15c69-129">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15c69-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





