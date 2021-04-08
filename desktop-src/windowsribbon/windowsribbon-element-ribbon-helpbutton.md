---
title: Ribbon. HelpButton (Eigenschaft)
description: Stellt einen Container für die Hilfe Schaltfläche dar.
ms.assetid: a64239b2-2440-4bcf-8fd7-079003de6d8c
keywords:
- Menüband. HelpButton-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- Ribbon.HelpButton
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49e343a5181479ede5d428937908ed4bf37764f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742296"
---
# <a name="ribbonhelpbutton-property"></a><span data-ttu-id="aeb12-104">Ribbon. HelpButton (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="aeb12-104">Ribbon.HelpButton property</span></span>

<span data-ttu-id="aeb12-105">Stellt einen Container für die [Hilfe Schaltfläche](windowsribbon-controls-helpbutton.md)dar.</span><span class="sxs-lookup"><span data-stu-id="aeb12-105">Represents a container for the [Help Button](windowsribbon-controls-helpbutton.md).</span></span>

## <a name="usage"></a><span data-ttu-id="aeb12-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="aeb12-106">Usage</span></span>

``` syntax
<Ribbon.HelpButton>
  child elements
</Ribbon.HelpButton>
```

## <a name="attributes"></a><span data-ttu-id="aeb12-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="aeb12-107">Attributes</span></span>

<span data-ttu-id="aeb12-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="aeb12-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="aeb12-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aeb12-109">Child elements</span></span>



| <span data-ttu-id="aeb12-110">Element</span><span class="sxs-lookup"><span data-stu-id="aeb12-110">Element</span></span>                                                           | <span data-ttu-id="aeb12-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aeb12-111">Description</span></span>                                   |
|-------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="aeb12-112">**HelpButton**</span><span class="sxs-lookup"><span data-stu-id="aeb12-112">**HelpButton**</span></span>](windowsribbon-element-helpbutton.md)<br/> | <span data-ttu-id="aeb12-113">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="aeb12-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="aeb12-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aeb12-114">Parent elements</span></span>



| <span data-ttu-id="aeb12-115">Element</span><span class="sxs-lookup"><span data-stu-id="aeb12-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="aeb12-116">**Menüband**</span><span class="sxs-lookup"><span data-stu-id="aeb12-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="aeb12-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aeb12-117">Remarks</span></span>

<span data-ttu-id="aeb12-118">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="aeb12-118">Optional.</span></span>

<span data-ttu-id="aeb12-119">Kann höchstens einmal für jedes [**Menüband**](windowsribbon-element-ribbon.md)auftreten.</span><span class="sxs-lookup"><span data-stu-id="aeb12-119">May occur at most once for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="aeb12-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aeb12-120">Examples</span></span>

<span data-ttu-id="aeb12-121">Im folgenden Beispiel wird das grundlegende Markup veranschaulicht, das zum Implementieren einer Menüband-Hilfe Schaltfläche erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="aeb12-121">The following example demonstrates the basic markup that is required to implement a Ribbon Help button.</span></span>

<span data-ttu-id="aeb12-122">In diesem Code Abschnitt wird die Befehls Deklaration **Ribbon. HelpButton** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aeb12-122">This section of code shows the **Ribbon.HelpButton** Command declaration.</span></span>


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



<span data-ttu-id="aeb12-123">In diesem Code Abschnitt wird die Deklaration des **Ribbon. HelpButton** -Steuer Elements angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aeb12-123">This section of code shows the **Ribbon.HelpButton** control declaration.</span></span>


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="requirements"></a><span data-ttu-id="aeb12-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aeb12-124">Requirements</span></span>



| <span data-ttu-id="aeb12-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aeb12-125">Requirement</span></span> | <span data-ttu-id="aeb12-126">Wert</span><span class="sxs-lookup"><span data-stu-id="aeb12-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="aeb12-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aeb12-127">Minimum supported client</span></span><br/> | <span data-ttu-id="aeb12-128">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aeb12-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="aeb12-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aeb12-129">Minimum supported server</span></span><br/> | <span data-ttu-id="aeb12-130">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aeb12-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





