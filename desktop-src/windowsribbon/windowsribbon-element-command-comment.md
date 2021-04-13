---
title: Command. Comment (Eigenschaft)
description: Stellt einen Kommentar oder eine Anmerkung für einen Befehl dar.
ms.assetid: 4ac5c7d4-9627-4703-bd3c-594d9497ba24
keywords:
- Command. Comment-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- Command.Comment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7df2131234623dd30fc90339634a932eca5bd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392142"
---
# <a name="commandcomment-property"></a><span data-ttu-id="fd6e6-104">Command. Comment (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fd6e6-104">Command.Comment property</span></span>

<span data-ttu-id="fd6e6-105">Stellt einen Kommentar oder eine Anmerkung für einen Befehl dar.</span><span class="sxs-lookup"><span data-stu-id="fd6e6-105">Represents a comment, or annotation, for a Command.</span></span>

## <a name="usage"></a><span data-ttu-id="fd6e6-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="fd6e6-106">Usage</span></span>

``` syntax
<Command.Comment/>
```

## <a name="attributes"></a><span data-ttu-id="fd6e6-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="fd6e6-107">Attributes</span></span>

<span data-ttu-id="fd6e6-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="fd6e6-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="fd6e6-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fd6e6-109">Child elements</span></span>

<span data-ttu-id="fd6e6-110">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="fd6e6-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="fd6e6-111">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fd6e6-111">Parent elements</span></span>



| <span data-ttu-id="fd6e6-112">Element</span><span class="sxs-lookup"><span data-stu-id="fd6e6-112">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="fd6e6-113">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="fd6e6-113">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="fd6e6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd6e6-114">Remarks</span></span>

<span data-ttu-id="fd6e6-115">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="fd6e6-115">Optional.</span></span>

<span data-ttu-id="fd6e6-116">Kann höchstens einmal für jeden [**Befehl**](windowsribbon-element-command.md)auftreten.</span><span class="sxs-lookup"><span data-stu-id="fd6e6-116">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="fd6e6-117">Der Kommentar ist einer Befehls Definition in der Menüband-Header Datei zugeordnet, z `#define cmdSave 25003 /* Save */` . b..</span><span class="sxs-lookup"><span data-stu-id="fd6e6-117">The comment is associated with a Command definition in the Ribbon header file, for example, `#define cmdSave 25003 /* Save */`.</span></span>

<span data-ttu-id="fd6e6-118">Dieses Element enthält einen Wert vom Typ *xs: String*.</span><span class="sxs-lookup"><span data-stu-id="fd6e6-118">This element contains a value of type *xs:string*.</span></span>

<span data-ttu-id="fd6e6-119">Die maximale Länge beträgt 250 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="fd6e6-119">The maximum length is 250 characters.</span></span>

## <a name="examples"></a><span data-ttu-id="fd6e6-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd6e6-120">Examples</span></span>

<span data-ttu-id="fd6e6-121">Im folgenden Beispiel wird das Markup für ein [**Command**](windowsribbon-element-command.md) -Element mit der **Command. Comment** -Deklaration veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="fd6e6-121">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Comment** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="fd6e6-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd6e6-122">Requirements</span></span>



| <span data-ttu-id="fd6e6-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd6e6-123">Requirement</span></span> | <span data-ttu-id="fd6e6-124">Wert</span><span class="sxs-lookup"><span data-stu-id="fd6e6-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="fd6e6-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd6e6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fd6e6-126">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd6e6-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="fd6e6-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd6e6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fd6e6-128">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd6e6-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





