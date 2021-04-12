---
title: Command.ID-Eigenschaft
description: Stellt eine eindeutige ID für einen Befehl dar.
ms.assetid: 937ca9d6-6910-4133-9cfa-d7e3f895f876
keywords:
- Command.ID-Eigenschaften Fenster (Menü)
topic_type:
- apiref
api_name:
- Command.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13e259e5fd74e3037afde3d4c001000b5a17a9bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478639"
---
# <a name="commandid-property"></a><span data-ttu-id="48d78-104">Command.ID-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="48d78-104">Command.Id property</span></span>

<span data-ttu-id="48d78-105">Stellt eine eindeutige ID für einen Befehl dar.</span><span class="sxs-lookup"><span data-stu-id="48d78-105">Represents a unique ID for a Command.</span></span>

## <a name="usage"></a><span data-ttu-id="48d78-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="48d78-106">Usage</span></span>

``` syntax
<Command.Id/>
```

## <a name="attributes"></a><span data-ttu-id="48d78-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="48d78-107">Attributes</span></span>

<span data-ttu-id="48d78-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="48d78-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="48d78-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="48d78-109">Child elements</span></span>

<span data-ttu-id="48d78-110">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="48d78-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="48d78-111">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="48d78-111">Parent elements</span></span>



| <span data-ttu-id="48d78-112">Element</span><span class="sxs-lookup"><span data-stu-id="48d78-112">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="48d78-113">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="48d78-113">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="48d78-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48d78-114">Remarks</span></span>

<span data-ttu-id="48d78-115">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="48d78-115">Optional.</span></span>

<span data-ttu-id="48d78-116">Kann höchstens einmal für jeden [**Befehl**](windowsribbon-element-command.md)auftreten.</span><span class="sxs-lookup"><span data-stu-id="48d78-116">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="48d78-117">Die ID ist einer Befehls Definition in der Menüband-Header Datei zugeordnet, z `#define cmdSave 25003 /* Save */` . b..</span><span class="sxs-lookup"><span data-stu-id="48d78-117">The ID is associated with a Command definition in the Ribbon header file, for example, `#define cmdSave 25003 /* Save */`.</span></span>

<span data-ttu-id="48d78-118">Dieses Element enthält einen Wert aus der Vereinigung der Typen *xs: positiveInteger* und *xs: String* , die auf einen ganzzahligen Wert zwischen 2 und 59999 (einschließlich) oder 0x2 und 0xea5f in Hexadezimal (einschließlich) beschränkt sind.</span><span class="sxs-lookup"><span data-stu-id="48d78-118">This element contains a value from the union of types *xs:positiveInteger* and *xs:string* constrained to an integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span>

<span data-ttu-id="48d78-119">Die maximale Länge beträgt 10 Zeichen, einschließlich optionaler führender Nullen.</span><span class="sxs-lookup"><span data-stu-id="48d78-119">The maximum length is 10 characters, including optional leading zeros.</span></span>

## <a name="examples"></a><span data-ttu-id="48d78-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="48d78-120">Examples</span></span>

<span data-ttu-id="48d78-121">Im folgenden Beispiel wird das Markup für ein [**Command**](windowsribbon-element-command.md) -Element mit einer **Command.ID** -Deklaration veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="48d78-121">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Id** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="48d78-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48d78-122">Requirements</span></span>



| <span data-ttu-id="48d78-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48d78-123">Requirement</span></span> | <span data-ttu-id="48d78-124">Wert</span><span class="sxs-lookup"><span data-stu-id="48d78-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="48d78-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48d78-125">Minimum supported client</span></span><br/> | <span data-ttu-id="48d78-126">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48d78-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="48d78-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48d78-127">Minimum supported server</span></span><br/> | <span data-ttu-id="48d78-128">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48d78-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





