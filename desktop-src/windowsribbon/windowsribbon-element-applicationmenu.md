---
title: Applicationmenu-Element
description: Stellt das Anwendungsmenü dar. | Applicationmenu-Element
ms.assetid: 815e0462-ea45-44b1-81bf-f5797b22e920
keywords:
- Windows-Menüband "applicationmenu-Element"
topic_type:
- apiref
api_name:
- ApplicationMenu
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a02193b4c3e61b4b8cf2f129619969f6a82a84ac
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219278"
---
# <a name="applicationmenu-element"></a><span data-ttu-id="4146e-105">Applicationmenu-Element</span><span class="sxs-lookup"><span data-stu-id="4146e-105">ApplicationMenu element</span></span>

<span data-ttu-id="4146e-106">Stellt das [Anwendungsmenü](windowsribbon-controls-applicationmenu.md)dar.</span><span class="sxs-lookup"><span data-stu-id="4146e-106">Represents the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

## <a name="usage"></a><span data-ttu-id="4146e-107">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="4146e-107">Usage</span></span>

``` syntax
<ApplicationMenu
  CommandName = "xs:positiveInteger or xs:string"
>
  child elements
</ApplicationMenu>
```

## <a name="attributes"></a><span data-ttu-id="4146e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4146e-108">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4146e-109">Attribut</span><span class="sxs-lookup"><span data-stu-id="4146e-109">Attribute</span></span></th>
<th><span data-ttu-id="4146e-110">type</span><span class="sxs-lookup"><span data-stu-id="4146e-110">Type</span></span></th>
<th><span data-ttu-id="4146e-111">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="4146e-111">Required</span></span></th>
<th><span data-ttu-id="4146e-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4146e-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4146e-113"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="4146e-113"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="4146e-114">xs: positiveingeteger oder xs: String</span><span class="sxs-lookup"><span data-stu-id="4146e-114">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="4146e-115">Nein</span><span class="sxs-lookup"><span data-stu-id="4146e-115">No</span></span><br/></td>
<td><span data-ttu-id="4146e-116">Ordnet das-Element einem <a href="windowsribbon-element-command.md"><strong>Befehl</strong></a>zu.</span><span class="sxs-lookup"><span data-stu-id="4146e-116">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="4146e-117">
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)</span><span class="sxs-lookup"><span data-stu-id="4146e-117">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="4146e-118">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="4146e-118">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="4146e-119">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="4146e-119">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="4146e-120">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="4146e-120">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="4146e-121">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4146e-121">Child elements</span></span>



| <span data-ttu-id="4146e-122">Element</span><span class="sxs-lookup"><span data-stu-id="4146e-122">Element</span></span>                                                                                             | <span data-ttu-id="4146e-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4146e-123">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="4146e-124">**Applicationmenu. recentitems**</span><span class="sxs-lookup"><span data-stu-id="4146e-124">**ApplicationMenu.RecentItems**</span></span>](windowsribbon-element-applicationmenu-recentitems.md)<br/> | <span data-ttu-id="4146e-125">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="4146e-125">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="4146e-126">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="4146e-126">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                     | <span data-ttu-id="4146e-127">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="4146e-127">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="4146e-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4146e-128">Parent elements</span></span>



| <span data-ttu-id="4146e-129">Element</span><span class="sxs-lookup"><span data-stu-id="4146e-129">Element</span></span>                                                                                   |
|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4146e-130">**Menü Band. applicationmenu**</span><span class="sxs-lookup"><span data-stu-id="4146e-130">**Ribbon.ApplicationMenu**</span></span>](windowsribbon-element-ribbon-applicationmenu.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="4146e-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4146e-131">Remarks</span></span>

<span data-ttu-id="4146e-132">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4146e-132">Required.</span></span>

<span data-ttu-id="4146e-133">Muss für jede [**Multifunktionsleiste. applicationmenu**](windowsribbon-element-ribbon-applicationmenu.md)genau einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="4146e-133">Must occur exactly once for each [**Ribbon.ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md).</span></span>

<span data-ttu-id="4146e-134">Die untergeordneten Elemente des **applicationmenu** -Elements müssen in der angegebenen Reihenfolge vorkommen:</span><span class="sxs-lookup"><span data-stu-id="4146e-134">The child elements of the **ApplicationMenu** element must occur in the specified order:</span></span>

1.  [<span data-ttu-id="4146e-135">**Applicationmenu. recentitems**</span><span class="sxs-lookup"><span data-stu-id="4146e-135">**ApplicationMenu.RecentItems**</span></span>](windowsribbon-element-applicationmenu-recentitems.md)
2.  [<span data-ttu-id="4146e-136">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="4146e-136">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)

## <a name="examples"></a><span data-ttu-id="4146e-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4146e-137">Examples</span></span>

<span data-ttu-id="4146e-138">Im folgenden Beispiel wird das grundlegende Markup für das [Anwendungsmenü](windowsribbon-controls-applicationmenu.md)veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="4146e-138">The following example demonstrates the basic markup for the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

<span data-ttu-id="4146e-139">Dieser Code Abschnitt zeigt die **applicationmenu** -Befehls Deklarationen.</span><span class="sxs-lookup"><span data-stu-id="4146e-139">This section of code shows the **ApplicationMenu** Command declarations.</span></span>


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



<span data-ttu-id="4146e-140">Dieser Code Abschnitt zeigt die **applicationmenu** -Steuerelement Deklarationen.</span><span class="sxs-lookup"><span data-stu-id="4146e-140">This section of code shows the **ApplicationMenu** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="4146e-141">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4146e-141">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="4146e-142">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="4146e-142">Minimum supported system</span></span><br/> | <span data-ttu-id="4146e-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4146e-143">Windows 7</span></span> |
| <span data-ttu-id="4146e-144">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="4146e-144">Can be empty</span></span>                        | <span data-ttu-id="4146e-145">Nein</span><span class="sxs-lookup"><span data-stu-id="4146e-145">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="4146e-146">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4146e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4146e-147">Anwendungsmenü-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="4146e-147">Application Menu control</span></span>](windowsribbon-controls-applicationmenu.md)
</dt> </dl>

 

 





