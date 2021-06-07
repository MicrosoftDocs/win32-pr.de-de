---
title: ApplicationMenu-Element
description: Stellt das Anwendungsmenü dar. | ApplicationMenu-Element
ms.assetid: 815e0462-ea45-44b1-81bf-f5797b22e920
keywords:
- ApplicationMenu-Element Windows-Menüband
topic_type:
- apiref
api_name:
- ApplicationMenu
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e535fbcc09a404ad7dd5a4019438f4513f5c77c6
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443051"
---
# <a name="applicationmenu-element"></a><span data-ttu-id="016df-105">ApplicationMenu-Element</span><span class="sxs-lookup"><span data-stu-id="016df-105">ApplicationMenu element</span></span>

<span data-ttu-id="016df-106">Stellt das [Anwendungsmenü](windowsribbon-controls-applicationmenu.md)dar.</span><span class="sxs-lookup"><span data-stu-id="016df-106">Represents the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

## <a name="usage"></a><span data-ttu-id="016df-107">Verwendung</span><span class="sxs-lookup"><span data-stu-id="016df-107">Usage</span></span>

``` syntax
<ApplicationMenu
  CommandName = "xs:positiveInteger or xs:string"
>
  child elements
</ApplicationMenu>
```

## <a name="attributes"></a><span data-ttu-id="016df-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="016df-108">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="016df-109">attribute</span><span class="sxs-lookup"><span data-stu-id="016df-109">Attribute</span></span></th>
<th><span data-ttu-id="016df-110">Typ</span><span class="sxs-lookup"><span data-stu-id="016df-110">Type</span></span></th>
<th><span data-ttu-id="016df-111">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="016df-111">Required</span></span></th>
<th><span data-ttu-id="016df-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="016df-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="016df-113"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="016df-113"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="016df-114">xs:positiveInteger oder xs:string</span><span class="sxs-lookup"><span data-stu-id="016df-114">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="016df-115">Nein</span><span class="sxs-lookup"><span data-stu-id="016df-115">No</span></span><br/></td>
<td><span data-ttu-id="016df-116">Ordnet das Element einem <a href="windowsribbon-element-command.md"><strong>Command zu.</strong></a></span><span class="sxs-lookup"><span data-stu-id="016df-116">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="016df-117">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)</span><span class="sxs-lookup"><span data-stu-id="016df-117">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="016df-118">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999( einschließlich) oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich.</span><span class="sxs-lookup"><span data-stu-id="016df-118">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="016df-119">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="016df-119">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="016df-120">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="016df-120">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="016df-121">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="016df-121">Child elements</span></span>



| <span data-ttu-id="016df-122">Element</span><span class="sxs-lookup"><span data-stu-id="016df-122">Element</span></span>                                                                                             | <span data-ttu-id="016df-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="016df-123">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="016df-124">**ApplicationMenu.RecentItems**</span><span class="sxs-lookup"><span data-stu-id="016df-124">**ApplicationMenu.RecentItems**</span></span>](windowsribbon-element-applicationmenu-recentitems.md)<br/> | <span data-ttu-id="016df-125">Kann höchstens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="016df-125">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="016df-126">**Menugroup**</span><span class="sxs-lookup"><span data-stu-id="016df-126">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                     | <span data-ttu-id="016df-127">Kann ein oder mehrere Male auftreten</span><span class="sxs-lookup"><span data-stu-id="016df-127">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="016df-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="016df-128">Parent elements</span></span>



| <span data-ttu-id="016df-129">Element</span><span class="sxs-lookup"><span data-stu-id="016df-129">Element</span></span>                                                                                   |
|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="016df-130">**Ribbon.ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="016df-130">**Ribbon.ApplicationMenu**</span></span>](windowsribbon-element-ribbon-applicationmenu.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="016df-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="016df-131">Remarks</span></span>

<span data-ttu-id="016df-132">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="016df-132">Required.</span></span>

<span data-ttu-id="016df-133">Muss genau einmal für jede [**Ribbon.ApplicationMenu-Datei**](windowsribbon-element-ribbon-applicationmenu.md)auftreten.</span><span class="sxs-lookup"><span data-stu-id="016df-133">Must occur exactly once for each [**Ribbon.ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md).</span></span>

<span data-ttu-id="016df-134">Die untergeordneten Elemente des **ApplicationMenu-Elements** müssen in der angegebenen Reihenfolge auftreten:</span><span class="sxs-lookup"><span data-stu-id="016df-134">The child elements of the **ApplicationMenu** element must occur in the specified order:</span></span>

1.  [<span data-ttu-id="016df-135">**ApplicationMenu.RecentItems**</span><span class="sxs-lookup"><span data-stu-id="016df-135">**ApplicationMenu.RecentItems**</span></span>](windowsribbon-element-applicationmenu-recentitems.md)
2.  [<span data-ttu-id="016df-136">**Menugroup**</span><span class="sxs-lookup"><span data-stu-id="016df-136">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)

## <a name="examples"></a><span data-ttu-id="016df-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="016df-137">Examples</span></span>

<span data-ttu-id="016df-138">Im folgenden Beispiel wird das grundlegende Markup für das [Anwendungsmenü](windowsribbon-controls-applicationmenu.md)veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="016df-138">The following example demonstrates the basic markup for the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

<span data-ttu-id="016df-139">Dieser Codeabschnitt zeigt die ApplicationMenu-Befehlsdeklarationen. </span><span class="sxs-lookup"><span data-stu-id="016df-139">This section of code shows the **ApplicationMenu** Command declarations.</span></span>


```XML
<!-- Command declarations for the Application Menu. -->
<Command Name="cmdFileMenu"
         Symbol="ID_FILE_MENU"
         Id="25000" />
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
<!-- Command declarations for Application Menu items. -->
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
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
<Command Name="cmdPrint"
         Symbol="ID_FILE_PRINT"
         Comment="Save"
         Id="25004"
         LabelTitle="Print" />
<Command Name="cmdExit"
         Symbol="ID_FILE_EXIT"
         Comment="Exit"
         Id="25005"
         LabelTitle="Exit" />
```



<span data-ttu-id="016df-140">Dieser Codeabschnitt zeigt die **ApplicationMenu-Steuerelementdeklarationen.**</span><span class="sxs-lookup"><span data-stu-id="016df-140">This section of code shows the **ApplicationMenu** control declarations.</span></span>


```XML
<!-- Control declarations for Application Menu items. -->
<Ribbon.ApplicationMenu>
  <ApplicationMenu CommandName="cmdFileMenu">
    <!-- Most recently used items collection. -->
    <ApplicationMenu.RecentItems>
      <RecentItems CommandName="cmdMRUItems"/>
    </ApplicationMenu.RecentItems>
    <!-- Menu items collection. -->
    <MenuGroup>
      <Button CommandName="cmdNew" />
      <Button CommandName="cmdOpen" />
      <Button CommandName="cmdSave" />
    </MenuGroup>
    <MenuGroup>
      <Button CommandName="cmdPrint" />
      <Button CommandName="cmdExit" />
    </MenuGroup>
  </ApplicationMenu>
</Ribbon.ApplicationMenu>
```



## <a name="element-information"></a><span data-ttu-id="016df-141">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="016df-141">Element information</span></span>

* <span data-ttu-id="016df-142">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="016df-142">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="016df-143">**Kann leer sein:** Nein</span><span class="sxs-lookup"><span data-stu-id="016df-143">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="016df-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="016df-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="016df-145">Anwendungsmenü-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="016df-145">Application Menu control</span></span>](windowsribbon-controls-applicationmenu.md)
</dt> </dl>

 

 





