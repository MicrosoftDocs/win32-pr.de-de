---
title: Ribbon. sizedefinitions (Eigenschaft)
description: Stellt einen Container für benutzerdefinierte Layoutvorlagen von Menü Band Steuerelementen dar.
ms.assetid: 1f5fcffc-7f2e-4763-b0a7-4e8f46534da8
keywords:
- Menüband. sizedefinitions-Eigenschaft (Fenster)
topic_type:
- apiref
api_name:
- Ribbon.SizeDefinitions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b8ffe5a3339b0f32e493a1f7ddc33789526695e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040190"
---
# <a name="ribbonsizedefinitions-property"></a><span data-ttu-id="88790-104">Ribbon. sizedefinitions (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="88790-104">Ribbon.SizeDefinitions property</span></span>

<span data-ttu-id="88790-105">Stellt einen Container für benutzerdefinierte Layoutvorlagen von Menü Band Steuerelementen dar.</span><span class="sxs-lookup"><span data-stu-id="88790-105">Represents a container for custom layout templates of Ribbon controls.</span></span>

## <a name="usage"></a><span data-ttu-id="88790-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="88790-106">Usage</span></span>

``` syntax
<Ribbon.SizeDefinitions>
  child elements
</Ribbon.SizeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="88790-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="88790-107">Attributes</span></span>

<span data-ttu-id="88790-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="88790-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="88790-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="88790-109">Child elements</span></span>



| <span data-ttu-id="88790-110">Element</span><span class="sxs-lookup"><span data-stu-id="88790-110">Element</span></span>                                                                   | <span data-ttu-id="88790-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="88790-111">Description</span></span>                                        |
|---------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="88790-112">**Sizedefinition**</span><span class="sxs-lookup"><span data-stu-id="88790-112">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/> | <span data-ttu-id="88790-113">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="88790-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="88790-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="88790-114">Parent elements</span></span>



| <span data-ttu-id="88790-115">Element</span><span class="sxs-lookup"><span data-stu-id="88790-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="88790-116">**Menüband**</span><span class="sxs-lookup"><span data-stu-id="88790-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="88790-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88790-117">Remarks</span></span>

<span data-ttu-id="88790-118">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="88790-118">Optional.</span></span>

<span data-ttu-id="88790-119">Kann höchstens einmal für jedes [**Menüband**](windowsribbon-element-ribbon.md)auftreten.</span><span class="sxs-lookup"><span data-stu-id="88790-119">May occur at most once for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="88790-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="88790-120">Examples</span></span>

<span data-ttu-id="88790-121">Im folgenden Codebeispiel wird eine grundlegende benutzerdefinierte Vorlage veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="88790-121">The following code example illustrates a basic custom template.</span></span>


```
<Ribbon.SizeDefinitions>
  <SizeDefinition Name="CustomTemplate">
    <GroupSizeDefinition Size="Large">
      <ControlSizeDefinition ImageSize="Large" IsLabelVisible="true" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
  </SizeDefinition>
</Ribbon.SizeDefinitions>
```



## <a name="requirements"></a><span data-ttu-id="88790-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88790-122">Requirements</span></span>



| <span data-ttu-id="88790-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88790-123">Requirement</span></span> | <span data-ttu-id="88790-124">Wert</span><span class="sxs-lookup"><span data-stu-id="88790-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="88790-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="88790-125">Minimum supported client</span></span><br/> | <span data-ttu-id="88790-126">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88790-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="88790-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="88790-127">Minimum supported server</span></span><br/> | <span data-ttu-id="88790-128">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88790-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="88790-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88790-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88790-130">Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien</span><span class="sxs-lookup"><span data-stu-id="88790-130">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





