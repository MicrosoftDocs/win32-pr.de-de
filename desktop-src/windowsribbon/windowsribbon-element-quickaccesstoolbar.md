---
title: Quickaccesstoolbar-Element
description: Stellt die Symbolleiste für den schnell Zugriff (QAT) dar, eine kleine Symbolleiste, die Verknüpfungen zu Menü Band Befehlen anzeigt.
ms.assetid: 59aa35c3-a844-46b3-b066-c9a321fb0891
keywords:
- Windows-Menüband für quickaccesstoolbar-Element
topic_type:
- apiref
api_name:
- QuickAccessToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0076890a8d9858d4bf410ecfdd866bf4f48fdbb6
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104389804"
---
# <a name="quickaccesstoolbar-element"></a><span data-ttu-id="53478-104">Quickaccesstoolbar-Element</span><span class="sxs-lookup"><span data-stu-id="53478-104">QuickAccessToolbar element</span></span>

<span data-ttu-id="53478-105">Stellt die [Symbolleiste für den schnell Zugriff (QAT)](windowsribbon-controls-quickaccesstoolbar.md)dar, eine kleine Symbolleiste, die Verknüpfungen zu Menü Band Befehlen anzeigt.</span><span class="sxs-lookup"><span data-stu-id="53478-105">Represents the [Quick Access Toolbar (QAT)](windowsribbon-controls-quickaccesstoolbar.md), a small toolbar that displays shortcuts to Ribbon Commands.</span></span>

## <a name="usage"></a><span data-ttu-id="53478-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="53478-106">Usage</span></span>

``` syntax
<QuickAccessToolbar
  CommandName = "xs:positiveInteger or xs:string"
  CustomizeCommandName = "xs:positiveInteger or xs:string">
  child elements
</QuickAccessToolbar>
```

## <a name="attributes"></a><span data-ttu-id="53478-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="53478-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="53478-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="53478-108">Attribute</span></span></th>
<th><span data-ttu-id="53478-109">type</span><span class="sxs-lookup"><span data-stu-id="53478-109">Type</span></span></th>
<th><span data-ttu-id="53478-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="53478-110">Required</span></span></th>
<th><span data-ttu-id="53478-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53478-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="53478-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="53478-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="53478-113">xs: positiveingeteger oder xs: String</span><span class="sxs-lookup"><span data-stu-id="53478-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="53478-114">Nein</span><span class="sxs-lookup"><span data-stu-id="53478-114">No</span></span><br/></td>
<td><span data-ttu-id="53478-115">Ordnet das-Element einem <a href="windowsribbon-element-command.md"><strong>Befehl</strong></a>zu.</span><span class="sxs-lookup"><span data-stu-id="53478-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="53478-116">
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)</span><span class="sxs-lookup"><span data-stu-id="53478-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="53478-117">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="53478-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="53478-118">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="53478-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="53478-119">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="53478-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53478-120"><strong>Customizecommandname</strong></span><span class="sxs-lookup"><span data-stu-id="53478-120"><strong>CustomizeCommandName</strong></span></span><br/></td>
<td><span data-ttu-id="53478-121">xs: positiveingeteger oder xs: String</span><span class="sxs-lookup"><span data-stu-id="53478-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="53478-122">Nein</span><span class="sxs-lookup"><span data-stu-id="53478-122">No</span></span><br/></td>
<td><span data-ttu-id="53478-123">Fügt ein zusätzliches Befehls Element in das QAT-Menü ein.</span><span class="sxs-lookup"><span data-stu-id="53478-123">Inserts an additional Command item in the QAT menu.</span></span><br/> <br/><span data-ttu-id="53478-124">
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)</span><span class="sxs-lookup"><span data-stu-id="53478-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <img src="images/markup/qat-customizecommandname.png" alt="Screen shot of a QAT menu with the More commands... Command item." /><br/> <span data-ttu-id="53478-125">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="53478-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="53478-126">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="53478-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="53478-127">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="53478-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="53478-128">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="53478-128">Child elements</span></span>



| <span data-ttu-id="53478-129">Element</span><span class="sxs-lookup"><span data-stu-id="53478-129">Element</span></span>                                                                                                                   | <span data-ttu-id="53478-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53478-130">Description</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="53478-131">**Quickaccesstoolbar. ApplicationDefaults**</span><span class="sxs-lookup"><span data-stu-id="53478-131">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> | <span data-ttu-id="53478-132">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="53478-132">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="53478-133">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="53478-133">Parent elements</span></span>



| <span data-ttu-id="53478-134">Element</span><span class="sxs-lookup"><span data-stu-id="53478-134">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53478-135">**Menüband. quickaccesstoolbar**</span><span class="sxs-lookup"><span data-stu-id="53478-135">**Ribbon.QuickAccessToolbar**</span></span>](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="53478-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53478-136">Remarks</span></span>

<span data-ttu-id="53478-137">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="53478-137">Required.</span></span>

<span data-ttu-id="53478-138">Muss für jede [**Multifunktionsleiste. quickaccesstoolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md)genau einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="53478-138">Must occur exactly once for each [**Ribbon.QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md).</span></span>

<span data-ttu-id="53478-139">Elemente im QAT können zur Laufzeit hinzugefügt oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="53478-139">Items in the QAT can be added or removed at run time.</span></span>

<span data-ttu-id="53478-140">Aus Gründen der Konsistenz zwischen Menüband-Anwendungen wird empfohlen, dass der *customizecommandname* -Befehls Handler ein QAT-Anpassungs Dialogfeld startet.</span><span class="sxs-lookup"><span data-stu-id="53478-140">For consistency across Ribbon applications, it is recommended that the *CustomizeCommandName* Command handler launch a QAT customization dialog.</span></span>

## <a name="examples"></a><span data-ttu-id="53478-141">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53478-141">Examples</span></span>

<span data-ttu-id="53478-142">Im folgenden Beispiel wird das grundlegende Markup für die **quickaccesstoolbar** veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="53478-142">The following example demonstrates the basic markup for the **QuickAccessToolbar**.</span></span>

<span data-ttu-id="53478-143">In diesem Code Abschnitt wird die **quickaccesstoolbar** -Befehls Deklaration veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="53478-143">This section of code shows the **QuickAccessToolbar** Command declaration.</span></span>


```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```



<span data-ttu-id="53478-144">In diesem Code Abschnitt wird die Deklaration des **quickaccesstoolbar** -Steuer Elements veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="53478-144">This section of code shows the **QuickAccessToolbar** control declaration.</span></span>


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="element-information"></a><span data-ttu-id="53478-145">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="53478-145">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="53478-146">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="53478-146">Minimum supported system</span></span><br/> | <span data-ttu-id="53478-147">Windows 7</span><span class="sxs-lookup"><span data-stu-id="53478-147">Windows 7</span></span> |
| <span data-ttu-id="53478-148">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="53478-148">Can be empty</span></span>                        | <span data-ttu-id="53478-149">Nein</span><span class="sxs-lookup"><span data-stu-id="53478-149">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="53478-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="53478-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53478-151">Symbolleisten-Steuerelement schnell Zugriff</span><span class="sxs-lookup"><span data-stu-id="53478-151">Quick Access Toolbar control</span></span>](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 





